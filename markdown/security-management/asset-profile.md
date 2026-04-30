---
title: Create an asset profile in Security Posture Control
description: Create an asset profile with conditions to group assets. You can use these asset profiles in your policies.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use the workspace, Security Posture Control, Security Operations]
---

# Create an asset profile in Security Posture Control

Create an asset profile with conditions to group assets. You can use these asset profiles in your policies.

## Before you begin

Roles required: SPC Admin Group or SPC Analyst Group

## Procedure

1.  Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Asset profiles**.

2.  Select **New**.

    The condition builder is displayed. Note that the name includes the date and time you created the profile.

3.  Select the pen icon to edit the profile name with a unique name.

4.  Select **Save metadata**.

5.  Select one from the list for Connection:

    The asset profile supports three Connection types.

    -   **With CMDB metadata** - Collection of CMDB CI properties such as Host name, OS, OS version, First and Last seen, for example, or connections that have network adaptors or installed software.
    -   **With aggregated data** - Collection of properties with aggregated values reported by different sources for a given asset. An example is the various ways sources might report an OS version: `windows11`,`Win11`, `Windows 11`, and so on.
    -   **From CI class** - Collection of CI classes that includes Computer, Server, Virtual Machine Instance and others.
    The operators and logic for this asset profile policy builder is similar to the one described in [Creating your own policies in the Security Posture Control application](spc-creating-policies.md).

6.  Select **Create**.

    Your profile is displayed on the Asset Profiles list.

    You can associate asset profiles to any policies.

7.  Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Policies and findings**.

8.  Select a policy.

9.  In the Policies and profiles section, select one or more asset profiles.

10. Select **Save changes**.

    The policy audits your assets based on data imported from your service graph connectors and includes the conditions of the asset profiles that you added. You can [Create and activate a configured insight for Security Posture Control](spc-create-custom-insight.md) and add asset profiles as a filter.

11. Navigate to **All** &gt; **Security Posture Control Workspace** &gt; **Configured insights**.

    You must [Create and activate a configured insight for Security Posture Control](spc-create-custom-insight.md) before data is displayed on this page.

    Since the visualizations on this page are configured by policies, you can filter them with asset profiles. Filter the data for the visualizations by following these steps:

12. Select the filter icon.

13. Select **Select**.

14. Select and move any of the asset profiles in the Available column to the Applied column.

15. Select **Apply**.

    The custom insights visualizations are filtered to show data for the policies that included the asset profiles you chose. A message in the Filter pane indicates how many configured insights are filtered out as a result of the asset profiles you added. There might be a delay for updates to trending data, because the Run SPC Policy scheduled job must complete to update trending data.


