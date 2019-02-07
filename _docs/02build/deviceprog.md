---
title: Program the Device
category: Build
order: 1
---

Now we will program the device to get it talking to IoT Hub.

1. In the new opened project window, click **F1** to open the command palette, type and select **Azure IoT Device Workbench: Provision Azure Services**. Follow the step by step guide to finish provisioning your Azure IoT Hub and creating the IoT Hub device. **Make sure you select an existing hub**

1. In the bottom-right status bar, check the **MXCHIP AZ3166** is shown as selected board and serial port with **STMicroelectronics** is used.

    ![Workbench Setup]({{ site.baseurl }}/img/workbenchsetup.png)

1. Click **F1** to open the command palette, type and select **Azure IoT Device Workbench: Configure Device Settings**, then select Config Device Connection String > Select IoT Hub Device Connection String. Enter the **Connection string primary Key** you saved earlier. If you do not have it, delete and re-add the device in the portal.

1. On DevKit, hold down **button A**, push and release the **reset** button, and then release **button A**. Your DevKit will enter configuration mode and save the connection string.

1. Click F1 again, type and select **Azure IoT Device Workbench: Upload Device Code**. It will start to  compile and upload the code to DevKit.

    The DevKit will reboot and start running the code. In Visual Studio you should see the device turn from blue to green in the Azure IoT Hub Devices area, if it doesnt hit the refresh icon next to the title text.

## [Next]({{ site.baseurl }}/02build/testprog)