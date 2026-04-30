---
title: Clone calibration attributes to an enterprise model
description: Clone an existing calibration attribute to an enterprise model to add a calibration attribute with similar settings.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise models, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Clone calibration attributes to an enterprise model

Clone an existing calibration attribute to an enterprise model to add a calibration attribute with similar settings.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Enterprise model management view.

2.  Select either the **All enterprise** tab or the tab for a specific model category, such as **Construction**.

3.  From the list of available enterprise models, select the enterprise model that you want to clone a calibration attribute to or from.

4.  On the **Calibration attributes** tab of the enterprise model record, use one of the following options to clone a calibration attribute:

    -   To clone a calibration attribute from this enterprise model to another enterprise model, use the following steps:
        1.  From the list of available calibration attributes, select the check box for the calibration attribute that you want to clone.
        2.  Select **Clone to models**.

        3.  In the Select models dialog box, select the **Clone as active** check box to automatically set the cloned calibration attribute to active.
        4.  Select the check box for the enterprise model that you want to clone the calibration attribute to.
        5.  Select **Clone**.

            The calibration attribute is cloned to the selected enterprise model.

            **Note:** If the selected enterprise model already contains another calibration attribute with the same name, this attribute is cloned with a numeric suffix appended to the name.

    -   To clone a calibration attribute from another enterprise model to this enterprise model, or to clone a common calibration attribute from your calibration attribute library to this enterprise model, use the following steps:
        1.  Select **Clone from**.

        2.  In the Select attribute to clone dialog box, select the **Clone as active** check box to automatically set the cloned calibration attribute to active.
        3.  Select the check box for the calibration attribute that you want to clone.
        4.  Select **Clone**.

            The calibration attribute is cloned to the enterprise model and appears in the list of available calibration attributes.

            **Note:** If the enterprise model already contains another calibration attribute with the same name, this attribute is cloned with a numeric suffix appended to the name.


**Parent Topic:**[Create and manage enterprise models](../concept/create-manage-enterprise-models.md)

