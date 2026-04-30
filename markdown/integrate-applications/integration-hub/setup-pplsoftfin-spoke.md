---
title: Set up the Oracle Peoplesoft Financial spoke
description: Integrate the Oracle Peoplesoft Financial and ServiceNow instances, and authenticate the requests using the basic authentication.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Oracle Peoplesoft Financial Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Oracle Peoplesoft Financial spoke

Integrate the Oracle Peoplesoft Financial and ServiceNow instances, and authenticate the requests using the basic authentication.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Oracle Peoplesoft Financial spoke.
-   Ensure that you have access to Oracle Peoplesoft Application Designer.
-   Roles required: ServiceNow admin and Oracle Peoplesoft Financial System Admin.

## Procedure

1.  In the Application Designer, import the Oracle Peoplesoft Financial project.

    1.  From the [ServiceNow® Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/6700409ddb1de4541e5c56a8dc961927) download the project file, SN\_PS\_FSCM\_INTEGRATION.zip and save it in the required local folder.

    2.  Import the Oracle Peoplesoft Financial project to the target environment that is, Oracle Peoplesoft Application Designer.

    3.  Navigate to **Copy Project** &gt; **From File** and select the project file.

        ![Import the project file.](../image/pplsoft-import-project.png)

    4.  Click **Copy** to copy the definition types.

        ![Copy the definition types.](../image/pplsoft-copy-def-types.png)

    5.  Verify that the project has all the objects; Application packages, Records, Services, and Service Operations.

    6.  Build the project by navigating to **Build** &gt; **Project**.

    7.  Select **Create Tables**, **Create Views**, and **Execute and build script** options.

        ![Build project.](../image/pplsoft-build-project.png)

        The required tables are created in the target Oracle Peoplesoft Financial database.

2.  Enable the required web services on your Oracle Peoplesoft Financial instance.

    1.  Log in to your Oracle Peoplesoft Financial instance as an System Admin.

    2.  Navigate to **Navigator** &gt; **People Tools** &gt; **Integration Broker** &gt; **Web Services** &gt; **Provide Web Service**.

    3.  In the Search Criteria, specify `sn_` for **Service Name** and click **Search**.

        ![ServiceNow webservices.](../image/peoplesoft-webservices.png)

    4.  Select the check box against the required web services and click **Next**.

        **Note:** Ensure that you select 24 ServiceNow web services.

        |Service|Description|
        |-------|-----------|
        |SN\_AP\_INV\_PYMNT\_STATUS|AP Invoice Payment Status|
        |SN\_AP\_INV\_VOUCHER\_ADD\_WS|ServiceNow Voucher Add|
        |SN\_ASSET\_LOAD\_WS|Asset Load|
        |SN\_BILL\_GET\_INV|Get Invoice|
        |SN\_CREATE\_VENDOR\_CI|Create Vendor|
        |SN\_EXECUTEQUERY|ServiceNow - QAS|
        |SN\_GET\_AP\_INVOICE\_DTL|AP Invoice Detail|
        |SN\_GET\_ASR|Advance Shipment Receipt|
        |SN\_GET\_ASSET|SN\_GET\_ASSET|
        |SN\_GET\_BID\_EVENT|ServiceNow Bid Event|
        |SN\_GET\_CC|Get Const centres|
        |SN\_GET\_CURRENCY\_RATES|Get Currency Rates|
        |SN\_GET\_GL\_ACCOUNT|Get GI Accounts|
        |SN\_GET\_GL\_BALANCE|Ledger Data|
        |SN\_GET\_GL\_BU|Get GL BU|
        |SN\_GET\_ITEM\_MASTER|Item Master|
        |SN\_GET\_POHDR|PO Header|
        |SN\_GET\_POLN|Get PO Line|
        |SN\_GET\_SHIPTO\_LOCATIONS|Get Ship to Locations|
        |SN\_GET\_SUPPLIERS|Get Suppliers/Vendors|
        |SN\_JOURNAL\_LOAD|ServiceNow Journal Load|
        |SN\_MANAGE\_PROCESSES|ServiceNow Process webservice|
        |SN\_PO\_CANCEL|SN PO CANCEL|
        |SN\_RECPT\_LOAD|Receipt frm SN|

    5.  Under **Operations**, select the check box against the required web service and click **Next**.

    6.  Click **View WSDL** to view the WSDL file and click **Next**.

    7.  In **Specify Publishing Options**, click **Finish**.

        Generated WSDL URL is displayed in this format: `<Base-URL>/<webservice-endpoint>.wsdl`

    8.  Navigate to **Navigator** &gt; **People Tools** &gt; **Integration Broker** &gt; **Web Services** &gt; **CI-Based Services**.

    9.  Perform the same steps that you had earlier performed for the webservices.

        **Note:** Configure the webservices as per your requirement.

