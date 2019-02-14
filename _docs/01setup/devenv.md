---
title: Development Environment
category: Setup
order: 4
---

**Note: Some of these steps may have already been completed on your system. Please check with the instructor which steps are still required to be completed.**

1. Download and Install the [Arduino IDE](https://www.arduino.cc/en/Main/Software). This provides the necessary tools for compiling and uploading Arduino code. **Use the Windows Installer not the Windows App**. Continue through the installer and **install any device software it asks**.

1. We need to get Visual Studio Code installed. Go [here](https://code.visualstudio.com/Download) and click the Windows Download.

    ![VS Code Download]({{ site.baseurl }}/img/vscode.png)

    When prompted to Run or Download. Hit Run and continue with the installation. Select the following options when prompted:

    ![VS Code Install]({{ site.baseurl }}/img/vscodeinstall.png)

1. Launch VS Code, look for **Arduino** by Microsoft in the extension marketplace and install it.

    ![Arduino Install]({{ site.baseurl }}/img/installarduino.png)

    **Note:** If you get any Firewall prompts, please allow them.

1. Look for **Azure IoT Tools** by Microsoft in the extension marketplace and install that too.

    We now need to install the drivers for the IoT DevKits USB interface so it can communicate with the machine.

1. Go **[here]({{ site.baseurl }}/resources/en.stsw-link009.zip)** and download and install the latest USB drivers. Run **dpinst_amd64.exe** and click **Install** on any prompts.

Your development environment is now all set up for the lab!. **Please disconnect your device from the computer**. We will now provision the device.

## [Next]({{ site.baseurl }}/01setup/deviceprovision)