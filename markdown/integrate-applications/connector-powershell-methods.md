---
title: PowerShell connector methods
description: The PowerShell connector methods act as interfaces with the Microsoft PowerShell to send requests and get responses in the RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ITSM connector, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# PowerShell connector methods

The PowerShell connector methods act as interfaces with the Microsoft PowerShell to send requests and get responses in the RPA Desktop Design Studio.

## CreateShell

Acts as an interface to pass your inputs in the form of commands and scripts. The CreateShell method is the first method you must use.

## InvokeCommand

Runs commands and block of scripts on local or remote computers and gets the output including errors, if any.

**Note:** You must execute the CreateShell method before executing this method.

-   **Input**

    [Command \(String\)](parameters-powershell-connectors.md#parameter-powershell-method-commandstring)

-   **Output**

    [Return](parameters-powershell-connectors.md#parameter-powershell-method-output-return)


## InvokeScript

Runs a script on local or remote computers and gets the output.

**Note:** You must execute the CreateShell method before executing this method.

-   **Input**

    [Script](parameters-powershell-connectors.md#parameter-powershell-input-script)

-   **Output**

    [Return](parameters-powershell-connectors.md#parameter-powershell-output-return)


## PSObjectToString

Accepts PowerShell objects from other methods or components and converts them to a string.

-   **Inputs**

    [PSObject](parameters-powershell-connectors.md#parameter-powershell-input-psobject)


## GetValuesByProperty

Accepts a PowerShell object and gets the values of the various properties.

-   **Inputs**

    [PSObject](parameters-powershell-connectors.md#parameter-powershell-input-psobject)

-   **Output**

    [Return \(String\)](parameters-powershell-connectors.md#PSOBjectToString-output-return)


## Disconnect

Disconnects the connection to the PowerShell.

## Serialize

Accepts a PowerShell object and returns the object as a string.

-   **Input**

    [PSObject](parameters-powershell-connectors.md#Serialize-input-PSObject)

-   **Output**

    [Return \(String\)](parameters-powershell-connectors.md#Serialize-output-Return)


**Parent Topic:**[ITSM connector](../concept/itsm.md)

