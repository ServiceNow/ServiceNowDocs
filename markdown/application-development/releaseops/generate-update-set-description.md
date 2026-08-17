---
title: Generate an update set description
description: Generate an update set description to quickly communicate the intent and scope of changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/releaseops/generate-update-set-description.html
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
keywords: [generate update set description, ReleaseOps, ReleaseOps AI, release lifecycle documentation AI agent, generate description]
breadcrumb: [Use, ReleaseOps, Deploying applications, Building applications]
---

# Generate an update set description

Generate an update set description to quickly communicate the intent and scope of changes.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

You must have the release lifecycle documentation AI agent turned on in AI Agent Studio. For more information, see [Configure release lifecycle documentation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/configure-release-lifecycle-documentation-ai-agent.md).

Update sets must be in certain states for you to generate descriptions using the release lifecycle documentation AI agent. The following table explains what update set locations and states support description generation.

<table id="table_o11_vm4_33c"><thead><tr><th>

Update set location

</th><th>

Required state

</th></tr></thead><tbody><tr><td>

Local update sets

</td><td>

-   In progress
-   Complete

</td></tr><tr><td>

Remote update sets

</td><td>

-   Loaded
-   Reviewed

</td></tr></tbody>
</table>You can’t generate an update set description for an update set marked as the default update set.

Role required: sn\_aia.viewer and update\_set\_admin

## Procedure

1.  Navigate to an update set.

    -   To navigate to a local update set, navigate to **All** &gt; **System update sets** &gt; **Local update sets**.
    -   To navigate to a remote update set, navigate to **All** &gt; **System update sets** &gt; **Retrieved update sets**.
2.  Select the update set from the list.

3.  On the update set record page, select **Generate description**.

    **Important:** Each time you generate a description using the release lifecycle documentation AI agent, the operation counts as an assist that is tracked by your ServiceNow Otto subscription. To track your ServiceNow Otto usage, see [Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md).

    The release lifecycle documentation AI agent generates the update set description, which might take several minutes. Once a description has been generated, the description is automatically added to the update set record.


**Parent Topic:**[Using ReleaseOps to manage deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/using-releaseops-to-manage-deployments.md)

