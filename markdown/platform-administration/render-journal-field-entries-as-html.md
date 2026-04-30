---
title: Render journal field entries as HTML
description: Journal fields can render text enclosed within code tags as HTML.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Journal field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Render journal field entries as HTML

Journal fields can render text enclosed within code tags as HTML.

## Before you begin

-   Role required: any role that grants write access to a journal field
-   System property: the glide.ui.security.allow\_codetag is set to the default value of **true**

    **Note:**

    To learn more about this property, see Allow JavaScript tags in embedded HTML \(instance security hardening\) in Instance Security Hardening Settings.


## About this task

By default, a High Security Setting escapes any HTML code you type in a journal field by replacing it with its equivalent HTML entity value. Escaping causes the system to display HTML code as text rather than forwarding it to the browser as rendering instructions.

## Procedure

1.  Enter `[code][/code]` tags around any code you want to render as HTML.

    **Note:** A single journal entry can contain multiple code tags as long as each code tag has a beginning and ending tag.

    For example, enter these lines:

<table id="table_ank_bj1_qy"><thead><tr><th>

Code entered

</th><th>

Result

</th></tr></thead><tbody><tr><td>

`[code]<a href="http://www.service-now.com">ServiceNow</a>[/code]`

</td><td>

The system renders a hyperlink to the ServiceNow web site.

</td></tr><tr><td>

`[code]<b>This text will be bold. </b>[/code]`

</td><td>

The system renders the sentence in bold.

</td></tr><tr><td>

`<b>This text will not be bold.</b>`

</td><td>

The system escapes the bold tags and renders them as text.

</td></tr><tr><td>

`[code]<script> gs.info(gs.getUserDisplayName());</script>[/code]`

</td><td>

The system escapes the content of the script tag.**Note:** By default, the HTML Sanitizer prevents the entry of &lt;script&gt; elements.

</td></tr></tbody>
</table>    For more examples of HTML formatting options, see the blog post [Formatting within Journal fields using HTML &amp; \[code\]](https://community.servicenow.com/community?id=community_blog&sys_id=4d9ceae1dbd0dbc01dcaf3231f9619e1) by a ServiceNow Technical Support Engineer in the ServiceNow Community.

2.  Click **Post**.

    **Note:** You cannot edit previous journal entries.


## Result

The system renders the text within code tags as HTML.

**Related topics**  


[General security settings properties](https://www.servicenow.com/docs/access?context=r_GeneralSecuritySettings&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

[HTML sanitizer](https://www.servicenow.com/docs/access?context=c_HTMLSanitizer&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

