---
title: Implementing a custom connector
description: Your custom connector retrieves content, metadata, and security principals from a system of your choice. It runs on your local or cloud server and uses the Custom Connector Gateway API to send its retrieved data to a Custom Connector Gateway external content connector defined on your ServiceNow AI Platform instance. The Custom Connector Gateway connector feeds the retrieved data to AI Search for indexing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/implementing-custom-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-10-29"
reading_time_minutes: 9
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Custom Connector Gateway external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Implementing a custom connector

Your custom connector retrieves content, metadata, and security principals from a system of your choice. It runs on your local or cloud server and uses the Custom Connector Gateway API to send its retrieved data to a Custom Connector Gateway external content connector defined on your ServiceNow AI Platform® instance. The Custom Connector Gateway connector feeds the retrieved data to AI Search for indexing.

You can implement your custom connector in any programming language or framework you prefer. As long as it satisfies the requirements listed in the following section, it's usable with the Custom Connector Gateway API and external content connector.

## Custom connector requirements

To operate with the Custom Connector Gateway, your custom connector must perform these tasks.

<table id="table_m5n_jfr_ljc"><thead><tr><th>

Requirement

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Retrieve content and metadata from source system documents

</td><td>

Crawl source system documents and retrieve all information that you want to make searchable in AI Search applications.If your source system has access permissions associated with user or group security principals, this crawl must also retrieve those access permissions for each document.

</td></tr><tr><td>

Retrieve source system security principals

</td><td>

Crawl user security principals and retrieve their details and group memberships.This task is only required if your source system has access permissions associated with user or group security principals.

</td></tr><tr><td>

Request an OAuth 2.0 access token

</td><td>

Obtain an OAuth 2.0 access token from your ServiceNow AI Platform instance.To learn about requesting an OAuth 2.0 access token, see [Custom Connector Gateway API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/custom-connector-gateway-api.md).

</td></tr><tr><td>

Request a JSON Web Token for the Custom Connector Gateway API

</td><td>

Create or retrieve a schema-specific JSON Web Token \(JWT\) from your ServiceNow AI Platform instance.Use this JWT to authenticate requests sent to the Custom Connector Gateway API endpoint on your instance's ingest gateway host.

</td></tr><tr><td>

Submit requests to the Custom Connector Gateway API endpoint on your instance's ingest gateway host

</td><td>

Send retrieved data to AI Search for indexing via requests submitted to the `xcc-ingest` Custom Connector Gateway API endpoint on your ingest gateway host.

</td></tr></tbody>
</table>The following architecture diagram illustrates how your custom connector interacts with services on other hosts.

\[Omitted image "MMASSET0022098\_architecture\_diagram\_horizontal.svg"\] Alt text: Architecture diagram showing connections between custom connector host, source system, ingest gateway host, ServiceNow AI Platform instance, and AI Search node

## Custom connector responsibilities

Your organization is responsible for implementing a custom connector that satisfies the preceding requirements.

You're also responsible for operating and securing your custom connector and the server it runs on.

## Retrieving content and metadata from source system documents

Your connector must crawl all source system documents that you want to index for search in AI Search applications. For each document crawled, it must retrieve all content and metadata that you want to index.

If documents in your source system have access permissions associated with user or group security principals, your custom connector must also retrieve those access permissions when crawling. AI Search preserves each document's access permissions so that only users with access to the original document can see it in search results.

As an example, to index files from a local filesystem, your connector must be able to identify and crawl all of those files. It must retrieve each file's content and any metadata that you want to make available in search, such as its size, its path, and so on. If your source filesystem supports user- and group-based access permissions, your custom connector must also retrieve all of these access permissions for each file when crawling the source filesystem.

## Retrieving source system security principals

If documents in your source system have access permissions associated with user or group security principals, your custom connector must retrieve details for each new or updated user security principal, including their group memberships. AI Search maps these security principal definitions to ServiceNow AI Platform instance users, preserving access permissions for your indexed documents.

Continuing the preceding examples, your custom connector must retrieve details \(including group memberships\) for all user security principals who have access to files in the source filesystem.

## Requesting an OAuth 2.0 access token

Your custom connector must be able to request an OAuth 2.0 access token from your ServiceNow AI Platform instance as described in [Client credentials grant workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/client-credentials-grant-workflow.md).

The connector's POST request body must specify the `grant_type=client_credentials` parameter and include values for the required `client_id` and `client_secret` parameters. It can omit the optional `scope` parameter.

The OAuth 2.0 access token returned by this request includes an `access_token` field and an `expires_in` field, with a duration value expressed in seconds. Your custom connector should cache the token and should proactively request a new token before the current one expires.

For more information on requesting an OAuth 2.0 access token for use with the Custom Connector Gateway connector, see [Custom Connector Gateway API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/custom-connector-gateway-api.md).

## Requesting a JSON Web Token \(JWT\) for the Custom Connector Gateway API

Your custom connector must be able to request a JSON Web Token \(JWT\) for the Custom Connector Gateway API from your ServiceNow AI Platform instance. This request requires the OAuth 2.0 access token for authentication.

Each JWT for the Custom Connector Gateway API is scoped to a specific Custom Connector Gateway external content connector. Only requests for this connector should use the JWT.

To get a JWT using the Custom Connector Gateway API, you can send a `generate` request to generate a new JWT or a `fetch` request to retrieve an existing \(cached\) JWT.

