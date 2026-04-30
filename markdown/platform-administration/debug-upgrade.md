---
title: Debug upgrade
description: Diagnose and resolve issues you suspect may have resulted from the most recent upgrade by enabling upgrade debugging during a user session. Each transaction lists whether an artifact was skipped, customized by the customer, or modified by ServiceNow during the last family-to-family or patch version upgrade.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Debug upgrade

Diagnose and resolve issues you suspect may have resulted from the most recent upgrade by enabling upgrade debugging during a user session. Each transaction lists whether an artifact was skipped, customized by the customer, or modified by ServiceNow during the last family-to-family or patch version upgrade.

Administrators and technical personnel can use this output as an adjunct to the Upgrade History and Upgrade Monitor modules. Debug Upgrade is a component of standard ServiceNow session debugging. You enable Debug Upgrade, process a transaction \(for example, load a form\), then analyze the reported upgrade information. See .

## Reported debug information

Debug Upgrade includes several expandable sections:

-   Skipped During Last Upgrade
-   Customer Customized
-   ServiceNow Modified During Last Upgrade

These sections serve as a starting point for diagnosing when a function or artifact does not operate as expected after an upgrade. Each listing sorts by the dates the artifacts were processed, with the most recent appearing first. Expand the appropriate section, and click the name of a listed artifact to view the underlying artifact record. These records include update version history, which represents the state of a customizable object at specific times. See [Version records](https://www.servicenow.com/docs/access?context=r_VersionRecords&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

The listed artifacts may require some kind of possible user intervention or action. Using underlying artifact detail, you can determine:

-   what artifacts have changed?
-   what artifacts have not been changed that would or should have?
-   what changed artifacts were missed?
-   what artifacts operate differently than expected \(if referencing something that has changed during last upgrade\)?

Depending on the answers to these questions, you may have to modify the selected artifact so it works in the way you expect. Conversely, you might simply accept the new updates made to the artifact, and its changed functionality.

## Skipped during last upgrade

Lists artifact records that were skipped during the last upgrade that also ran during the last transaction. These records are standard objects that missed changes from ServiceNow because they were modified at some point by a user. See [Resolve conflicts for an individual record](../task/upgrademon-resolve_conflicts.md).

## Customer customized

Lists all artifact records that were customized at some point by users that also ran during the last transaction. This listing is not strictly related to the actual activities performed during the last upgrade session. The listing does include the records that appear under Skipped During Last Upgrade. However, not all records that appear in the Customer Customized list are included in Skipped During Last Upgrade.

**Note:** Customizations that you designate for replacement during upgrades, by setting the **Replace on Upgrade** field in the customization record to true, do not appear on the Customer Customized section list.

While this listing is not directly related to the activities performed during the last upgrade, it may be worthwhile to look at individual customization records listed on it. Some of the listed customization records may be referencing other records changed or skipped during upgrade. The activities performed during the last upgrade may have an impact on, or affect these relationships.

## ServiceNow modified during last upgrade

Lists all standard \(non-customized\) artifact records modified by ServiceNow during the last upgrade that also ran during the last transaction.

-   **[Enable and use debug upgrade](../task/enable-debug-upgrade.md)**  
Enable Debug Upgrade to analyze post-upgrade issues that may require follow up, then disable it when finished with the upgrade debugging session.

**Parent Topic:**[Upgrades and conversions](../../../customer-support/concept/upgrades-conversions.md)

**Related topics**  


[Upgrade History module: Track every upgrade](../../../customer-support/concept/c_UpgradeHistory.md)

[Upgrade Monitor module: Upgrade an individual instance](upgrademon-landing-page.md)

