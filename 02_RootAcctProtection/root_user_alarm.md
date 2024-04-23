## Configuring an AWS CloudWatch Alarm Based on CloudTrail Logs for Root User Activity

This guide will help you set up an alarm in AWS CloudWatch to monitor root user activities logged in CloudTrail. These steps are crucial for enhancing security and responding promptly to potentially unauthorized root account activities.

### Step 1: Ensure CloudTrail Logging is Enabled
- **Log in** to the AWS Management Console.
- Navigate to **CloudTrail** and ensure that logging is enabled and configured to deliver logs to a cCloudWatch log group.

### Step 2: Open CloudWatch
- In the AWS Management Console, go to the "Services" menu.
- Select **CloudWatch** under the Management & Governance section.

### Step 3: Create a Metric Filter
- Navigate to **Logs** in the CloudWatch sidebar.
- Select the log group associated with your CloudTrail logs.
- Click on **Create Metric Filter**.

### Step 4: Define the Metric Filter Pattern
- In the filter pattern box, enter the following pattern to identify root user activity:
````
{ $.userIdentity.type = "Root" && $.userIdentity.invokedBy NOT EXISTS && $.eventType != "AwsServiceEvent" }
````
- Click **Next**.

### Step 5: Set Metric Details
- For **Filter Name**, enter a descriptive name like `RootUserActivity`.
- For **Metric Namespace**, enter `CloudTrailMetrics`.
- For **Metric Name**, enter `RootUserActivityCount`.
- Set **Metric Value** to `1`.
- Click on **Create Filter**.

### Step 6: Create an Alarm
- After creating the metric filter, click on **Create Alarm**.
- Set the **Whenever** condition to `>= 1` for the `RootUserActivityCount` metric to trigger the alarm on any detected activity.
- Define the **Statistic** as `Sum` and the **Period** as `5 minutes`.

### Step 7: Configure Actions
- In the **Actions** section, set up the notification:
- Under **Alarm state trigger**, choose `ALARM`.
- Select an **SNS topic** to notify, or create a new SNS topic to send notifications to an email or an SMS.
- Click **Next**.

### Step 8: Add Alarm Details
- Name your alarm, e.g., `AlarmForRootUserActivity`.
- Optionally, add a description.
- Click **Next** and review all settings.

### Step 9: Confirm and Create Alarm
- Review all configurations to ensure accuracy.
- Click on **Create Alarm** to activate it.

