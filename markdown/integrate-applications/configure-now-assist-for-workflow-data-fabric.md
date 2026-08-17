---
title: Configure ServiceNow Otto for Workflow Data Fabric \(WDF\)
description: If you have the admin role, you can configure the ServiceNow Otto for Workflow Data Fabric \(WDF\) application to enable AI capabilities across the Workflow Data Fabric platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/configure-now-assist-for-workflow-data-fabric.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Configure ServiceNow Otto for Workflow Data Fabric \(WDF\)

If you have the admin role, you can configure the ServiceNow Otto for Workflow Data Fabric \(WDF\) application to enable AI capabilities across the Workflow Data Fabric platform.

## Before you begin

To install any ServiceNow Otto plugin, you must have ServiceNow Otto capabilities activated. For more information, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

Role required: admin

## About this task

Use the AI Admin Hub console to configure ServiceNow Otto for WDF. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

The oneExtend LLM skill is included in ServiceNow Otto for WDF.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Find the ServiceNow Otto for WDF plugin \(sn\_nowassist\_wdf\) using the filter criteria and search bar and install the plugin \(sn\_nowassist\_wdf\).

    For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

3.  Select the ServiceNow Otto for WDF plugin tile, select **Install**, and confirm.

4.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home** and create the **ServiceNow Product Documentation** connector to index and enhance AI search with content from the ServiceNow product documentation site.

    Core functionality isn’t affected if skipped, but some AI agent capabilities may be limited. For more information, see [https://www.servicenow.com/docs/r/platform-administration/ai-search/servicenow-product-documentation-external-content-connector.html](https://www.servicenow.com/docs/r/platform-administration/ai-search/servicenow-product-documentation-external-content-connector.html).

    \[Omitted image "wdf-ai-doc-connector.png"\] Alt text: Screenshot showing the product documentation content connector tile.

5.  Activate the flow generation skill.

    Core functionality isn’t affected if skipped, but some AI agent capabilities may be limited.

    1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

        \[Omitted image "wdf-ai-config1.png"\] Alt text: Screenshot showing the Flow generation tile.

    2.  On the **Flow generation** tile, select **Turn on** and confirm to activate the skill.

        You’re asked to specify any ACLs permitted to access the flow generation skill and configure role restrictions. You can leave these fields empty. For more information, see [https://www.servicenow.com/docs/r/build-workflows/now-assist-for-creator/turn-on-the-flow-generation-skill.html](https://www.servicenow.com/docs/r/build-workflows/now-assist-for-creator/turn-on-the-flow-generation-skill.html).

        \[Omitted image "wdf-ai-config2.png"\] Alt text: Screenshot showing the Flow generation activation screen.

    3.  Delete a skill by selecting **Deactivate skill** on the skill's tile, and confirm.


**Related topics**  


[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

