---
title: Set up a software model for an SCCM application
description: Using the applications discovered on the SCCM server, set up a software model used by the Software Asset Management application to manage licenses.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up a software model for an SCCM application

Using the applications discovered on the SCCM server, set up a software model used by the Software Asset Management application to manage licenses.

## Before you begin

Role required: sn\_client\_sf\_dist.csd\_admin or admin

Before creating software models, you must discover the applications available for deployment on the SCCM server. See [Retrieve SCCM data for client software distribution](t_RetrieveSCCMDataClientSWDist.md#) for details.

## About this task

You can link an SCCM application to an existing software model or create a new model.

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **SCCM** &gt; **SCCM Applications**.

    A list of applications discovered on the SCCM server appears.

2.  Open an SCCM application record.

3.  To link to an existing model, click the magnifying glass icon in the **Model** field and select a model from the list.

    ![SCCM application record](../image/SCCMApplicationRecord.png "SCCM application record")

4.  To create a model, click **Create Software Model** under **Related Links**.

    1.  Complete the software model fields.

        See for details.

    2.  Click **Submit**.

        The view returns to the SCCM Applications form.


**Parent Topic:**[Configuring SCCM](../concept/configuring-sccm.md)

