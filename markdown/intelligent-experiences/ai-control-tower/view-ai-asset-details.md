---
title: View AI asset record details
description: View the AI asset governance details to track the lifecycle status, phase, and the install status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/view-ai-asset-details.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [generative AI]
breadcrumb: [AI asset inventory, AI assets, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# View AI asset record details

View the AI asset governance details to track the lifecycle status, phase, and the install status.

## Before you begin

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the AI assets view.

3.  From the navigation menu of the AI assets view, under AI asset inventory, select an AI asset.

    The AI asset details page is displayed.

4.  On the page, review the AI asset details.

<table id="choicetable_pq3_wwl_ngc"><thead><tr><th align="left" id="d120906e90">

Field

</th><th align="left" id="d120906e93">

Description

</th></tr></thead><tbody><tr><td id="d120906e99">

**Asset tag**

</td><td>

The asset tag contains the unique ID assigned to every asset. Each asset tag consists of a type prefix followed by a 20-digit number.

</td></tr><tr><td id="d120906e108">

**Name**

</td><td>

The name of the AI asset. Identifies the asset in lists, searches, and records.

</td></tr><tr><td id="d120906e117">

**Description**

</td><td>

A brief summary of what the AI asset does. Explains the asset's purpose without opening the full record.

</td></tr><tr><td id="d120906e126">

**Managed status**

</td><td>

Indicates whether the asset is actively governed. Values typically include Managed and Unmanaged.

</td></tr><tr><td id="d120906e139">

**Version**

</td><td>

The Version number of the asset.

</td></tr><tr><td id="d120906e148">

**Asset type**

</td><td>

Categorizes the AI asset by its type.-   generative AI
-   agentic AI
-   Classical AI
-   AI model
-   AI system
-   AI prompts
-   AI datasets
-   MCP servers


</td></tr><tr><td id="d120906e184">

**Provider**

</td><td>

The vendor or team that built or supplies the AI asset.

</td></tr><tr><td id="d120906e193">

**Vendor**

</td><td>

Who has sold the Asset

</td></tr><tr><td id="d120906e202">

**Department**

</td><td>

Department where the asset is allocated

</td></tr><tr><td id="d120906e211">

**Managed by**

</td><td>

Managed by the user who owns the asset

</td></tr><tr><td id="d120906e221">

**License details**

</td><td>

License details of the asset

</td></tr><tr><td id="d120906e230">

**Supported locations**

</td><td>

The geographic regions or environments where the asset is approved to operate, relevant for data residency and compliance purposes.

</td></tr><tr><td id="d120906e239">

**Source system**

</td><td>

The system from which the asset record originated, such as an import script or an external discovery tool.

</td></tr><tr><td id="d120906e248">

**State**

</td><td>

The operational state of the asset.-   Deployed
-   Retired
-   Development
-   Unknown
-   N/A


</td></tr><tr><td id="d120906e274">

**Lifecycle phase**

</td><td>

The current phase of the asset-   New
-   Assess
-   Build and test
-   Deploy
-   Offboarding


</td></tr><tr><td id="d120906e300">

**Lifecycle status**

</td><td>

The current status within the lifecycle phase of the asset.-   In Review
-   Approved
-   Rejected
-   Deployed
-   AI steward review
-   Approved for development
-   Ready for deployment
-   Approved for deployment
-   Canceled


</td></tr><tr><td id="d120906e340">

**Risk classification**

</td><td>

Risk classification of the asset

</td></tr><tr><td id="d120906e349">

**Created**

</td><td>

Creation date

</td></tr><tr><td id="d120906e358">

**Updated**

</td><td>

Updated date

</td></tr><tr><td id="d120906e367">

**Documentation**

</td><td>

A free-text or rich-text field for attaching additional reference material, links, or notes about the asset.

</td></tr><tr><td id="d120906e376">

**Aggregated risk score**

</td><td>

Inherent rating — The risk level of the asset before any controls are applied. Reflects the raw risk based on the asset's nature and use.

 Control effectiveness — A measure of how well the existing controls mitigate the identified risks.

 Residual rating — The remaining risk level after controls are applied. A lower residual rating indicates effective risk mitigation.

</td></tr></tbody>
</table>
