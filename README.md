# Day-6-Deploying-a-Windows-Server-on-Vultr-Cloud

In today’s post, I’ll be going through the process of deploying a Windows Server on Vultr Cloud. We’re moving our Windows Server and Ubuntu Server out of VPC 2.0 because we want them to be publicly accessible on the internet. This step-by-step tutorial will show you how to deploy a Windows Server with minimal effort.

## Logical Diagram

*(Include your diagram here)*

## Step 1: Login to Vultr Cloud

To get started, log in to your Vultr Cloud account. Once you’re logged in, navigate to the top right corner of the dashboard and click on the **Deploy +** button to create a new server.

## Step 2: Choose the Server Type

For this deployment, we will use **Cloud Compute — Shared CPU**. This option is ideal for light processing tasks and is cost-effective for smaller workloads, such as the one we are setting up.

## Step 3: Select Your Preferred Plan

Next, you’ll need to select a plan for your Windows Server:

- **Plan Type:** Regular Cloud Compute
- **Configuration:** 55GB SSD storage, 1 vCPU, and 2GB memory

This setup provides a solid balance between cost and performance, suitable for general use cases and basic Windows Server tasks.

## Step 4: Deploy Your Windows Server

After selecting your preferred plan, click on the **Deploy Now** button. The installation process will begin, and it usually takes around 5 to 7 minutes to complete.

## Step 5: Access Your Windows Server

Once the installation is complete, you’ll receive the credentials for your new Windows Server from Vultr Cloud. Use these credentials to log in to your server. Now, your Windows Server is ready and publicly accessible on the internet!

## Conclusion

Deploying a Windows Server on Vultr Cloud is a straightforward process that can be completed in just a few minutes. This setup is perfect for those looking to make their server publicly available while keeping costs low. Stay tuned for more tutorials.
