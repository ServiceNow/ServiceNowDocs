---
title: Enable synthesized response in Virtual Agent API
description: You can now enable synthesized response in the conversations with the primary bot.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Enable synthesized response in Virtual Agent API

You can now enable synthesized response in the conversations with the primary bot.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_provider.list` in the filter.

2.  Select the VA Bot to Bot Provider record.

3.  In the **Provider Properties** related tab, do the following:

    1.  Select and open the **synthesized\_text\_citation\_strategy** system property to configure the output text.

<table id="table_anh_zv4_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the custom adapter property: **synthesized\_text\_citation\_strategy**.

</td></tr><tr><td>

Value

</td><td>

Property value that controls how Virtual Agent API sends the synthesized text response with citation labels and links.

 If you want to configure the way citations are displayed in the response, then choose any of the following options:

-   endnotes \(default\): With this selection, the citation label and links are displayed at the end of synthesized text response.
-   inline-link: With this selection, the citation links are attached to the citation reference \(\[1\], \[2\]..\).
-   inline-link-with-endnotes: With this selection, the synthesized response is displayed with both endnotes and inline-link.
-   none: With this selection, the citation label and links aren't displayed in the synthesized text response. The third-party chat systems can use their own logic using **citations** to render the output text from the synthesized response.


</td></tr></tbody>
</table>    2.  Select and open the **synthesized\_carousel\_strategy** system property to configure the picker.

<table id="table_cnh_zv4_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the custom adapter property: **synthesized\_carousel\_strategy**.

</td></tr><tr><td>

Value

</td><td>

Property value that controls how Virtual Agent API sends the synthesized text response with carousel.

 -   replace-label \(default\): With this selection, Virtual Agent API sends the synthesized text response in labels.
-   separate-control: With this selection, Virtual Agent API sends the synthesized text response in a separate output text control and the carousel with the options.


</td></tr></tbody>
</table>    3.  Click **Update**.

**Parent Topic:**[Using Virtual Agent API](../concept/use-virtual-agent-api.md)

