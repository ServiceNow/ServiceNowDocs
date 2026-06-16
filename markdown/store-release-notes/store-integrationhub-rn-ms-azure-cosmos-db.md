---
title: Microsoft Azure Cosmos DB Spoke release notes
description: Version history for the Microsoft Azure Cosmos DB Spoke on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-ms-azure-cosmos-db.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Microsoft Azure Cosmos DB Spoke release notes

Version history for the Microsoft Azure Cosmos DB Spoke on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.0.0 - November 2024**
    -   New:
        -   Microsoft Azure Cosmos DB Spoke now makes use of the default alias for Microsoft Resource Management Spoke \(sn\_azure\_rm\_spoke.Microsoft\_Azure\_Resource\_Management\)
        -   New connection &amp; credential alias for Microsoft Azure Cosmos DB SAS \(sn\_azure\_cd\_spoke.Microsoft\_Azure\_Cosmos\_DB\_SAS\)
        -   Authentication Template for easy spoke setup
        -   New actions that make use of new connection &amp; credential aliases:
            -   Casandra Database Management: Create Cassandra Keyspace \(create\_cassandra\_keyspace\_v2\),Delete Cassandra Keyspace \(delete\_cassandra\_keyspace\_v2\),Look up Cassandra Keyspace \(look\_up\_cassandra\_keyspace\),Look up Cassandra Keyspace Throughput \(look\_up\_cassandra\_keyspace\_throughput\),Look up Cassandra Keyspaces \(look\_up\_cassandra\_keyspaces\_v2\),Update Cassandra Keyspace Throughput \(update\_cassandra\_keyspace\_throughput\_v2\)
            -   Core SQL Database Management: Create Database \(create\_database\_v2\),Create Permission \(create\_permission\_v2\),Create User \(create\_user\_v2\),Delete Database \(delete\_database\_v2\),Delete Permission \(delete\_permission\_v2\),Delete User \(delete\_user\_v2\),Look up Database \(look\_up\_database\),Look up Databases \(look\_up\_databases\_v2\),Look up Permission \(look\_up\_permission\),Look up Permissions \(look\_up\_permissions\_v2\),Look up User \(look\_up\_user\),Look up Users \(look\_up\_users\_v2\),Replace Permission \(replace\_permission\),Replace User \(replace\_user\)
            -   Database Account Management: Create DB Account \(create\_db\_account\_v2\),Delete DB Account \(delete\_db\_account\_v2\),Enable or Disable Options on DB Account \(enable\_or\_disable\_options\_on\_db\_account\),Get Throughput Settings \(Metadata\) \(get\_throughput\_settings\_metadata\),Look up Access Keys \(look\_up\_access\_keys\),Look up Connection Strings \(look\_up\_connection\_strings\_v2\),Look up DB Account \(look\_up\_db\_account\),Look up DB Accounts by Resource Group \(look\_up\_db\_accounts\_by\_resource\_group\),Look up DB Accounts by Subscription ID \(look\_up\_db\_accounts\_by\_subscription\_id\),Look up Usages \(look\_up\_usages\),Regenerate Access Key \(regenerate\_access\_key\),Update Failover Priority \(update\_failover\_priority\_v2\)
            -   Mongo Database Management: Create MongoDB Database \(create\_mongodb\_database\),Delete MongoDB Database \(delete\_mongodb\_database\),Look up MongoDB Database \(look\_up\_mongodb\_database\),Look up MongoDB Database Throughput \(look\_up\_mongodb\_database\_throughput\),Look up MongoDB Databases \(look\_up\_mongodb\_databases\_v2\),Update MongoDB Database Throughput \(update\_mongodb\_database\_throughput\_v2\)
    -   Removed:
        -   Deprecate old credential Azure\_Cosmos \(alias sn\_azure\_cd\_spoke.Azure\_Cosmos\)
        -   Deprecate actions that make use of old credential alias:
            -   Casandra Database Management: Create Cassandra Keyspace \(Deprecated\) \(create\_cassandra\_keyspace\),Delete Cassandra Keyspace \(Deprecated\) \(delete\_cassandra\_keyspace\),Get Cassandra Keyspace Information \(Deprecated\) \(get\_cassandra\_keyspace\),Look up Cassandra Keyspaces \(Deprecated\) \(look\_up\_cassandra\_keyspaces\),Update Cassandra Keyspace Throughput \(Deprecated\) \(update\_cassandra\_keyspace\_throughput\)
            -   Core SQL Database Management: Create Database \(Deprecated\) \(create\_database\),Create Permission \(Deprecated\) \(create\_permission\),Create User \(Deprecated\) \(create\_user\),Delete Database \(Deprecated\) \(delete\_database\),Delete Permission \(Deprecated\) \(delete\_permission\),Delete User \(Deprecated\) \(delete\_user\),Get Database Information \(Deprecated\) \(get\_a\_database\),Get Permission Information \(Deprecated\) \(get\_a\_permission\),Get User Information \(Deprecated\) \(get\_a\_user\),Look up Databases \(Deprecated\) \(look\_up\_databases\),Look up Permissions \(Deprecated\) \(look\_up\_permissions\),Look up Users \(Deprecated\) \(look\_up\_users\),Replace Permission \(Deprecated\) \(replace\_a\_permission\),Replace User \(Deprecated\) \(replace\_a\_user\)
            -   Database Account Management: Create DB Account \(Deprecated\) \(create\_database\_account\),Delete DB Account \(Deprecated\) \(delete\_db\_account\),Enable/Disable Options On DB Account \(Deprecated\) \(enable\_options\_on\_db\_account\),Find Throughput Settings \(Deprecated\) \(find\_throughput\_settings\),Get DB Account Information \(Deprecated\) \(get\_db\_account\_information\),Look up Connection Strings \(Deprecated\) \(look\_up\_connection\_strings\),Look up DB Account By Resource Group \(Deprecated\) \(look\_up\_by\_resource\_group\),Look up DB Account By Subscription ID \(Deprecated\) \(list\_db\_accounts\),Look up Keys \(Deprecated\) \(look\_up\_keys\),Look up Usages \(Deprecated\) \(list\_usages\),Regenerate Key \(Deprecated\) \(regenerate\_key\),Update Failover Priority \(Deprecated\) \(update\_failover\_priority\)
            -   Mongo Database Management: Create MongoDB Database \(Deprecated\) \(create\_mongodb\_account\),Delete MongoDB Database \(Deprecated\) \(delete\_mongo\_db\_database\),Get MongoDB Database Information \(Deprecated\) \(get\_mongodb\_database\_information\),Look up MongoDB Database \(Deprecated\) \(look\_up\_mongodb\_databases\),Update MongoDB Database Throughput \(Deprecated\) \(update\_mongodb\_database\_throughput\)
-   **Version 1.0.3 - September 2022**

    Fixed: Improve installation performance of spoke

-   **Version 1.0.2 - September 2021**

    Patch release of Microsoft Azure Cosmos DB spoke for IntegrationHub. This version includes few fixes for Look up MongoDB Database action.

-   **Version 1.0.1 - June 2021**

    Patch release of Microsoft Azure Cosmos DB spoke for IntegrationHub. This version adds KMF modules for additional security of the password2 fields.

-   **Version 1.0.0 - September 2020**

    New: Provides actions to automate the management of database accounts and Core SQL, Cassandra, and MongoDB in Azure.


**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

