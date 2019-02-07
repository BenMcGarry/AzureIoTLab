---
title: Deploy the Remote Monitoring Solution Accelerator
category: Setup
order: 2
---

Before you can configure your IoT device, you need to deploy your Remote Monitoring Solution Accelerator and add a new physical device to the solution.

The **MXChip DevKit** device you use in this lab sends data to an instance of the Remote Monitoring solution accelerator. 

To deploy a Remote Monitoring solution, go [here](https://www.azureiotsolutions.com/Accelerators) and log in using your Microsoft Account with an Azure subscription. 

1. Select **Remote Monitoring** and click on the **Try Now** button. 

1. Use the following information for the Remote Monitoring solution:
    - **Deployment name**: Give it a name
    - **Azure Subscription**: Select your subscription
    - **Deployment options**: C# Microservices
    - **Azure Location**: West Europe 

    Click **Create** at the bottom of the page and wait for the Remote Monitoring solution to provision. When the provisioning is complete, Click **Go to your solution accelerator** to open the solution dashboard. If you are prompted for any permissions, just accept them.

    ![Remote Monitoring Solution Dashboard]({{ site.baseurl }}/img/solutiondashboard.png)


We have now setup the Solution Accelerator, now we will configure the **MXChip DevKit**.


## [Next]({{ site.baseurl }}/01setup/device)