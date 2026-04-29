---
title: Reclassify a CI
description: You can upgrade, downgrade, or switch the class of a CI by modifying its Class attribute.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Reclassify a CI

You can upgrade, downgrade, or switch the class of a CI by modifying its **Class** attribute.

## Before you begin

Role required: sn\_cmdb\_editor, asset, or itil \(In general, the roles required to update a CI\)

## About this task

Each class is defined with a unique set of attributes. This set consists of attributes that were derived from the parent class, and additional attributes defined for the class.

When you reclassify a CI, the following occurs.

1.  The set of attributes is adjusted to match the set of attributes of the newly assigned class. Attributes are added or removed as needed.
2.  If any attributes are unique to the current class and are not defined in the newly reclassified class, they are lost.
3.  A new record with the CI's current sys\_id is inserted to the table of the new class, with the appropriate set of attributes for the class \(the sys\_id of the CI is retained\).

Depending on the reclassification, the following occurs.

-   **Downgrade**

    The CI class is updated to a class that is higher in the class hierarchy, and the newly assigned class is a parent of the current class. For example, reclassifying a CI from the cmdb\_ci\_server class to the cmdb\_ci\_computer class.

    For example, the cmdb\_ci\_server class has attributes that the cmdb\_ci\_computer class does not have. During the downgrade, these attributes and their respective values are not included in the new CI record that is inserted into the cmdb\_ci\_computer class.

-   **Upgrade**

    The CI class is updated to a class that is lower in the class hierarchy, and the newly assigned class is a derived child of the current class and has additional attributes. For example, reclassifying a CI from the cmdb\_ci\_computer class to the cmdb\_ci\_server.

-   **Switch**

    The newly assigned class is in a different branch in the class hierarchy and has a different set of attributes than the current class. For example, reclassifying a CI from the cmdb\_ci\_linux\_server class to the cmdb\_ci\_win\_server class.

    A switch is a combination of a downgrade and an upgrade. For example if the CI is downgraded to the cmdb\_ci\_server, and then upgraded to the cmdb\_ci\_win\_server class. Therefore, attributes are lost in the same manner as in a downgrade operation.


**Note:** Avoid the CI class downgrade and CI class switch operations as those can lead to data loss. When automatic CI reclassification is enabled \(which is by default\), the [identification process](../concept/c_CMDBIdentifyandReconcile.md) can result in some automatic reclassifications which lead to data loss.

For information about CI reclassification by the Identification and Reconciliation Engine \(IRE\) and related system properties that control the behavior of automatic CI reclassification, see [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

## Procedure

1.  Locate the CI that you want to reclassify and display it in a list view.

    You can use the application navigator. Or for example, if the CI is a server, then in the navigation search box, type `cmdb_ci_server.list` to display the CI in the **Servers** view.

2.  Ensure that the **Class** field is displayed in the list.

    If you do not see this attribute, personalize the list to add the **Class** field.

3.  Double-click the **Class** value for the CI, and select a new class.

4.  Click the green check box to confirm your selection.


**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Create a CI class](t_CreateCIType.md)

[Delete CIs](delete-class-records-ci-class-mgr.md)

[View and edit class definitions and metadata](t_ViewTableDefinitions.md)

[Update the list of classes in the Principal Class filter](update-principal-class-filter.md)

