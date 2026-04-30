---
title: Configure integration services for Oracle EBS
description: For configuring integration services, provide the connection end point and the Oracle EBS ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure integration services for Oracle EBS

For configuring integration services, provide the connection end point and the Oracle EBS ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.

Configure integration services for Oracle EBS. 

## Before you begin

-   Verify that the application scope is set to Oracle EBS spoke.
-   Verify that the MID Server is installed and configured in your ServiceNow instance to connect to the ERP server. For more details, see [Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    **Note:** The MID Server integration is required only for an Oracle EBS ERP integration using SOAP services.

-   For REST type service, REST API details, as provided by ERP.

Role required: sn\_fcms\_intg.integration\_user

## About this task

If the application requires multiple Oracle EBS ERP instances, create separate web services for each ERP instance. You can create Integration Service records for entities using the `sn_fcms_intg_service` table.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Open the ERP source for which you need to configure integration services.

    For example, Oracle EBS.

3.  In the Integration Services list, select the service that you want to configure.

    ![Look up Legal Entities from Oracle EBS](../image/oracle-ebs-fullpull.png "Look up Legal Entities from Oracle EBS")

4.  On the integration service record, fill in the fields.

<table id="table_ygn_3bx_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity

</td><td>

The type of entity for which you want to configure the integration services.

</td></tr><tr><td>

Application

</td><td>

Name of the application. For example, Oracle EBS.

</td></tr><tr><td>

ERP Source configuration

</td><td>

The ERP source mapped to the entity. For example, Oracle EBS.

</td></tr><tr><td>

Active

</td><td>

The status of the interaction service. By default, the check box is inactive.

</td></tr><tr><td>

Subflow

</td><td>

The subflow used to fetch primary data.

</td></tr><tr><td>

Properties

</td><td>

Creates a JSON record in the integration service, which is then passed to the ERP subflows to retrieve complete data.

 To pass JSON into the subflow, create a property named "query" and assign it a JSON query as its value, like this:

```
[
  {
    "parameter": "LEGAL_ENTITY_NAME",
    "operator": "=",
    "value": "Vision ADB",
    "operand": "NONE"
  }
]
```

 -   **Enabling Full Pull**:

Use this property to fetch the complete data.

    -   Create a property named "`full_pull`" and set its value to `true`.
    -   Additionally, you can create another property like, "`initial_load_start_date_time`" and set its value to `2025-02-15T04:10:34`.
-   **Enabling Delta Pull**:

Use this property to fetch the incremental data.

Set the value of the "`full_pull`" property to `false`.

</td></tr><tr><td>

Order

</td><td>

Option to choose the order in which the entity should be displayed.

</td></tr></tbody>
</table>5.  Select **Update**.

    The integration service is configured for the selected entity.


**Parent Topic:**[Configure the Source-to-Pay integration with Oracle EBS](../concept/configuring-source-to-pay-oracle-ebs-integration.md)

**Related topics**  


[ERP source configuration for Oracle EBS](../concept/erp-source-configuration-oracle.md)

[Define ERP source configuration for Oracle EBS](define-erp-source-oracle.md)

[Load data to ERP user-mapping table for Oracle EBS](load-data-erp-user-mapping-oracle-ebs.md)

[Look up primary data in Oracle EBS](../concept/look-up-primary-data-oracle-ebs.md)

[Scheduled jobs to look up primary data in Oracle EBS](../concept/scheduled-jobs-to-primary-data-oracle-ebs.md)

