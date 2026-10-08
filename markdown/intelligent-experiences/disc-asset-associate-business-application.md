---
title: Associate a business application with an AI system
description: Associate an existing business application with an AI system asset, independently of whether the Enterprise Architecture Workspace plugin is installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/disc-asset-associate-business-application.html
release: zurich
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 2
keywords: [business application, AI system, relationships]
breadcrumb: [Managing AI asset details, Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Associate a business application with an AI system

Associate an existing business application with an AI system asset, independently of whether the Enterprise Architecture Workspace plugin is installed.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner

## About this task

You can associate a business application with an AI system either while creating the AI system asset, or afterward by editing an existing AI system's relationships.

This association requires the Enterprise Architecture for AICT plugin, which installs automatically with AI Control Tower Core at the required version. For upgrade-order considerations, see [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-ea-common-upgrade-considerations.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower** &gt; **Inventory**.

2.  On the Inventory page, select **Add AI asset**.

    The Add AI asset dialog box appears.

3.  In the dialog box, select **Enter asset details**.

4.  From the list of available asset types, select **AI system**.

    The dialog box closes and you're automatically redirected to the Add AI system asset form.

5.  In the **Details** section of the form, fill in the fields.

    For field information, see [Create AI system assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-system-assets-newexperience.md).

6.  Select **Next**.

7.  On the Relationships page, from the **Related to** list, select **Business Applications**.

8.  Select **Add from inventory**.

9.  In the Select Business Applications dialog box, select the check box next to each business application to associate, and then select **Add**.

10. Select **Next** or **Submit for review**.

    -   If you're creating a new asset, select **Next** to continue to **Use and Purpose**.
    -   If you're editing an existing asset, select **Submit for review**.

## Result

The selected business applications appear in the **Details** tab for that AI system.

**Parent Topic:**[Managing AI asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-ai-asset-details.md)

**Related topics**  


[Managing AI asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-ai-asset-details.md)

[Create AI system assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/create-ai-system-assets-newexperience.md)

[Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-ea-common-upgrade-considerations.md)

[AI Control Tower integration with Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-portfolio-management/eaw-aict.md)

