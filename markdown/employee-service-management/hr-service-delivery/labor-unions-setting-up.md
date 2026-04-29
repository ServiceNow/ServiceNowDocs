---
title: Setting up labor unions
description: Set up HR Service Delivery labor unions to define information about the labor unions you support. You can associate an employee membership to a specific union and union chapter.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Labor unions, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Setting up labor unions

Set up HR Service Delivery labor unions to define information about the labor unions you support. You can associate an employee membership to a specific union and union chapter.

To create a union structure, you must set up a Union first.

After setting up a Union, you can set up:

-   Local chapters
-   Employee membership
-   Union contacts

-   **Tables**

    The following tables are included:

    -   Labor Union \[sn\_hr\_core\_labor\_union\]
    -   Local Union Chapter \[sn\_hr\_core\_local\_union\_chapter\]
    -   Labor Union Contact \[sn\_hr\_core\_labor\_union\_contact\]
    -   Employee Union Membership \[sn\_hr\_core\_employee\_union\_membership\]
-   **Roles**

    The following roles are needed for access to Labor Unions records:

<table id="table_d4h_hwp_npb"><thead><tr><th>

HR role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR profile reader \[sn\_hr\_core.profile\_reader\]

</td><td>

The HR profile reader role can access and read: -   Unions
-   Union Contacts
-   Employee Union Membership


</td><td>

N/A

</td></tr><tr><td>

HR profile writer \[sn\_hr\_core.profile\_reader\]

</td><td>

The HR profile writer role can access and read:-   Unions
-   Union Contacts
-   Employee Union Membership
 The HR profile writer role can also create and edit employee union memberships.

</td><td>

HR profile reader \[sn\_hr\_core.profile\_reader\]

</td></tr><tr><td>

HR admin \[sn\_hr\_core.admin\]

</td><td>

The HR admin role can access, read, create, and edit:-   Unions
-   Local Chapters
-   Union Contacts
-   Employee Union Membership


</td><td>

-   HR profile reader \[sn\_hr\_core.profile\_reader\]
-   HR profile writer \[sn\_hr\_core.profile\_reader\]


</td></tr></tbody>
</table>    HR profile writer \[sn\_hr\_core.profile\_reader\]:

    The HR profile writer role contains the HR profile reader role. It can access and read Unions, Union Contacts, and Employee Union Membership. It can also edit Employee Union Membership.


-   **[Create a labor union](../task/labor-unions-create.md)**  
Create a union with details that identify it.
-   **[Create a local chapter](../task/labor-unions-local-chapter.md)**  
Use Local Chapters to set up and track the chapters of your union. Local chapters are children to labor unions.
-   **[Create union contacts](../task/labor-union-contacts.md)**  
Use Union Contacts to create and track the people who work for a union or local chapter organization.

**Parent Topic:**[Labor unions](labor-unions.md)

