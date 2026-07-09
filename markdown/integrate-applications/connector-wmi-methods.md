---
title: WMI connector methods
description: The Windows Management Instrumentation \(WMI\) connector methods act as interfaces with the WMI to send various requests and get responses in the RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/connector-wmi-methods.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ITSM connector, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# WMI connector methods

The Windows Management Instrumentation \(WMI\) connector methods act as interfaces with the WMI to send various requests and get responses in the RPA Desktop Design Studio.

## Connect

Establishes a connection with the WMI. You must execute this method first before executing any other method.

-   **Input**

    [Hostname](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)

    [Username](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)

    [Password](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## GetDiskDetails

Returns the disk details such as the name, manufacturer, model, and media type of a local or remote computer.

-   **Output**

    [Hashtable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## GetEnvironmentValue

Returns the environment variable values in the local or remote computers.

-   **Input**

    [Var](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## GetProcessesByCpuUsage

Returns the CPU usage by all processes in the remote or local computer.

-   **Output**

    [Return \(Sorted Dictionary\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## GetProcessesByMemUsage

Gets the memory usage by all processes in the remote or local computer.

-   **Output**

    [Return \(Sorted Dictionary\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## PageFaultsPerSecond

Gets the total page exceptions per second. It returns the page exceptions as objects.

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## PageFilePercentUsage

Gets the usage of page files by the local or remote computers as percentages. It returns the page percentages as objects.

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## PercentMemoryUsage

Returns the percentage of the total memory that is used in the local or remote computers. It returns the percentages as objects.

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## PercentProcessorUsage

Gets the percentage of the total processes that are used in the local or remote computers. It returns the percentages as objects.

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## Query

Queries a local or remote computer by specifying the class and filter.

-   **Input**

    [Class](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)

    [Filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


## TotalPhysicalMemory

Provides the total available physical memory. It returns the output as an object.

## AvailableMBytes

Provides the total available megabytes.

-   **Output**

    [Return](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connector-wmi-method-parameters.md)


**Parent Topic:**[ITSM connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/itsm.md)

