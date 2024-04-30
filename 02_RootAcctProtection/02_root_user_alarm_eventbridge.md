## Monitoring Root Account Usage with AWS EventBridge

This guide details the steps to set up a rule in AWS EventBridge for monitoring all activities performed by the root user account.

### Prerequisites
- Ensure you have administrative access to the AWS Management Console.
- AWS CloudTrail should be enabled to record API activities.

### Steps to Set Up the Rule

#### **Step 1: Access EventBridge**
- Sign in to the **AWS Management Console**.
- Navigate to **EventBridge** under Application Integration services.

#### **Step 2: Create a New Rule**
- Click on **Rules** in the left-hand navigation panel.
- Press the **Create rule** button.

#### **Step 3: Define the Event Pattern**
- Provide a name for your rule, such as `RootAccountMonitoring`.
- Set the rule type to **Event pattern**.
- Select **Custom pattern** and enter the following JSON to target root account activities:

```json
{
  "source": ["aws.signin"],
  "detail-type": ["AWS API Call via CloudTrail"],
  "detail": {
    "userIdentity": {
      "type": ["Root"]
    }
  }
}
```

#### **Step 4: Select the Event Bus**
- Choose the **default** event bus.

#### **Step 5: Specify the Target**
- Click on **Add target**.
- Choose the service that will handle the event (e.g., AWS Lambda, SNS, SQS).
- Configure the specific settings for your target.

#### **Step 6: Finalize the Rule**
- Optionally, add tags for easier management.
- Review all settings and click **Create rule** to finalize.

#### **Step 7: Test the Configuration**
- Simulate root account activity to ensure the rule triggers appropriately.
- Verify the response from the configured target service.

### Conclusion
This setup enables effective monitoring of the root account, enhancing your AWS security by alerting you to potentially critical activities.

