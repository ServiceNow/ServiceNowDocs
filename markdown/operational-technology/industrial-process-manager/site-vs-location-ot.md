---
title: Site vs location
description: The site and location attributes have different uses for Operational Technology \(OT\).
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Industrial Process Manager, Operational Technology]
---

# Site vs location

The site and location attributes have different uses for Operational Technology \(OT\).

## Site

A site is part of the ISA Equipment Model Entity and describes an industrial site where your production process takes place. Sites are logical and you can use them to define an equipment model. You can then use that equipment model to provide access control. For more information about access control, see [Assign or remove equipment model site access for non-administrators](../task/create-user-criteria-for-equipment-model-entity-site-users.md).

Sites can have a location but they aren't considered a location. Any OT device can have a location and be assigned to an equipment model entity site.

## Location

Location refers to the value stored in the **Locations** \(cmn\_location\) table. It's the physical location of an equipment model or device. For example, if one of your equipment models belongs to the site Atlanta and is located in Atlanta, GA, you would list its location as **Atlanta, GA**.

**Parent Topic:**[Industrial Process Manager reference](manufacturing-process-mgr-reference.md)

