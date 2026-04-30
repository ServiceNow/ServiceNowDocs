---
title: Content Ownership
description: Define who has permission to create content, where they can publish it, and which employees can view it.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setup employee communications, Configure, Employee Center, Employee Service Management]
---

# Content Ownership

Define who has permission to create content, where they can publish it, and which employees can view it.

Content Ownership enables system admins and content admins to designate exclusive access to certain Content Publishing features to specific content managers.

Content Ownership gives control over three areas of Content Publishing:

-   Who sees the content \(Audience\)
-   Where can a content manager publish content \(Topic or Page\)
-   What content can the content manager create \(Content item\)

<table id="table_c3r_454_2bc"><thead><tr><th>

Ownership area

</th><th>

Examples

</th><th>

Relevant links

</th></tr></thead><tbody><tr><td>

Who - AudienceAssign content managers the ability to publish content for specific employees

</td><td>

-   Geographic audiences: target content to audiences based on their geographic location. For example, benefit information may be different for your employees located in the United States as opposed to other locations.
-   Type of employment: target content for employees that are contractors, new hires, or employees requiring visa transfers.

</td><td>

[Assign ownership of an audience](../task/ecpro-ca-cd-audience-delegation.md)[Create an audience](../task/ec-audiences.md)

</td></tr><tr><td>

Where - Topic or Portal pageAssign content managers to specific topics or pages

</td><td>

-   Designated topics in the taxonomy
-   Designated pages in the portal
-   Pages containing rich content

</td><td>

[Assign ownership to a portal page](../task/ecpro-portal-page-restriction.md)[Assign ownership to a topic](../task/ecpro-assign-ownership-topic.md)

</td></tr><tr><td>

What - Content itemAssign content managers to specific content items

</td><td>

-   Sensitive content, such as:
    -   Mergers or acquisitions
    -   Reduction in Force \(RIF\)
    -   Content specific to geographic region
    -   Legal announcements
-   Rich content
-   News

</td><td>

[Assign ownership of content](../task/ecpro-ca-cd-content-restriction.md)

</td></tr></tbody>
</table>## Impact on roles

-   System admin \(admin\) has total control and visibility into Content Publishing and Content Experiences during and after restriction set up.
-   Content Administrators \(sn\_cd.content\_admin\) have full and complete access to add, edit, and publish content within the restricted areas and functions for Employee Center Pro.
-   Content Managers \(sn\_cd.content\_manager\) have restricted access to authoring and publishing capabilities. Review the tables below to understand how content managers access to audiences, pages, topic, and content items changes when a user or group is assigned to the record.

    The following graphic shows a content manager's access permissions to a record based in whether they are assigned to that record or not.

    **Note:** These access permission changes apply only when a record is assigned to at least one user or group. If a record does not have an assignment, it is accessible to all content managers.

    ![content managers access to records](../images/ecpro-content-ownership-impact.png "Access to records")


## Activating Content Ownership

The following plug-ins are required:

-   Employee Center Pro
-   Content Publishing
-   Content Governance \(only required if using Content Governance features\)
-   Content Experiences \(only required if using Content Experiences features\)

**Note:** For more information on activating the above plug-ins, see [Understanding Employee Center plugins](install-plugins.md) and [Install Employee Center Pro](../task/install-ec-pro.md).

After activating the required plug-ins, enable the Content Manager Ownership properties. See [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md). When the Content Manager Ownership properties are enabled, Content Ownership related lists appear in records for audiences, content items, topics, and portal pages.

