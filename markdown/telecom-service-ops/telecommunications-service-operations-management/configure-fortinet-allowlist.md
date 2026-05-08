---
title: Configure Fortinet allowlist
description: Configure connector definitions to limit polling to specific Fortinet ADOMs using allowlist settings.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Configure Fortinet SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Fortinet allowlist

Configure connector definitions to limit polling to specific Fortinet ADOMs using allowlist settings.

## Before you begin

Role required: tsom\_visibility\_admin

## About this task

You can now configure an allowlist of Fortinet ADOMs on each connector instance to limit polling to specific entities. Use multiple connector instances with disjoint allowlists to distribute collection across MID Servers and avoid polling interval overruns in large-scale deployments. Specify the ADOM from which the connector pulls data.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Search for Fortinet in the search box.

3.  Select the desired connector from the list, then the desired Connector Instance.

4.  Enter the adom name in the **adom** field in the**Connector Instance Values** section.

    The following table describes the **adom** field.

    |Field|Description|
    |-----|-----------|
    |Field Name|adom|
    |Field Type|Single-line text field|
    |Format|Single value, for example: ABC|
    |Matching|Exact string match against the name returned by the source system API|
    |Default|DVT- replace with a valid ADOM name|

    ![Screenshot showing the adom field in the Connector Instance Values section with example configuration](../images/fortinet-allowlist.png)Fortinet

5.  Select **Update** to save.

    The connector applies these values at each polling cycle.


