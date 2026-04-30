---
title: Map enterprise roles to enterprise classes
description: Gain additional access to model categories by mapping individual enterprise roles to additional enterprise classes.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Map enterprise roles to enterprise classes

Gain additional access to model categories by mapping individual enterprise roles to additional enterprise classes.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

To map enterprise roles to enterprise classes, you need to first provide roles access to the classes and then expose the tabs associated with those classes in the designated workspace.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Admin center**.

2.  Select **Roles-to-class access**

3.  Select the role record that you want o configure.

    The respective class access rules page opens. For example, if you select the Facility asset technician enterprise class access rules record, the Facility asset technician enterprise class access rules page opens.

4.  Select a model category from the **Additional model categories** list.

    The classes related to the model category appear in the **Class names**.

5.  Select **Save**.

    The role is now assigned to the classes that you selected. You need to now expose the model and asset tabs related to these classes by navigating to the Model and asset tabs in the Admin center.

6.  Select Model and asset tabs in the Admin center.

7.  Select the model category name, that you assigned to the role, to open the class tab configuration page.

8.  Select **Include in tab** and **Include in dialog box**.

9.  Select **Save**.

    Role access is granted to the additional classes and the model and asset tabs associated with those classes are automatically visible in the specific workspace. Additionally, all dashboards are updated with data pertaining to the classes that you configured.


