---
title: Yokohama Patch 4 Hotfix 2
description: The Yokohama Patch 4 Hotfix 2 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-10"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 4 Hotfix 2

The Yokohama Patch 4 Hotfix 2 release contains fixes to these problems.

-   **Build information:**

    Build date: 07-05-2025\_0001

    Build tag: glide-yokohama-12-18-2024\_\_patch4-hotfix2-07-03-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Virtual Agent Web Client

 PRB1874847

</td><td>

The **Cancel** icon doesn't close the tooltip, and the citation and feedback options aren't displayed when opened in a new tab

</td><td>

Two issues occur in this problem when using the Enhanced Chat in Customer Service Management \(CSM\) and interacting with the **Create case for a product** citation link. In the first scenario, selecting the **Cancel** icon after hovering over the**Create case for a product** link doesn't close the tooltip. In the second scenario, when selecting the **Create case for a product**, the 'Feedback options' and 'Go to search results' options are not displayed in the new tab.

</td><td>

Scenario 1:

 1.  Log in to the instance.
2.  Open Customer Service Management \(CSM\).
3.  Select the **Enhanced Chat** icon.
4.  Input the query, **Can you help me in raising a ticket for my product issue?**
5.  Notice the options in the response received:
    -   Create case for a product: Submit a case about your product, and our support team will assist you Create case for a product.
    -   Get Help with a Product \(Template\): Use this template to get help regarding a product issue Get Help with a Product \(Template\).
    -   The 'Feedback options' and 'Go to search results' options are displayed.
6.  Hover over the **Create case for a product** citation link.
7.  Select **Cancel**.

 Observe that selecting the **Cancel** icon doesn't close the tooltip.

 Scenario 2:

 1.  Log in to the instance.
2.  Open Customer Service Management \(CSM\).
3.  Select the Enhanced Chat icon.
4.  Input the query, **Can you help me in raising a ticket for my product issue?**
5.  Notice the options in the response received:
    -   Create case for a product: Submit a case about your product, and our support team will assist you Create case for a product.
    -   Get Help with a Product \(Template\): Use this template to get help regarding a product issue Get Help with a Product \(Template\).
    -   The 'Feedback options' and 'Go to search results' options are displayed.
6.  Select **Create case for a product**.
7.  Notice that the catalog form page is opened in a new tab, and the 'Chat' icon is loaded.

 Observe that the 'Feedback options' and 'Go to search results' options are not displayed in this new tab.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 4 Hotfix 1](yokohama-patch-4-hf-1-PO.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

