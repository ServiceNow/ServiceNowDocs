---
title: Configure the properties for Hardware Vulnerability Assessment
description: Configure the properties required to perform hardware vulnerability assessment.
locale: en-US
release: yokohama
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup, Configure, Industrial Workspace, Operational Technology]
---

# Configure the properties for Hardware Vulnerability Assessment

Configure the properties required to perform hardware vulnerability assessment.

## Before you begin

Role required: sn\_vul.manage\_exposure\_assessment and admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Guided Setup** &gt; **Operational Technology Vulnerability Response** &gt; **Hardware Vulnerability Assessment** &gt; **Configure Vulnerability Assessment Properties** &gt; **Configure** &gt; **Vulnerability Assessment**.

    Alternatively, you can navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Properties** &gt; **Vulnerability Assessment**.

2.  Perform the following configurations.

<table id="choicetable_gnl_snc_xfc"><thead><tr><th align="left" id="d74532e111">

Property

</th><th align="left" id="d74532e114">

Description

</th></tr></thead><tbody><tr><td id="d74532e120">

**`sn_vul_analyst.auto_create_vits`: This property determines if new vulnerable item records are created automatically for fully matched hardware vulnerability assessments. When set to true, new vulnerable item records are created automatically for fully matched hardware vulnerability assessments.

**

</td><td>

Select **Yes**.

 The default value is **Yes**. When set to **Yes**, new vulnerable item records are created automatically for fully matched hardware vulnerability assessments.

 Clear this check box if you want to create vulnerable items \(VITs\) manually.

</td></tr><tr><td id="d74532e152">

**`sn_vul_analyst.assess_unmapped_disc_models`: Enabling this property includes discovery models without CPE mappings in the assessment.

**

</td><td>

The default value is **No**.

 Select **Yes** to perform vulnerability assessments for discovery models of OT devices that aren’t CPE-mapped.

</td></tr><tr><td id="d74532e178">

**`hva_confidence_score_threshold`: This property controls the minimum confidence score threshold required for creation of vulnerability assessments. Only matches with scores equal to or above this threshold will generate vulnerability assessments. The threshold value must be a decimal number between 0.0 and 1.0. The default value is 0.75.

**

</td><td>

Edit the value according to your requirement.

 The default value is 0.75.

**Note:** You can set the value for Confidence Score to 0. But an assessment won't be created with a 0 Confidence Score.

</td></tr></tbody>
</table>3.  Select **Save**.


**Parent Topic:**[Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup](configure-hva-using-guided-setup.md)

