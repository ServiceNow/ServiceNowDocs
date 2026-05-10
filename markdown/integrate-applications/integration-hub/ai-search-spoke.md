---
title: AI Search Spoke
description: Store data from the required third-party application in the AI Search server through Workflow Studio. Access data through the AI Search portal.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# AI Search Spoke

Store data from the required third-party application in the AI Search server through Workflow Studio. Access data through the AI Search portal.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

AI Search spoke v2.0.3 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are activated:

-   AI Search \(com.glide.ais\)
-   External Content for AI Search \(com.glide.ais.external\_content\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The AI Search spoke provides actions to automate tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_hfv_43j_h4b"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Commit Index

</td><td>

Commits queued documents in the batcher and indexes them. Synchronously returns feedback about the indexed content.

</td></tr><tr><td>

Delete Document

</td><td>

Deletes a record from the AI Search content index.

</td></tr><tr><td>

Delete Documents

</td><td>

Deletes all records that use a specified external content schema table from the AI Search content index. You can optionally specify a Glide query to limit the set of documents deleted from the specified schema table.

</td></tr><tr><td>

Get Max File Size

</td><td>

Retrieves the maximum file size which can be ingested into AI Search.

</td></tr><tr><td>

Ingest Document

</td><td>

Ingests properties of the specified document into the batcher. In releases starting with Rome, you can optionally specify security principal access permissions for the document.

 Specify the document's properties as name-value pairs in a JSON object formatted as in the following example:

```
{
  "title": "Report 2021-02-26",
  "author": "Abel Tuter",
  "url": "http://example.com/reports/2021/02/26/"
}
```

 You can specify the document's security principal access permissions as name-value pairs in a JSON object formatted as in the following example:

```
{
  "everyone": false,
  "groups.deny": [
    "report-users",
    "hr-users"
  ],
  "groups.read": [
    "report-admins",
    "hr-admins"
  ],
  "none": false,
  "users.deny": [
    "ad\bow-ruggeri",
    "don_goodliffe"
  ],
  "users.read": [
    "ad\beth-anglin",
    "ad\abel-tuter",
    "carol.coughlin@sharepoint"
  ]
}
```

 For more details on security principal access permissions, see [External content access permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-access-perms-ext-docs-ais.md).

</td></tr><tr><td>

Ingest Document Using Download URL

</td><td>

Downloads a document from a URL and ingests it into the batcher. In releases starting with Rome, you can optionally specify security principal access permissions for the document.

 Add the URL's domain to the AI Search spoke's list of trusted domains before you specify this action's **Download URL** input. For details on modifying the spoke's list of trusted domains, see [Set up the AI Search spoke](../task/setup-ais-spoke.md).

 This action doesn't support authentication session IDs or cookies, so the document URL must allow unauthenticated access.

 Specify the document's properties as name-value pairs in a JSON object formatted as in the following example:

```
{
  "title": "Report 2021-02-26",
  "author": "Abel Tuter"
}
```

The document's **url** property is automatically populated with the value of the **Download URL** input.

 You can specify the document's security principal access permissions as name-value pairs in a JSON object formatted as in the following example:

```
{
  "everyone": false,
  "groups.deny": [
    "report-users",
    "hr-users"
  ],
  "groups.read": [
    "report-admins",
    "hr-admins"
  ],
  "none": false,
  "users.deny": [
    "ad\bow-ruggeri",
    "don_goodliffe"
  ],
  "users.read": [
    "ad\beth-anglin",
    "ad\abel-tuter",
    "carol.coughlin@sharepoint"
  ]
}
```

 For more details on security principal access permissions, see [External content access permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-access-perms-ext-docs-ais.md).

</td></tr><tr><td>

Initialize Batcher

</td><td>

Initializes a new batcher to queue documents for indexing.

</td></tr><tr><td>

Is AIS Available For Ingestion

</td><td>

Checks whether AI Search is available for ingestion.

</td></tr><tr><td>

Look up Supported File Extensions

</td><td>

Retrieves file extensions supported by AI Search.

</td></tr><tr><td>

Release Batcher

</td><td>

Releases a used batcher from pool.

</td></tr><tr><td>

Update By Query

</td><td>

Updates all the records in the AI Search content index that match the specified query.

</td></tr></tbody>
</table>See [Set up the AI Search spoke](../task/setup-ais-spoke.md) for information about setting up the AI Search spoke.

