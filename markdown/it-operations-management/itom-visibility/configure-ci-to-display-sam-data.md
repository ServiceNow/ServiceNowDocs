---
title: Configure a CI to display Software Asset Management data
description: Configure computer configuration item \(CI\) forms to display data from the Software Installations \[cmdb\_sam\_sw\_install\] table.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-02-24"
reading_time_minutes: 1
breadcrumb: [Discovery with Software Asset Management, Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Configure a CI to display Software Asset Management data

Configure computer configuration item \(CI\) forms to display data from the Software Installations \[cmdb\_sam\_sw\_install\] table.

## Before you begin

Confirm you have installed and activated the Software Asset Management \(com.sn\_samp\_master\) plugin.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Servers** &gt; **All**.

    Alternatively, enter `cmdb_ci_computer.list` in the filter navigator to open the Computer \[cmdb\_ci\_computer\] table list view.

2.  Select a **Name** from the list to open any computer CI record.

3.  Right-click in the header of the record and select **Configure** &gt; **Related Lists** from the context menu.

    The Configuring related lists on Computer form page displays.

4.  Scroll through the Available list and select **Software Installation-&gt;Installed on**.

5.  Select the add icon.

    Software Installation-&gt;Installed on now displays in the Selected list.

6.  Select **Save**.

7.  Select the back icon to return to the computer record.

    The Software Installations tab now displays in the record's related list.


**Parent Topic:**[Discovery with Software Asset Management](../concept/c_DiscoSWAssetMgmtTableSchema.md)

