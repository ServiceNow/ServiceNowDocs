---
title: Set up the Oracle EBS spoke
description: Integrate the ServiceNow instance and your Oracle EBS instance using a basic authentication to authenticate the ServiceNow requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Oracle EBS Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Oracle EBS spoke

Integrate the ServiceNow instance and your Oracle EBS instance using a basic authentication to authenticate the ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription.
-   Activate the Oracle EBS spoke.
-   Admin access to the Oracle EBS account.
-   Role required: admin

## Procedure

1.  From the [ServiceNow® Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/3e41ef4adb7fe81039f49ee4db961994) download the project file, Oracle\_e-business\_suite spoke\_dependencies.zip and save it in the required local folder.

2.  Unzip the contents of the Oracle\_e-business\_suite spoke\_dependencies.zip file.

3.  In SQL Developer or an SQL client, compile all the PKB and PLS files in the APPS schema.

    ![Compile the PLS and PKB files.](../image/oebs-compile.png)

4.  In Oracle EBS server, deploy the Oracle EBS REST API.

    For the steps to enable the REST API per extension, see [Administering Custom Integration Interfaces and Services](https://docs.oracle.com/cd/E18727_01/doc.121/e12169/T511175T543269.htm).

    You must perform these steps for every PLS file. While deploying each PLS file, you must provide the relevant values. Here, the procedure is outlined using `XXSN_CREATE_PO_PKG.pls` as an example.

    1.  Copy and upload the compiled package .pls files to these respective directories:

        -   `$PO_TOP/patch/115/sql/tmp/`
        -   `$PO_TOP/patch/115/sql/`
        **Note:** Ensure that you replace the `$PO_TOP` with the module the package belongs to such as, `$AP_TOP`, `$PO_TOP`, and so on.

    2.  Log in to PuTTY of your Oracle EBS server and execute the Integration Repository Parser.

        1.  To generate an iLDT \(\*.ildt\) file, execute the Integration Repository Parser using this syntax:

            ```
            $IAS_ORACLE_HOME/perl/bin/perl $FND_TOP/bin/irep_parser.pl -g -v -username=sysadmin po:patch/115/sql:XXSN_CREATE_PO_PKG.pls:12.0=$PO_TOP/patch/115/sql/tmp/XXSN_CREATE_PO_PKG.pls
            ```

        2.  If you aren't generating .ildt file for the XXSN\_CREATE\_PO\_PKG.pls file, replace `po` and `$PO_TOP` with required `Top`.
        3.  If you aren't generating .ildt file for the XXSN\_CREATE\_PO\_PKG.pls file, replace `XXSN_CREATE_PO_PKG.pls` with the required package name.
        ![Uploaded package name](../image/oebs-package-name.png)

    3.  Upload the generated iLDT file to Integration repository by executing this command:

        ```
        $FND_TOP/bin/FNDLOAD apps/apps 0 Y UPLOAD $FND_TOP/patch/115/import/wfirep.lct XXSN_CREATE_PO_PKG_pls.ildt
        ```

        **Note:** Replace `XXSN_CREATE_PO_PKG_` with the required package name.

        ![Package name](../image/oebs-pkg-name.png)

    4.  Log in to your Oracle E-Business Suite instance as system administrator.

    5.  Switch to the **Integrated SOA Gateway** responsibility and select **Integration Repository**.

        ![Select Integration Repository.](../image/oebs-integration-repo.png)

    6.  Search for the web service with the internal name, `XXSN_CREATE_PO_PKG`.

        ![Search with the internal name of web service.](../image/oebs-search-int-name.png)

    7.  Click the link in the search result to access the list of available metods in the interface package.

        ![PLSQL interface.](../image/oebs-plsql-interface.png)

        **Note:** In the PL/SQL interface type, both SOAP and REST web services are available. However, this procedure focuses on the REST web service.

    8.  Click the **REST Web Service** tab.

        1.  Set an alias for this service. For exmaple, `hr`.
        2.  Click **Deploy**.
    9.  View the Create PO method by clicking the **REST Web Service** tab.

        ![Deploy the services.](../image/oebs-ret-emp-num.png)

        ![Deploy the services.](../image/oebs-ret-emp-num2.png)

    10. Enter the unique service alias name, select the **Create PO** method, and click **Deploy**.

        ![Deployment confirmation,](../image/oebs-conf-msg.png)

        A confirmation message is displayed that the service is successfully deployed.

    11. Click **View WADL** to access the physical location of the service endpoint where the service is hosted.

    12. Open the **Grants** tab, select **Create PO**, and click **Create Grant**.

        ![](../image/oebs-create-grant.png)

    13. Select a grantee type, enter the user name to whom you want to give the grant access to use the web service, and click **Create Grant**.

        ![Grant access to use the web service.](../image/oebs-give-grant.png)

        A confirmation message is displayed mentioning that the grant has been successfully created.

        ![Confirmation message.](../image/oebs-grant-conf.png)

        **Note:** To revoke grant, click **Revoke Grants** in the **Grants** tab and select the required users.

    14. Perform the above steps for all the required actions and ensure that you use the same names \(associated with the respective action\) as mentioned in the Resource Path column of the following table:

        ![Action names.](../image/action-alias-oebs.png)

    15. Restart the server and using PuTTY, perform these steps up on logging in to the Oracle EBS server.

        1.  Execute the commands: `cd $ADMIN_SCRIPTS_HOME` and `./adadminsrvctl.sh stop`.
        2.  Enter the WebLogic password and EBS password.
        3.  Execute the command, `./adadminsrvctl.sh start`.
        4.  Enter the WebLogic password and EBS password.
        5.  To check the status, execute the command, `./adadminsrvctl.sh status`.
5.  Create a credential record for the Oracle EBS spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays the message `What type of Credentials would you like to create?`.

    3.  Select **Basic Auth Credentials**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the credential record. For example, `OEBS Cred`.|
        |User name|User name to log in to the Oracle EBS instance.|
        |Password|Password to log in to the Oracle EBS instance.|
        |Active|Option to actively use the credential record.|

    5.  Click **Submit**.

6.  Create a connection record for the Oracle EBS spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the record for the Oracle EBS spoke.

    3.  From the **Connections** tab, click **New**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the connection record. For example, `OEBS Conn`.|
        |Credential|Credential record you created for the Oracle EBS spoke.|
        |Connection URL|Connection URL to connect to your Oracle EBS instance.|

    5.  Click **Submit**.


