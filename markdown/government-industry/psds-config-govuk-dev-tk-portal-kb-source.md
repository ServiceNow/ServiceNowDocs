---
title: Configure Knowledge Base sources
description: Associate the GDS Service Portal with one or more knowledge bases to display articles from this knowledge base in the portal widgets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-govuk-dev-tk-portal-kb-source.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 1
breadcrumb: [Configure knowledge base, Configure UK GDS Service Portal, GOV.UK Developer Toolkit, Set up self-service, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Knowledge Base sources

Associate the GDS Service Portal with one or more knowledge bases to display articles from this knowledge base in the portal widgets.

## About this task

**Note:**

Users with the knowledge\_admin or admin role can configure the widget instance options used on the Knowledge Management Service Portal pages. Use the context menu to access the widget instance options and configure a widget instance. For more information, see [Configure Widgets Instance Options for GOV.UK Design System Service Portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-govuk-dev-tk-portal-widgets-instances.md).

You can also use the external content integration feature to integrate content from various external sources and enable unified knowledge search results. For more information, see [Integration with external knowledge sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-external-content-integration.md).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Knowledge Bases** to create or edit the knowledge base you want to associate with the GDS Service Portal.

2.  Navigate to **All** &gt; **Service Portals** &gt; **Portals**.

3.  In the Knowledge Bases related list, select **Edit**.

    **Note:** If you don't see the **Edit** option, confirm that you have the GOV.UK Developer Toolkit application scope selected in the application picker.

4.  On the **Edit Members** form, select one or more knowledge bases to add to the GDS Service Portal, and move the desired knowledge bases from the available items in the **Collection** column to the **Knowledge Bases List** column.

5.  Select **Update**.


## Result

The knowledge bases are displayed on the KB homepage for the portal. If no knowledge bases are added, all knowledge bases are available in the portal. If knowledge bases are mapped, only those knowledge bases are available in the portal. All search results and all widgets display results from the mapped knowledge bases only.

## What to do next

Determine whether certain users or categories of users can access knowledge bases and knowledge articles by controlling contribute and read access. For more information, see [Managing access to knowledge bases and knowledge articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/user-access-knowledge.md).