```
POST https://<instance-name>.service-now.com/api/sn_ext_conn/xcc_api/jwt/<sys_id>/generate
Authorization: Bearer <oauth_access_token>
Content-Type: application/json
{}
```

```
GET https://<instance-name>.service-now.com/api/sn_ext_conn/xcc_api/jwt/<sys_id>/fetch
Authorization: Bearer <oauth_access_token>
```

In both of these requests, replace values as follows:

-   Replace `<instance-name>` with the hostname of your ServiceNow AI Platform instance.
-   Replace `<sys_id>` with the sys\_id of the Custom Connector Gateway external content connector to use for all requests you submit to the API endpoint with this JWT.

    **Note:** For details on finding the sys\_id of a Custom Connector Gateway external content connector, see [Get the sys\_id for a Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/get-sys-id-custom-connector-gateway-external-content-connector.md).

-   Replace `<oauth_access_token>` with the `access_token` value from the OAuth 2.0 access token returned by your OAuth 2.0 access token request.

For simplicity, your custom connector can submit a `fetch` request first, and only fall back to submitting a `generate` request if no current JWT exists for the specified schema.

The JWT generated by the `generate` request expires. Your custom connector should generate a new JWT before the current one expires.

For more information on requesting a JWT for use with the Custom Connector Gateway connector, see [Custom Connector Gateway API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/custom-connector-gateway-api.md).

## Submitting requests to the Custom Connector Gateway API endpoint

Your custom connector must submit its retrieved data to AI Search via requests sent to the `xcc-ingest` Custom Connector Gateway API endpoint on your ingest gateway host. Each source system document requires one add request, as does each security principal. Removing documents and security principals from the index to clean up stale content is also possible via delete requests. All of these requests require the Custom Connector Gateway API JWT for authentication.

Continuing the preceding examples, after a crawl, your custom connector must send an ADDDOCUMENT request for each file added or changed in the source system. To facilitate removal of stale content, it can optionally send a TOUCHDOCUMENT request for each file unchanged in the source system. It must send an ADDPRINCIPAL request for each security principal with new or updated details \(including group memberships\). And it should send a DELETEBYQUERY request after each crawl to remove stale content from the AI Search index.

The following table summarizes the requests supported by the `xcc-ingest` Custom Connector Gateway API endpoint on your ingest gateway host.

|Request type|Description|
|------------|-----------|
|ADDDOCUMENT|Add a document to the AI Search index. If a document with the same ID already exists in the index, update \(overwrite\) that document instead.|
|ADDPRINCIPAL|Add a user mapping for an external user security principal to a user defined on your ServiceNow AI Platform instance. If an existing user mapping exists for the instance user, update \(overwrite\) that mapping instead.|
|DELETEALLDOCUMENTS|Delete all documents indexed by this custom connector.|
|DELETEALLPRINCIPALS|Delete all user mappings defined for this custom connector.|
|DELETEBYQUERY|Delete all documents indexed by this custom connector that match a search query expression.|
|DELETEDOCUMENT|Delete a specified document indexed by this custom connector.|
|DELETEPRINCIPAL|Delete the user mapping for a specified external user security principal defined for this custom connector.|
|TOUCHDOCUMENT|Update the last-seen timestamp for a document without reindexing its content or metadata.|

For complete details on the `xcc-ingest` Custom Connector Gateway API endpoint and the requests it supports, see [Custom Connector Gateway API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/custom-connector-gateway-api.md).

## The ingest gateway host

The ingest gateway host is a server provided by ServiceNow to facilitate Custom Connector Gateway API operations. It's distinct from both your ServiceNow AI Platform instance and your AI Search node.

Your custom connector must send all Custom Connector Gateway API requests to the `xcc-ingest` endpoint on the ingest gateway host associated with your ServiceNow AI Platform instance. To get the hostname for this ingest gateway host, ask a user with the admin role on your instance to look up the value of the **sn\_itom\_cloud\_svc.itomgateway\_url** system property. For details on this procedure, see [Find the hostname for your ingest gateway host](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/find-hostname-ingest-gateway-host.md).

## Cleaning up stale content

When a source document is deleted between crawls, its entry remains in the AI Search index until you delete it. To remove stale document entries from the index, follow this algorithm when submitting Custom Connector Gateway API requests after each content crawl.

1.  Record the current time. As an example, your connector might set the value of a variable called `crawl_start` to the timestamp for the current time.
2.  Submit all ADDDOCUMENT and TOUCHDOCUMENT requests from the content crawl to the `xcc-ingest` Custom Connector Gateway API endpoint. Use ADDDOCUMENT requests to add new documents or to update documents that were modified since the previous crawl. Use TOUCHDOCUMENT requests to update the last-seen timestamps for documents that are unchanged since the previous crawl.

    **Note:** AI Search automatically sets the `last_seen_rt` field on each indexed document with a value indicating its actual ingestion time. Your custom connector shouldn't set this field on ADDDOCUMENT requests.

3.  After all ADDDOCUMENT requests are complete, submit a DELETEBYQUERY request with the query condition `last_seen_rt:RANGE(*, <timestamp>, upper=exclusive)`, replacing `<timestamp>` with the timestamp that you recorded in the first step. This request deletes the stale index entries for all documents that weren't encountered during the most recent crawl.

    As an example, you might specify `last_seen_rt:RANGE(*, \"2026-07-20 00:00:00\", upper=exclusive)` as the query for the DELETEBYQUERY request.


**Parent Topic:**[Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/custom-connector-gateway-external-content-connector.md)

