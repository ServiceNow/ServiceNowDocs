---
title: Generate a certificate
description: Generate a certificate to use with the Discovery Console for OT or upload your own certificates. This certificate allows the Console to boot up.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Discovery Console for OT, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Generate a certificate

Generate a certificate to use with the Discovery Console for OT or upload your own certificates. This certificate allows the Console to boot up.

## Before you begin

**Note:** If you choose to do so, you can create your own certificate if it is required by your company's policies.

Role required: admin

## About this task

After the Discovery Console for OT is installed, there are default, preloaded certificates that allow the Console to power up. However, following this initial boot, it is recommended that you use the Console to generate a new CA. This task describes how to generate a new Console certificate for the Discovery Console for OT.

![Generate certificate](../images/settings-certificate.png)

## Procedure

1.  Navigate to the Discovery Console for OT **Settings &gt; Certificate** tab.

2.  Generate a new bundle or upload an existing bundle.

    **Note:** You are not obligated to use the ServiceNow provided certificates and you may choose to use your own.

<table id="choicetable_pp4_qnb_ghc"><thead><tr><th align="left" id="d29335e110">

Option

</th><th align="left" id="d29335e113">

Description

</th></tr></thead><tbody><tr><td id="d29335e119">

**Generate a new bundle**

</td><td>

1.  Under **Update Certificate**, select **Generate New Bundle**.
2.  Select the **Generate Bundle** button.


</td></tr><tr><td id="d29335e146">

**Upload an existing bundle**

</td><td>

1.  Under **Update Certificate**, select **Upload Bundle \(.p12\)**.
2.  Use the **Choose File** button and select the bundle to upload.
3.  If needed, enter a **Bundle Password**.
4.  Select the **Upload Bundle** button.


</td></tr></tbody>
</table>    **Note:** Generating or uploading a certificate also updates any current certificates.


## Result

A certificate is generated. The Discovery Console for OT reboots.

