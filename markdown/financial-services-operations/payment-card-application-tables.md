---
title: Payment card tables
description: This section describes the tables in the Payment card application and shows how they store and manage physical payment card information.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Payment Card, Data Models, Explore, Financial Services Operations \(FSO\)]
---

# Payment card tables

This section describes the tables in the Payment card application and shows how they store and manage physical payment card information.

## Payment card tables installed

|Table|Description|
|-----|-----------|
|Payment Card \[sn\_payment\_card\_base\]|Parent table that contains the details of various payment cards. Extends the Install Base Item \[sn\_install\_base\_item\] table.|
|Credit Card \[sn\_payment\_card\_credit\]|Contains the details of credit cards. Extends the Payment Card \[sn\_payment\_card\_base\] table.|
|Debit Card \[sn\_payment\_card\_debit\]|Contains the details of debit cards. Extends the Payment Card \[sn\_payment\_card\_base\] table.|

## Expanded Model and Asset Classes tables

The Expanded Model and Asset Classes Store application contains a Payment Card Model \[sn\_ent\_payment\_card\_model\] table that extends System and Smart Card Model \[sn\_ent\_system\_smart\_card\_model\]. This table represents payment cards as a material, physical good.

For more information, see [Expanded Model and Asset Classes Store application](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

**Parent Topic:**[Payment card](../concept/payment-card-application.md)

**Related topics**  


[Expanded Model and Asset Classes Store application](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)

