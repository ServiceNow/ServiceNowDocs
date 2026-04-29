---
title: Associate suggested technology models to an application service
description: As an application owner, you can run the software product suggestions engine to fetch software products. These models can be related to an application service instead of mapping them manually.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Using Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Associate suggested technology models to an application service

As an application owner, you can run the software product suggestions engine to fetch software products. These models can be related to an application service instead of mapping them manually.

## Before you begin

**Important:**

Starting with the Xanadu release, the Technology Portfolio Management module has been deprecated from Enterprise Architecture \(formerly Application Portfolio Management\). However, if you’re an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still use the Technology Portfolio Management module. If you’re a new activation user, the Technology Portfolio Management module isn’t available.

You can leverage the same functionality by using the Technology Portfolio Management store application within the Enterprise Architecture Workspace. To learn more, see [Manage the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](../concept/eaw-concept/eaw-tpm.md).

Role required: sn\_apm.apm\_user

The Enterprise Architecture user has read-only permission to access the following tables:

-   Hardware \[cmdb\_ci\_hardware\]
-   Hardware Model \[cmdb\_hardware\_product\_model\]
-   Hardware Model Lifecycle \[cmdb\_hardware\_model\_lifecycle\]
-   Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]
-   Software Installation \[cmdb\_sam\_sw\_install\]
-   Software Model \[cmdb\_software\_product\_model\]
-   Software Model Lifecycle \[sam\_sw\_model\_lifecycle\]

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Application Portfolio** &gt; **All Business Applications**.

    You can follow one of the following options:

    -   Right-click the name of a business application and click **Manage Technology Models** option.
    -   Click the name of the business application to open the record in the form view. Then click **Manage Technology Models** button.
2.  Right-click the application service record in the Technology Models Retrieval Logs list.

3.  Click **Fetch Product Models** option.

4.  To fetch all the hardware models on which the business application runs, select the **Hardware Models Only** check box in the Fetch Product Models pop-up that opens.

    The technology models suggestions engine retrieves only the hardware models.

5.  To fetch all the hardware and the software, select the **Hardware and Software Models** check box.

    **Note:**

    The **Hardware and Software Products** check box appears when you activate Software Asset Management Professional \(com.snc.samp\) plugin.

    The hardware product models that are associated to the application service are listed in the Application Service Hardware Models \[sn\_apm\_tpm\_app\_service\_hardware\_model\] mapping table. The Technology Models Retrieval Logs \[sn\_apm\_suggestion\_engine\_run\_log\] table lists the number of hardware models on which an application service runs. The software models associated to the application service are listed in Application Service Software Models \[sn\_apm\_tpm\_service\_software\_model\] database table.

    By default, the technology models suggestion engine checks only the hardware and hardware installed with new software installs since the last run of the job. However, if you require the engine to check all hardware irrespective of its last run, then enforce a check on all installs.

6.  Select the **Force Check All Installs** check box to check all hardware irrespective of the check until the last run of the job.

    The engine retrieves different application instances for that business application.

    **Force Check All Installs** option also scans and suggests updated software models when there are variations in the mapping between the discovery model and the software models. Variations occur when the software models are either updated manually or through normalization rules.

7.  Click **OK**.

    In the Technology Models Retrieval Logs list, you can view the:

    -   Progress of the engine in the **Percent Complete** column corresponding to the application service record. A message, `Progress Worker to Fetch models is submitted successfully for Attendance Management Service` is also displayed at the top.
    -   Number of the software models that the engine suggests in the **Software Product Suggestions Count** column.
    -   Number of hardware models on which an application service runs in the **Hardware Model Count** column.
8.  Check the **Status** for the selected application service.

    The **Percent Complete** should be 100%. Or, click the information icon \(\) to view the log status of the application service.

9.  Click the application service record in the Technology Models Retrieval Logs list view.

    **Retrieved Software Products** tab lists all the software models retrieved from the associated hardware of the application instance in the Technology Models Retrieval view. You can also view the total number and names of the software models that the engine suggests associating with the application service.

10. Select the check box adjacent to the software model and click **Associate Software Products** action from the **Action on selected rows** list to associate the software product to the application service.

    The status of the software model changes to **Associated**. A record is created in the Application Service Software Products mapping table. You can also view the associated software products in the [TPM timeline](view-technology-risks-in-timeline.md) view.

    When you run the job for the first time, all the extracted software products are in status **New**. However, the status of the suggested software product changes based on the actions taken on the previous run of the job.

    In the Actions choice list below the software product list, you can select an action.

    For information about the status of the software models, see [Status of the Software models](../reference/status-software-models.md).

11. Click the **Application Service Software Models** tab to view the list of software models associated to the application service.

    To delete an application service software model record, select the record to mark for deletion and click delete in the **Action on selected rows** list. To associate an application service to a software model, see [Associate an application service to a software model](associate-business-service-to-software-model.md).

12. Click the **Application Service Hardware Models** tab to view the hardware product models that are associated to the application service.

    The Application Service Hardware Models \[sn\_apm\_tpm\_app\_service\_hardware\_model\] mapping table stores the data. To associate an application service to a hardware model, see [Associate an application service to hardware model](associate-application-service-hardware-model.md).


**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

