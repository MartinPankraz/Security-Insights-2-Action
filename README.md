# 🕵️ Security-Insights 2 Action with SOAR 🚀 - Automatic locking of users on suspicious activity in SAP systems

`Content supporting hands-on session 1 "Automatisches Sperren von Benutzern bei ungewöhnlichen Aktivitäten" @ DSAG Technology Days March 2023`

Security incidents **affect every company** at some point. Given the threat landscape: It is **not** a question of **if but when**. According to [Statista 2022](https://www.statista.com/statistics/1275029/length-of-downtime-after-ransomware-attack/) the average downtime duration increases year over year and circles around 22 days currently. That is enough for some companies to suffer considerable damage or even go out of business. **SAP systems are a prime target** for cyber attackers.

The ability to detect suspicious activity automatically and timely react on them is key to reduce damage. This practice is called `Security Orchestration, Automation and Response (SOAR)`.

## 🔭 Introduction

In this hands-on session you will embark on a journey to design automatic workflows based on raised security incidents from SAP S/4HANA. You will learn how to use Azure Sentinel to detect suspicious activity and how to automate the locking of users in SAP systems and Azure AD.

## 🧙🏾‍♀️Epic Quests

Before you go: verify [prerequisites](PREREQUISITES.md) are met (backpack, lunch box, good-bye kiss, haunted jewelry, etc.)

0. [The Journey](student/quest0.md) - Where will those quests take us
1. [Novice's path](student/quest1.md) - Raise an incident in Microsoft Sentinel and investigate the incident details
2. [Apprentice's curious road](student/quest2.md) - Understand the workflow and see the `SAP user blocking` in action
3. [Debutant's journey](student/quest3.md) - Adjust the workflow blueprint to add the transaction code to the Microsoft Teams message
4. [Master's trail](student/quest4.md) - Go all in and add Azure AD user locking

🏆Finish the final quest, collect the pass phrase, and redeem it to [claim your badge](https://webhostingforconverter.z16.web.core.windows.net/claim-reward.html) 😎

Get the slide deck from [here](https://aka.ms/dsagtt23-sentinel-slides).

## ✨Recommended courses and further learning

### Applied security science

- [Ransomware struck on-premises but Azure Cloud survived | a customer story](https://customers.microsoft.com/en-us/story/1512571257640211870-campari-group-consumer-goods-sap-on-azure)
- [Get started with SAP and Azure integration scenarios](https://learn.microsoft.com/azure/sap/workloads/integration-get-started)
- [Microsoft Sentinel solution for SAP® applications: security content reference](https://learn.microsoft.com/azure/sentinel/sap/sap-solution-security-content)

### Handy work

- Adaptive [Card Desginer](https://adaptivecards.io/designer/), the [Schema explorer](https://adaptivecards.io/explorer/AdaptiveCard.html), and the [templating language](https://learn.microsoft.com/adaptive-cards/templating/language)
- Outlook [Actionable Messages](https://learn.microsoft.com/outlook/actionable-messages/) and [Debugger](https://appsource.microsoft.com/product/office/wa104381686?tab=overview&exp=ubp8)
- [Kusto Query Language Overview](https://learn.microsoft.com/azure/data-explorer/kusto/query/)
- [Kusto Query learning exercise - Data Detective](https://detective.kusto.io/)

### SAP Legacy interfaces at their best

- [Connect to SAP RFCs/BAPIs from workflows in Azure Logic Apps](https://learn.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector)

## 📢Feedback

This repos encourages contributions and feedback via the [GitHub Issues](https://github.com/MartinPankraz/Security-Insights-2-Action/issues/new/choose).

## 🚸 Adventure Guides [🔗](mentor/quest1.md)

- [Holger Bruchelt - Microsoft Engineering](https://www.linkedin.com/in/holger-bruchelt/)
- [Martin Pankraz - Microsoft Engineering](https://www.linkedin.com/in/martin-pankraz/)
- [Ofer Inbar - Microsoft Sentinel Engineering](https://www.linkedin.com/in/ofer-inbar/)
- [Sebastian Ullrich - Microsoft Cloud Solution Architect](https://www.linkedin.com/in/sebastian-ullrich-677b36168/)
- [Martin Steiner - Microsoft Security Cloud Solution Architect](https://www.linkedin.com/in/martin-steiner-28312b141/)
