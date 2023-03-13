# Prerequisites

**[🏠Home](README.md)** - [ Quest 0 >](student/quest0.md)

- Ensure availability of SAP system S/4HANA 2022 or higher (e.g. using [SAP CAL](https://cal.sap.com/) - Fully activated Appliance) with **static** IP address
- Access to Azure subscription with rights to deploy resources (consider [free sign-up](https://azure.microsoft.com/free/) for easy sandboxing, note: sign-up is gated by credit card but **no charges will occur**)
- Access to Microsoft Teams and Office tenant (consider sign-up with [M365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) for easy sandboxing)

> **Note** - have a look at [this document](RequestMS365Developer.pdf) for additional guidance for the M365 Dev Program sign-up process.

- Ensure availability of the [On-premises data Gateway](https://www.microsoft.com/download/details.aspx?id=53127) with access to the SAP S/4HANA System. This is required to access RFC/BAPIs in the SAP system behind your firewall. In our case we have installed the required tools on the "Windows Remote Desktop" of the SAP S/4HANA 2022, Fully-Activated Appliance CAL system

## Additional preparations (already done for a hosted Hands-On sessions)

- Install the On-prem data Gateway with access to the SAP S/4HANA System. This is required to access RFC/BAPIs in the SAP system behind your firewall. In our case we have installed the required tools on the "Windows Remote Desktop" of the SAP S/4HANA 2022, Fully-Activated Appliance CAL system

## Configuration on the Azure Subscription

### Create a new Azure Sentinel Workspace

Maintain the SAP Watchlist in Azure Sentinel. To do so, we need to create a new Azure Sentinel Workspace.

### Configure SAP and the Microsoft Sentinel Collector

### Downloading required files

- Download the [On-premises data gateway](https://www.microsoft.com/download/details.aspx?id=53127); Similar like the SAP Cloud Connector the On-premises data gateway can establish a connection from systems behind your firewall to Azure.
- Download the [SAP .Net Connector](https://support.sap.com/en/product/connectors/msnet.html). Preferably select the **NCo 3.0**, Complied with .NET Framework 4. You need an S-User to sign-in and download this file.

## Installing  SAP .Net Connector

Start by installing the SAP .Net Connector. Just launch the SapNCox64Setup setup from the downloaded ZIP file and complete the installation.

## Installing the On-premises data gateway

Run the GatewayInstall installation file previously downloaded. In the last step you need to sign-in with your Azure Active Directory users (that is also used for your Azure subscription, so that we can later also use Logic Apps). Please make sure that during the installation you specify the Azure region from which you will also use your Logic Apps later on in the Azure subscription.

<p align="center" width="100%">
<img alt="OPDG Select region" src="img/student/Quest0/OPDG-Region.jpg"  width="600">
</p>

> **Note** - You might need to up the .NET Framework to the latest version (in case of the CAL images, an update to .NET Framework 4.8 is required). The easiest way is to do this using the [.NET Framework 4.8 Web Installer](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net48-web-installer)

## Where to next?

**[🏠Home](README.md)** - [ Quest 0 >](student/quest0.md)

[🔝](#)
