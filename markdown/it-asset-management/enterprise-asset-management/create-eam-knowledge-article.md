---
title: Create a knowledge article for Enterprise Asset Management
description: Create and edit knowledge articles within a knowledge base to share information across your organization.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Knowledge articles, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a knowledge article for Enterprise Asset Management

Create and edit knowledge articles within a knowledge base to share information across your organization.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Asset knowledge base**.

2.  Select **New** in the Asset knowledge base page.

3.  On the form, fill in the fields.

    For detailed information on the fields, refer to the [Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) application

<table id="choicetable_y22_jbc_mzb"><thead><tr><th align="left" id="d102945e86">

Field

</th><th align="left" id="d102945e89">

Description

</th></tr></thead><tbody><tr><td id="d102945e95">

**Number**

</td><td>

Number of the article. This field is automatically populated.

</td></tr><tr><td id="d102945e104">

**Knowledge base**

</td><td>

The knowledge base selected for the article. Enterprise Asset Knowledge Base is selected by default. You can select a different knowledge base if you want to.**Note:** An article can only be associated with one knowledge base. You can change the knowledge base, but only if the selected article template is available in the knowledge base.

</td></tr><tr><td id="d102945e115">

**Category**

</td><td>

The category for this article. Select a Knowledge base before you can select a category. Articles without a category appear on the knowledge homepage in the \(empty\) category.

</td></tr><tr><td id="d102945e124">

**Valid to**

</td><td>

The date this knowledge article expires. Articles don’t appear in search results after the Valid to date or if the Valid to date is empty.

 The default value of the this field is derived from the **Article Validity** field configured for the knowledge base. The Valid to date starts from the date that the article was created until the number of days specified in the **Article Validity** field. If the **Article Validity** field is empty, the default date in the **Valid to** field for the knowledge article is set to January 1, 2100.

 An article author or editor can select whether to keep or change the default Valid to date.

 On the first day of each month, the application sends an email notification to a list of authorized recipients to remind them about articles that are expire in the next month. The recipient can then extend the Valid to date to continue using the article.

**Note:** If the system date format or user preferences is set to use `yy` year format, you might face issues when the Valid to date is set to the default date. Contact your administrator or modify the user preferences to use a date format with the `yyyy` year format.

</td></tr><tr><td id="d102945e166">

**Article type**

</td><td>

The type of article, either HTML or wiki.

</td></tr><tr><td id="d102945e175">

**Workflow**

</td><td>

The publication state of the article, such as Draft, In Review, or Published. When inserting a new article from an existing article, the state of the new article is reset to Draft.

</td></tr><tr><td id="d102945e184">

**Source task**

</td><td>

The task this knowledge article was created in response to, if any. This field is set automatically when you create the knowledge article from a task record.

</td></tr><tr><td id="d102945e193">

**Attachment link**

</td><td>

Option for downloading an attached file automatically when a user accesses the article, instead of opening the article view. Add one or more attachments to the article to use this option.**Note:** You may attach multiple files, but most web browsers permit users to download only the first one. To ensure download of all the files, bundle them into an archive, such as with WinZip, and attach the archive. The Attachment link option applies to articles accessed from search links only. Articles accessed as links within other knowledge articles won’t replicate this behavior.

</td></tr><tr><td id="d102945e204">

**Display attachments**

</td><td>

Option for displaying attachments to users viewing this knowledge article. Attachments appear below the article text. Add one or more attachments to the article to use this option.

</td></tr><tr><td id="d102945e213">

**Short Description**

</td><td>

The title of the article. This title appears when browsing and searching for a knowledge article, and at the top of the article. You can enter up to 100 characters in this field.

</td></tr><tr><td id="d102945e223">

**Article body**

</td><td>

Content for the article. A preview of the content appears when browsing and searching for a knowledge article.

 Use the editing functions in the HTML editor to create content.

</td></tr></tbody>
</table>4.  Select **Save** to create the article.


