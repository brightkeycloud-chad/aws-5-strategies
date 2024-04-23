## Creating an AWS EventBridge Rule for AWS Health Events with SNS Topic Target

This guide outlines the process of setting up an AWS EventBridge rule to capture AWS Health events and send notifications to an SNS topic. This is useful for monitoring and responding to AWS Health notifications such as service availability, maintenance updates, and other important events affecting your AWS resources.

### Step 1: Sign in to AWS Management Console
- **Access the Console**: Open your web browser and navigate to the [AWS Management Console](https://aws.amazon.com/console/).
- **Log in** with your AWS account credentials.

### Step 2: Navigate to the Amazon EventBridge Console
- From the AWS Management Console, go to the **Services** menu.
- Click on **EventBridge** under the Application Integration section.

### Step 3: Create a New Rule
- In the EventBridge console, select **Rules** from the left-hand navigation pane.
- Click on **Create rule**.

### Step 4: Configure the New Rule
- **Name your rule**: Enter a descriptive name, such as `AWSHealthNotifications`.
- **Define the rule description** (optional): Provide a brief description of what the rule does.

### Step 5: Set the Event Pattern
- Under **Define pattern**, select **Event pattern**.
- Choose **Pre-defined pattern by service**.
- For **Service provider**, select **AWS**.
- For **Service name**, choose **Health**.
- For **Event type**, select **All Events** to capture all AWS Health events. You can also customize this selection to capture only specific types of Health events.

### Step 6: Select the Event Bus
- Confirm the **Event bus** is set to **default**. This is typically sufficient unless you have custom event buses.

### Step 7: Set the Target
- Scroll to **Select target**.
- For **Target**, choose **SNS topic** from the dropdown.
- **Select your SNS topic**: Choose an existing SNS topic from the list or create a new SNS topic if needed. To create a new topic, you must go to the SNS console, create the topic, and then return to this setup.

### Step 8: Configure Input
- Under **Configure input**, choose **Matched event**. This setting will pass the entire event to the SNS topic.

### Step 9: Create the Rule
- Click on **Create** to finalize the creation of your rule.
