---
title: Using real-time prevention monitoring
description: When working with application or configuration file types, if the real-time scanning functionality is configured and active, the Scan Engine displays information for the findings.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Real-time prevention monitoring for Scan Engine, Scan Engine, Platform Health, Using Impact, Impact]
---

# Using real-time prevention monitoring

When working with application or configuration file types, if the real-time scanning functionality is configured and active, the Scan Engine displays information for the findings.

Finding levels of Review and Suggest are shown in blue, while Recommend and Act are shown in red. These information windows can contain the following fields, depending on their severity.

<table id="table_ydc_zvk_hhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Finding level

</td><td>

The severity level of the finding, as well as a brief description of the finding.

</td></tr><tr><td>

Details

</td><td>

Generally, the line number the finding occurred on.

</td></tr><tr><td>

Steps to resolve issue

</td><td>

Some suggested steps the developer can follow to resolve the finding.

</td></tr><tr><td>

Exception reason required

</td><td>

If the finding is at the Recommend level, this field reminds developers they can submit an exception for the issue if they believe it is not a finding.

</td></tr><tr><td>

Supporting documentation

</td><td>

-   If the definition this finding applies to contains a **Supporting Documentation** link, it appears here as a hyperlink that opens in a new browser tab.
-   This information can be linked to documentation, knowledge base articles, FAQs, and more.

</td></tr><tr><td>

Impact

</td><td>

-   Lists the finding’s impact level and **Impact to Instance** for the associated definition.
-   The impact to instance is a number between 1 and 10, where 10 is the most impactful.

</td></tr></tbody>
</table>Using the information provided, you can do one of the following:

-   Correct the issue. If the issue is corrected, the Scan Engine will not return a new finding notice.
-   In the case of a Recommend level finding, submit an exception, then **Update** the page. See [Submit exceptions for the Scan Engine findings](submitting-exception-reasons-scan-engine.md).

Real-time messaging enforcement can be disabled with the Scan Engine properties page. By disabling enforcement, users will see the messaging but will not be required to make corrections for Act and Recommend findings.

In addition, visibility of real-time messaging for certain users can also be configured with the Scan Engine properties page. You can limit the users that will receive real-time messaging to a specific group if necessary.

For more information, refer to [Configure Scan Engine properties](../task/configure-scan-engine-properties.md).

