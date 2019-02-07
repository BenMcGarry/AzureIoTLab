---
title: Development Environment
category: Setup
order: 4
---

**Note: Some of these steps may have already been completed on your system. Please check with the instructor which steps are still required to be completed.**

1. Install the [Arduino IDE](https://www.arduino.cc/en/Main/Software). This provides the necessary tools for compiling and uploading Arduino code. **Use the Windows Installer not the Windows App**

1. We need to get Visual Studio Code installed. Go [here](https://code.visualstudio.com/Download) and click the Windows Download.

    ![VS Code Download]({{ site.baseurl }}/img/vscode.png)

    When prompted to Run or Download. Hit Run and continue with the installation. Select the following options when prompted:

    ![VS Code Install]({{ site.baseurl }}/img/vscodeinstall.png)

1. Launch VS Code, look for Arduino in the extension marketplace and install it.

    ![Arduino Install]({{ site.baseurl }}/img/installarduino.png)

1. Look for **Azure IoT Tools** in the extension marketplace and install that too.

1. We now need to configure VS code with Arduino settings.

    In Visual Studio Code, click **File > Preference > Settings.** On the left **expand Extensions** then select **Arduino Configuration**.

1. Under **Arduino: Additional URLs**, select **Edit in settings.json** then add the below to the **User Settings** window on the right.

    ```"arduino.additionalUrls": "https://raw.githubusercontent.com/VSChina/azureiotdevkit_tools/master/package_azureboard_index.json"```  

1. Under **Arduino: Command Path** enter the following details:

    ```C:\\Program Files (x86)\\Arduino```

    It should look like the image below.

    ![Arduino Settings]({{ site.baseurl }}/img/arduinosettings.png)

1. Click **F1** to open the command palette, type and select **Arduino: Board Manager.** Search for **AZ3166** and install the latest version. If you get any Firewall prompts, allow them.

    We now need to install the drivers for the IoT DevKits USB interface so it can communicate with the machine.

1. Go **[here]({{ site.baseurl }}/resources/en.stsw-link009.zip)** and download and install the latest USB drivers. Run **dpinst_amd64.exe,** click Install on any prompts.

Your development environment is now all set up for the lab!. **Please disconnect your device from the computer**. We will now provision the device.

## [Next]({{ site.baseurl }}/01setup/deviceprovision)