---
title: Flightpath
description: Flightpath keeps a record of rule engine activity and field changes in real time, helping administrators analyze system behavior and troubleshoot complex configuration flows with pause and restart options.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Flightpath

Flightpath keeps a record of rule engine activity and field changes in real time, helping administrators analyze system behavior and troubleshoot complex configuration flows with pause and restart options.

Flightpath helps administrators understand how the rules engine responds to end-user inputs. When recording, Flightpath keeps track of:

-   Rules engine responses \(rules run and fields changed\) to end-user input
-   Computation time for each rules engine run

To help troubleshoot long user flows, the administrator can pause Flightpath and reinitiate recording any number of times.

## Demonstration

The following video demonstrates the Flightpath feature tracking rules engine responses.

[Flightpath](https://www.youtube.com/watch?v=GGW1PvuNZjE)

## Prerequisites

-   Salesforce-integrated use cases:

    CPQ environment Explorer 07.22 or later.

    Salesforce Logik.io Managed Package version 1.2 or greater. Navigation in Salesforce: Admin Setup &gt; Apps &gt; Packaging &gt; Installed Packages &gt; CPQ Managed Package

    The Salesforce administrator must add the `LGK FlightPath_c` field to the Quote Line Editor field set \(Salesforce: Admin Setup &gt; Object Manager &gt; Quote &gt; Field Sets &gt; Line Editor\). Place the Flightpath field in the field set. Limit its visibility to the appropriate administrator roles.

-   Headless/eCommerce use cases:

    Your CPQ environment must be Explorer 07.22 or later.

    Append the following text to your configure API call to CPQ: `?logExecution= <value>`. Example: `https://<siteURL>.<sector>.logik.io/c?logExecution=<value>`

    Valid values for &lt;value&gt; are:

    -   true: CPQ configuration returns Flightpath controls. Should be shown only to administrative users.
    -   false: CPQ returns no Flightpath controls. Suitable for non-administrative users such as partners, customers, and direct sales.
-   End-user UI:

    Append the following to your configure URL: `&log=<value>`

    Examples:

    -   Configurator:

        ```
        https://<siteURL>.<sector>.logik/ui/configure/<product id>?v=1&<other parameters>&log=<value>
        ```

    -   Transaction management:

        ```
        https://<siteURL>.<sector>.logik.io/ui/transact/<transaction id>?v=1&log=active
        ```

        For transaction management, valid values include:

        -   none
        -   available
        -   active

