---
title: Financial Services Complaint Management data model
description: The Financial Services Complaint Management data model provides a framework that is used in the complaint management workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/financial-services-complaint-management/fso-complaints-mgmt-data-model.html
release: zurich
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Complaint Management, Common applications, Financial Services Operations \(FSO\)]
---

# Financial Services Complaint Management data model

The Financial Services Complaint Management data model provides a framework that is used in the complaint management workflow.

This data model is aligned to the Financial Services Operations Core data model. See [Financial Services Operations Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-operations-core-data-model.md) to learn about Financial Services Operations Core data model.

The following diagram shows the tables and their relationships that comprise the complaints management data model.

This data model uses a combination of tables to store data:

-   Tables that are included with complaints management application.

    For more information on tables that are installed with Financial Services Complaint Management, see [Components installed with Financial Services Complaint Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-complaint-management/installed-with-fso-complaints-mgmt.md).

-   Tables that are from the Customer Service Management \(CSM\) application.
    -   Extends the Sold Product \[sn\_install\_base\_sold\_product\] table for financial account and financial transaction tables.
    -   Uses these CSM tables to support customers: Consumer \[csm\_consumer\], Account \[customer\_account\], and Contact \[customer\_contact\]

        For more information on these CSM tables that store customer records, see Accounts and contacts and Consumers.

-   ServiceNow AI Platform tables.

    Extends the Product Model \[cmdb\_model\] table to support financial products in Financial Services Operations.


The data model also includes access control lists \(ACLs\) and the following user roles to restrict access to different tables:

-   Internal roles for agents, users working in front, middle, and back-office of financial institutions
-   External roles for accounts, contacts, and consumers

