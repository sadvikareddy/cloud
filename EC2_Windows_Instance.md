 Amazon EC2 - Windows Instance Setup

 Steps to Launch a Windows Instance on EC2

 1. Log in to AWS Management Console
- Go to [AWS Management Console](https://aws.amazon.com/console/).
- Enter your credentials.

 2. Navigate to EC2 Service
- In the console, find and select **EC2** from the list of AWS services.

 3. Launch a New Instance
- Click on **Launch Instance** to begin setting up a new virtual machine.

 4. Choose an Amazon Machine Image (AMI)
- For a Windows server, select a Windows AMI (e.g., **Microsoft Windows Server 2019 Base**).
- Ensure the AMI is within the AWS Free Tier if you want to avoid charges.

 5. Select Instance Type
- Choose an instance type suitable for your workload. The `t2.micro` instance is a good starting point and is included in the Free Tier.

 6. Configure Instance Details
- Review the instance configuration settings. For a basic setup, default settings are sufficient.
- Optionally, configure networking, IAM role, shutdown behavior, and more.

 7. Add Storage
- Specify the storage size and type. The default size for Windows Server is usually adequate for basic usage.

 8. Configure Security Group
- Create a new security group with the following settings:
  - RDP (Remote Desktop Protocol): Port 3389 (to allow remote access to the Windows instance).
- Important: Set the source IP for RDP access to your IP to restrict public access.

 9. Review and Launch
- Review all configurations, then click on *Launch*.

 10. Choose or Create a Key Pair
- Select an existing key pair or create a new one to access your instance.
- Download the key pair file ('.pem') if you're creating a new one. **Keep this file secure** as it’s necessary for accessing your instance.

 11. Launch the Instance
- Click on Launch Instances. Your Windows instance will now start.

 Accessing Your Windows Instance

 1. Connect to Instance Using Remote Desktop
- Go back to the **EC2 dashboard**, select your instance, and click on **Connect**.
- Select **RDP Client** and download the **Remote Desktop file** provided.

 2. Decrypt Password
- In the Connect panel, click **Get Password**.
- Upload your key pair (`.pem`) file to decrypt the administrator password.
- Copy this password for remote access.

 3. Open Remote Desktop Connection
- Open the Remote Desktop application on your computer.
- Use the IP address of the instance (found in the EC2 dashboard) and paste the password to log in.

 4. Secure Access to Your Instance
- After connecting, it’s a best practice to configure firewalls, install necessary software, and secure your instance based on your project needs.

 Stopping and Terminating the Instance
- Stop the instance when not in use to avoid charges.
- Terminate the instance when it’s no longer needed.



