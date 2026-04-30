---
title: Execute a skipped record rule
description: Run skipped record rules based on your set conditions to resolve skipped records in an upgrade. The rules either execute automatically during an upgrade or can run on demand after an upgrade.Execute the skipped record rules on demand on the skipped records whenever it's required.Execute the skipped record rules automatically during the upgrade on the skipped records.
locale: en-US
release: zurich
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Upgrade Skipped Record Rules Editor tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer]
---

# Execute a skipped record rule

Run skipped record rules based on your set conditions to resolve skipped records in an upgrade. The rules either execute automatically during an upgrade or can run on demand after an upgrade.

**Parent Topic:**[Upgrade Skipped Record Rules Editor tool in Upgrade Console](../concept/um-skipped-rules-tool.md)

**Related topics**  


[Create a skipped record rule](um-create-skipped-record-rule.md)

## Execute a skipped record rule on demand

Execute the skipped record rules on demand on the skipped records whenever it's required.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Administration** &gt; **Skipped Record Rules Editor**.

    A list of available rules shows up.

    **Note:** By default, a few inactive sample rules have been provided. You can set it to active if you want to use the sample rules.

2.  Execute the rules on demand using either of the following ways.

<table id="choicetable_rvp_hgn_sdb"><thead><tr><th align="left" id="d317349e135">

Option

</th><th align="left" id="d317349e138">

Steps

</th></tr></thead><tbody><tr><td id="d317349e144">

**Using Run Now**

</td><td>

1.  Select the rule that you want to execute from the list.
2.  Select **Run Now** from the configuration list action items.

**Note:** When you select **Run Now**, a progress bar shows up to display the progress of the rule execution.

</td></tr><tr><td id="d317349e170">

**Using View Latest Upgrade History tab**

</td><td>

1.  Select the **View Latest Upgrade History** tab. The System Upgrades form shows up.

**Note:** The skipped record rules are executed only on the latest upgrade.

2.  Select **Run skipped Record Rules** on the form.

**Note:** All the active rules get executed. You can't choose the specific active rules to run while using this process.

</td></tr></tbody>
</table>
## Execute a skipped record rule automatically

Execute the skipped record rules automatically during the upgrade on the skipped records.

These rules are executed on the skipped records automatically during the upgrade process. The prediction of the rules execution on the skipped records can be previewed on the Skipped list prediction card in the Upgrade Preview module.

Once the execution of the rules are done, the summary can be reviewed in the Upgrade Summary of Upgrade Monitor.

**Note:** Skipped record rules and upgrade plans can't be implemented together in an upgrade.

