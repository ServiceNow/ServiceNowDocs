---
title: Success Probability definitions
description: Success Probability definition is a configuration that defines the probability and the matching conditions of a change request.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference section for Change Management, Change Management, IT Service Management]
---

# Success Probability definitions

Success Probability definition is a configuration that defines the probability and the matching conditions of a change request.

By default, the success probability definition is defined for Change Success Score, Change Model Success, and Calculated.

The order field determines the execution order of the definitions, the order with least value is given higher precedence.

The default values are created for Change Model Success, Change Success Score, and Calculated irrespective of the probability selected on the success probability definition.

Change manager can modify the existing records in the table. The Success Score Validations business rule validates if any record is created with the allowed minimum and maximum values for Change Model Success and Change Success Score.

When Change Model Success or Change Success Score is set as probability on the Success probability definition, the corresponding related list is visible on the Success probability definition record, however, when Calculated is set all the three related lists are visible on the record.

The “Greater than or equal to” field of Change Model Success and Change Success Score related list determines the Success Probability that must be returned by the Success probability definition.

For example, if the Probability is set to Calculated on the record, and if Change Model Success evaluates to High and Change Success Score evaluates to Moderate, the success Probability definition returns High as the Success Probability.

![Success probability matrix](../image/success-probability-matrix.png)

You can edit the value in the Calculated success probability column for each combination of Change model success and Change success score. When you modify the choices for success probability on a change request, you must click **Refresh probability mappings** under **Related Links** to update the combinations of related records for Change Model Success, Change Success Score, and Calculated probabilities. You can also update the multiple records by executing **Refresh probability mappings** on the list.

**Note:**

Success probability plugin supports domain separation. The **sn\_chg\_probability\_success**, **sn\_chg\_probability\_model\_success**, and **sn\_chg\_probability\_calculated\_lookup** tables are process separated when you install the domain separation plugin.

**Parent Topic:**[Reference section for Change Management](reference-change-management.md)

