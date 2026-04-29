---
title: Additional details record producer - Mapping Variable types and limitations
description: When you create a record producer to configure additional details on a reservation form, the variables types and column type must be set differently. In case of reservations, the record producer supports only a few UI policies and client scripts.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workplace Reservation Management references, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Additional details record producer - Mapping Variable types and limitations

When you create a record producer to configure additional details on a reservation form, the variables types and column type must be set differently. In case of reservations, the record producer supports only a few UI policies and client scripts.

## Mapping Variable 'Type' with column type

When you add variables to the record producer, based on the type of field you want, select the **Type** of the variable as follows. For example, In the Workplace Reservation table, in the Columns related list, to set the column **Type** as a **String**, on the record producer, select the variable **Type** as **Multi Line Text**:

|Workplace Reservations Table, Column - 'Type'|Record producer, Variable - 'Type'|
|---------------------------------------------|----------------------------------|
|True/False|checkbox|
|Date|Date|
|Date/Time|Date/Time|
|Duration|Duration|
|HTML|HTML|
|IP Address \(Validated IPV4, IPV6\)|IP address|
|List|List collector|
|Choice|Lookup multiple choice|
|Choice|Lookup Select Box|
|Password \(1 &amp; 2 Way Encrypted\)|Masked|
|String|Multi Line Test|
|Choice|Multiple Choice|
|Integer|Numeric Scale|
|Reference|Reference|
|Choice|Select Box|
|String|Single Line Text|
|URL|URL|
|String|Wide Line Single Text|
|Choice|Yes/no|

**Note:** The max length of a **Single Line Text** is 40. For a longer length, use **Multi Line Text**.

## Additional details record producer - Limitations

When you configure the record producer, note the following:

-   **Script** field is not applicable.
-   You can add **Catalog UI Policies** to the record producer.
-   Only the following **Catalog Client Scripts** type are supported:
    -   OnChange
    -   OnLoad

**Note:** The record producer is only used to retrieve data related to the additional fields.

**Record producer Related list**: The following record producer related lists are not applicable:

-   Variable Sets
-   Not Available For
-   Categories
-   Catalogs
-   Catalog Data Lookup Definitions
-   Related Articles
-   Related Catalog Items
-   Assigned Topics

In the Available For Related list, you must create a **User Criteria** with the **Advanced** setting enabled. In the **Script** field, you must set "answer=false", so that the record producer is not be visible outside the reservation details page.

**Variables Related list**: The following Variables related lists are not applicable:

-   Permission
-   Availability

## Configuring additional details column in Workplace Reservation table - Limitations

In the Workplace Reservation \(sn\_wsd\_rsv\_reservation\) table, Columns related list, when you add fields \(columns\) that are not included, note the following:

-   On the Dictionary Entry form, the **Mandatory**, **Read only** and **Display** fields are not applicable.
-   The columns in the table are created to only store the data.
-   The **Max length** field is considered to save the data with **Max length**.

**Parent Topic:**[Workplace Reservation Management references](../concept/rsv-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Reservation Management](components-installed-with-wsd-reservation-mgmt.md)

[Properties installed with Workplace Reservation Management](properties-installed-with-wsd-reservation-mgmt.md)

[Workplace Reservation Management - Field descriptions](../concept/workplace-reservation-management-field-descriptions.md)

[Proximity calculation when browsing near a person](proximity-calculation-for-browse-near-person.md)

[Reservable module derivation logic for Space details](../concept/reservation-logic-for-myfavorites-space-details.md)

[Mobile push notifications for workplace reservations](reservation-push-notifications.md)

[Location privacy settings and impact](location-privacy-settings-and-impact.md)

