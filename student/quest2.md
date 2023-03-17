# Quest 2 - Apprentice's curious road

[< Quest 1](quest1.md) - **[🏠Home](../README.md)** - [ Quest 3 >](quest3.md)

🌟🌟
🕒 10 mins

## Introduction

In this section we will work with your playbook assigned to your "personal SAP incident" raised in Quest 1 to execute a workflow to inform the SAP security folks with an actionable alert in Microsoft Teams.

## The path

1. Navigate to the resource group [`dsag-participants`](https://portal.azure.com/#@cloud.boban.co/resource/subscriptions/29198fb7-1044-4412-8cab-a054d04cb6f5/resourceGroups/dsag-participants/overview) or choose [`Active Playbooks`](https://portal.azure.com/#view/Microsoft_Azure_Security_Insights/MainMenuBlade/~/Automation/id/%2Fsubscriptions%2F29198fb7-1044-4412-8cab-a054d04cb6f5%2Fresourcegroups%2Frg-demo-eunorth%2Fproviders%2Fmicrosoft.securityinsightsarg%2Fsentinel%2Fsen-demo-eunorth-001) from the Automation pane in Sentinel to find your Logic App (or in other words Sentinel playbook). The instance name contains your user name.

2. Familiarize yourself with the playbook and its various steps. Are you able to identify how the SAP user lock request is submitted to SAP? What Teams Channel ID is being used?

> **Note**: The Microsoft Teams connector supports dynamic dropdowns showing the names of your Teams team and channel. However, for maintenance and good design practice on the Logic App we chose to use variables for re-usability. This way you may change the target channel for all occurrences of the Teams task on the Logic App in one place. You may retrieve the IDs from Teams via the three dots ... and `Get link to team`, `Get link to channel` or from the URL once you navigated there.

3. Open a new tab and navigate to [teams.microsoft.com](https://teams.microsoft.com/_#/conversations/General?threadId=19:KonRsOls_Pbe9OCeWzF68sAdhZURrmvq0i6CWLsRFWs1@thread.tacv2&ctx=channel), login with your given M365 sandbox user (e.g. dsag01@M365B596876.onmicrosoft.com) and find your Teams Channel within the team `DSAG Hands-On Session 1`. Your incident notifications from Sentinel will show up here.

4. In case your alert rule didn't trigger an execution yet, feel free to intentionally execute from the Sentinel Incident UI. Choose again Actions -> Run playbook.

<p align="center" width="100%">
<img alt="Connection Details" src="../img/student/Quest2/run-playbook.png"  width="500">
</p>

5. Find the adaptive card posted to your Teams Channel and click on the `Block User on...` button.

> **Note** - Optionally see the [Outlook message](https://outlook.office.com/mail/) informing about and linking to the Microsoft Teams message.

<p align="center" width="100%">
<img alt="Connection Details" src="../img/student/Quest2/submit-lock.png"  width="600">
</p>

6. You will see the adaptive card change. Shortly after a message from SAP will be posted as reply to your initial block request in the same Teams thread.

> **Note** - you may follow the detailed execution steps from your Logic App's `Runs history`. Navigate to the Overview pane and choose the ribbon `Runs history`.

7. Verify that you locked the SAP backend user that caused the incident (yourself 😉 in this case) by trying to log in via the [SAP WebGUI](https://51.137.42.4:44300/sap/bc/gui/sap/its/webgui?sap-client=001&sap-language=EN). And don't worry we posted the unlock option via Teams too.

<p align="center" width="100%">
<img alt="Connection Details" src="../img/student/Quest2/locked-user.png"  width="300">
</p>
8. Make sure to unlock the user again by leveraging the unlock option via Teams mentioned above!
9. </p>
## Where to next?

[< Quest 1](quest1.md) - **[🏠Home](../README.md)** - [ Quest 3 >](quest3.md)

[🔝](#)
