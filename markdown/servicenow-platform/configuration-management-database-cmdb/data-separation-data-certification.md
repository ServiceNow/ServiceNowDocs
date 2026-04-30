---
title: Domain separation and Data Certification
description: Domain separation is supported in Data Certification processing. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Data Certification

Domain separation is supported in Data Certification processing. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic

-   Business logic: Ensure data goes into the proper domain for the application’s service provider use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all consider domain at production run time.
-   The owner of the instance needs to be able to set up the application to function normally across multiple tenants.

Use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the client must be able to see my response.

## How domain separation works in Data Certification

-   Data Certification has only basic domain separation. As long as the Certification Instances \(CIs\) or records that must be certified are correctly domain-separated and the users who must certify the CIs or records are in a domain that can view the data, Data Certification works as expected.
-   Recommendation: The instance owner must be responsible for assigning Certification Tasks and Certification Instances to the correct domain. Changing the domain for these records does not change functionality, but limits the view of the records.

## How to set up domain separation for Data Certification

After enabling the Domain Separation plugin, there are no additional steps required to set up domain separation for Data Certification.

-   instance owners determine which CIs or records that need to be certified can be domain-separated.
-   Customers can configure a domain-separated environment by assigning tasks to a domain, but if the data is already domain-separated, then only users with the right domain permissions can view the data in a certification task.

## How tenant domains manage their own application data

It's not necessary to set the domain on the certification tables but it can be done if the instance owner should want that. As long as the CI’s or records that must be certified are domain-separated, users with the correct domain permissions can view them.

## Domain-separated tables

-   cert\_instance – Changing the domain on this table does not change any functionality, nor does it change the domains of the tasks created from the table.
-   cert\_task – Changing the domain on this table changes the domain viewing permissions of the task.
-   cert\_element – It is not recommended to change the domain on these records. As long as the CIs or records to be certified are already domain-separated, cert\_element records will reflect that.
-   cert\_filter – Changing the domain on this table changes the domain viewing and filtering of CIs or records.

## Use cases

Instance owners who have multiple clients that certify the infrastructure they own can assign domains to those CIs and the Certification Tasks to restrict the view from one client to another.

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

