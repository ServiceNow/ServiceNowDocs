---
title: Third-party Risk Management upgrade information
description: ServiceNow Third-party Risk Management application upgrade information for the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-03-03"
reading_time_minutes: 2
---

# Third-party Risk Management upgrade information

ServiceNow® Third-party Risk Management application upgrade information for the Xanadu release.

## Important information for upgrading Vendor Risk Management to Xanadu

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

## Plugin requirements

TPRM

-   Activate the Third-party Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Third-party Risk Due Diligence application \[com.sn\_tprm\_dd\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

VRM

-   Activate the Vendor Risk Management application \[com.sn\_vdr\_risk\_asmt\].
-   Activate the Vendor Risk Management Workspace application \[sn\_vrm\_ws\] if you want to use the Vendor Risk Management workspace.

For more information on licensing or metering, see [Tracking a managed activity](https://www.servicenow.com/docs/access?context=tprm-managed-activity&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US), [Third-party Risk Management \(TPRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1431058) and [Vendor Risk Management \(VRM\) Licensing](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1362674).

## VRM to TPRM changes

-   The name of the application changed from Vendor Risk Management to Third-party Risk Management as part of the Vancouver release.
-   The internal assessment \[sn\_vdr\_asmt\_internal\_assessment\] table is introduced, extending the tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] table.
-   The Due Diligence Review \(DDR\) workflow is introduced, which uses both the internal assessment and the external \(VRA\) assessment.

    **Note:** If you have customizations on the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables, they might need modifications to work with the DDR workflow.

-   The Third-party Scores \[sn\_vdr\_risk\_asmt\_security\_score\] table has been relabeled to Risk Intelligence Scores \[sn\_vdr\_risk\_asmt\_security\_score\] to reduce confusion.
-   All instances of “vendor” are changed to “third party” in the user interface, though some global instances might remain unchanged.

    **Note:** If you don’t want to use the due diligence workflow, your original workflow \(Tiering assessment and External assessments \(VRAs\) should be the same\).


## VRM and TPRM data model

The Vendor Risk Management data model primarily uses the term “vendor” and includes the Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\] and VRA \[sn\_vdr\_risk\_asmt\_assessment\] tables.

The Third-party Risk Management data model uses the term “third-party” in most user interface elements and introduces the DDR workflow, which uses both internal \[sn\_vdr\_asmt\_internal\_assessment\] and \[sn\_vdr\_risk\_asmt\_assessment\] external assessments.

The following models show VRM's and TPRM's capabilities.

![Relationship Vendor risk management main tables. For a text description, see the text that preceded and follows this data model.](../image/vrm-data-model.png "VRM data model")

The components included in the Vendor Risk Management data model are as follows:

-   Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Company \[core\_company\]
-   Vendor risk assessment \[sn\_vdr\_risk\_asmt\_assessment\]
-   Vendor engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Vendor contact \[vm\_dr\_contact\]
-   Assessment metric type \[asmt\_metric\_type\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_assessment\_template\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Engagement level risk rating \[sn\_vdr\_risk\_asmt\_engagement\_level\_rating\]

![Relationship between due diligence, and third-party management main tables. For a text description, see the text that preceded and follows this data model.](../image/tprm-data-model-upgrade.png "TPRM data model")

The components included in the Third-party Risk Management data model are as follows:

-   Risk intelligence score \[sn\_vdr\_risk\_asmt\_security \_score\]
-   Internal assessment \[sn\_vdr\_asmt\_internal\_assessment\]
-   Tiering assessment \[sn\_vdr\_risk\_asmt\_vdr\_tiering\_assessment\]
-   Event-driven management history \[sn\_tprm\_dd\_rule\_execution\_history\]
-   Third-party due diligence request \[sn\_tprm\_dd\_request\]
-   Company \[core\_company\]
-   Event-driven management rule \[sn\_tprm\_dd\_generation\_rule\]
-   Third-party risk assessment \[sn\_vdr\_risk\_asmt\_assessment\]
-   Third-party engagement \[sn\_vdr\_risk\_asmt\_vendor\_engagement\]
-   Vendor contact \[vm\_dr\_contact\]
-   Assessment metric type \[asmt\_metric\_type\]
-   Assessment template \[sn\_vdr\_risk\_asmt\_assessment\_template\]
-   Third-party risk issue \[sn\_vdr\_risk\_asmt\_issue\]
-   Engagement risk scoring rule \[sn\_vdr\_risk\_asmt\_engagement\_risk\_scoring\_rule\]
-   Engagement level risk rating \[sn\_vdr\_risk\_asmt\_engagement\_level\_rating\]

**Parent Topic:**[Third-party Risk Management release notes](grc-tprm-rn.md)

