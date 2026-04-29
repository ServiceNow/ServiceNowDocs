---
title: Create a domain by creating an account for Now Assist for Customer Service Management \(CSM\)
description: Create a domain by creating an account in the account table in the Customer Service Management \(CSM\) application. By creating an account, you also create a domain. If you have the admin role, you can create multiple domains by creating different accounts as needed.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Domain separation, Configure, Now Assist for CSM, Customer Service Management]
---

# Create a domain by creating an account for Now Assist for Customer Service Management \(CSM\)

Create a domain by creating an account in the account table in the Customer Service Management \(CSM\) application. By creating an account, you also create a domain. If you have the admin role, you can create multiple domains by creating different accounts as needed.

## Before you begin

Role required: admin

## About this task

Enable the **csm\_auto\_account\_domain\_generation** system property. This system property is installed with the CSM application and is available only after the domain separation plugin is active. When this property is enabled \(the value is set to True\), the CSM application automatically creates a domain of the same name when a new account is created.

**Note:** Enabling this property doesn’t add domains for existing accounts. It only creates the domains for new accounts. Adding domains for existing accounts requires a migration script.

When creating a domain, follow these general guidelines:

-   Only one domain can be the default domain.
-   Only one domain can be the primary domain.

## Procedure

1.  Change the current domain to the domain that you want by selecting the domain under the domain scope.

    For example, if you want to create a domain under the global scope that would inherit its settings by default, select the global domain in the domain scope. If you want to create a child domain under a specific parent domain, change the domain scope to that parent domain.

    ![Different domains that are created under the global scope.](../image/domain-separation-change-domain.png "Example of the different domains under domain scope")

2.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Accounts** or **All** &gt; **customer\_account.list**.

3.  In the Accounts table, create an account by selecting **New**.

4.  Create a domain with the same name as the account by selecting **Save**.

    ![Parent and child domains that were created under the global domain scope.](../image/domain-separation-domain-names.png "Different domain names")

    For example, when you create an account named ParentDomain under the global scope, you also create a domain with the same name. All the domains that are created under the global scope will be under the TOP \(top level\) domain. If you create an account called ChildDomain within the ParentDomain domain, the domain with the same name is also created under the ParentDomain domain.

5.  Navigate to **All** &gt; **Domain Admin** &gt; **Domains**.

    The domains can be viewed in the Domain table, or you can directly create a domain in the Domain table.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the domain.|
    |Type|Domain type that describes the domain. By default, the domain types are Vendor, Customer, and MSP. You can also add your own choices.|
    |Primary|Option to select if this domain is to be the top-level domain in the hierarchy. The top-level domain only has child domains and no parent domains.|
    |Default|Domain that is to be the default domain for your hierarchy.|
    |Parent|Name of the domain that is higher in the hierarchy. This field must have a value for the domain to appear in the domain map.|
    |Active|Option to make the domain available for use. You must select this option for this domain to appear in the domain map.|
    |Description|Description for the domain.|

    Each domain record can also have several related records:

    -   Companies
    -   Contains Domains
    -   Contained By
6.  Create a domain in the Domain table by selecting **New**.

7.  Add the field values and select **Submit**.

    The domain has been created.

8.  Create users in the Users table under each domain.

9.  After adding the field values, select **Submit**.

10. Assign the appropriate roles and groups to the users.

    For example, if you create an Agent user in the ParentDomain, they have access to both the ParentDomain and ChildDomain. However, an Agent user that you create in the ChildDomain only has access to the ChildDomain.

11. Select **Save**.


## What to do next

To change the domain hierarchy, go to the Contains Domains related list. Select the domain records that are the child \(contained\) domains of the contained relationship.