3.  Provide the required permissions to the web services.

    1.  Log in to your Oracle Peoplesoft Financial instance as a System Admin.

    2.  Navigate to **Navigator** &gt; **People Tools** &gt; **Integration Broker** &gt; **Web Services** &gt; **Service Utilities** &gt; **Service Operation Permissions**.

    3.  Select **Service** option, specify the service name in **Service**, and click **Search**.

        ![Permissions for the web services.](../image/peoplesoft-permission.png)

    4.  Select the check box against the required web service and click **Set Security**.

    5.  In **Web Service Access**, provide access as per your requirement and click **Save**.

        ![Provide the required access.](../image/peoplesoft-access.png)

4.  Using SQL Developer or Data Mover in Oracle Peoplesoft Application Designer, connect to the database and run these scripts to ensure that the journal entry, SN\_ACCT\_ENTRY is built.

    ```
    SET DEFINE OFF;
    
    Insert into PS_SOURCE_TBL (SETID,SOURCE,EFFDT,EFF_STATUS,DESCR,JRNL_BALANCE_OPTN,JRNL_EDIT_ERR_OPTN,JRNL_AMT_ERR_OPTN,JRNL_DT_ERR_OPTN,JRNL_DT_ERR_OPTN2,CONTROL_TOTAL_OPTN,CURRENCY_BAL_OPTN,EXCHANGE_RATE_OPTN,BASE_CUR_ADJ_OPTN,JRNL_FOREIGN_OPTN,POST_ZERO_SW,JRNL_APPRVL_OPTN,BD_JRNL_APPR_OPTN,BUSPROCNAME,APPR_RULE_SET,BUSPROCNAME_BD,APPR_RULE_SET_BD,PHYSICAL_NATURE,DOC_TYPE_OPTN,DOC_TYPE) values ('SHARE','SN',to_date('01-JAN-00','DD-MON-RR'),'A','ServiceNow','R','R','R','D','D','R','D','D','D','D','N','D','D',' ',' ',' ',' ',' ','D',' ');
    
    ```

    ```
    Insert into PS_JRNLGEN_DEFN (SETID,ACCTG_DEF_NAME,DESCR,RECNAME,RECNAME_UPDATE,RECNAME_REFREC_KEY,FIELDNAME_ACCTDATE,FIELDNAME_MON_AMT,FIELDNAME_FRN_AMT,FIELDNAME_STAT_AMT,FIELDNAME_DESCR,FIELDNAME_JRNL_REF,FIELDNAME_OPEN_KEY,FIELDNAME_STLMT_DT,FIELDNAME_DT_STAMP,SYSTEM_SOURCE,BUDGET_AMT_TYPE,PNLNAME,DRILL_DOWN_OPTN,KK_SKIP,JGEN_KK_OPTN,KK_AMOUNT_TYPE,APPL_JRNL_ID_DFLT) values ('SHARE','SNOW_PSFT','ServiceNow Accounting Entries','SN_ACCT_ENTRY','SN_ACCT_ENTRY',' ','ACCOUNTING_DT','MONETARY_AMOUNT','FOREIGN_AMOUNT','STATISTIC_AMOUNT','LINE_DESCR',' ','JRNL_LN_REF','ACCOUNTING_DT','DTTM_STAMP','GOT','OT','JGEN_ACCTG_DRILL','Y','1','V','1',' ');
    ```

    ```
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',1,'ACCOUNT','ACCOUNT','Y');
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',2,'ALTACCT','ALTACCT','Y');
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',3,'OPERATING_UNIT','OPERATING_UNIT','Y');
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',4,'DEPTID','DEPTID','Y');
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',5,'PRODUCT','PRODUCT','Y');
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',6,'PROJECT_ID','PROJECT_ID','Y');
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',7,'AFFILIATE','AFFILIATE','Y');
    Insert into PS_JRNLGEN_DEFNV (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,CHARTFIELD,CF_SUMMARIZE_OPT) values ('SHARE','SNOW_PSFT',8,'STATISTICS_CODE','STATISTICS_CODE','Y');
    
    ```

    ```
    Insert into PS_JRNLGEN_DEFMB (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME) values ('SHARE','SNOW_PSFT',1,'BUSINESS_UNIT');
    Insert into PS_JRNLGEN_DEFMB (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME) values ('SHARE','SNOW_PSFT',2,'TRANSACTION_ID');
    Insert into PS_JRNLGEN_DEFMB (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME) values ('SHARE','SNOW_PSFT',3,'LEDGER_GROUP');
    Insert into PS_JRNLGEN_TGRP (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,FIELD_VALUE1) values ('SHARE','SNOW_PSFT',1,'BUSINESS_UNIT',' ');
    Insert into PS_JRNLGEN_TGRP (SETID,ACCTG_DEF_NAME,FIELD_SEQUENCE,FIELDNAME,FIELD_VALUE1) values ('SHARE','SNOW_PSFT',2,'TRANSACTION_ID',' ');
    Insert into PS_JRNLGEN_APPL_ID (SETID,APPL_JRNL_ID,EFFDT,EFF_STATUS,DESCR,JOURNAL_ID_MASK,JRNL_DT_OPTN,JRNL_DT_ALT_OPTN,JOURNAL_DATE,STAY_IN_PERIOD,SOURCE,CURR_EFFDT_FLG,JRNL_DESCR,LINE_DESCR,TRANS_REF_NUM,JRNL_LN_REF,HOW_SPECIFY,ACCOUNT_SPECIFY,DEFAULT_SPECIFY,TREE_NAME,TREE_LEVEL,REVERSAL_CD,ENTRY_SYNC,BUS_UNIT_OPTN,DOC_TYPE) values ('SHARE','SNOW_PSFT',to_date('01-JAN-00','DD-MON-RR'),'A','ServiceNow Journal Template','SN','A','BF',null,'N','SN','J','ServiceNow External Journals','ServiceNow Journal Template',' ',' ','D','1','D',' ',' ','N','Y','A','GN-JG');
    
    ```

    ```
    Insert into PS_JRNLGEN_REQUEST(OPRID,RUN_CNTL_ID,REQUEST_NBR,PROCESS_FREQUENCY,PROCESS_STATUS,PROCESS_INSTANCE,PROCESS_ORIG,DTTM_STAMP_SEC,SETID,FROM_DT_OPTN,FROM_DT,TO_DT_OPTN,TO_DT,APPL_JRNL_ID,LEDGER_GROUP,BUSINESS_UNIT,ACCTG_DEF_NAME,JRNL_EDIT_OPTN,JRNL_BGTCHK_OPTN,JRNL_POST_OPTN,RTM_PRCS_FLG) values ('VP1','SN-PSFT',1,'A','C',200255,'P',to_timestamp('16-JUL-20 02.03.43.204000000 PM','DD-MON-RR HH.MI.SSXFF AM'),'SHARE','N',null,'C',null,'SNOW_PSFT','RECORDING',' ','SNOW_PSFT','Y','N','N',' ');
    ```

    ```
    Insert into PS_PRCSRUNCNTL (OPRID,RUN_CNTL_ID,LANGUAGE_CD,LANGUAGE_OPTION) values ('VP1','SN-PSFT','ENG','O');
    Insert into PS_PRCSRUNCNTL (OPRID,RUN_CNTL_ID,LANGUAGE_CD,LANGUAGE_OPTION) values ('VP1','SN_LOAD_1','ENG','O');
    Insert into PS_PRCSRUNCNTL (OPRID,RUN_CNTL_ID,LANGUAGE_CD,LANGUAGE_OPTION) values ('VP1','SN_PSFT_AP_VOUCHER_BUILD','ENG','O');
    
    ```

