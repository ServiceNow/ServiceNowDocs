---
title: PowerShell connector methods
description: The PowerShell connector methods act as interfaces with the Microsoft PowerShell to send requests and get responses in the RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/connector-powershell-methods.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ITSM connector, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# PowerShell connector methods

The PowerShell connector methods act as interfaces with the Microsoft PowerShell to send requests and get responses in the RPA Desktop Design Studio.

## CreateShell

Acts as an interface to pass your inputs in the form of commands and scripts. The CreateShell method is the first method you must use.

## InvokeCommand

Runs commands and block of scripts on local or remote computers and gets the output including errors, if any.

**Note:** You must execute the CreateShell method before executing this method.

-   **Input**

    [Command \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)


## InvokeScript

Runs a script on local or remote computers and gets the output.

**Note:** You must execute the CreateShell method before executing this method.

-   **Input**

    [Script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)


## PSObjectToString

Accepts PowerShell objects from other methods or components and converts them to a string.

-   **Inputs**

    [PSObject](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)


## GetValuesByProperty

Accepts a PowerShell object and gets the values of the various properties.

-   **Inputs**

    [PSObject](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)

-   **Output**

    [Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)


## Disconnect

Disconnects the connection to the PowerShell.

## Serialize

Accepts a PowerShell object and returns the object as a string.

-   **Input**

    [PSObject](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)

-   **Output**

    [Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/parameters-powershell-connectors.md)


**Parent Topic:**[ITSM connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/itsm.md)

