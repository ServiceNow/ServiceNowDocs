---
title: License calculation for SAP cloud use types
description: Use SAP S/4HANA cloud use types and their weighting factors to calculate Full Usage Equivalent \(FUE\) licenses for different types of users of SAP S/4HANA Cloud applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/license-calculation-sap-cloud.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# License calculation for SAP cloud use types

Use SAP S/4HANA cloud use types and their weighting factors to calculate Full Usage Equivalent \(FUE\) licenses for different types of users of SAP S/4HANA Cloud applications.

FUE licenses are allocated to different cloud use types, each with a specific weighting factor. For an overview of the FUE licensing framework, see [Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md).

A weighting factor determines how many FUE licenses a cloud use type consumes.

A single FUE license can be distributed across these four cloud use types:

-   Self-Service Use: This use type applies to users who access SAP S/4HANA Cloud self-service portals to view data, run reports, and perform basic business processes. It supports lightweight administrative tasks like monitoring data consumption and managing use rights.
-   Core Use: This use type includes all Self-Service rights and provides restricted access to SAP S/4HANA Cloud. Core users can view data, run reports, and perform basic business processes for routine tasks and targeted information access.
-   Advanced Use: This use type includes all Core Use rights and grants full access to SAP S/4HANA Cloud. Users can create and edit data, run reports, and use all available business processes to manage key business operations.
-   Developer Use: This use type grants authorized users access to the development tools provided with the SAP S/4HANA Cloud ABAP environment.

## Weighting factors

The following table lists the weighting factor for each cloud use type.

|SAP cloud use type|SAP cloud use type name|Weighting factor|
|------------------|-----------------------|----------------|
|Self-service|Cloud for Self-Service Use|30|
|Core|Cloud for Core Use|5|
|Advanced|Cloud for Advanced Use|1|
|Developer|Cloud, Developer Access|0.5|

## FUE license calculation

To determine the total number of FUE licenses required, use the following formula:

`Total FUE = Σ (Users in a cloud use type ÷ Weighting factor of that use type)`

The following example shows the FUE licenses required for each cloud use type:

|Cloud use type|Number of users|Weighting factor|FUE licenses required|
|--------------|---------------|----------------|---------------------|
|Self-Service|270|30|9|
|Core|75|5|15|
|Advanced|40|1|40|
|Developer|10|0.5|20|
|Total FUE licenses required| | |84|

A user can belong to more than one cloud use type but is counted as a single user. The assigned use type depends on the following rules:

-   The Developer use type takes priority. For a user in the Developer use type, the assignment depends on the **SAP client** field on the SAP System Users \[samp\_sap\_system\_user\] table:
    -   If the **SAP client** field indicates a developer environment, the user is counted under the Developer use type.
    -   If the **SAP client** field does not indicate a developer environment, licenses are not calculated for the user.
-   For a user in a use type other than Developer, the use type is resolved by the following priority order, from highest to lowest:

    1.  Advanced
    2.  Core
    3.  Self-Service
    For example, a user who belongs to the Advanced and Self-Service use types is counted under the Advanced use type.


The calculation assigns users across use types to arrive at the lowest total number of FUE licenses required for your SAP S/4HANA Cloud, Private Edition users. Reconciliation compares this total with the purchased rights recorded in your software entitlements to determine your license compliance position.

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/references.md)

**Related topics**  


[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

