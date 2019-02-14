---
title: Device Provisioning
category: Setup
order: 5
---

We now need to the IoT device provisioned and talking to Azure.

1. In Visual Studio Code, in the bottom left corner look for **"Azure IoT Hub Devices"**. Click it then select **"Set IoT Hub Connection String"**.

    ![IoT Hub]({{ site.baseurl }}/img/iothub.png)

    A menu should appear at the top asking for the string to me input. For now minimise Visual Studio Code as we need to get the string.

    ![IoT Connection String]({{ site.baseurl }}/img/iotstring.png)

1. Go to the [Azure Portal](https://portal.azure.com), click **Resource Groups** on the left blade then click the resource group that contains your Remote Monitoring solution.

1. Click on **IoT Hub** within the resource group then on the left blade select **Shared access policies**. Click the **registryRead** policy to reveal the shared access keys.

1. Copy the **Connection string - primary key** then go back to Visual Studio Code and enter the connection string in the box that appeared previously. If it has disappeared, repeat the steps above until it shows.

    Once entered, you should see a list of green devices appear under Azure IoT Hub Devices.

    ![IoT Devices]({{ site.baseurl }}/img/iotdevices.png)

1. Reconnect your Dev Kit to the computer. VS Code will detect the device and open the Azure IoT Device Workbench.

1. Scroll down and you should see the **Remote Monitoring** solution. Click **Open Sample** and it should open up a new window with the project and code sample. **Select the default location it gives you for the workbench folder**.

    ![Code Sample]({{ site.baseurl }}/img/codesample.png)

We now need to add the physical device to Solution Accelerator.

1. Go back to your Solution Accelerator tab, it should now have provisioned. Click **Go to your solution accelerator** to go to the portal. **Accept any permissions it requests**. You should now see the Remote Monitoring dashboard. On the left click **Devices** then click **+ New device** at the top right.

    ![New Device]({{ site.baseurl }}/img/newdevice.png)

1. Fill in the New device form with the following details:

    - Device: **IoT Device**
    - Type: **Real**
    - Device ID: **AZ3166**
    - Authentication type: **Symmetric Key**
    - Authentication key: **Auto generate keys**

Click **Apply** at the bottom. Wait for the portal to finish provisioning the device. 

1. It should show device connection strings after the provisioning is complete, copy the **Connection string primary Key** into a Notepad window as we will need this later.

Your device is now provisioned and ready to be used! Next we will build and upload the code to the device

## [Next]({{ site.baseurl }}/02build/deviceprog)