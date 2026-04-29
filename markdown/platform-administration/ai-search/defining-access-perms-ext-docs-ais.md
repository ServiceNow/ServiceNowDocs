---
title: Defining access permissions for external documents
description: You can specify access permissions for externally defined users and groups when ingesting external documents. AI Search preserves these permissions during indexing so that user content security filters can operate on them at search time.External content security includes permissions that describe user and group access for an external document. When indexing an external document, AI Search stores these permissions so that content security filters can limit user access to the indexed search result.Certain user roles provide special access permissions for external content indexed records.Make external group deny access permissions take precedence over external user read access permissions for all external documents ingested through an indexed source.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [External content security, Indexing and searching external content, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Defining access permissions for external documents

You can specify access permissions for externally defined users and groups when ingesting external documents. AI Search preserves these permissions during indexing so that user content security filters can operate on them at search time.

For details on including access permissions for externally defined users and groups in ingested external documents, see the POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint of the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

**Parent Topic:**[External content security for AI Search](external-content-security-ais.md)

## External content access permissions

External content security includes permissions that describe user and group access for an external document. When indexing an external document, AI Search stores these permissions so that content security filters can limit user access to the indexed search result.

### Access permissions

AI Search supports the following access permissions on ingested external documents.

<table id="table_pwv_q5f_vpb"><thead><tr><th>

Security principal

</th><th>

Description

</th></tr></thead><tbody><tr><td>

everyone

</td><td>

Boolean option that indicates whether access to the external document is allowed for all users. AI Search applies this global access permission to the indexed record created from the document. Set this permission for an ingested document via the \[array\].principals.everyone request body parameter in a request to the POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint of the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 When set to **true**, this permission overrides all **groups** and **users** permissions.

 This permission is mutually exclusive with **none**. Only one of these two permissions can be set to **true** for any external document.

</td></tr><tr><td>

groups.deny

</td><td>

List of externally defined groups that are denied access to the external document. ServiceNow AI Platform® users mapped to any of these external groups can't view the indexed search result record created from the document. Set this permission for an ingested document via the \[array\].principals.groups.deny request body parameter in a request to the POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint of the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 This permission takes precedence over **groups.read**. If the same group has both read and deny access permissions for a document, AI Search denies members of the group access to the indexed record.

 By default, **users.read** takes precedence over this permission. To reverse this precedence order for an indexed source, see [Change the precedence of user read and group deny permissions for an external content indexed source](defining-access-perms-ext-docs-ais.md#).

</td></tr><tr><td>

groups.read

</td><td>

List of externally defined groups that are allowed access to the external document. ServiceNow AI Platform users mapped to any of these external groups can view the indexed search result record created from the document. Set this permission for an ingested document via the \[array\].principals.groups.read request body parameter in a request to the POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint of the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 **groups.deny** permission takes precedence over this permission. If the same group has both read and deny access permissions for a document, AI Search denies members of the group access to the indexed record.

</td></tr><tr><td>

none

</td><td>

Boolean option indicating whether access to the external document is denied for all users. AI Search applies this global denial permission to the indexed record created from the document. Set this permission for an ingested document via the \[array\].principals.none request body parameter in a request to the POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint of the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 When set to **true**, this permission overrides all **groups** and **users** permissions.

 This permission is mutually exclusive with **none**. Only one of these two permissions can be set to **true** for any external document.

</td></tr><tr><td>

users.deny

</td><td>

List of externally defined users that are denied access to the external document. ServiceNow AI Platform users mapped to any of these external users can't view the indexed search result record created from the document. Set this permission for an ingested document via the \[array\].principals.users.deny request body parameter in a request to the POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint of the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 This permission takes precedence over **users.read**. If the same user has both read and deny access permissions for a document, AI Search denies that user access to the indexed record.

</td></tr><tr><td>

users.read

</td><td>

List of externally defined users that are allowed access to the external document. ServiceNow AI Platform users mapped to any of these external users can view the indexed search result record created from the document. Set this permission for an ingested document via the \[array\].principals.users.read request body parameter in a request to the POST /ais/external\_content/ingestDocument/\{schema\_table\_name\} endpoint of the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 **users.deny** takes precedence over this permission. If the same user has both read and deny access permissions for a document, AI Search denies that user access to the indexed record.

 By default, this permission takes precedence over **groups.deny**. To reverse this precedence order for an indexed source, see [Change the precedence of user read and group deny permissions for an external content indexed source](defining-access-perms-ext-docs-ais.md#).

</td></tr></tbody>
</table>### Precedence order for principal permissions

The precedence order for **\[array\].principals** permissions on an ingested external document depends on the value of the **user\_read\_takes\_precedence\_over\_group\_deny** attribute for the document's indexed source.

<table id="table_vlm_d2t_vpb"><thead><tr><th>

Attribute value

</th><th>

Precedence order for principal permissions

</th></tr></thead><tbody><tr><td>

true

</td><td>

From highest precedence to lowest:1.  **everyone** and **none**
2.  **users.deny**
3.  **users.read**
4.  **groups.deny**
5.  **groups.read**

 **Note:** This is the default attribute value for external content indexed sources.

</td></tr><tr><td>

false

</td><td>

From highest precedence to lowest:1.  **everyone** and **none**
2.  **users.deny** and **groups.deny**
3.  **users.read** and **groups.read**

 **Note:** For instructions on setting this attribute value, see [Change the precedence of user read and group deny permissions for an external content indexed source](defining-access-perms-ext-docs-ais.md#).

</td></tr></tbody>
</table>For details on how content security permissions from certain user roles interact with these external content security principals, see [Special external content access permissions by role](defining-access-perms-ext-docs-ais.md#).

## Special external content access permissions by role

Certain user roles provide special access permissions for external content indexed records.

<table id="table_kp5_cnd_vpb"><thead><tr><th>

Role

</th><th>

Permissions

</th></tr></thead><tbody><tr><td>

AI Search administrator \[ais\_admin\]

</td><td>

An AI Search administrator can access all external content indexed records in a search application.**Note:** To bypass all search source and content security filtering in the Search Preview UI, you also need the impersonator and AI Search high security administrator \[ais\_high\_security\_admin\] roles. For details on this procedure, see [Diagnose search result access issues using the Search Preview UI](../task/diagnose-srch-result-access-ais.md).

</td></tr><tr><td>

Guest user \[public\]

</td><td>

Non-authenticated guest users can only access external content indexed records that have the **everyone** permission set to **true**.

</td></tr><tr><td>

Self-registered external user \[snc\_external\]

</td><td>

Self-registered external users that belong to groups can access external content indexed records based on their group memberships. External users that don't belong to any group can only access external content indexed records that have the **everyone** permission set to **true**. For more details on self-registered external users, see [Self-register to ServiceNow instance](https://www.servicenow.com/docs/access?context=external-user-self-registration&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr></tbody>
</table>## Change the precedence of user read and group deny permissions for an external content indexed source

Make external group deny access permissions take precedence over external user read access permissions for all external documents ingested through an indexed source.

### Before you begin

The External Content for AI Search plugin \(com.glide.ais.external\_content\) must be activated in your instance.

The source table for the indexed source must be an external content schema table.

Role required: ais\_admin

### About this task

By default, external user read access permissions \(**users.read**\) on an external document take precedence over external group deny access permissions \(**groups.deny**\) on the same document.

For example, suppose you ingest external content through an indexed source with a user mapping that maps ServiceNow AI Platform® user **beth.anglin@example.com** to external user **ad\\beth-anglin** and external group **report-users**. If an external document grants read access to **ad\\beth-anglin** and denies access to **report-users**, AI Search allows **beth.anglin@example.com** to view the indexed search result record for the external document.

To reverse this default behavior for an indexed source, making external group deny permissions take precedence over external user read permissions for all of its indexed records, change the value of the indexed source's **user\_read\_takes\_precedence\_over\_group\_deny** attribute. In the preceding example, making this change would prevent **beth.anglin@example.com** from viewing the indexed search result record for the external document.

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  If the Advanced Configuration related list doesn't appear on the form, follow the steps in [Add a related list to a form](../../form-administration/concept/configure-form-layout.md#), selecting the **AI Search Indexed Source Attribute-&gt;Indexed Source** list in the slushbucket.

3.  In the Advanced Configuration related list, select **New**.

4.  On the Indexed Source Attribute form, enter the following field values.

    |Field|Value|
    |-----|-----|
    |Attribute|user\_read\_takes\_precedence\_over\_group\_deny|
    |Value|false|

    For a description of the field values, see [Indexed Source Attribute form](../reference/indexed-source-attribute-form-ais.md).

5.  Select **Submit**.

    The attribute and value appear in the Advanced Configuration related list.


### Result

The change in permission preference takes effect for search results from the external content indexed source.

