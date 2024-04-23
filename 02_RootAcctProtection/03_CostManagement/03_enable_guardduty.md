## Configuring AWS GuardDuty in a Single Region

AWS GuardDuty is a threat detection service that continuously monitors for malicious or unauthorized behavior to help protect your AWS accounts and workloads. The following steps will guide you through setting up GuardDuty in a single region using the default configuration settings.

### Step 1: Sign in to AWS Management Console
- **Open your browser** and navigate to the [AWS Management Console](https://aws.amazon.com/console/).
- **Log in** with your AWS account credentials.

### Step 2: Open the GuardDuty Console
- From the AWS Management Console, go to the **Services** menu.
- Find and click on **GuardDuty** under the Security, Identity, & Compliance section.

### Step 3: Activate GuardDuty
- If this is your first time using GuardDuty, the console will display a welcome screen with an **"Get Started"** button. Click on it.
- If GuardDuty has been previously activated and then suspended in your account, you may instead see a dashboard. In this case, look for the **"Resume"** button and click it.

### Step 4: Confirm Region and Enable GuardDuty
- Verify that the correct region is selected in the region selector at the top right corner of the navigation bar. GuardDuty will be activated for the region you are currently viewing.
- On the Get Started or Resume GuardDuty screen, confirm by clicking **"Enable GuardDuty"**.

### Step 5: Review Default Configuration
- Upon enabling GuardDuty, it will use its default settings for threat detection. This includes monitoring and analyzing data such as CloudTrail Logs, VPC Flow Logs, and DNS logs.
- You do not need to perform any additional configuration steps to accept these defaults.

### Step 6: Explore the GuardDuty Dashboard
- Once activated, explore the GuardDuty dashboard. Here you can review findings, update settings, and manage other security features.
- GuardDuty automatically begins to analyze and process the data to detect potential security threats and displays any findings on the dashboard.

Remember, GuardDuty operates on a per-region basis. If you need protection in multiple regions, you will need to repeat these steps for each region where you want GuardDuty enabled.

