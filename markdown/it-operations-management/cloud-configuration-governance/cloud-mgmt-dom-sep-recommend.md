---
title: Domain separation in Cloud Provisioning and Governance - considerations for service providers
description: Review the following considerations to effectively create, implement, and maintain domain separation for Cloud Provisioning and Governance services in the instance that you are setting up for your customers.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Domain separation in Cloud Provisioning and Governance - considerations for service providers

Review the following considerations to effectively create, implement, and maintain domain separation for Cloud Provisioning and Governance services in the instance that you are setting up for your customers.

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

## How domain separation works in Cloud Provisioning and Governance

Domain separation for Cloud Provisioning and Governance aligns one or more companies to a domain. To use domain separation with the application, assign all user accounts to a specific company associated with that domain.

All entities that are related to the company, such as cloud accounts and service accounts, are created in the same domain as the company. When a new company is created, create a domain with a unique name and assign it to the company. All related entities for an account, such as contacts and cases, must reside in the same domain. When you create a related entity for a domain-separated account, the entity is assigned to the company domain.

Members of a domain can only view the data that is contained within their domain or child domains that are lower in the domain hierarchy. By default, all users and all records are members of the global domain unless you assign them to a particular domain. Once you assign a user or a record to a domain, the instance compares the user's domain to the record's domain to determine whether the user can view the record.

Service Providers \(SPs\) use domain separation to segregate data for each customer. Users in a given domain can only view the data in their own domains or in child domains. SPs typically control the top-level domain, which allows them to view data that is associated with all domains. Don't delegate administration to cloud admin users of the child domains in Cloud Provisioning and Governance.

Pool-Filter, Resource profile, Billing, Quota, Permissions, IPAM, Budget, and Notifications are domain separated. Not all tables in Cloud Provisioning and Governance are domain separated. While most top-level tables are domain separated, several child tables are not domain separated. However, the fact that all tables are not domain separated, doesn’t impact the working of the application in a domain-separated context.

**Warning:** Do not modify the blueprint-related tables directly in the table records.

## Instance setup considerations for Service Providers

While domain separation provides multi-tenancy support, multi-tenancy is still contained within a single instance. Some global properties, data, and processes are shared across all domains. The following image illustrates domain separation hierarchy for unrestricted and restricted use cases.

![Service provider hierarchy](../image/bp-cm-ds-hierarchy.png)

Perform the following tasks to set up your domain-separated instance:

-   -   **[Create a domain.](https://www.servicenow.com/docs/access?context=t_CreateADomain&version=australia&pubname=australia-platform-security&ft:locale=en-US)**
    -   You can create as many domains as needed, but make sure that you don't create unnecessary domains on the instance. A large number of domains on the instance can impact performance. Before you create new domains, check the domain hierarchy under **Domain Admin** &gt; **Domain Map**. Check whether you actually need to create a new domain, or an existing domain hierarchy can work instead.

        Select a primary domain to indicate the top-level domain in the domain map. The Top domain represents a single common parent domain, which acts as a single parent node, for the Service Provider domains. For more information, see [Select a primary domain](https://www.servicenow.com/docs/access?context=t_SelectAPrimaryDomain&version=australia&pubname=australia-platform-security&ft:locale=en-US).

    -   Create the SP domain under the top domain and set the domain as default. Keeping your domains organized is a crucial part of the domain separation process. Ensure that you are aware of the importance of setting a default. The system automatically assigns task and user records that are not already assigned to a domain to the default domain. For more information, see [Make a domain the default](https://www.servicenow.com/docs/access?context=t_MakeAnMSPDomainTheDefault&version=australia&pubname=australia-platform-security&ft:locale=en-US) for instructions on how to make a default domain.

    -   Create a domain hierarchy. For more information, see [Create Domain hierarchy](https://www.servicenow.com/docs/access?context=bp-domain-hierarchy&version=australia&pubname=australia-platform-security&ft:locale=en-US).

        Create a domain hierarchy that mirrors organization structures for grouping under the top domain. Because you can perform discovery and provisioning only from the leaf domain, set up leaf domains in the hierarchy that represent concrete entities and organizations.

        Based on the domain hierarchy, users have access to data in their home domain and any child domains. The process flows down and the data bubbles up. You can assign user records with a domain value that represents the user’s home domain. While users have no access to data in parent domains, peer domains, or domains in other branches of the hierarchy. A process that is setup in a parent domain is applicable to all child domains. For more information, see

        -   [Service provider reference architecture](https://www.servicenow.com/docs/access?context=bp-sp-reference-arch-ds&version=australia&pubname=australia-platform-security&ft:locale=en-US)
        -   [Domain separation architecture data](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=australia&pubname=australia-platform-security&ft:locale=en-US)
        Customer data is affected based on domain hierarchies:

        -   Parent/child: Process and data affected
            -   Design that is based on a process flow.
            -   Remember that the parent domains can access all data in the child domains.
        -   "Contains" domain: Only data is affected. For example, making SP in the diagram contain TOP does not make processes in SP run in the TOP domain and downward.
            -   Grants data access rights to individuals in groups that require dedicated access to certain domains.
            -   Contains causes or conditions to be added to database queries that can cause performance issues with large domain and data sets.
        -   Visibility: Hierarchy that is always visible to users once you provide access. Only the data is affected, not the processes.
            -   Grants data access of a domain to another domain that did not have that access when the parent-and-child hierarchy was built.
            -   Enables users to see all the data in the domains that they have visibility access for, all the time, regardless of the record they are working on.

                **Note:** Use sparingly, as Visibility can allow complete access that you may not intend.

    -   [Add a new company](https://www.servicenow.com/docs/access?context=t_AddANewCompany&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

        You can add companies that represent vendors, manufacturers, or customers with whom you do business. These companies provide a way to categorize users, groups, and assets.

        Create companies and leaf domains for each customer that you are supporting on a single instance. Companies help you associate users to the domain. Company and domain must have either one-to-one mapping or many-to-one mapping. This makes assigning users to a domain easier and manageable for SPs.

        **Important:** When you create a company for each domain, use a prefix with a unique identifier, such as "COMPANY\_" or "ORG\_".

        To customize the ServiceNow instance for each company, you can enter contact phone numbers, street addresses, and additional notes. You can also customize the company logo and banner text that your end users see at the top of each page. For more information see [Create a new company profile](https://www.servicenow.com/docs/access?context=t_CreateACompanyProfile&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

-   Create user groups and assign roles and domain to the users of each new company. You assign users to companies to associate them with domains. Associate a company with a user to map the user to a domain.
    1.  Navigate to **Organizations** &gt; **Company,** and click **New** to create new users. For more information on creating users, see, [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

        **Note:** Don’t use the manual-managed domain option to choose the domain for users.

    2.  Create groups and assign roles to the groups. Users that are assigned to the group inherit the roles. You can create cloud user portal users for a company in the leaf domain. For more information on creating groups, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    3.  Create these users in each of the leaf domains:
        -   MID Server user for each leaf domain and company. Assign the mid\_server role to MID Server users.
        -   Domain admin for each leaf domain and company. Assign the sn\_cmp.cmp\_root\_admin role to cloud \(domain\) administrators.
        -   Domain user for each leaf domain. Assign the sn\_cmp.cloud\_service\_user role to cloud users.
        -   \(Optional\) Create users for additional roles in leaf domains \(roles like designer, governor\).

            To provide limited visibility for certain domains to certain users, add them via groups. For more information, see [Grant visibility domains to an individual user](https://www.servicenow.com/docs/access?context=t_GrVisDomIndUser&version=australia&pubname=australia-platform-security&ft:locale=en-US).

    4.  Create a "contains" domain relationship between the SP domain and the TOP domain.

        **Note:** By creating a "contains" relationship, you allow all the administrators in the Service Provider domain to have access to all the domain data. Users of global domain are unable to see data from card layout as by default expand domain scope is not allowed.

        For more information on how to control what specific users and what an entire domain of users can view, see [Visibility domains and Contains domains](https://www.servicenow.com/docs/access?context=c_DomainVisibility&version=australia&pubname=australia-platform-security&ft:locale=en-US).


## Next Steps

For more information on onboarding customers or companies in a domain-separated instance for Cloud Provisioning and Governance services, see [On-board a Company](cust-onboard-dom-sep-sp.md).

**Related topics**  


[Domain Separation](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

[Understanding Domain Separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=australia&pubname=australia-platform-security&ft:locale=en-US)