5.  Configure a connection record for the Oracle Peoplesoft Financial spoke.

    1.  Log in to the ServiceNow instance as an admin.

    2.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**

    3.  Select the **Connections** tab.

    4.  Locate the **Oracle\_PeopleSoft** alias and click **View Details**.

        **Note:** Don't click **Add Connection**.

        ![Oracle Peoplesoft spoke connection template alias](../image/orc-peoplesft-conn-template.png)

    5.  Click **Configure**.

        ![Oracle Peoplesoft spoke connection template configuration](../image/orc-pplesft-con-tempt-confg.png)

    6.  On the **Configure Connection**, fill in the fields.

<table id="table_bb4_lrl_q1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL obtained from the generated WSDL URL. **Note:** Remove the `<webservice-endpoint>.wsdl` part of the WSDL URL while specifying the Connection URL.

</td></tr><tr><td>

User name

</td><td>

User name of your Oracle Peoplesoft Financial account.

</td></tr><tr><td>

Password

</td><td>

Password of your Oracle Peoplesoft Financial account.

</td></tr></tbody>
</table>    7.  Click **Configure Connection**.

6.  Provide Oracle Peoplesoft Financial credentials to use the Process Trigger action.

    1.  Log in to the ServiceNow instance as an admin.

    2.  Navigate to **Oracle Peoplesoft Credentials** &gt; **Oracle Peoplesoft Credentials**.

    3.  Click **New**.

    4.  On the form, enter the username and password of user with the required permissions.

    5.  Click **Submit**.

7.  Retrieve details of the daily suppliers up to the required date.

    1.  Log in to the ServiceNow instance as an admin.

    2.  Navigate to **PSFT Flow Execution** &gt; **PSFT Flow Executions**.

    3.  Click **New**.

    4.  Select the date up to which you want to retrieve the daily suppliers data in **Last Successfull Execution**.

    5.  Click **Submit**.

    Based on the trigger you have configured in the Polling Suppliers subflow, data is retrieved periodically. To view the data, navigate to **PSFT** &gt; **PSFT Data**.


