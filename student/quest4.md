# Quest 4 - Master's trail

[< Quest 3](quest3.md) - **[🏠Home](../README.md)**

🌟
🕒 10 mins

## Introduction

Our SAP security folks need more power! In this section we will enhance the playbook and expand the user locking scope to Azure AD. After all, shutting that suspicious user out on SAP is not enough. We need to make sure that the user is locked out of all the systems that the user has access to.

## The path

- Explore the [Microsoft Graph API](https://learn.microsoft.com/graph/api/user-update?view=graph-rest-1.0&tabs=http) and [explorer](https://developer.microsoft.com/graph/graph-explorer) to learn more about the Azure AD user entity and how to block a user.
- Add a new step to the playbook to lock the user in Azure AD with the built-in Logic Apps connector for Azure AD to update users.
- Add an additional flow step after to reply to the preceding Teams message to notify successful AAD block using the Teams connector with the `reply to` action. It was used before in your Logic App for the SAP blocking part too.

If you succeed you successfully locked yourself out and threw away the 🗝️. Well done!

Claim your badge [here](https://webhostingforconverter.z16.web.core.windows.net/claim-reward.html).

## Where to next?

[< Quest 3](quest3.md) - **[🏠Home](../README.md)**

[🔝](#)
