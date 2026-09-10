---
title: PostgreSQL authentication method fields
description: Fields that appear on the New PostgreSQL Connection form depending on the selected authentication type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/postgresql-authentication-method-fields-zcc.html
release: australia
topic_type: reference
last_updated: "2026-08-27"
reading_time_minutes: 1
keywords: [PostgreSQL, authentication, zero copy connector]
breadcrumb: [Reference, Zero Copy Connectors, Workflow Data Fabric]
---

# PostgreSQL authentication method fields

Fields that appear on the New PostgreSQL Connection form depending on the selected authentication type.

## Authentication type: AWS IAM

|Field|Description|
|-----|-----------|
|Database user|Database user for the connection when authenticating with AWS IAM. Required.|
|AWS region|AWS region where the RDS instance is hosted. Required.|
|AWS access key ID|Access key ID for the AWS IAM credentials used to authenticate. Required.|
|AWS secret access key|Secret access key for the AWS IAM credentials used to authenticate. Required.|

## Authentication type: GCP IAM

|Field|Description|
|-----|-----------|
|Service account key \(JSON\)|Uploaded file or pasted JSON content for the GCP service account key. Required.|
|Database user|Database user for the connection when authenticating with GCP IAM. Required.|
|GCP token scope|OAuth scope requested for the GCP IAM token. Not required.|

## Authentication type: OAuth

|Field|Description|
|-----|-----------|
|OAuth credential type|Type of OAuth credential used to authenticate. Confirmed values: Azure Service Principal, Access Token. Required.|
|Database user|Database user for the connection when authenticating with OAuth. Required.|
|Azure tenant ID|Azure AD tenant ID for the service principal. Required.|
|Azure client ID|Client ID \(application ID\) of the Azure AD service principal. Required.|
|Azure client secret|Client secret for the Azure AD service principal. Required.|
|Azure token scope|OAuth scope requested for the Azure AD token. Not required.|

**Parent Topic:**[Zero Copy Connectors reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/reference-zcc.md)

**Related topics**  


[Create a PostgreSQL connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-postgresql-connection-zcc.md)

