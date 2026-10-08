---
title: Australia Patch 6 Hotfix 1
description: The Australia Patch 6 Hotfix 1 release contains fixes to these problems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/australia-patch-6-hf-1-PO.html
release: australia
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 5
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 6 Hotfix 1

The Australia Patch 6 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 09-18-2026\_1033

    Build tag: glide-australia-02-11-2026\_\_patch6-hotfix1-09-16-2026


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

Knowledge Management

 PRB1990998

</td><td>

Selecting 'Machine Translate' on a source article with knowledge blocks is overriding translated block content

</td><td>

Before selecting 'Machine Translate', there are different block numbers in the different language articles. After, the block in the targeted translation article is replaced with the English version block.

</td><td>

1.  Log in to a base instance as a user with elevated privileges.
2.  Navigate to the English version of any article that has a published translated version and has blocks in it.
3.  Navigate to the article body section of the English version.
4.  Add a test sentence.
5.  Select the **Update** button to save changes to the English version.
6.  Scroll to the 'Related Links' section.
7.  Select **Translate**.
8.  From the 'Translate to' option, select the language of the existing translated version of the article.
9.  Validate the blocks on both the language articles.

Observe that there are two different block numbers.

10. Select the **Machine Translate** button.
11. Confirm that the translated content includes the test sentence.

 Observe that the block has been replaced with the English version block in the targeted translation article.

</td></tr><tr><td>

Knowledge Management

 PRB1999848

</td><td>

Anchor tags \('\#'\) in URLs are stripped from Word document imports in knowledge articles

</td><td>

The anchor shouldn't be removed and the link should take the user to anchored area. Instead, the anchor is removed, and the link takes the user to the top of the page.

</td><td>

1.  Navigate to **Knowledge** &gt; **Import articles**.
2.  Import a Word document that has a URL with an anchor tag.
3.  Verify that the import is completed.

 Observe that the anchor tag part of the URL is removed from the link. When the user selects the URL, it navigates to the top of page instead of the anchored area.

</td></tr><tr><td>

Knowledge Management

 PRB2063214

</td><td>

Tables in the generated KB article are displayed with bold borders, which differs from the source document formatting

</td><td>

This logic comes from the Word to HTML conversion from the KM API.

</td><td>

1.  Navigate to Policy and **Compliance** &gt; **Compliance Workspace**.
2.  Create a policy record \(or use an existing draft policy\).
3.  Populate the required policy fields.
4.  Assign yourself as the policy owner.
5.  Enable the policy for knowledge publication \(if applicable in the environment\).
6.  Create a .docx file that includes a table.
7.  Upload the file using the **Import Policy Text** button.
8.  Verify that the document content is imported into the policy text section.
9.  Save and update the policy record.
10. Move the policy through the life cycle: **Draft** &gt; **Review** &gt; **Awaiting Approval** &gt; **Approved**.
11. Publish the policy by selecting **Publish**.
12. Confirm the policy transitions to the 'Published' state.
13. Verify whether a corresponding Knowledge Article is automatically generated in kb\_knowledge and linked to the policy record.

 Observe that the generated Knowledge Article may incorrectly display tables with bold borders.

</td></tr><tr><td>

Knowledge Management

 PRB2070212

</td><td>

Second-level bullet points render as filled black circles instead of the expected empty/hollow circle

</td><td>

The bullet style for second-level items is incorrect. The logic comes from the Word to HTML conversion from the KM API.

</td><td>

1.  Navigate to Policy and **Compliance** &gt; **Compliance Workspace**.
2.  Create a policy record \(or use an existing draft policy\).
3.  Populate the required policy fields.
4.  Assign yourself as the policy owner.
5.  Enable the policy for knowledge publication \(if applicable in the environment\).
6.  Create a .docx file that includes a bulleted list with two levels.
7.  Upload the file using the **Import Policy Text** button.
8.  Verify that the document content is imported into the policy text section.
9.  Save and update the policy record.
10. Move the policy through the life cycle: **Draft** &gt; **Review** &gt; **Awaiting Approval** &gt; **Approved**.
11. Publish the policy by selecting **Publish**.
12. Confirm the policy transitions to the 'Published' state.
13. Verify whether a corresponding Knowledge Article is automatically generated in kb\_knowledge and linked to the policy record.

 Observe that the generated Knowledge Article may render second-level bullet points as filled black circles.

</td></tr><tr><td>

Knowledge Management

 PRB2082853

</td><td>

When Word documents are converted to policy text or knowledge articles, hyperlinks appear on a new line instead of remaining on the same line

</td><td>

The dom element of the hyperlink gets nested inside the paragraph for the hyperlink, which continues on the same line correctly. However, the JAVA code points to the closing of a paragraph tag before the hyperlink tag, so it becomes a sibling and not a child. This makes it go to a new line.

</td><td>

1.  Create a document with three links in the same line.
2.  Import the document as a knowledge article.

 Observe that some of the links appear on a new line.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-6.md)
-   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-5.md)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3.md)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-security-notables.md)
-   [All other Australia fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)

