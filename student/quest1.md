# Quest 1 - Novice's path

[< Quest 0](quest0.md) - **[🏠Home](../README.md)** - [ Quest 2 >](quest2.md)

🌟
🕒 20 mins

## Introduction

In this section we will raise an incident in Microsoft Sentinel by navigating to the "watched" transaction SE80 in SAP and investigate the incident details. Familiarize yourself with the environment from the [Sentinel overview dashboard](https://portal.azure.com/#view/Microsoft_Azure_Security_Insights/MainMenuBlade/~/0/id/%2Fsubscriptions%2F29198fb7-1044-4412-8cab-a054d04cb6f5%2Fresourcegroups%2Frg-demo-eunorth%2Fproviders%2Fmicrosoft.securityinsightsarg%2Fsentinel%2Fsen-demo-eunorth-001).

<p align="center" width="100%">
<img alt="Sentinel Overview" src="../img/student/Quest1/overview.png"  width="800">
</p>

## The path

Use the [SAP WebGUI<sup>1</sup>](https://51.137.42.4:44300/sap/bc/gui/sap/its/webgui?sap-client=001&sap-language=EN) to connect to the provided SAP system with your given user (ignore certificate warning and proceed to the website). From the SAP Menu, select `Create Incident` which will start `SE80` and gets the scenario started. 

<p align="center" width="100%">
<img alt="Create Incident" src="../img/student/Quest1/CreateIncident.png"  width="800">
</p>

Incident collection runs every 5 minutes, so you will be investigating another recent incident till your own personal one arrives to familiarize yourself with the process.

> **Note**:
>
> <sup>1</sup> If you are familiar with the SAPGUI, you may connect using SID Q01, instance number 00, client 001 and app server IP 51.137.42.4 directly.

> **Warning**: some participants had restrictive browser settings in the past prohibiting access to a SAP CAL instance via SAP WebGUI with self-signed certificates. In case you encounter access issues please reach out to your mentor and discuss alternatives. We may trigger the transaction on behalf of your user as a last resort.

<p align="center" width="100%">
<img alt="Connection Details" src="../img/student/Quest1/sentinel-main.png"  width="800">
</p>

1. Find your way to the [shared Sentinel instance](https://portal.azure.com/?feature.customportal=false#view/Microsoft_Azure_Security_Insights/MainMenuBlade/~/6/id/%2Fsubscriptions%2F29198fb7-1044-4412-8cab-a054d04cb6f5%2Fresourcegroups%2Frg-demo-eunorth%2Fproviders%2Fmicrosoft.securityinsightsarg%2Fsentinel%2Fsen-demo-eunorth-001) using your given M365 user and navigate to the **Incidents** tab.

2. Adjust the filter to `last 7 days`. You should now see the incident with id `24` raised by the SAP System `Q01`. Click on the incident (View full details) to see the details and identify which SAP user and which transaction caused it.

> **Note**:
> If you are getting a security error, make sure that you are in the right Azure Directory. Click on the your user symbol on the top right and click on `Switch directory`
<p align="center" width="100%">
<img alt="Switch Directory" src="../img/student/Quest1/SwitchDirectory.png"  width="600">
</p>

On the line with `Contoso (cloud.boban.co)` click on Switch and try again.
<p align="center" width="100%">
<img alt="Switch Directory" src="../img/student/Quest1/SwitchDirectory2.png"  width="800">
</p>

Can you learn anything from the description, evidence, and the related entities?

Can you find the latest update time for the SAP Audit Log?

3. Open the Connectors page (Configuration -> Data Connectors), click on the `Microsoft Sentinel for SAP` connector, and navigate from `Open Connector Page`. To simplify the navigation, consider using either the search functionality or changing the status filter from All to Connected.

4. Continue to the watchlist section under Configuration, identify the relevant list to learn which transaction codes are currently considered sensitive. Use the button `View in Logs` to expand values.

By now your own personal incident should have arrived.

5. Navigate to it and select `Create Automation Rule` in the Actions dropdown.

<p align="center" width="100%">
<img alt="Connection Details" src="../img/student/Quest1/create-automation-rule.png"  width="800">
</p>

6. Choose your incident name, your account name (e.g. dsag01@M365B596876.onmicrosoft.com) as condition for your rule. Finally add your playbook (or in other words Azure Logic App) under the "Actions" section. Select the playbook which has again user name as part of the name.

This way only your individual interactions will be pushed to your personal workflow and Teams Channel.

<p align="center" width="100%">
<img alt="Connection Details" src="../img/student/Quest1/assign-playbook.png"  width="800">
</p>

7. Click apply.

## Where to next?

[< The Journey](quest0.md) - **[🏠Home](../README.md)** - [ Quest 2 >](quest2.md)

[🔝](#)
