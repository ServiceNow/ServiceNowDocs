---
title: Install based item form
description: An install base item refers to an application service configuration item. Each install base item references the configuration item record for the customer. If issues arise with a configuration item, customer service agents can trace which install base items that the case is affecting.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Repair form, Reference, Manufacturing Commercial Operations]
---

# Install based item form

An install base item refers to an application service configuration item. Each install base item references the configuration item record for the customer. If issues arise with a configuration item, customer service agents can trace which install base items that the case is affecting.

<table id="table_cnh_w1g_4fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique ID of the install base item. This field is automatically filled in, but you can change it.

</td></tr><tr><td>

Name

</td><td>

Name of the install base item.

</td></tr><tr><td>

Configuration Item

</td><td>

Configuration item that is associated with the install base item.The sn\_customerservice\_manager role must also have the app\_service\_user role to create the install base items for the Application Service configuration item class. For more information, see Application services.

Service models have a model category called the Application Service, which links a service model to the Application Service CI class. For more information, see Models and Model categories.

</td></tr><tr><td>

Consumer

</td><td>

Consumer that is associated with the install base item. **Note:** The Account field is hidden if the **Consumer** field is entered first.

</td></tr><tr><td>

Owned by

</td><td>

Business manager of the install base item. If the business manager is entered in the configuration item, this field is automatically filled in with the information from the configuration item.

</td></tr><tr><td>

Supported by

</td><td>

If the CI contains this information, this field is automatically filled in with the information from the configuration item.

</td></tr><tr><td>

Product

</td><td>

Product model that is associated with an install base and is used to identify the services that are associated with any product model.**Note:** A product model must have a single specification. The specification that is associated with the product model appears only on the install base form.

</td></tr><tr><td>

Location

</td><td>

Location that is associated with the product.

</td></tr><tr><td>

Status

</td><td>

Option that determines whether the product is original or a replacement.

</td></tr><tr><td>

Life cycle stage

</td><td>

CSDM life cycle stage of an install base item.

</td></tr><tr><td>

Life cycle stage status

</td><td>

CSDM life cycle stage status of an install base item.

</td></tr><tr><td>

Active

</td><td>

Option that represents whether the install base is active or inactive. If the state is active, related cases for a product can be created.**Note:** A synchronization between the active state, install date, and uninstall date is present. On the install base form, if the **State** is **In Use**, it means that the **Active** option is selected. If the **Active** option remains unselected then the **State** is set to **Inactive**.

</td></tr><tr><td>

Install date

</td><td>

Date on which the install base becomes active.

</td></tr><tr><td>

Uninstall date

</td><td>

Date on which the install base becomes inactive.

</td></tr><tr><td>

Asset

</td><td>

Asset that is associated with an install base.

</td></tr><tr><td>

Specification

</td><td>

Specification that is associated with an install base item. Option that helps in fulfilling orders to create an install base item and its hierarchy.**Note:** The **Specification** field appears only to CSM agents, managers, and contributor persona.

</td></tr></tbody>
</table>**Parent Topic:**[Repair form](repair-form.md)

**Related topics**  


[Create an install base item](../concept/mco-create-install-base-item.md)

