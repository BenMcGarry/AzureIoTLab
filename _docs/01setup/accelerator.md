---
title: Remote Monitoring Solution Accelerator
category: Setup
order: 2
---

Before you can configure your IoT device, you need to deploy your Remote Monitoring Solution Accelerator and add a new physical device to the solution.

The **MXChip DevKit** device you use in this lab sends data to an instance of the Remote Monitoring solution accelerator. 

To deploy a Remote Monitoring solution, go to the Solution Accelerator website [here](https://www.azureiotsolutions.com/Accelerators).

1. Select **Remote Monitoring** and click on the **Try Now** button. 

1. **Sign in with the account you just activated your Azure Subscription on.**

1. Use the following information for the Remote Monitoring solution:
    - **Deployment name**: Give it a name
    - **Azure Subscription**: Select your subscription
    - **Deployment options**: C# Microservices
    - **Azure Location**: West Europe 

    Click **Create** at the bottom of the page and the Remote Monitoring solution will start to provision. This will take around 30 minutes so we will continue with the setup. **Please leave the tab open**.
    
When the provisioning is eventually complete, Click **Go to your solution accelerator** to open the solution dashboard. If you are prompted for any permissions, just accept them.

![Remote Monitoring Solution Dashboard]({{ site.baseurl }}/img/solutiondashboard.png)

While the Solution Accelerator is provisioning, we will configure the **MXChip** and check back later.

## [Next]({{ site.baseurl }}/01setup/device)