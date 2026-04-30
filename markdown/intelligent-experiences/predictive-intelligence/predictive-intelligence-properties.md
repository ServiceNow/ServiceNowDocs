---
title: Predictive Intelligence properties
description: The Predictive Intelligence properties control certain aspects of its machine-learning solution frameworks and solution training process, as well as other areas of the application.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Predictive Intelligence references, Predictive Intelligence, Enable AI experiences]
---

# Predictive Intelligence properties

The Predictive Intelligence properties control certain aspects of its machine-learning solution frameworks and solution training process, as well as other areas of the application.

Using the maint role, navigate to **Predictive Intelligence** &gt; **Configuration** to review or edit these properties.

**Note:** Some properties require other roles to review or edit.

<table id="table_ewc_w21_rpb"><thead><tr><th>

Property

</th><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Override ml\_solution\_definition record's readonly state during training

</td><td>

glide.platform\_ml.override\_training\_lock

</td><td>

-   True: Overrides the **readonly** state during training, enabling you to edit ml\_solution\_definition.
-   False: ml\_solution\_definition remains in the **readonly** state.

</td></tr><tr><td>

Minimum number of records for Regression

</td><td>

glide.platform\_ml.api.min\_regression\_records

</td><td>

Sets the minimum number of records required for Regression solution training.-   Type: Integer
-   Default value: 10000

**Note:** Support for new regression solutions is deprecated with the Washington DC release. You can edit and train any existing solutions, but you can't create new ones.

</td></tr><tr><td>

Maximum number of records for Regression

</td><td>

glide.platform\_ml.api.max\_regression\_records

</td><td>

Sets the maximum number of records that can be used in Regression solution training.-   Type: Integer
-   Default value: 300000

**Note:** Support for new regression solutions is deprecated with the Washington DC release. You can edit and train any existing solutions, but you can't create new ones.

</td></tr><tr><td>

The time \(in ms\) an in-training solution will wait without updates before timing out

</td><td>

glide.platform\_ml.training\_timeout

</td><td>

Sets the time-out time in milliseconds for an in-training solution.-   Type: Integer
-   Default value: 21600000 \(ms\)

</td></tr><tr><td>

Maximum model size

</td><td>

glide.platform\_ml.api.model\_size

</td><td>

Sets the maximum number of records you can use to train a model. -   Type: Integer
-   Default value: 524288000

</td></tr><tr><td>

Maximum number of records used in training

</td><td>

glide.platform\_ml.api.csv\_max\_line

</td><td>

Sets the maximum number of records that can be used in Classification solution training.-   Type: Integer
-   Default value: 300000

</td></tr><tr><td>

Minimum number of records used in training

</td><td>

glide.platform\_ml.api.csv\_min\_line

</td><td>

Sets the minimum number of records required for Classification solution training. -   Type: Integer
-   Default value: 10000

</td></tr><tr><td>

Maximum number of days worth of records on request can retrieve

</td><td>

glide.platform\_ml.api.csv\_split\_days

</td><td>

Sets the maximum number of days a single request can retrieve from your records.-   Type: Integer
-   Default value: 30

</td></tr><tr><td>

Maximum number of records per table for word corpus

</td><td>

glide.platform\_ml.api.max\_wordcorpus\_records

</td><td>

Sets the maximum number of records per table for Word Corpus creation for Similarity and Clustering solutions.-   Type: Integer
-   Default value: 300000

**Note:** With the Washington DC release, clustering and similarity solutions use Workflow solutions. These are pre-trained so a word corpus isn't needed. The Word Corpus field is removed from Workflow solution forms.

</td></tr><tr><td>

Maximum number of records for similarity window \(to lookup results\)

</td><td>

glide.platform\_ml.api.max\_similarity\_window\_records

</td><td>

Sets the maximum number of records that the Similarity Window can retrieve to look up results. -   Type: Integer
-   Default value: 100000

</td></tr><tr><td>

Maximum number of records for Clustering

</td><td>

glide.platform\_ml.api.max\_clustering\_records

</td><td>

Sets the maximum number of records you can include in a cluster. -   Type: Integer
-   Default value: 100000

</td></tr></tbody>
</table>|Property|Property Name|
|--------|-------------|
|Shared service scheduler url|glide.shared\_service\_scheduler.url|

|Property|Property Name|
|--------|-------------|
|Maximum number of artifacts cached \(in MB\)|glide.cache.size.ml\_object\_cache|
|Artifact cache compression scheme|glide.platform\_ml.artifact.cache\_compression\_scheme|

**Parent Topic:**[Predictive Intelligence references](reference-predictive-intelligence.md)

**Related topics**  


[Domain separation and Predictive Intelligence](../concept/domain-separation-predictive-intelligence.md)

[Data Encryption in Predictive Intelligence](predictive-intelligence-encryption.md)

[Predictive Intelligence language support](../concept/predictive-intelligence-localization.md)

[Predictive Intelligence roles](predictive-intelligence-roles.md#)

