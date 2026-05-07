---
title: Classify imported licenses in the Software Bill of Materials Workspace
description: Classify the component licenses you upload with your SBOM files with the License Classification feature.
locale: en-US
release: australia
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Classifying licenses and resolving component licenses in the Software Bill of Materials workspace, Use, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Classify imported licenses in the Software Bill of Materials Workspace

Classify the component licenses you upload with your SBOM files with the License Classification feature.

## Before you begin

Classifying new license information is an ongoing process. You might prefer to keep the total number displayed on the Unclassified card low. As a license manager, you might prefer to check for licenses that need classification every few days and after you upload SBOM files.

Role required: sn\_sbom\_response.managelicense

## Procedure

1.  Navigate to **Workspaces** &gt; **SBOM Workspace** &gt; **License administration** &gt; **License Classification**.

    **Note:** Unless you also have the sn\_sbom\_response.licenseresolver role, only the License classification tab is visible.

2.  Select a card to filter licenses by their classifications.

3.  To classify licenses, choose one.

<table id="choicetable_inv_wvz_ycc"><thead><tr><th align="left" id="d477653e100">

Option

</th><th align="left" id="d477653e103">

Description

</th></tr></thead><tbody><tr><td id="d477653e109">

**Bulk edit records or edit more than one record on the list.**

</td><td>

1.  Select multiple records.
2.  Double-click the Classification column header.
3.  Update the classification.


</td></tr><tr><td id="d477653e130">

**Edit and update the classification on the record.**

</td><td>

1.  Select a record from the list to open it.
2.  Add work notes and attachments, if required.
3.  Select **Save**.


</td></tr></tbody>
</table>4.  After you classify licenses, you are ready to [Resolve classified licenses to components](vr-sbom-assign-license.md).


