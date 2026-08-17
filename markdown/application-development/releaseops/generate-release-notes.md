---
title: Generate release notes
description: Generate release notes to document app changes and versions over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/releaseops/generate-release-notes.html
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 2
keywords: [generate release notes, release notes generation, ReleaseOps, ReleaseOps AI, release lifecycle documentation AI agent, generate description]
breadcrumb: [Use, ReleaseOps, Deploying applications, Building applications]
---

# Generate release notes

Generate release notes to document app changes and versions over time.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

You must have the release lifecycle documentation AI agent turned on in AI Agent Studio. For more information, see [Configure release lifecycle documentation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/configure-release-lifecycle-documentation-ai-agent.md).

A release must be in the **Complete** state to generate release notes using the release lifecycle documentation AI agent.

Role required: sn\_aia.viewer, update\_set\_admin, and sn\_releaseops.release\_notes\_user

## Procedure

1.  Navigate to **All** &gt; **ReleaseOps** &gt; **Releases**.

2.  Select the release from the list.

3.  On the release record page, select **Generate release notes**.

    **Important:** Each time you generate release notes using the release lifecycle documentation AI agent, the operation counts as an assist that is tracked by your ServiceNow Otto subscription. To track your ServiceNow Otto usage, see [Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md).

    The release lifecycle documentation AI agent generates the release notes, which might take several minutes. Once release notes have been generated, you can view them in the **Release notes** tab of the release.

4.  Edit the release notes manually as needed.

    1.  On the release record page, select the Release notes tab.

    2.  Select the most current version of the release notes, or the version that you want to edit, by selecting the link in the **Version** column.

    3.  Edit the release notes as needed.

    4.  Select **Update**.

5.  Regenerate the release notes as needed.

    **Note:** If your license entitles you to use App Engine Management Center \(AEMC\), you can regenerate \(not generate\) release notes using the release lifecycle documentation AI agent inside AEMC.

    1.  If you aren't already on a release notes record page, navigate to a release record through either of the following navigation paths.

        -   From App Engine Management Center \(AEMC\), navigate to the **Release management** tab.
        -   From ReleaseOps, navigate to **All** &gt; **ReleaseOps** &gt; **Releases**.
    2.  Select the release from the list.

    3.  Navigate to the release notes.

        -   In AEMC, select **View notes**.
        -   In ReleaseOps, select the **Release notes** tab.
    4.  Select the most current version of the release notes, or the version that you want to edit, by selecting the link in the **Version** column.

    5.  Select **Regenerate**.


**Parent Topic:**[Using ReleaseOps to manage deployments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/releaseops/using-releaseops-to-manage-deployments.md)

