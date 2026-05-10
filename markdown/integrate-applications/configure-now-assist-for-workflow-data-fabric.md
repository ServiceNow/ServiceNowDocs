---
title: Configure Now Assist for Workflow Data Fabric \(WDF\)
description: If you have the admin role, you can configure the Now Assist for Workflow Data Fabric \(WDF\) application to enable AI capabilities across the Workflow Data Fabric platform.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Assist for Workflow Data Fabric \(WDF\), Workflow Data Fabric Home, Workflow Data Fabric]
---

# Configure Now Assist for Workflow Data Fabric \(WDF\)

If you have the admin role, you can configure the Now Assist for Workflow Data Fabric \(WDF\) application to enable AI capabilities across the Workflow Data Fabric platform.

## Before you begin

To install any Now Assist plugin, you must have Now Assist capabilities activated. For more information, see [Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for WDF. For additional information, see [Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

The oneExtend LLM skill is included in Now Assist for WDF.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Find the Now Assist for WDF plugin \(sn\_nowassist\_wdf\) using the filter criteria and search bar and install the Now Assist for WDF plugin \(sn\_nowassist\_wdf\).

    For information about the installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

3.  Select the Now Assist for WDF plugin tile, select **Install**, and confirm.

4.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home** and create the **ServiceNow Product Documentation** connector to index and enhance AI search with content from the ServiceNow product documentation site.

    Core functionality isn’t affected if skipped, but some AI agent capabilities may be limited. For more information, see [https://www.servicenow.com/docs/r/platform-administration/ai-search/servicenow-product-documentation-external-content-connector.html](https://www.servicenow.com/docs/r/platform-administration/ai-search/servicenow-product-documentation-external-content-connector.html).

    ![Screenshot showing the product documentation content connector tile.](../image/wdf-ai-doc-connector.png)

5.  Activate the flow generation skill.

    Core functionality isn’t affected if skipped, but some AI agent capabilities may be limited.

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

        ![Screenshot showing the Flow generation tile.](../image/wdf-ai-config1.png)

    2.  On the **Flow generation** tile, select **Turn on** and confirm to activate the skill.

        You’re asked to specify any ACLs permitted to access the flow generation skill and configure role restrictions. You can leave these fields empty. For more information, see [https://www.servicenow.com/docs/r/build-workflows/now-assist-for-creator/turn-on-the-flow-generation-skill.html](https://www.servicenow.com/docs/r/build-workflows/now-assist-for-creator/turn-on-the-flow-generation-skill.html).

        ![Screenshot showing the Flow generation activation screen.](../image/wdf-ai-config2.png)

    3.  Delete a skill by selecting **Deactivate skill** on the skill's tile, and confirm.


**Related topics**  


[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)

[Configuring Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-na-landing.md)

