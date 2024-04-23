## Creating an AWS Zero-Spend Budget Using the 1-Click Template

AWS offers a 1-click template to quickly set up a zero-spend budget, which is ideal for monitoring accounts where no spending is expected. This can be particularly useful for test environments or projects that should incur no costs. Follow these steps to create your zero-spend budget.

### Step 1: Sign in to AWS Management Console
- **Access the Console**: Open your web browser and navigate to the [AWS Management Console](https://aws.amazon.com/console/).
- **Log in** with your AWS account credentials.

### Step 2: Navigate to the AWS Budgets Dashboard
- From the AWS Management Console, go to the **Services** menu.
- Click on **Cost Management** and then select **Budgets** to open the AWS Budgets Dashboard.

### Step 3: Use the 1-Click Template
- In the AWS Budgets Dashboard, you'll find an option for creating budgets using a 1-click template.
- Click on the **Create budget** button.
- Select the **1-Click** tab. Here, AWS provides several predefined templates, including the zero-spend budget template.

### Step 4: Select the Zero-Spend Budget Template
- Locate the zero-spend budget template from the list of available templates. This template is specifically designed to alert you if any costs are incurred.
- Click on the template to select it.

### Step 5: Configure Notification Settings
- Once you select the zero-spend budget template, you will need to configure how you want to receive notifications.
- Enter your **email address** or set up an **Amazon SNS topic** to receive alerts. This step is crucial to ensure you are promptly informed of any unexpected charges.

### Step 6: Review and Confirm the Budget
- After setting your notification preferences, review all settings to ensure they meet your requirements.
- Ensure that the budget amount is set to **$0.00** and that the alert is set to trigger at any expenditure.
- Click on **Confirm and create** to finalize the creation of your zero-spend budget.
