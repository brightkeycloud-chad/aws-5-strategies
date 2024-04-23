## Enabling AWS S3 Storage Lens and Creating a Default Dashboard with Advanced Metrics

AWS S3 Storage Lens offers a comprehensive view of object storage usage and activity across multiple accounts within your AWS Organization. It can help optimize storage costs and improve data protection. Here’s how to enable it and create a default dashboard with advanced metrics:

### Step 1: Sign in to AWS Management Console
- **Access the Console**: Open your web browser and navigate to the [AWS Management Console](https://aws.amazon.com/console/).
- **Log in** with your AWS account credentials.

### Step 2: Navigate to the Amazon S3 Console
- From the AWS Management Console, go to the **Services** menu.
- Click on **S3** under Storage.

### Step 3: Open S3 Storage Lens
- In the S3 console, select **Storage Lens** from the left sidebar.
- You will be directed to the Storage Lens dashboard page.

### Step 4: Create a New Dashboard
- Click on **Create dashboard**.
- Enter a **Name** for your dashboard, such as `MyStorageLensDashboard`.
- Optionally, you can add a description to help identify the dashboard.

### Step 5: Choose the Scope of the Dashboard
- You can select whether the dashboard should cover all S3 usage across your AWS account or specific regions or buckets.
- Choose **All regions** for the most comprehensive analysis.

### Step 6: Enable Advanced Metrics and Recommendations
- Under the **Metrics and Recommendations** section, toggle **Advanced metrics and recommendations** to Enabled.
- This option provides deeper insights, including additional metrics and cost efficiency recommendations.

### Step 7: Configure Export Settings (Optional)
- If you want to export your Storage Lens data, specify an S3 bucket where the report files will be delivered.
- Set the frequency and format of the export.

### Step 8: Review and Confirm
- Review all settings to ensure they are correct.
- Click on **Create dashboard** to finalize the creation of your Storage Lens dashboard.

### Step 9: Access Your Dashboard
- Once the dashboard is created, it will appear in the list of Storage Lens dashboards.
- Click on your newly created dashboard to view detailed metrics and recommendations.
