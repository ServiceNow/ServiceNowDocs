---
title: Customer Service Management and CSDM tables
description: Customer Service Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Customer Service Management.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customer Service Management and the CSDM guidelines, Getting started with Customer Service Management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Customer Service Management and CSDM tables

Customer Service Management manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Customer Service Management.

## CSM tables managed by CSDM

![CSDM tables managed by CSM.](../image/csdm-tables-managed-by-csm.png "CSM tables managed by CSDM")

CSM references the following CSDM tables:

1.  Sold Product table \[sn\_install\_base\_sold\_product in CSM

    Represents the product purchased by an Account or Consumer, and references the Product Model table \[cmdb\_model\] or Service Model table \[cmdb\_service\_product\_model\] for a Customer \(Account or Consumer\).

2.  Install Base Item table \[sn\_install\_base\_item\] in CSM

    Represents the products installed or in use by an account or consumer. Install Base Items are CIs consumed by the customer and generally reference the Application Services table \[cmdb\_ci\_service\_discovered\] for SaaS products.

    Multiple sold products can be used on a given Install Base Item by using the Installed Products table \[sn\_install\_base\_m2m\_installed\_product\].

3.  A Service Model references the Service Offerings table \[service\_offering\]. Multiple Service Offerings can be associated with a single Service Model.
4.  After the product is sold to a customer, the Sold Product table references the Service Offering table \[service\_offering\]. This reference helps to identify the customers subscribed to an offering.
5.  Customers can request services related to the products they have purchased by linking the Catalog Items table \[sc\_cat\_item\] to the Product Model or Service Model by using the Product-to-Catalog Items Relationships table \[sn\_prod\_cat\_rel\_m2m\_product\_catalog\_item\].
6.  Account table \[customer\_account\] in CSM

    Extends the Company table. The Account table can be a customer account, a partner account, or both.

7.  Contact table \[customer\_contact\] in CSM

    Extends the User table. A user is an employee of an account. A contact record stores information about a contact, such as the name, phone number, and email address. A contact can also have a user ID and can log in to the customer portal.

8.  Consumer table \[csm\_consumer\] in CSM

    A consumer is a customer in the business-to-consumer \(B2C\) business model.


## CSDM tables used by CSM

![CSDM tables used by CSM.](../image/csdm-tables-used-by-csm.png "CSDM tables used by CSM")

1.  Company \[core\_company\], Business Unit \[business\_unit\], Department \[cmn\_department\], Location \[cmn\_location\], Groups \[sys\_user\_group\], Users \[sys\_user\]
2.  Product Model tables \[cmdb\_model\], and \[cmdb\_service\_product\_model\]
3.  Contract table \[ast\_contract\]
4.  Mapped Application Service table \[cmdb\_ci\_service\_discovered\]
5.  Configuration Item table \[cmdb\_ci\_\*\]
6.  Business Service table \[cmdb\_ci\_service\_business\]
7.  Business Service Offering table \[service\_offering\]
8.  Request Catalog table \[sc\_cat\_item\]

## Products that add value to CSM

When you use CSM with other ServiceNow products, you increase the value you get from CSM. These other ServiceNow products include:

-   **IT Service Management \(ITSM\)**

    Services have the context of the business, applications, information, and technologies layered beneath them.

-   **Event Management**

    Enables organizations to identify service health-related issues on a single management console. Event Management provides alert aggregation and root cause analysis \(RCA\) for discovered services, application services, and automated alert groups.

-   **Service Portfolio Management \(Service Portfolio Management\)**

    Enables organizations to document and manage services using a standardized, structured format.


## Products that benefit from CSM

-   **IT Service Management \(ITSM\)**

    Enables organizations to link incidents, problems, changes, and requests to cases, and have the context of the customer \(consumer or account\) reporting the issue.

-   **IT Operations Management \(ITOM\)**

    Enables organizations to identify the Install Base Items and the customers affected by service issues. Helps organizations to provide proactive customer service.

-   **Service Portfolio Management \(Service Portfolio Management\)**

    Enables customers that have subscribed to the Service Offering to see who owns the service.


