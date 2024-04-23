## Creating an AWS Config Rule for Required Tags

Ensuring that AWS resources are properly tagged according to organizational standards is crucial for management, cost tracking, and compliance. AWS Config allows you to enforce tagging policies by using the `required-tags` managed rule. Follow these steps to create this rule in your AWS account.

### Step 1: Sign in to AWS Management Console
- **Access the Console**: Open your web browser and navigate to the [AWS Management Console](https://aws.amazon.com/console/).
- **Log in** with your AWS account credentials.

### Step 2: Navigate to AWS Config
- From the AWS Management Console, go to the **Services** menu.
- Click on **Config** under the Management & Governance section.

### Step 3: Configure AWS Config (if not already set up)
- If AWS Config is not already set up, you will need to set up the service by specifying an S3 bucket for storing configuration history and changes, an IAM role for AWS Config to access your resources, and optionally an SNS topic for notifications.
- Follow the initial setup wizard to configure these components.

### Step 4: Create a New Rule
- In the AWS Config console, click on **Rules** in the left-hand navigation pane.
- Click on **Add rule**.

### Step 5: Choose the Managed Rule
- In the Add rule interface, you can either browse through the list or use the search box to find the rule.
- Type `required-tags` into the search box.
- Select the `required-tags` managed rule from the list.

### Step 6: Configure the Rule
- **Name your rule**: Enter a unique name for the rule, such as `RequireStandardTags`.
- **Description** (optional): Provide a description of what the rule does, e.g., "Ensures specific tags are present on all resources."
- **Rule parameters**:
  - **tag1Key**: Enter the key for the first required tag, e.g., `Project`.
  - Continue to add parameters for additional tags as needed, such as `tag2Key` for the second tag, etc.
- You can specify up to 6 tags that are required (tag1Key to tag6Key).

### Step 7: Choose Remediation Action (optional)
- If you want AWS Config to automatically remediate this rule when it is violated (e.g., tag the resources automatically), set up the remediation action.
- Select an SSM Automation document that applies the required tags and specify the necessary parameters for the SSM document to function.

### Step 8: Save the Rule
- Click on **Save** to create the rule.
- AWS Config will now evaluate the resources in your account against this rule and report on compliance.
