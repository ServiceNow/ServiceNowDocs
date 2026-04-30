---
title: Set up the Oracle EBS spoke
description: Integrate the ServiceNow instance and your Oracle EBS instance using a basic authentication to authenticate the ServiceNow requests.Configure Oracle Database 12C and later versions to work with the Oracle E-Business Suite spoke by deploying REST APIs and setting up ServiceNow connections.Configure Oracle Database 19C and later versions to work with the Oracle E-Business Suite spoke by deploying REST APIs and setting up ServiceNow connections.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Oracle EBS Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Oracle EBS spoke

Integrate the ServiceNow instance and your Oracle EBS instance using a basic authentication to authenticate the ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Oracle EBS spoke.
-   Admin access to the Oracle EBS account.
-   Role required: admin.

## Set up for Oracle Database 12C and later versions

Configure Oracle Database 12C and later versions to work with the Oracle E-Business Suite spoke by deploying REST APIs and setting up ServiceNow connections.

### Before you begin

Role required: admin

### Procedure

1.  From the [ServiceNow® Store Oracle E-Business Suite Spoke Dependencies for Oracle Database 12c and 18c](https://store.servicenow.com/sn_appstore_store.do#!/store/application/3e41ef4adb7fe81039f49ee4db961994) download the project file, Oracle\_e-business\_suite spoke\_dependencies.zip and save it in the required local folder.

2.  Unzip the contents of the Oracle\_e-business\_suite spoke\_dependencies.zip file.

3.  In SQL Developer or an SQL client, compile all the PKB and PLS files in the APPS schema.

    ![Compile the PLS and PKB files.](../image/oebs-compile.png)

4.  In Oracle EBS server, deploy the Oracle EBS REST API.

    For the steps to enable the REST API per extension, see [Deploying REST Web Services](https://docs.oracle.com/cd/E18727_01/doc.121/e12169/T682519T513044.htm#isgig_restdeploy).

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


## Set up for Oracle Database 19C and later versions

Configure Oracle Database 19C and later versions to work with the Oracle E-Business Suite spoke by deploying REST APIs and setting up ServiceNow connections.

### Before you begin

Role required: admin

### Procedure

1.  From the [ServiceNow® Store Oracle EBS Spoke Dependencies for Oracle Database 19c or later](https://store.servicenow.com/sn_appstore_store.do#!/store/application/dd28be0e977bb6d00cd036a71153af10/1.0.0) download the project file, Oracle\_e-business\_suite spoke\_dependencies.zip and save it in the required local folder.

2.  Unzip the contents of the Oracle\_e-business\_suite spoke\_dependencies.zip file.

3.  In SQL Developer or an SQL client, compile all the PKB and PLS files in the APPS schema.

4.  Review the module package reference to identify the correct values for your deployment.

    The following table lists the `.pls` filename, `$TOP` variable, product short-code, and service alias required for each Oracle EBS module. Use the values in this table wherever the steps below reference a module-specific path, product code, or alias.

    |Module|Package \(.pls filename\)|$TOP variable|Product code|Service alias|
    |------|-------------------------|-------------|------------|-------------|
    |General Ledger|`xxsn_gl_integration_pkg.pls`|`$GL_TOP`|`gl`|`xxsn_gl_integration_pkg`|
    |AP — Supplier|`xxsn_supplier_integration_pkg.pls`|`$AP_TOP`|`ap`|`xxsn_supplier_integration_pkg`|
    |Purchasing|`xxsn_po_integration_pkg.pls`|`$PO_TOP`|`po`|`xxsn_po_integration_pkg`|
    |Accounts Payable|`xxsn_ap_integration_pkg.pls`|`$AP_TOP`|`ap`|`xxsn_ap_integration_pkg`|
    |Fixed Assets|`xxsn_fa_integration_pkg.pls`|`$FA_TOP`|`fa`|`xxsn_fa_integration_pkg`|
    |Sourcing|`xxsn_pon_integration_pkg.pls`|`$PON_TOP`|`pon`|`xxsn_pon_integration_pkg`|
    |Inventory|`xxsn_inv_integration_pkg.pls`|`$INV_TOP`|`inv`|`xxsn_inv_integration_pkg`|
    |Common|`xxsn_common_integration_pkg.pls`|`$FND_TOP`|`fnd`|`xxsn_common_integration_pkg`|
    |Receivables|`xxsn_ar_integrations_pkg.pls`|`$AR_TOP`|`ap`|`xxsn_ar_integrations_pkg`|
    |Order Management|`xxsn_om_integration_pkg.pls`|`$ONT_TOP`|`ont`|`xxsn_om_integration_pkg`|

5.  In Oracle EBS server, deploy the Oracle EBS REST API.

    For the steps to enable the REST API per extension, see [Deploying REST Web Services](https://docs.oracle.com/cd/E18727_01/doc.121/e12169/T682519T513044.htm#isgig_restdeploy).

    You must perform these steps for every PLS file. While deploying each PLS file, you must provide the relevant values. Here, the procedure is outlined using `xxsn_gl_integration_pkg.pls` as an example.

    1.  Copy and upload the compiled package .pls files to these respective directories:

        -   `$GL_TOP/patch/115/sql/tmp/`
        -   `$GL_TOP/patch/115/sql/`
        **Note:** Ensure that you replace the `$GL_TOP` with the `$TOP` variable for the module the package belongs to. For the correct `$TOP` variable per module, see the module package reference table in the previous step.

        ![Upload the .pls file to the Oracle EBS application server directories.](../image/oebs-upload-pls-19c.jpg)

    2.  Grant `777` permissions to the uploaded `.pls` file.

        In your SFTP client, right-click the `.pls` file, click **Properties**, and set the **Octal** permission value to `0777`.

        ![Properties dialog showing Octal permission set to 0777 for the .pls file.](../image/oebs-file-permissions-19c.jpg)

        **Note:** 777 permissions are required for the Integration Repository parser to process the file. Without this step, the command in the next substep fails.

    3.  Log in to PuTTY of your Oracle EBS server and execute the Integration Repository Parser.

        1.  To generate an iLDT \(\*.ildt\) file, execute the Integration Repository Parser using this syntax:

            ```
            $IAS_ORACLE_HOME/perl/bin/perl $FND_TOP/bin/irep_parser.pl -g -v -username=sysadmin gl:patch/115/sql:xxsn_gl_integration_pkg.pls:12.0=$GL_TOP/patch/115/sql/xxsn_gl_integration_pkg.pls
            ```

        2.  If you aren't generating the .ildt file for the `xxsn_gl_integration_pkg.pls` file, replace `gl` and `$GL_TOP` with the product code and `$TOP` variable for the required module. For the correct values per module, see the module package reference table in the previous step.
        3.  If you aren't generating the .ildt file for the `xxsn_gl_integration_pkg.pls` file, replace `xxsn_gl_integration_pkg.pls` with the required package name.
        ![PuTTY terminal showing irep_parser.pl output ending with Done all files.](../image/oebs-irep-parser-output-19c.jpg)

    4.  Upload the generated iLDT file to Integration repository by executing this command:

        ```
        $FND_TOP/bin/FNDLOAD apps/apps 0 Y UPLOAD $FND_TOP/patch/115/import/wfirep.lct xxsn_gl_integration_pkg_pls.ildt
        ```

        **Note:** Replace `xxsn_gl_integration_pkg_` with the required package name.

        ![PuTTY terminal showing FNDLOAD command with log filename and report filename output.](../image/oebs-fndload-output-19c.jpg)

    5.  Log in to your Oracle E-Business Suite instance as system administrator.

    6.  Switch to the **Integrated SOA Gateway** responsibility and select **Integration Repository**.

        ![Oracle EBS Home page with Integrated SOA Gateway highlighted in the navigation menu.](../image/oebs-isg-home-19c.jpg)



        ![Integration Repository welcome page with Search button highlighted.](../image/oebs-integration-repo-search-19c.jpg)

    7.  Search for the web service with the internal name, `xxsn_gl_integration_pkg`.

        ![Integration Repository search page with xxsn_gl_integration_pkg entered in the Internal Name field.](../image/oebs-search-int-name-19c.jpg)

        ![Search results showing Oracle General Ledger Service Now Integration Service link.](../image/oebs-search-result-19c.jpg)

    8.  Click the link in the search result to access the list of available methods in the interface package.

        ![PLSQL Interface page for Oracle General Ledger Service Now Integration Service showing Overview, REST Web Service, and Grants tabs.](../image/oebs-plsql-interface-19c.jpg)

        **Note:** In the PL/SQL interface type, both SOAP and REST web services are available. However, this procedure focuses on the REST web service.

    9.  Click the **REST Web Service** tab.

        1.  In the **Service Alias** field, enter the service alias for your module. For the correct alias value per module, see the module package reference table in the previous step.

            **Note:** The service alias must exactly match the value in the **Service Alias** column of the module package reference table. Aliases are case-sensitive.

        2.  Click **Deploy**.
    10. View the General Ledger Integration service method by clicking the **REST Web Service** tab.

        ![REST Web Service tab showing Service Alias field with xxsn_gl_integration_pkg entered, all service operations listed with GET and POST checkboxes, and the Deploy button.](../image/oebs-rest-ws-tab-19c.jpg)

    11. Enter the unique service alias name, select the required method, and click **Deploy**.

        ![Confirmation banner showing the web service for Oracle General Ledger Service Now Integration Service was successfully deployed.](../image/oebs-deploy-conf-19c.jpg)

        A confirmation message is displayed that the service is successfully deployed.

    12. Click **View WADL** to access the physical location of the service endpoint where the service is hosted.

    13. Open the **Grants** tab, select the required method, and click **Create Grant**.

        ![Grants tab showing all service methods selected and the Create Grant button.](../image/oebs-grants-tab-19c.jpg)

        ![Create Grants page showing selected methods and Grantee Type set to All Users.](../image/oebs-create-grant-form-19c.jpg)

    14. Select a grantee type, enter the user name to whom you want to give the grant access to use the web service, and click **Create Grant**.

        ![Confirmation banner showing that the grant was created successfully for all service operations.](../image/oebs-grant-conf-19c.jpg)

        A confirmation message is displayed mentioning that the grant has been successfully created.

        **Note:** To revoke grant, click **Revoke Grants** in the **Grants** tab and select the required users.

    15. Perform the above steps for all the required actions and ensure that you use the same names \(associated with the respective action\) as mentioned in the Resource Path column of the following table:

    16. Restart the server and using PuTTY, perform these steps up on logging in to the Oracle EBS server.

        1.  Execute the commands: `cd $ADMIN_SCRIPTS_HOME` and `./adadminsrvctl.sh stop`.
        2.  Enter the WebLogic password and EBS password.
        3.  Execute the command, `./adadminsrvctl.sh start`.
        4.  Enter the WebLogic password and EBS password.
        5.  To check the status, execute the command, `./adadminsrvctl.sh status`.
        ![PuTTY terminal showing adadminsrvctl.sh stop command completing with exit status 0.](../image/oebs-wls-stop-19c.jpg)

        ![PuTTY terminal showing adadminsrvctl.sh start command output.](../image/oebs-wls-start-19c.jpg)

        ![PuTTY terminal showing adadminsrvctl.sh status output confirming the AdminServer is running.](../image/oebs-wls-status-19c.jpg)

6.  Create a credential record for the Oracle EBS spoke.

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

7.  Create a connection record for the Oracle EBS spoke.

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


