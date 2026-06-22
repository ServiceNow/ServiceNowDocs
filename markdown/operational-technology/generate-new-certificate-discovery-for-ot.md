---
title: Generate a certificate
description: Generate a certificate to use with the Discovery Console for OT or upload your own certificates. This certificate allows the Console to boot up.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/generate-new-certificate-discovery-for-ot.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Discovery Console for OT, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Generate a certificate

Generate a certificate to use with the Discovery Console for OT or upload your own certificates. This certificate allows the Console to boot up.

## Before you begin

**Note:** If you choose to do so, you can create your own certificate if it is required by your company's policies.

Role required: admin

## About this task

After the Discovery Console for OT is installed, there are default, preloaded certificates that power up the Console. However, following this initial boot, it's recommended that you use the Console to generate a new Certificate Authority \(CA\). This task describes your options for generating the Console CA.

\[Omitted image "settings-certificate-download.png"\] Alt text: Console certificate

**Note:** You can also select the link **Download Console Certificate Bundle \(.zip\)**. See the table for more information on this option.

## Procedure

1.  Navigate to the Discovery Console for OT **Settings &gt; Certificate** tab.

2.  Generate a new bundle, upload an existing bundle.

    **Note:** You're not obligated to use the ServiceNow provided certificates and you may choose to use your own.

<table id="choicetable_pp4_qnb_ghc"><thead><tr><th align="left" id="d29514e113">

Option

</th><th align="left" id="d29514e116">

Description

</th></tr></thead><tbody><tr><td id="d29514e122">

**Generate a new bundle**

</td><td>

1.  Under **Update Certificate**, select **Generate New Bundle**.
2.  Select the **Generate Bundle** button.


</td></tr><tr><td id="d29514e149">

**Upload an existing bundle**

</td><td>

1.  Under **Update Certificate**, select **Upload Bundle \(.p12\)**.
2.  Use the **Choose File** button and select the bundle to upload.
3.  Enter a **Bundle Password**.
4.  Select the **Upload Bundle** button.


</td></tr><tr><td id="d29514e188">

**Download Console Certificate Bundle \(.zip\)**

</td><td>

The bundle contains the Console's Certificate and the web browser certificate. These certificates establish trust between these applications and confirm their communications are secure and encrypted.

</td></tr></tbody>
</table>    **Note:** Generating or uploading a certificate also updates any current certificates.


## Result

A certificate is generated. The Discovery Console for OT reboots.

