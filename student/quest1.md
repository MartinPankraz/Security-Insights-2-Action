# Quest 1 - Novice's path

[< Quest 0](quest0.md) - **[🏠Home](../README.md)** - [ Quest 2 >](quest2.md)

🌟
🕒 20 mins

## Introduction

In this section we will raise an incident in Microsoft Sentinel by navigating to the "watched" transaction SE80 in SAP and investigate the incident details.

## Video guide provided by our Mentors

<p align="center" width="100%">
    <a href="https://youtu.be/eoByMm89DH0" target="_blank" rel="noopener noreferrer">
        <img alt="Walkthrough video link" src="../img/student/Quest1/youtube-teaser.png"  width="800">
    </a>
</p>

The video shall provide hints where lore, poetic code snippets, and narrative cannot.

## The path

Use the [SAP WebGUI]() to connect to the provided SAP system with your given user. The navigation bar and the prompt `SE80` get the scenario started. Incident collection runs every 5 minutes, so you will be investigating another recent incident till your own personal arrives to familiarize yourself with the process.

<p align="center" width="100%">
<img alt="Connection Details" src="../img/student/Quest1/path.jpg"  width="600">
</p>

Find your way to the [shared Sentinel instance](https://portal.azure.com/?feature.customportal=false#view/Microsoft_Azure_Security_Insights/MainMenuBlade/~/6/id/%2Fsubscriptions%2F29198fb7-1044-4412-8cab-a054d04cb6f5%2Fresourcegroups%2Frg-demo-eunorth%2Fproviders%2Fmicrosoft.securityinsightsarg%2Fsentinel%2Fsen-demo-eunorth-001) using your given M365 user and navigate to the **Incidents** tab. You should see incident with id `1` raised by the SAP System `S4H`. Click on the incident (View full details) to see the details and identify which SAP user and which transaction caused it.

Can you learn anything from the description, evidence, and the related entities?

Continue to the watchlist section under Configuration, identify the relevant list to learn which transaction codes are currently considered sensitive. Use the button `View in Logs` to expand values.

## Where to next?

[< The Journey](quest0.md) - **[🏠Home](../README.md)** - [ Quest 2 >](quest2.md)

[🔝](#)
