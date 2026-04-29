---
title: NLU Workbench properties
description: Refer to these system properties for the Natural Language Understanding \(NLU\) application.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Natural Language Understanding, Natural Language Understanding, Enable AI experiences]
---

# NLU Workbench properties

Refer to these system properties for the Natural Language Understanding \(NLU\) application.

## NLU Workbench properties and their usage

To access your system properties, use the admin or nlu\_admin role and the following path in the application navigator: **All** &gt; **NLU Workbench** &gt; **Settings**.

<table id="table_qdh_gfv_15b"><thead><tr><th>

Label and Name

</th><th>

Default value

</th><th>

Plugin

</th><th>

Recommended usage

</th></tr></thead><tbody><tr><td>

Maximum number of utterances per intent**glide.nlu.utterances\_per\_intent.value\_limit**

</td><td>

200

</td><td>

NLU Workbench

</td><td>

Use fewer than 200 utterances per intent to keep your model well balanced in terms of intent size.**Note:** Value must be greater than 5 and less than or equal to 300.

</td></tr><tr><td>

Maximum number of records in a Table vocabulary source**glide.platform\_ml.api.max\_nlu\_lookupsource\_records**

</td><td>

100,000

</td><td>

NLU Workbench

</td><td>

Keep the value under 100,000.

</td></tr><tr><td>

Maximum number of values in a List vocabulary source**glide.nlu.static\_lookup.value\_limit**

</td><td>

1,000

</td><td>

NLU Workbench

</td><td>

Keep the value under 1,000.

</td></tr><tr><td>

Enable pre-built vocabulary for software names**glide.mlpredictor.option.nlu.@LookupSources:software**

</td><td>

enabled

</td><td>

NLU Workbench

</td><td>

Enable pre-built vocabulary so the system can recognize software names.

</td></tr><tr><td>

Enable pre-built vocabulary for hardware names**glide.mlpredictor.option.nlu.@LookupSources:hardware**

</td><td>

enabled

</td><td>

NLU Workbench

</td><td>

Enable pre-built vocabulary so the system can recognize hardware names.

</td></tr></tbody>
</table><table id="table_mq3_cx4_hsb"><thead><tr><th>

Label and Name

</th><th>

Default value

</th><th>

Plugin

</th><th>

Recommended usage

</th></tr></thead><tbody><tr><td>

Maximum number of records for Intent Discovery classification**sn\_nlu\_discovery.intent\_discovery\_max\_classification\_limit**

</td><td>

300,000

</td><td>

Intent Discovery

</td><td>

Keep the number of records less than 500,000.

</td></tr><tr><td>

Minimum number of records for Intent Discovery classification**sn\_nlu\_discovery.intent\_discovery\_min\_classification\_limit**

</td><td>

10,000

</td><td>

Intent Discovery

</td><td>

Use at least 10,000 records to get high quality results.

</td></tr><tr><td>

Minimum number of records for NLU performance analysis**sn\_nlu\_workbench.glide.nlu.performance.min\_clustering\_records**

</td><td>

5,000

</td><td>

NLU Workbench - Advanced Features

</td><td>

Use at least 5,000 records to get high quality results.

</td></tr><tr><td>

NLU Conflict Detection - Moderate Threshold**sn\_nlu\_workbench.glide.nlu.conflict.moderate\_threshold**

</td><td>

.85

</td><td>

NLU Workbench - Advanced Features

</td><td>

Must be a decimal between 0 and 1. Keep this threshold less than the Critical Threshold.

</td></tr><tr><td>

NLU Conflict Detection - Critical Threshold**sn\_nlu\_workbench.glide.nlu.conflict.critical\_threshold**

</td><td>

.95

</td><td>

NLU Workbench - Advanced Features

</td><td>

Must be a decimal between 0 and 1. Keep this threshold greater than the Moderate Threshold.

</td></tr><tr><td>

The maximum number of rows in a batch test import file**sn\_nlu\_workbench.glide.nlu.batch\_test.max\_import\_rows**

</td><td>

10,000

</td><td>

NLU Workbench - Advanced Features

</td><td>

Make sure your batch test import file has no more than 10,000 rows.

</td></tr><tr><td>

The maximum number of utterances to display for feedback in the expert feedback loop**glide.mlpredictor.option.nlu.activeLearning.label\_candidate\_table.max\_response\_size**

</td><td>

300

</td><td>

NLU Workbench - Advanced Features

</td><td>

Pull no more than 300 utterances from your users' Virtual Agent chat logs to display for feedback in the Expert Feedback Loop application.The minimum umber of utterances a user should review before tuning the model

</td></tr><tr><td>

The minimum number of utterances a user should review before tuning the model**sn\_nlu\_workbench.glide.nlu.optimize.min\_labeled\_data**

</td><td>

100

</td><td>

NLU Workbench - Advanced Features

</td><td>

Provide and save feedback for at least 100 utterances from your users' Virtual Agent chat logs so you can execute the Tune Model feature in the Expert Feedback Loop application.

</td></tr><tr><td>

The maximum number of records to fetch from Virtual Agent chat logs**glide.mlpredictor.option.nlu.activeLearning.va\_chat\_logs.max\_row\_limit - 3000**

</td><td>

3,000

</td><td>

NLU Workbench - Advanced Features

</td><td>

If there is high NLU usage, increasing the default value to a maximum of 50,000 records will increase the data available for the active learning job to filter up on and display in the Expert Feedback Loop application to give feedback on.

</td></tr><tr><td>

Size limit on Label Candidate Table \(used for pruning the table\)**glide.mlpredictor.option.nlu.activeLearning.label\_candidate\_table.max\_data\_size - 10000**

</td><td>

10,000

</td><td>

NLU Workbench - Advanced Features

</td><td>

The recommended usage for this property is the same as the property above.

</td></tr><tr><td>

Size limit on Labeled Data Table \(used for pruning the table\)**glide.mlpredictor.option.nlu.activeLearning.label\_table.max\_data\_size - 10000**

</td><td>

10,000

</td><td>

NLU Workbench - Advanced Features

</td><td>

The recommended usage for this property is the same as the property above.

</td></tr><tr><td>

Enable this property to unblock your instance during NLU model training. The training will be scheduled for an off-peak time, and we will notify you when it's done. **glide.mlpredictor.scheduled.nlu.model.training**

</td><td>

False

</td><td>

NLU Workbench - Advanced Features

</td><td>

False

</td></tr></tbody>
</table>To get more feedback data from Virtual Agent \(VA\) chat logs, refer to the **Procuring additional VA feedback data on demand** section in the [Expert Feedback Loop documentation](../concept/nlu-expert-feedback-loop.md).

**Parent Topic:**[Exploring Natural Language Understanding](../concept/nlu-explore.md)

