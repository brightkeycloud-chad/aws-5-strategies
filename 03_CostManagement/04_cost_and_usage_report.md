## Enabling AWS Cost and Usage Report

The AWS Cost and Usage Report (CUR) allows you to receive detailed information about your AWS costs and usage, which can be delivered to an Amazon S3 bucket for further analysis. Follow these steps to enable and configure your AWS Cost and Usage Report.

### Step 1: Sign in to AWS Management Console
- **Access the Console**: Open your web browser and navigate to the [AWS Management Console](https://aws.amazon.com/console/).
- **Log in** with your AWS account credentials.

### Step 2: Navigate to the Billing and Cost Management Dashboard
- From the AWS Management Console, go to the **Services** menu.
- Click on **Billing** to open the Billing and Cost Management Dashboard.

### Step 3: Access the Cost and Usage Reports Section
- In the Billing and Cost Management Dashboard, select **Cost & Usage Reports** from the navigation pane on the left.

### Step 4: Create a New Report
- Click on **Create report**.
- Enter a **Name** for your report. Choose a name that makes it easy to identify the report's purpose, such as `DetailedUsageReport`.

### Step 5: Configure Report Content
- Check the box for **Include resource IDs** to include the IDs of individual resources in the report. This option provides more detailed visibility into which resources are incurring costs.
- Click **Next**.

### Step 6: Define Report Storage
- Enter the **S3 bucket name** where you want the reports to be stored. You must have the necessary permissions to use this bucket.
- Click **Configure** to set up permissions, or if already configured, verify the settings. AWS will provide a policy that you need to apply to your S3 bucket to allow the AWS Cost and Usage Report service to deliver reports to it.

### Step 7: Configure Report Preferences
- Choose the **Report path prefix** if you want to organize your reports in a specific folder structure within the bucket.
- Select the **Time granularity** (hourly or daily) to determine how frequently data is aggregated in your reports.
- Choose the **Report versioning** option to have each report overwrite the previous one or to deliver a new report version each time.
- Select the data integration formats: **CSV**, **Parquet**, or both.
- Click **Next**.

### Step 8: Review and Complete Setup
- Review all your settings to ensure they are correct.
- Click **Review and Complete** to finalize the setup.
- AWS will start delivering your Cost and Usage Report to the specified S3 bucket according to the schedule you've set.
