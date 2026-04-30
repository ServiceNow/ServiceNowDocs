---
title: Normalization of discovery models using machine learning
description: Use machine learning to improve your normalization rates in real time by normalizing your unrecognized discovered software.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Software discovery and normalization, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Normalization of discovery models using machine learning

Use machine learning to improve your normalization rates in real time by normalizing your unrecognized discovered software.

The Software Asset Management application uses machine learning to improve normalization of discovery models. The prediction values currently supported by machine learning are version, full version, and edition.

Opt in for machine learning normalization by activating the Software Asset Management – Machine Learning Normalization \(com.sn\_sam\_ml\_normalization\) plugin.

Once the plugin is activated, ensure that the **Enable ML Normalization for discovered software** \(com.snc.samp.enable.ml\_normalization\) property is selected. For more details on this property, see [Software Asset Management properties](../reference/sam-properties.md). You can opt out of machine learning normalization by disabling this property. If you opt out, normalization of discovery models only takes place against the content service rules.

The scheduled job, `SAM-Normalize discovery models using content library rules`, triggers on a daily basis and normalizes the discovery models based on the content rules. This scheduled job runs irrespective of whether the Software Asset Management – Machine Learning Normalization plugin is activated or not. If this plugin is activated, then the partially normalized discovery models are picked up by another scheduled job, `SAM-Normalize discovery models using machine learning`. The scheduled job, `SAM-Normalize discovery models using content library rules` is enhanced to invoke the on-demand scheduled job, `SAM-Normalize discovery models using machine learning` and also validates machine learning predictions.

Once the scheduled job, `SAM-Normalize discovery models using machine learning` is complete, you can view the updated values in the following machine learning based columns in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table:

-   ML prediction values: Indicates the predicted values for the attributes.
-   ML model version: Indicates the model version that was used for predicting the attributes.
-   ML normalization status: Indicates the status of machine learning normalization. Values for this column include:
    -   ML normalized: Discovery model is normalized by machine learning
    -   Reverted: Discovery model is normalized by machine learning but the user reverted the normalized values
    -   Content overridden: Machine learning predictions over-written by new content rules

**Note:** The status of the scheduled job, `SAM-Normalize discovery models using machine learning` is tracked in the Software Asset Job Result \[samp\_job\_log\] table.

As the content rules are always getting updated, the weekly scheduled job `SAM-Normalize discovery models using content library rules` picks up the discovery models normalized by machine learning and tries to normalize these models with the latest content rules. If the predicted values of machine learning differ from the predictive values of the content service, the machine learning predictions are overwritten with the content service values. The content service prediction values always get precedence over the machine learning prediction values.

**Note:** For details on the normalization rules for the predictive values, refer to tables titled **Normalization rules for licensed products** and**Normalization rules for non licensed products**.

You can manually normalize a discovery model by reverting the normalization values. When you revert normalizations in the Software Discovery Model form, all the normalized values, got from content and machine learning, are removed. The discovery model reverts to a status of Match not Found.

**Note:** When you revert a discovery model normalized by machine learning, the content rules are not deactivated. However, if a discovery model is normalized only by content rules, then the content rules are deactivated.

<table id="table_qyb_5pf_gnb"><thead><tr><th>

Fields

</th><th>

Normalization status

</th></tr></thead><tbody><tr><td>

All fields are normalized**Note:** All the fields include publisher, product, version, edition, and full version.

</td><td>

Normalized

</td></tr><tr><td>

Only the publisher is normalized

</td><td>

Publisher normalized

</td></tr><tr><td>

If none of the fields are normalized: publisher, product, version, edition, full version

</td><td>

Match not found

</td></tr><tr><td>

Only product and publisher are normalized.

</td><td>

Partially normalized

</td></tr></tbody>
</table>|Fields|Normalization status|
|------|--------------------|
|If only publisher and product are normalized|Normalized|
|Only the publisher is normalized|Publisher normalized|
|If none of the fields are normalized: publisher, product, version, edition, full version|Match not found|

**Parent Topic:**[Software discovery and normalization](c_SAMDiscovery.md)

