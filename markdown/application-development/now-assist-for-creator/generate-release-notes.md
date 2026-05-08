---
title: Generate release notes
description: Generate release notes to document app changes and versions over time.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Release lifecycle documentation AI agent, Use agentic AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Generate release notes

Generate release notes to document app changes and versions over time.

## Before you begin

You must have the release lifecycle documentation AI agent turned on in AI Agent Studio. For more information, see [Configure release lifecycle documentation AI agent](../concept/configure-release-lifecycle-documentation-ai-agent.md).

A release must be in the **Complete** state to generate release notes using the release lifecycle documentation AI agent.

Role required: sn\_aia.viewer, update\_set\_admin, and sn\_releaseops.release\_notes\_user

## Procedure

1.  Navigate to **All** &gt; **ReleaseOps** &gt; **Releases**.

2.  Select the release from the list.

3.  On the release record page, select **Generate release notes**.

    **Important:** Each time you generate release notes using the release lifecycle documentation AI agent, the operation counts as an assist that is tracked by your Now Assist subscription. To track your Now Assist usage, see Monitoring Now Assist usage in Subscription Management.

    The release lifecycle documentation AI agent generates the release notes, which might take several minutes. Once release notes have been generated, you can view them in the **Release notes** tab of the release.

4.  Edit the release notes manually as needed.

    1.  On the release record page, select the Release notes tab.

    2.  Select the most current version of the release notes, or the version that you want to edit, by selecting the link in the **Version** column.

    3.  Edit the release notes as needed.

    4.  Select **Update**.

5.  Regenerate the release notes as needed.

    **Note:** If you have an App Engine Management Center \(AEMC\) subscription, you can regenerate \(not generate\) release notes using the release lifecycle documentation AI agent inside AEMC.

    1.  If you aren't already on a release notes record page, navigate to a release record through either of the following navigation paths.

        -   From App Engine Management Center \(AEMC\), navigate to the **Release management** tab.
        -   From ReleaseOps, navigate to **All** &gt; **ReleaseOps** &gt; **Releases**.
    2.  Select the release from the list.

    3.  Navigate to the release notes.

        -   In AEMC, select **View notes**.
        -   In ReleaseOps, select the **Release notes** tab.
    4.  Select the most current version of the release notes, or the version that you want to edit, by selecting the link in the **Version** column.

    5.  Select **Regenerate**.


**Parent Topic:**[Release lifecycle documentation AI agent](../concept/release-lifecycle-documentation-agent-landing.md)

