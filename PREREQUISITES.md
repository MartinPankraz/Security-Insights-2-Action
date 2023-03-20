# Prerequisites

**[🏠Home](README.md)** - [ Quest 0 >](student/quest0.md)

- Ensure availability of SAP NetWeaver system (e.g. using [SAP CAL](https://cal.sap.com/) - Fully activated Appliance) with **static** IP address
- Access to Azure subscription with rights to deploy resources (consider [free sign-up](https://azure.microsoft.com/free/) for easy sandboxing, note: sign-up is gated by credit card but **no charges will occur**)
- Access to Microsoft Teams and Office tenant (consider sign-up with [M365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) for easy sandboxing)

> **Note** - have a look at [this document](RequestMS365Developer.pdf) for additional guidance for the M365 Dev Program sign-up process.

## Additional preparations (already done for a hosted Hands-On sessions)

### Create a new Azure Sentinel Workspace

Maintain the SAP Watchlist in Azure Sentinel. To do so, we need to create a new Azure Sentinel Workspace.

### Configure SAP and the Microsoft Sentinel Collector

Use the [official documentation](https://learn.microsoft.com/azure/sentinel/sap/deployment-overview).

### Spin up and configure Azure API Management for SAP SOAP

- Create and activate an enterprise service from the SAP function module BAPI_USER_LOCK and BAPI_USER_UNLOCK. Blogs like [this](https://www.saptechnicalguru.com/interfacing-exposing-web-services/) might help with the setup.
- Generate the SOAP service binding via SOAMANAGER in SAP and save the WSDL to a file.
- Import the WSDL into your Azure API Management instance, choose Interface `your maintained SOAP binding name` and maintain import method `SOAP to REST`.

> **Warning**: Some SOAP services and their WSDL's contain incompatible attributes like `wsp:Policy`. You need to drop them from the WSDL before you are able to import.

- Consider simplifying the SOAP body in your API Management Design view. We recommend dropping all entities from the inbound section except

```xml
<urn:BAPI_USER_LOCK>
    <RETURN>
    </RETURN>
    <USERNAME>{{body.bAPI_USER_LOCK.uSERNAME}}</USERNAME>
</urn:BAPI_USER_LOCK>
```

## Where to next?

**[🏠Home](README.md)** - [ Quest 0 >](student/quest0.md)

[🔝](#)
