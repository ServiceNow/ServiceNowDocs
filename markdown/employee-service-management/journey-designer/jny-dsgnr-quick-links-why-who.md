---
title: Creating and managing quick links for journeys
description: Quick links give employees quick access to varied resources directly from a journey. Administrators, journey owners, and mentors are able to add linked resources to journeys.
locale: en-US
release: yokohama
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Journey designer features, Installation and configuration overview, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Creating and managing quick links for journeys

Quick links give employees quick access to varied resources directly from a journey. Administrators, journey owners, and mentors are able to add linked resources to journeys.

**Note:** Journey owners and mentors must be given **Can add quick links** permission by an administrator. Journey permissions are assigned and managed in journey configurations. See, [Update users' permissions for journeys](../task/jny-dsgnr-update-user-permissions.md).

There are two types of quick links that can be added to a journey from **Journey designer**.

-   Administrator configured links: Administrators add quick links to journey types. These quick links are added to all journeys that are created from that journey type.
-   User configured links: Journey owners and mentors with **Can add quick links** permission add or delete web-based links directly to a user's journey.

    **Note:** Administrator added quick links can't be deleted by journey owners or mentors.


## Quick links added by administrators

From the **Manage Journey Type Quick Links** page, administrators create and configure quick links in a journey configuration.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Content type**

</td><td>

The content type represents the type of knowledge the quick link goes to:-   **Knowledge**: Articles within a knowledge base that can be shared across an organization.
-   **Catalog item**: Hardware and software items that can be tracked and offered in the service catalog.
-   **Page**
-   **External link**: Links to websites with a valid URL format, for example `https://www.domain.com`.

 **Note:** Selecting a content type opens additional fields used with that content type.

</td></tr><tr><td>

**Quick link name**

</td><td>

The name of the link that is visible in the journey.

</td></tr><tr><td>

**Title**

</td><td>

The title entered in this field overrides the default title of the quick link.

</td></tr><tr><td>

**Short description**

</td><td>

The description added in this field overrides the default description of the quick link.

</td></tr><tr><td>

**Icon**

</td><td>

The icon displayed for a quick link in a journey.

</td></tr></tbody>
</table>## Quick links added by managers and mentors

Managers and mentors with edit journey permission add external links to a journey.

|Field|Description|
|-----|-----------|
|**Link text**|The user readable text that is visible in the journey.|
|**Link address**|Manager and mentors add valid external links. The Quick Links widget checks for a valid URL format. For example, `https://www.website.com`.|

-   **[Create a quick link as an administrator](../task/jny-dsgnr-admin-created-qlink.md)**  
Journey designer administrators create quick links that are part of a journey configuration. Administrator created quick links cannot be deleted or edited by journey owners or mentors.
-   **[Delete a quick link created by an administrator](../task/jny-dsgnr-delete-admin-created-qlink.md)**  
To delete an administrator created quick link in Journey designer, you must be an administrator.

**Parent Topic:**[Configure Journey designer features](jny-dsgnr-configuration.md)

