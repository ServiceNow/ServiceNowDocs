---
title: Create SAP users, roles, and authorizations
description: Create the SAP user, roles, and authorization objects required for the Software Asset Management integration with the central and satellite SAP systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/create-sap-users-roles-auth.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 4
keywords: [SAP users, SAP roles, SAP authorizations, PFCG, SAM integration]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create SAP users, roles, and authorizations

Create the SAP user, roles, and authorization objects required for the Software Asset Management integration with the central and satellite SAP systems.

## Before you begin

The SAP transport files must be imported into the central system before configuring users and roles.

Role required: SAP Basis administrator

## About this task

The Software Asset Management integration requires a dedicated SAP user with separate roles for the central system and each satellite system. Central system roles control background job scheduling and service access. Satellite system roles control RFC execution and table display access.

## Procedure

1.  Create a user ID `S_SERVICENOW` in your SAP system.

    If the user already exists, remove the current authorizations and set up new authorizations with central and satellite system permissions.

2.  Create a central system role.

    1.  Navigate to transaction code **PFCG**.

    2.  On the Role Maintenance page, enter a role name in the **Role** field.

        For example, `Z_SNOW_CTR`.

        \[Omitted image "sap-role-auth-central.png"\] Alt text: Role creation in the SAP central system

    3.  In the **Description** field, enter a brief description of the role and save.

    4.  Add authorization object `S_SERVICE` and add external service name `/NOW/SAMP//NOW/SAMP_USER_DETAILS_WSDL`.

        \[Omitted image "sap-roles-auth-object-service.png"\] Alt text: Adding authorization object for services and external service name in the SAP central system

    5.  Add authorization object `S_BTCH_ADM` and select the **N \(No administrator authorization\)** option in the **Activities** field.

        \[Omitted image "sap-role-auth-admin.png"\] Alt text: Adding authorization object for administration and activities in the SAP central system

    6.  Add authorization object `S_BTCH_JOB`, select **RELE \(Release Jobs\)** in the **Activities** field, and leave the **JOBGROUP** field empty.

        \[Omitted image "sap-role-auth-batch.png"\] Alt text: Adding authorization object for background jobs and activities in the SAP central system

    7.  If the central system is a SAP S/4HANA system, add authorization object `S_PROGNAM` and the following values in the corresponding fields.

        -   **P\_ACTION** — `BTCSUBMIT`
        -   **P\_PROGNAM** — `/NOW/SAMP_USER_PROG_BCKJOB_RUN`
        \[Omitted image "sap-role-auth-prognam.png"\] Alt text: Adding authorization object for program name and activities in the SAP central system

3.  Create a satellite system role.

    1.  Navigate to transaction code **PFCG**.

    2.  On the Role Maintenance page, enter a role name in the **Role** field.

        For example, `Z_SNOW_CLT`.

        \[Omitted image "sap-role-auth-satellite.png"\] Alt text: Role creation in the SAP satellite system

    3.  In the **Description** field, enter a brief description of the role and save.

    4.  Add authorization object `S_RFC` and fill in the following values for the fields.

<table id="table_twp_rzh_hjc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Activity

</td><td>

`16`This code refers to Execute.

</td></tr><tr><td>

RFC\_NAME

</td><td>

`/OSP/CORE`, `/OSP/PRGN_GET_ALL_AGRS`, `BAPI_USER_GETLIST`, `BAPI_USER_GET_DETAIL`, `MENU_READ_TSTC`, `RFC_READ_TABLE`, `RFCPING`, `SCSM_COLLECTOR`, `SDTX`, `SMNV_MIGRATION`, `STR9`, `SU_USER`, `SWNC_COLLECTOR_GET_AGGREGATES`, `SYSU`, `TR_SYS_PARAMS`, `/NOW/SAMP`, `/NOW/SAMP_HANADB`

</td></tr><tr><td>

RFC\_TYPE

</td><td>

`FUGR` and `FUNC`Here, FUGR is the Function Group and FUNC is the Function Module.

</td></tr></tbody>
</table>        \[Omitted image "sap-role-auth-rfc.png"\] Alt text: Adding authorization object for RFC access, activity, and type in the SAP satellite system

    5.  Add authorization object `S_TABU_DIS` and enter `03` in the **Activity** and `&NC&`, `SS` in the **Table Authorization Group** field.

        \[Omitted image "sap-role-auth-display.png"\] Alt text: Adding authorization object for table maintenance and activity in the SAP satellite system

    6.  Add authorization object `S_TABU_NAM` and fill in the following values for the fields.

<table id="table_hzj_1w3_hjc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Activity

</td><td>

`03`This code refers to Display.

</td></tr><tr><td>

Table Name

</td><td>

`AGR_FLAGS`, `AGR_TEXTS`, `TSTCT`, `TUPL`, `TUPLT`, `TUREP`, `TUTYPA`, `TUTYPNOW`, `TUTYPPL`, `USR41_MLD`, `T000`

</td></tr></tbody>
</table>        \[Omitted image "sap-role-auth-generic.png"\] Alt text: Adding authorization object for generic standard tools and activity in the SAP satellite system

    7.  Add authorization object `S_TOOLS_EX` and enter `S_TOOLS_EX_A` in the **Authorization name in user master main** field.

        \[Omitted image "sap-role-auth-tools.png"\] Alt text: Adding authorization object for performance monitoring tools and activity in the SAP satellite system

    8.  Add authorization object `S_BTCH_ADM` and select the **N \(No administrator authorization\)** option in the **Activities** field.

    9.  Add authorization object `S_BTCH_JOB`, select **RELE \(Release Jobs\)** in the **Activities** field, and leave the **JOBGROUP** field empty.

    10. Add authorization object `S_RZL_ADM` and enter `01` in the **Activity** field.

        \[Omitted image "sap-role-auth-rzl-adm.png"\] Alt text: Adding authorization object and activity in the SAP satellite system

    11. Add authorization object `S_USER_GRP` and enter `03` in the **Activity** field and `SUPER` in the **User group in user master main** field.

        \[Omitted image "sap-role-auth-user.png"\] Alt text: Adding authorization object for user group and activity in the SAP satellite system

4.  Assign the central system role to the `S_SERVICENOW` user in the central system, and the satellite system role to the same user in each satellite system.

    |Authorization object|Description|
    |--------------------|-----------|
    |S\_RFC|Verifies that the called RFC user is authorized to execute RFC function modules.|
    |S\_SERVICE|Verifies the start of your external services.|
    |S\_TCODE|Initiates an SAP transaction from the command box or menu.|
    |S\_BTCH\_ADM|Manages background processing.|
    |S\_BTCH\_JOB|Manages background jobs.|
    |S\_RZL\_ADM|Maintains external system commands.|
    |S\_TABU\_DIS|Controls table access to users.|
    |S\_TABU\_NAM|Provides authorizations for tables based on the table name instead of the table authorization group.|
    |S\_TOOLS\_EX|Monitors tool performance.|
    |S\_USR\_GRP|Performs user maintenance for several transactions.|


## What to do next

Select the Remote Function Call \(RFC\) connections that the SAP ABAP program uses to import data from your SAP clients. For details, see [Select SAP clients to import data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/select-sap-clients-import.md).

