---
title: Components installed with Labor Unions
description: Tables and roles related to the Labor Unions module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/labor-unions-setting-up.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Labor unions, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Components installed with Labor Unions

Tables and roles related to the Labor Unions module.

## Tables

The following tables are included:

-   Labor Union \[sn\_hr\_core\_labor\_union\]
-   Local Union Chapter \[sn\_hr\_core\_local\_union\_chapter\]
-   Labor Union Contact \[sn\_hr\_core\_labor\_union\_contact\]
-   Employee Union Membership \[sn\_hr\_core\_employee\_union\_membership\]

## Roles

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
</table>-   **[Create a labor union](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/labor-unions-create.md)**  
Create a union with details that identify it.
-   **[Create a local chapter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/labor-unions-local-chapter.md)**  
Use Local Chapters to set up and track the chapters of your union. Local chapters are children to labor unions.
-   **[Create union contacts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/labor-union-contacts.md)**  
Union Contacts track the people who work for a union or local chapter organization.
-   **[Create employee union memberships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/labor-union-employee-membership.md)**  
Use Employee Union Membership to input and track your union employees. Creating union memberships allows you to gain visibility into employee membership through an HR profile and target content or tasks through HR criteria.

**Parent Topic:**[Labor unions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/labor-unions.md)

