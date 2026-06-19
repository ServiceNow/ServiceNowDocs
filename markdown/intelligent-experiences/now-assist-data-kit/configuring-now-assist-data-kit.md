---
title: Configuring Now Assist Data Kit
description: Configure system properties, plugins, and roles to enable all features of Now Assist Data Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/configuring-now-assist-data-kit.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [Now Assist Data Kit, Enable AI experiences]
---

# Configuring Now Assist Data Kit

Configure system properties, plugins, and roles to enable all features of Now Assist Data Kit.

## System properties

Some Now Assist Data Kit features require system properties that are not enabled by default. Configure the following properties in System Properties after installation.

|Property|Value|Description|
|--------|-----|-----------|
|`sn_data_kit.enable_ground_truth`|true|Enables the **Create ground truth guidelines** button on dataset records. Must be created manually in the **Global** application scope as a String type. If this property does not exist or is set to any other value, the button does not appear.|

## Required plugins for sensitive data scanning

The sensitive data scan feature requires the following plugins to be active on your instance. Activate these before using [Find and cleanse sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/sensitive-data.md).

-   `sn_data_discovery`
-   `sn_dp_store_app` \(Data Privacy\)
-   `com.glide.data_privacy`

## Role configuration

After installing Now Assist Data Kit, assign roles to users who need access. The platform `admin` role alone does not grant access to the application. All users, including administrators, require at least `sn_data_kit.analyst` to access the Now Assist Data Kit Home page. For full role descriptions and special considerations, see .

