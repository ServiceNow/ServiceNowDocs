---
title: Dealer tables
description: This section explains the dealer tables in Manufacturing Commercial Operations.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-29"
reading_time_minutes: 1
breadcrumb: [Dealer portal, Data model of Manufacturing Commercial Operations, Manufacturing Commercial Operations reference, Manufacturing Commercial Operations]
---

# Dealer tables

This section explains the dealer tables in Manufacturing Commercial Operations.

## Dealer plugin

The dealer \[sn\_dealer\_mgmt\] feature adds or modifies the existing tables:

-   Service Organization \[sn\_customer\_service\_organization\]
-   Business Location \[sn\_csm\_business\_location\]
-   Internal Business Location \[sn\_csm\_business\_location\_internal\]
-   External Business Location \[sn\_cms\_business\_location\_external\]
-   Service Organization member \[sn\_cms\_service\_organization\_member\]
-   Service Organization External Staff \[sn\_cms\_svc\_org\_member\_responsibility\]
-   Channel Partner \[sn\_prm\_channel\_partner\]
-   Service Organization External Staff \[sn\_csm\_service\_organization\_external\_staff\]
-   User \[sys\_user\]

The dealer plugin adds the following tables.

<table id="table_ht5_lmw_t2c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dealer\[sn\_dealer\_mgmt\_dealer\]

</td><td>

Stores the sales dealer agent records.

</td></tr><tr><td>

Service Organization\[sn\_customer\_service\_organization\]

</td><td>

Stores records for service organizations, including business locations and internal business locations.

 A service organization provides the base framework that supports the customer value chain. The chain includes the internal and external service organization.

 For example, automobile manufacturers with multiple dealerships.

</td></tr><tr><td>

Business Location\[sn\_csm\_business\_location\]

</td><td>

Stores business location records. Business location is a type of service organization.

</td></tr><tr><td>

Internal Business Location\[sn\_csm\_business\_location\_internal\]

</td><td>

Stores the internal business location records that are involved in providing goods and services. For example, stores and branches.

</td></tr><tr><td>

External Business Location\[sn\_csm\_business\_location\_external\]

</td><td>

Stores the external business location records that are involved in providing goods and services. For example, franchises and dealerships.

</td></tr><tr><td>

Channel Partner\[sn\_prm\_channel\_partner\]

</td><td>

Stores the channel partner information such as name, contact details.

</td></tr><tr><td>

User\[sys\_user\]

</td><td>

Stores the user records, such as user id and password.

</td></tr><tr><td>

Service Organization member\[sn\_csm\_service\_organization\_member\]

</td><td>

Stores records of the relation between the member and service organization.

</td></tr><tr><td>

Service Organization External Staff\[sn\_csm\_service\_organization\_external\_staff\]

</td><td>

Stores records for the users who belong to external service organizations.

</td></tr><tr><td>

Service Organization Member Responsibility\[sn\_csm\_svc\_org\_member\_responsibility\]

</td><td>

Configure the responsibilities of the staff working at service organizations or its extended entities.

</td></tr></tbody>
</table>To learn more about the Service Model Foundation, see [Configuring Customer Service Management](https://www.servicenow.com/docs/access?context=configure-customer-service&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

