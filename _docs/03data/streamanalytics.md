---
title: Stream Analytics
category: Data
order: 1
---

We want to setup a PowerBI dashboard using a live stream of data from the MXChip and a historic stream from a PaaS SQL database. This is not configured in the IoT hub by default so we need to create a Stream Analytics query to output the telemetry to a PowerBI data source and a SQL DB.

1. In the [Azure Portal](https://portal.azure.com), In the left-hand blade, click on **Resource Groups** and select your IoT resource group. You will see all the resources that make up the IoT solution accelerator here.

    ![Resource Group]({{ site.baseurl }}/img/resourcegroup.png)

1. Click the **+ Add** button at the top of the blade, in the search box type **Stream Analytics job**. When it appears click it and click the **Create** button when the blade opens. Use the following settings for the Stream Analytics job:

    ![Stream Analytics Search]({{ site.baseurl }}/img/search.png)

    - **Job name**: Give it a name
    - **Subscription**: Select your subscription
    - **Resource group**: Select your existing IoT resource group
    - **Location**: West Europe
    - **Hosting environment**: Cloud
    - **Streaming units**: 1  

    Then click **Create**.

    ![Stream Analytics]({{ site.baseurl }}/img/streamanalytics.png)powerbiauth.png

    When it is created you should see a screen like this:

    ![Stream Analytics Dashboard]({{ site.baseurl }}/img/streamanalyticsdash.png)  

1. You need to configure the Input. This is where Stream Analytis gets the data from, in this case its directly from the IoT Hub. Click **Inputs** on the left-hand blade menu then click **+ Add stream input**. Choose **IoT Hub** from the options.

1. Give the Input the alias of **DeviceTelemetry** and ensure **Select IoT Hub from your subscriptions** is selected. It should automaticly pre-fill the options from your IoT Hub as you only have one. Click **Save**.

    ![Stream Input]({{ site.baseurl }}/img/streaminput.png)

1. Now you need to add a PowerBI output to the job. Click **Outputs** in the left-hand blade, then click **+ Add** and choose **Power BI** from the list.

1. Use the the following settings:

    - **Output alias**: PowerBi
    - **Dataset name**: Give it a name of your choice
    - **Table name**: Give it a name of your choice 

    Now click **Authorize**. You will need authorise using an account with a PowerBI subscription, or alternatively, sign up for a free one using the link. **This requires a custom company email domain rather than your @outlook.com account.**

    ![PowerBI Authorisation]({{ site.baseurl }}/img/powerbiauth.png)

1. Now you have your first output, you can go back to the Stream Analytics query and direct some data into it. Close the Outputs blade to return back to the main Stream Analytics blade.

1. On the left-hand blade, click **Query** and a window should open for you to type your query into. In the main window enter the following query:

    ```
    SELECT
        *
    INTO
        [PowerBI]
    FROM
        [DeviceTelemetry]
    WHERE
        IoTHub.ConnectionDeviceId = 'AZ3166'
    ```

    Hit **Save** at the top. Once saved close the Query blade.

    This is selecting all messages (*) from the DeviceTelemetry stream where the Device ID is DevKit, and directing them into your new PowerBI output. If you gave your PowerBI output an alias different to PowerBi, ensure that you use your alias in the INTO field.

1. Go back to the main Stream Analaytics page and click **Start** at the top, this will start the processing. For the Job output start time ensure **Now** is selected and click **Start**. It will take a few minutes to start but you should see the status change to Running when completed.

    Now data will be sent from the MXChip directly to a live streaming feed in PowerBI.

Now we will create an Azure SQL Database for hold the historic data.

## [Next]({{ site.baseurl }}/03data/sqldb)