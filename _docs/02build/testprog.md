---
title: Test the Project
category: Build
order: 2
---

We will now test the project to ensure that data is being sent from the MXChip to Azure IoT services.

The device will now send data over Wi-Fi to your Azure IoT Suite. To see the results, follow these steps:

1. Go to your Azure IoT suite and click **Dashboard**. If you have closed the tab, go to the solution accelerator website and re-launch the created solution.

    On the page, you should be able to see the status of your DevKit sensors. For example on the telemtry area, click Humidity and you should see the AZ3166 device listed with real data.

    ![Device Telemetry]({{ site.baseurl }}/img/iotdata.png)

    On the Devices tab, if you click on the sensor name (AZ3166), a tab opens on the right side of the dashboard where you can see the MX Chip sensors chart in real time.

    ![Specific Device Telemetry]({{ site.baseurl }}/img/iotdata2.png)

Now we have confirmed the MX Chip is sending data to Azure, we can start to properly visualise the data in PowerBI.

The next tutorial walks you through creating two PowerBI dashboards; one a realtime chart from a live streaming dataset and the other from data sent to a SQL database.

Building dashboards in Power BI means that you can also make each panel interact with one another as you select specific pieces. For example, you could have a filter that shows you only information about your simulated trucks and each piece of your dashboard would interact to show you only simulated truck information. If you would like to use a tool other than Power BI, you can also extend these steps to use your visualization tool of choice and hook into the Cosmos Database, or custom database if you've set one up. 

## [Next]({{ site.baseurl }}/03data/streamanalytics)