---
title: Create rules
description: The use of rules to normalize a field is intended for large lists of variant field values.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Normal values, Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create rules

The use of rules to normalize a field is intended for large lists of variant field values.

## About this task

Always test your rules before applying them to all the existing records in the database. Prior to creating the rule, make sure to generate the list of [Pending Values](../concept/c_FieldNormalization.md) and create a [normal value](../concept/c_FieldNormalization.md) for the field. A normalized field can have a combination of aliases and rules.

## Procedure

1.  In a Normalization record, open the **Normal Values** related list.

2.  Open a Normal Value record.

3.  Open the **Rules** related list in the Normal Value form, and then click **New**.

    The Field Normalization Rule form provides the following fields:

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for this rule. For example, this name might be Xeon CPU Type.|
    |Order|Order in which this rule should be evaluated. The platform parses the rules in the order configured until it finds one that evaluates to true.|
    |Active|Enables or disables this rule. By default, new rules are active \(true\)|
    |Make alias|If this check box is selected, and the rule evaluates to true, the rule makes an alias automatically from a pending value. If this check box is not selected, and the rule evaluates to true, the platform automatically changes the value for the named field in the record to the normal value, but does not create an alias.|
    |Case sensitive|All pending values for the named field must match the case of the same value in a rule to be normalized.|
    |Rule|Use the ServiceNow rule builder to construct the rules for normalizing fields. Rules automate the transformation of large numbers of pending field values into aliases.|

4.  Create a set of rules to incorporate all the possible variants of the pending values.

    For this example, the rules might be:

    -   **Intel Xeon**: CPU type matches pattern \*Intel\*Xeon\*. This rule normalizes all variants in which **Intel** precedes **Xeon**, including **Intel Xeon**, **Intel\(R\) Xeon\(TM\) CPU 2.80GHz**, and **Intel\(R\) Xeon\(TM\) CPU 3.00GHz**.
    -   **Xeon**: CPU type contains Xeon
    -   **L3350**: CPU type contains L3350
    -   **E3350**: CPU type contains E3350
    For every rule that is created, the platform generates a **Rule applier** data job. In the testing mode, the **Start** controls are not available, and the job cannot be run until the mode is changed to **Active**.

5.  Test all the rules before making the normalization record **Active**.

    Testing Rules

    **Note:** Users must have the normalization\_tester role to create test records.

    Field normalization records are created in the **Test** mode by default, enabling administrators to test normalization rules thoroughly before applying them to the existing records in the database. In the testing mode, the **Start** controls are not available for the **Rule applier** data job. The job can be run only when testing is complete and the **Mode** has been changed to **Active**. In the testing mode, only records that have been created or updated by a user with the normalization\_tester role are normalized. The normalizer and normalization\_tester roles can be combined for a single user or granted separately.


