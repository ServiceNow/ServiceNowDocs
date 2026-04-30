---
title: Update the project summary header and footer of your email using script include
description: Use the script include to modifying the email template for project summary.
locale: en-US
release: zurich
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Script include, project summary header and footer]
breadcrumb: [Configure, Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Update the project summary header and footer of your email using script include

Use the script include to modifying the email template for project summary.

## Before you begin

Ensure the Now Assist for SPM is installed and email project summary skill is active.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Script Includes**.

2.  Open the **ProjectInsightsEmailTemplateCustomConstants** script include and update the **ProjectInsightsEmailTemplateCustomConstants.EMAIL\_HEADER\_HTML** constant for email's header.

    This example demonstrates the script include for email's header as follows:

    ```
     ProjectInsightsEmailTemplateCustomConstants.EMAIL_HEADER_HTML = `<p><span style="color: white;"><a href="https://www.servicenow.com/" target="_blank" rel="noopener noreferrer nofollow"><span style="color: white; text-decoration: none;"><span style="color: blue;"><img style="height: 30px; width: 150px; border: none;" src="sn_spm_gen_ai.sn-logo-project-insights.png" alt="servicenow logo" height="30px" border="0" /></span></span></a></span></p>`;
    ```

3.  Update the **ProjectInsightsEmailTemplateCustomConstants.EMAIL\_FOOTER\_HTML** constant for email's footer.

    This example demonstrates the script include for email's footer as follows:

    ```
    ProjectInsightsEmailTemplateCustomConstants.EMAIL_FOOTER_HTML = `<p style="border-top: 1px solid #293e40; line-height: 0;"><span style="color: #999999;">&nbsp;</span></p><div style="caret-color: #212121; color: #212121; font-family: Aptos; font-size: 16px; width: 100%; margin: 0 auto; padding: 0; background-color: #ffffff;">      <!-- Logo Section -->      <div style="line-height: 0.8;">        <span>          <a href="https://www.servicenow.com/" target="_blank" rel="noopener noreferrer nofollow" style="text-decoration: none;">            <img src="sn_spm_gen_ai.sn-logo-project-insights.png" alt="servicenow logo" style="height: 20px; width: auto; border: none;" />          </a>        </span>      </div>      <!-- Address and Footer Information -->      <div style="font-family: 'Century Gothic', CenturyGothic, Helvetica, sans-serif; font-size: 12px; line-height: 0.8; color: #293e40; margin-top: 5px;">        <p style="margin-bottom: 0; padding: 0; line-height: 0.8; font-size: 10px;">          <span>2225 Lawson Lane, Santa Clara, CA 95054, United States</span>        </p>        <p style="margin-bottom: 0; padding: 0; line-height: 0.8; font-size: 10px; color: #293e40;">          <span>&copy; 2024 ServiceNow. All rights reserved</span>        </p>      </div>    </div>`;
    ```

    On completion, the project summary email template is customized with the header and footer.


