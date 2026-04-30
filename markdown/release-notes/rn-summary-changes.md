---
title: Changes to Xanadu features and products
description: Cumulative release notes summary on changes to Xanadu features and products.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 71
breadcrumb: [Release notes summaries for Xanadu features, Release notes for upgrading from Washington DC, Learn about the Xanadu release, Xanadu release notes]
---

# Changes to Xanadu features and products

Cumulative release notes summary on changes to Xanadu features and products.

Existing  products were updated and changed in Xanadu. This includes the renaming of certain buttons or features.

<table id="rn-summary-changes-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Search

</td><td>

-   **[Facets display refinement filters in the search user's language](https://www.servicenow.com/docs/access?context=create-facet-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

When displaying reference field values as facet refinement filters, AI Search uses field value translations for the search user's language if available. If no translations are available for the user's language, AI Search uses translations for the system language.

-   **[Late binding security implementation preserves correct click rank search signals](https://www.servicenow.com/docs/access?context=content-security-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

When late binding security removes inaccessible results, click rank search signals correctly reflect the final result ordering.


</td></tr><tr><td>

API

</td><td>

<table id="table_vlp_vl5_zbc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table id="table_brb_jrn_xwb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideAggregate - Global](https://www.servicenow.com/docs/access?context=c_GlideAggregateAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addAggregate\(\)
-   addHaving\(\)
-   getValue\(\)
-   groupBy\(\)
-   orderBy\(\)
-   orderByAggregate\(\)

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added support for dynamic schema.-   addQuery\(\)
-   getDisplayValue\(\)
-   getValue\(\)
-   orderBy\(\)
-   orderByDesc\(\)
-   setDisplayValue\(\)
-   setValue\(\)

</td></tr><tr><td>

[HistoryWalker - Scoped, Global](https://www.servicenow.com/docs/access?context=HistoryWalkerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added parameter for specifying the type of history walker implementation to use.HistoryWalker\(\)

</td></tr></tbody>
</table><table id="table_ajg_1t5_szb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[AWA Manual Assignment API](https://www.servicenow.com/docs/access?context=awa_manual_assign-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new request body parameters. POST /awa/workitems/\{work\_item\_sys\_id\}/assignments

</td></tr><tr><td>

[Continuous Integration/Continuous Delivery \(CICD\) API](https://www.servicenow.com/docs/access?context=cicd-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new optional query parameters for specifying whether to run a test suite as a performance test and in Cloud Runner. POST /sn\_cicd/testsuite/run

</td></tr></tbody>
</table><table id="table_ert_xdv_dcc"><thead><tr><th>

Application

</th><th>

App version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Lead to Cash Core

</td><td>

V1.3.1

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

The LeadtoCashCore script include is enhanced to support reconfiguration use cases:-   createInstance\(\) - Returns **\_state** identifying whether the entity record is in an active or inactive state.
-   delta\(\) - **additionalParams** now supports the ability to ignore attributes to compare in source and dirtyJSONs.
-   effect\(\) - **additionalParams** now supports the ability to provide context variable keys instead of dictionary field names. Additionally, effect\(\) returns the **\_state** parameter identifying whether the entity record is in an active or inactive state.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

V2.0.0

</td><td>

[LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

commitInstance\(\) now returns the dataObject object which displays the status of an asynchronous transaction for users to review and submit the transaction for further fulfillment.

</td></tr></tbody>
</table><table id="table_n4j_mxv_lbc"><thead><tr><th>

 

</th><th>

 

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

CSM Openframe

</td><td>

V1.0

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added **workitem\_rejected** and **workitem\_accepted** response payloads.subscribe\(\)

</td></tr><tr><td>

CSM Openframe

</td><td>

V1.1

</td><td>

[openFrameAPI - Client](https://www.servicenow.com/docs/access?context=c_openFrameAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added **isAutoAccepted** flag in response payloads.subscribe\(\)

</td></tr></tbody>
</table><table id="table_nq4_nxv_lbc"><thead><tr><th>

Application

</th><th>

App version

</th><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

Customer Contracts and Entitlements

</td><td>

V4.0

</td><td>

[Service Contract API](https://www.servicenow.com/docs/access?context=servicecontract-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Product specification information and automatically generated identification number were added to the following endpoints:-   GET /sn\_pss\_core/servicecontract/\{id\}
-   GET /sn\_pss\_core/servicecontract/contractline/\{id\}
-   POST /sn\_pss\_core/servicecontract
-   POST /sn\_pss\_core/servicecontract/contractline

</td></tr><tr><td>

Entitlements Verification

</td><td>

V2.0

</td><td>

[Verify Entitlements API](https://www.servicenow.com/docs/access?context=verifyentitlements-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Product specification information and automatically generated identification number were added to the following endpoints:-   GET /sn\_ent\_verify/verifyentitlements
-   GET /sn\_ent\_verify/verifyentitlements/getEntitlementCharacteristic/\{id\}

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   For all endpoints, the namespace and endpoint paths changed from sn\_ind\_tmt\_ord to sn\_tmf\_api.
-   The following methods return two new parameters, **href** and **orderDate**.
    -   GET /sn\_tmf\_api/order/serviceOrder
    -   POST /sn\_tmf\_api/order/serviceOrder/cancelserviceorder
    -   Service Order Open API – POST /sn\_tmf\_api/order/serviceOrder
    -   POST /sn\_tmf\_api/order/serviceOrder/outboundresponse

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

V2.1.0

</td><td>

[Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

-   For all endpoints, the namespace and endpoint paths changed from sn\_ind\_tmt\_ord to sn\_tmf\_api.
-   productOffering methods return two new optional parameters, **href** and **lifecycleStatus**:
    -   GET /sn\_tmf\_api/catalogmanagement/productOffering
    -   GET /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}
    -   PATCH /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}
    -   POST /sn\_tmf\_api/catalogmanagement/productOffering
-   productSpecification methods return three new optional parameters, **isBundle**, **href**, and **lifecycleStatus**:
    -   GET /sn\_tmf\_api/catalogmanagement/productSpecification
    -   GET /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}
    -   PATCH /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}
    -   POST /sn\_tmf\_api/catalogmanagement/productSpecification

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

V3.5.0

</td><td>

[TISC API](https://www.servicenow.com/docs/access?context=tisc-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

The **sort\_by** and **sort\_direction** request body parameters are no longer supported. Observables returned in the response are sorted by **sys\_id** in ascending order.POST /sn\_sec\_tisc/threat\_intel\_data/observables

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

 

</td><td>

[WSD Extra Service Request API](https://www.servicenow.com/docs/access?context=wsd_extra_serv_req-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new request body parameter, reservationDateTimeChanged.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable API](https://www.servicenow.com/docs/access?context=wsd_reservable-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.GET /sn\_wsd\_rsv/reservable/list\_reservables/\{sys\_ids\}

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

V2.11.0

</td><td>

[WSD Reservable V2 API](https://www.servicenow.com/docs/access?context=wsd_reservable-V2-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td><td>

Added new query parameter, reservation\_start\_time.POST /sn\_wsd\_rsv/v2/reservable/list\_reservables

</td></tr></tbody>
</table>

</td></tr><tr><td>

Access Management

</td><td>

-   **[Deny-Unless condition for ACLs](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

A new decision type field helps administrators define the conditions that give or deny users access to data. It enables more granular decision-making while defining the right access strategy on the platform.

-   **[Enhanced ACL Security](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

If an ACL is misconfigured or empty, you can deny access to data by default, enhancing the overall security of the platform.

-   **[ACL Query Behavior](https://www.servicenow.com/docs/access?context=r_SecurityJumpStartACLRules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Fine-tune your access control by dictating rules for querying data with the introduction of new operators: query match and query range.

-   **&gt;[Explicit Roles behavior adjustment](https://www.servicenow.com/docs/access?context=explicit-roles&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

When the system property `glide.security.explicit_roles.do_not_fix` is true, the **snc\_internal** role is no longer added in memory or to the User Roles \[sys\_user\_has\_role\] table.


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[APO landing page](https://www.servicenow.com/docs/access?context=acc-pay-workspace-landing-page&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Task owners can view and handle invoice tasks more efficiently using task filters, widgets and bar charts in the Accounts Payable Operations workspace.

-   **[Accounts Payable Operations integration framework](https://www.servicenow.com/docs/access?context=using-integration-to-create-invoice&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Updated invoice integration using tax fields enables you to process invoices more quickly.


</td></tr><tr><td>

Adoption Services

</td><td>

-   ****

Use the new Guided Setup player process backend powered by the Playbooks backend. App development team admins that create Guided Setups for their products now have all capabilities that are part of the Playbooks. This change creates a similar Guided Setup player experience with new visual enhancements to the UI.

-   **Create a guided setup**

Use the new capabilities offered with the Playbooks \(PAD\) backend to define the activities that PAD can support in addition to the existing activities of the Guided Setup builder. For example, you can use Conditional Flow, which would be introduced in the Guided Setup flow.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **[AI Search Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The **Date range** interactive filter now allows you to access data from the last 180 days, rather than the last 90 days.


</td></tr><tr><td>

Agent Client Collector

</td><td>

-   **Use the updated Windows event check**

Starting in version 3.12.0, the Windows event check `os.windows.check-event-log` has been renamed `os.windows.check-event-log-count` and has enhanced data gathering capabilities.


-   **Updated plugin dependency**

Starting in version 4.1.0, the Service Error Management plugin is dependent on the ACC-F scoped app. The plugin gets installed automatically when the customer installs the ACC-F scoped app from the ServiceNow store.

-   **[New allow list parameter for checks running in shell execution mode](https://www.servicenow.com/docs/access?context=check-definition-form&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Starting in version 4.1.0, when running a check in with execution mode \(**Exec Mode**\) set to **shell**, add the **allow\_shell** parameter and set it to **true** for the allow list entry corresponding to the check.


</td></tr><tr><td>

Agent Workspace for HR Case Management

</td><td>

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

The Agent Workspace for HR Case Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For information about how to upgrade, see the [rn-summary-changes.md\#hr-aws-rn-accessibility](rn-summary-changes.md#hr-aws-rn-accessibility) that follows.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Email enhancements](https://www.servicenow.com/docs/access?context=csm-front-line-case-page-modeless-dialogs&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US#section_vfl_qcs_m1c)**

The Compose Email modeless dialog includes the following enhancements:

    -   A collapsible header that includes the **To**, **Cc**, **Bcc**, and **Subject** fields.
    -   Icons in the footer that enable you to discard the current email draft, apply a template, view a list of recent email drafts, and add attachments.
    -   Compose Email modeless dialog that you can open to see the last saved email draft.

</td></tr><tr><td>

Audit Management

</td><td>

-   **[Domain separation and Audit Management](https://www.servicenow.com/docs/access?context=audit-management-domain-separation&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Changes are made to the domain assignment process to manage data segregation by the Managed Service Providers related to the objects in Audit Management and Advanced Audit.

-   **[Role change for users approving workflows](https://www.servicenow.com/docs/access?context=r_InstallWAudit&version=xanadu&pubname=xanadu-governance-risk-compliance&section=r_RolesInstallWAudit&ft:locale=en-US)**

Approvers for an engagement and audit plan can also use the Audit approver \(sn\_audit.approver\) role as a lite operator role to approve audit workflows.


</td></tr><tr><td>

Authentication

</td><td>

-   **[Multi-factor Authentication \(MFA\)](https://www.servicenow.com/docs/access?context=mfa-config-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Use the FIDO2 authenticator, passkeys, biometric authenticators, and hardware security keys as multi-factor authentication \(MFA\) factors without requiring an authenticator app setup.


</td></tr><tr><td>

Business Continuity Management

</td><td>

-   **[Element definitions and variables](https://www.servicenow.com/docs/access?context=element-definitions&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

You can now add a Windows server asset in the Windows server element definition or a Linux server asset in the Linux server element definition. However, you can’t add the Windows server asset or the Linux server asset in the filter of the Hardware element definition.


</td></tr><tr><td>

Case management for CSM

</td><td>

-   **[Case type selector configuration](https://www.servicenow.com/docs/access?context=csm-case-type-select-modals-product-service&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Configure the Product Service select version of the case type selector to hide the product filter.

-   **[Roles included with the customer service manager role](https://www.servicenow.com/docs/access?context=r_RolesInstalledWithCustomerService&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

The customer service manager role \[sn\_customerservice\_manager\] includes the approver user role \[approver\_user\]. For upgrade customers, the approver user role replaces the approval admin role \[approval\_admin\]. Users with the customer service manager role can approve the approval requests that are assigned to them.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=improve-opportunities&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Added different variants of the two enhanced types of base system opportunities that you can use on a project to identify and address common inefficiencies in customer operations:

    -   Rule-based finding definitions: Execute one or more finding rule chains in sequence according to the definitions. The records that match the logic of these specifications are classified as a match for improvement opportunities.
    -   Automated finding definitions: Show improvement opportunities by using the default patterns that are already available for selection.

</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[Share a Space in CWM and manage sharing permissions](https://www.servicenow.com/docs/access?context=share-space-in-cwm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

While sharing a space with other collaborators, you can now search users and groups by email along with their name. This feature helps you choose the right collaborator in cases where individual users or groups have the same name.


</td></tr><tr><td>

Compliance Case Management

</td><td>

A new graphical chart enables your compliance case managers to monitor and access their compliance cases by the subtype classification.

</td></tr><tr><td>

Configuration Compliance

</td><td>

-   **[Test result and remediation task state transitions](https://www.servicenow.com/docs/access?context=spc-findings-state-transition&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Enhancements to policy audits for Security Posture Control verify that retired assets are not evaluated by activated policies. If the state of an asset transitions from **Retired** back to **Active**, it is included in the next policy evaluation.

-   **[Non-zero risk score for passed test results](https://www.servicenow.com/docs/access?context=config-compliance-risk-calculator-example&version=xanadu&pubname=xanadu-security-management&section=cc-rollupcalc-example&ft:locale=en-US)**

The risk score is calculated for passed test results to determine how much risk is mitigated.

-   **[Deprecated the privilege to delete a test result for the Admin role](https://www.servicenow.com/docs/access?context=installed-with-config-compliance&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

As an admin with the sn\_vulc.admin role, you can’t delete a test result. This privilege is now given to the sn\_vulc.delete granular role.


-   **[Updates to the Risk Score calculation for a Remediation Task](https://www.servicenow.com/docs/access?context=v11create-rollup-calc&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The average risk score of all the test results in a Remediation Task is considered for the risk score calculation of a Remediation task.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[Access changes for the sn\_cmdb\_editor and sn\_cmdb\_admin user roles](https://www.servicenow.com/docs/access?context=installed-with-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   Starting with Xanadu Patch 9 \(zbooted or upgraded\), access has been reduced for the sn\_cmdb\_editor \(CMDB Editor\) and the sn\_cmdb\_admin \(CMDB Admin\) user roles which are used in [CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). The sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Xanadu Patch 10 \(zbooted or upgraded\), you must manually run the scheduled job '**Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the permissions that are necessary for performing some CMDB Workspace tasks.

This scheduled job modifies user roles as follows:

        -   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
        -   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the 'Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles' scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).
-   **[CMDB Health](https://www.servicenow.com/docs/access?context=c_CMDBHealth&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   Configuring and using CMDB Health is simplified by the removal of some concepts such as overall health scores.
    -   Sections on the CMDB Health Dashboard reporting on compliant CIs are clearly separated from report sections for non-compliant CIs that require your attention.
    -   Failure thresholds for KPIs and metrics enforce an upper limit of 100,000 to avoid excessive processing when a large number of CIs fail the specified metric tests.
    -   The CMDB Health Dashboard still shows non-compliance data that was gathered even if the process is stopped due to excessive failures so you can fix the specific failures already detected.
    -   CI health reporting is integrated into CI forms in CMDB Workspace.
-   **[CMDB Workspace store app](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   [CMDB 360](https://www.servicenow.com/docs/access?context=cmdb360-exp-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US):
        -   Manage performance by filtering the data included in Coverage charts in the CMDB 360 dashboard in CMDB Workspace by principal class setting or by whether tables are within the CMDB hierarchy.
        -   Manage the scope of data processed by CMDB 360 by setting a maximum threshold for the number of multisource records per class and tracking those classes that exceed that threshold in a table so that those classes are excluded from future CMDB 360 calculations. You can override this exclusion to include selected classes even if they exceed the threshold.
    -   [Data Certification](https://www.servicenow.com/docs/access?context=data-cert-exp-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

When reviewing Data Certification tasks in CMDB Workspace, use a single click to select all the records associated with a task, to certify or fail the certification in bulk.

    -   [CI timeline in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

When a CI timeline on the CI details pane in CMDB Workspace fails to load, the error message that appears now includes a link that you can select to go to the CI timeline in the base system.

-   **[CSDM and the CMDB Data Foundations Dashboards](https://www.servicenow.com/docs/access?context=csdm-cmdb-foundations-dashboards&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   Limit the performance impact of some of the CMDB and CSDM metrics such as the **CIs Processed via IRE** and **Business Application with Application Service Relationship** by adjusting the settings for triggering the system to automatically deactivate those metrics.
    -   Identify current and non-current metric data by viewing the **Updated** column in the list views of CMDB.
    -   Access the CSDM Data Foundations dashboard from the [Management view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-mangmnt-view&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   **[Select a parent class in an IRE identification rule](https://www.servicenow.com/docs/access?context=t_CreateCIIdentificationRule&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Avoid the unnecessary creation of a duplicate CI by setting the **Search On Table** field in an identification rule to one of the parent classes of the current class. When Identification and Reconciliation \(IRE\) identifies a CI in a parent class that matches a CI in the payload, IRE updates that CI with the details from the payload without creating a duplicate CI.

-   **[Improved migration and ongoing sync of CSDM life-cycle data](https://www.servicenow.com/docs/access?context=csdm-life-cycle-standard-values&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

The one-time operation aligns CSDM life-cycle values in asset and CI tables. After the initial alignment, business rules can run on regular schedules to ensure that life-cycle values for the asset, CI, and IBI tables remain aligned. Using standard life-cycle values significantly improves data accuracy to help optimize value for many ServiceNow AI Platform applications.

-   **[Application Services dashboard](https://www.servicenow.com/docs/access?context=app-service-dashboard&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Internal queries on the Application Services dashboard that filters for application services now checks not only for all the records in the Application Service \[cmdb\_ci\_service\_auto\] class, but for those records in which the value of **Service classification** is **Application Service**.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **[Deprecated the privilege to delete a container vulnerable item for the Admin role](https://www.servicenow.com/docs/access?context=installed-with-cvr-data&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

As an admin with the sn\_vul.vulnerability\_admin role, you can't delete a container vulnerable item. This privilege is now given to the sn\_vul.delete granular role.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[Role changes for Continuous Authorization and Monitoring Workspace users](https://www.servicenow.com/docs/access?context=cam-roles-list&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Reader \(sn\_irm\_cont\_auth.reader\), Authorization Official \(sn\_irm\_cont\_auth.authorization\_official\), and Executive Reader \(sn\_irm\_cont\_auth.executive\_read\) can now access Continuous Authorization and Monitoring Workspace.

-   **[OSCAL Catalog model export](https://www.servicenow.com/docs/access?context=oscal-support-cam&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

In exporting the control-related information as part of the Catalog model, the child control objectives of a control objective are mapped to the Control field. Furthermore, related control objectives of the control objective are mapped to the Links field.

-   **[Enhancements in CAM Workspace](https://www.servicenow.com/docs/access?context=cam-ws-home-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

The following enhancements have been made in CAM Workspace:

    -   New pop-ups with additional capabilities are added to the hybrid controls creation.
    -   POA&amp;Ms include all authorization package issues.
    -   The **Family** field and **Family ID** field are added to the Control objective page.
    -   The **Notes** field and **Attachment** field are added to the Assessment procedure page.
    -   The **360° View** button is configured in all pages of CAM Workspace.
-   **[CAM user role changes](https://www.servicenow.com/docs/access?context=assign-cam-roles&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Defining roles and assigning privileges and permissions for approvals is critical to ensure security in the CAM application. The user role changes are:

    -   The Information Owner \(sn\_irm\_cont\_auth.information\_owner\) role can also update information types of an authorization package, and the role also contains the Audit user \(sn\_audit.user\) role in addition to the Reader \(sn\_irm\_cont\_auth.reader\) role.
    -   The Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\) role can update the authorization package, and the role contains the Compliance user \(sn\_compliance.user\) and Reader \(sn\_irm\_cont\_auth.reader\) roles.
    -   The Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\) role can update the authorization package.
    -   The Reader \(sn\_irm\_cont\_auth.reader\) role contains the Audit reader \(sn\_audit.reader\) role.
    -   The System User \(sn\_irm\_cont\_auth.system\_user\) role contains the Audit user \(sn\_audit.user\) role.
    -   The System Owner \(sn\_irm\_cont\_auth.system\_owner\) role also contains the Audit user \(sn\_audit.user\) and Compliance user \(sn\_compliance.user\) roles.

</td></tr><tr><td>

Core ServiceNow AI Platform

</td><td>

-   **[TinyMCE upgrade](https://www.servicenow.com/docs/access?context=c_UseHTMLFields&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The HTML editor field now uses upgraded version of TinyMCE. TinyMCE has been upgraded from v4 to v6.8.2. This upgrade provides enhanced table functions as well as enhanced formatting and editing features like accordion, addition of custom styles through dictionary attributes, enable/disable text menubar, enhanced power paste. These enhancements enable users to format content to better suit their needs. Add the supported plugins to the system property **glide.ui.html.editor.enabled\_plugins​** and add the supported toolbar options to the system property **glide.ui.html.editor.toolbar** to configure the editor according to your needs. The upgrade includes changes in plugin names, toolbar names and new system properties to support configurations for the new version.

-   **[Business calendar enhancements](https://www.servicenow.com/docs/access?context=define-business-calendar-entries&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Business calendar enhancements include the ability to create business calendar spans and their names \(accessible across both global and scoped applications\), add a new calendar field called **Calendar type**, and differentiate more easily between similar calendar names.

-   **[Send REST Request - Inbound test step supports mutual authentication](https://www.servicenow.com/docs/access?context=test-steps-rest-category&version=xanadu&pubname=xanadu-application-development&section=atf-send-rest-request-inbound&ft:locale=en-US)**

Use mutual authentication with the **Send REST Request - Inbound** test step by selecting an X.509 certificate.

-   **[Apply ACLs to GraphQL API paths](https://www.servicenow.com/docs/access?context=build-graphql-scripted-schema&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)**

Specify which level of a GraphQL API to apply ACLs to with the **Path ACL Depth** field.

-   **[REST and SOAP API analytics dashboards migrated to Platform Analytics experience](https://www.servicenow.com/docs/access?context=c_APIAnalyticsReports&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)**

The REST and SOAP API analytics dashboards have been migrated from Core UI to the Platform Analytics experience. Access the dashboards from **All** &gt; **System Web Services** &gt; **Analytics Usage Overview**. After upgrading, the Core UI dashboards are still available from **All** &gt; **System Web Services**.

-   **[Control access for HTTP headers in CORS requests](https://www.servicenow.com/docs/access?context=t_DefineACORSRule&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)**

Configure whether to allow credentials in requests with the **Access-Control-Allow-Credentials** field and which HTTP headers to allow in requests with the **Access-Control-Allow-Headers** field.

-   **[Deactivate CORS rules](https://www.servicenow.com/docs/access?context=t_DefineACORSRule&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)**

Turn a CORS rule \[sys\_cors\_rule\] on or off with the **Active** field.

-   **[Rhino update for the JavaScript engine on the platform](https://www.servicenow.com/docs/access?context=c_JS_engine_upgrade&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)**

Rhino was updated to improve the performance of the JavaScript engine on the platform.

-   **[Web requests from integration users update the Last login and Last login time fields on user records](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

By default, the Last login and Last login time fields in a user record \[sys\_user\] are updated when an integration user sends a web request to an instance. To turn off this functionality, set both the **glide.basicauth.update\_last\_login\_time** and the **glide.oauth.update\_last\_login\_time** system properties to false.


</td></tr><tr><td>

Creator Studio

</td><td>

-   **[Better performance for reference-based form questions](https://www.servicenow.com/docs/access?context=creator-studio-form-elements-ref&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

The selection of a table for reference-based form questions has been improved. For example **Record choices** or **Multi-select** questions.


</td></tr><tr><td>

Data Privacy

</td><td>

-   **[Discover and anonymize journal fields](https://www.servicenow.com/docs/access?context=classifying-data&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Journal fields are now supported for Data Discovery and Data Anonymization with Workspace UI.

-   **[Data pattern regular expression length increased](https://www.servicenow.com/docs/access?context=configure-data-discovery-patterns&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

The data pattern regular expression length limit is increased to 1000 characters.

-   **[New base system data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

New base system data patterns are supported. See [Default data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information.

-   **Indicators for Security Center dependencies**

Indicators for missing Security Center dependencies have been added.


</td></tr><tr><td>

Data management for CSM

</td><td>

-   **[Unparenting service organizations from a company](https://www.servicenow.com/docs/access?context=associate-company-with-bus-loc&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Enhanced the adoption of the service organization model to accommodate the various industry verticals, such as Healthcare and Life Sciences Service Management, Public Sector Digital Services, and Financial Services Operations, by unparenting the service organizations from the company table.

-   **[Field Service Management integration with Service Model Foundation](https://www.servicenow.com/docs/access?context=track-work-orders-on-the-blsp&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Enabled your location staff to track the work orders for their business locations by using the business location service portal \(BLSP\).

-   **[Data model for sold products](https://www.servicenow.com/docs/access?context=create-sold-item&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**
    -   You can now view the Provider Service Organization information that has sold a product or service to the customer on the Sold Product form.
    -   You can now use the **Product Location** and **Product Specification** fields on the Sold Product table \(sn\_install\_base\_sold\_product\) to capture information about the location of the sold product and the sold product that is associated with an offer.
-   **[Product Instance directive for Install Base Management](https://www.servicenow.com/docs/access?context=create-a-sync-between-an-install-base-class-and-asset-class&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Synchronized the changes between the asset and corresponding install base hierarchy with the extended product instance hierarchy.

-   **[Customer Life Cycle Management Workflows](https://www.servicenow.com/docs/access?context=customer-life-cycle-management-workflows&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

You can now select multiple sold products at the same time to trigger the **Suspend**, **Resume**, and **Disconnect** flows to update the existing root sold products and their services.


-   **[Compose Sales and Order Management workflows](https://www.servicenow.com/docs/access?context=compose_sales_and_order_management_workflows&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

You can now use the sales and order management API to support use cases for order reconfiguration. To learn more about reconfiguration, see [LeadtoCashCore - Scoped](https://www.servicenow.com/docs/access?context=LeadToCashCoreAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).


-   ****
    -   Perform **Modify**, **Suspend**, **Resume**, and **Disconnect** actions on product inventory records from the Product Inventories related list.

**Note:** The Product Inventories related list is available only from the Yokohama release. If you're using the Washington or Xanadu versions, you can manually add the related list.

To retain both the Product Inventory and Sold product related lists, filter out the product inventory records from the sold product list. Use the product inventories related list to perform the MACD actions.


-   **Sales and Order Management Request tracker**
    -   Monitor the status of sales and order management workflows and enable agents to track the status of synchronous and asynchronous flows.
    -   Use the enhances inbound Queue to view detailed request information for the sales and order management workflows and improve user experience.

</td></tr><tr><td>

Decision tables in Workflow Studio

</td><td>

-   **Theme updates**

Some details in the decision table UI have been updated to follow standard ServiceNow AI Platform themes.

-   **Usability enhancement for scrolling within decision tables**

In large decision tables, scroll within the table to see more rows. Note that the headers stay at the top of the table.


</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

DevOps Change Configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [Accessibility information](rn-summary-changes.md#devops-rn-accessibility) section that follows.

-   **[DevOps data in change request](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

View, add, and edit DevOps data in a manually created change request in Service Operations Workspace for a unified change request experience in both DevOps Change Workspace and Service Operations Workspace.

-   **[Enhancements to DevOps Model change](https://www.servicenow.com/docs/access?context=devops-change-multimodel&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   In-product guidance enables you to leverage DevOps models and easily create DevOps changes without disruption of your change process.
    -   To make the Change - DevOps – Implement flow of the DevOps model more suitable for DevOps changes, change tasks are no longer automatically created.
    -   The new Change – DevOps – Update execution state flow in the DevOps model means you no longer have to activate the DevOps Change Request Manual Approval flow to send a callback to the third-party orchestration tool.
    -   Fast-track your change process by using a new DevOps Simplified change model, which doesn’t contain the Assess state. Change approval for this model is based on the DevOps Simplified Model Change policy.
-   **[Branch details for artifacts and packages](https://www.servicenow.com/docs/access?context=using-dev-ops-release-change&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Branch details from pipeline executions are now available for artifacts and packages for better tracking.

-   **[Create lists](https://www.servicenow.com/docs/access?context=add-new-list-in-list-module&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Option to create customized lists added to the Changes, Tools, and Administration modules in the DevOps Change Workspace.

-   **[Jira Server connection using API key](https://www.servicenow.com/docs/access?context=create-jira-tool-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Connect to your Jira Server using API key authentication rather than basic authentication.

-   **[GitHub Actions reruns](https://www.servicenow.com/docs/access?context=github-actions-integration-with-devops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Re-running failed GitHub jobs will now use the existing change request created for the failed jobs instead of creating new change requests.

-   **[Generalized Docker Container solution to support any orchestration tool](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Use the generalized and extensible Docker Container solution to integrate any orchestration tool with DevOps Change Velocity for invoking pipeline actions like change request creation and collecting relevant DevOps data without having to rely on tool specific plugins or extensions.

-   **[Simplified onboarding of planning tools that are not supported in the base system](https://www.servicenow.com/docs/access?context=onboard-gitlab-to-devops-change-velocity-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Integrate planning tools that are not supported in the base system by leveraging transformer rules. GitLab Issues is now available as one of the planning tools and is built leveraging this new approach so you can discover plans, import work items, and configure webhooks for work items \(issues\) in GitLab.

-   **[Enhanced manual DevOps change creation experience](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Add work items data in a manually created DevOps change request in  Service Operations Workspace  for  ITSM.

-   **[Default BitBucket branch property](https://www.servicenow.com/docs/access?context=dev-ops-administration&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Specify the default Bitbucket branch name that must be used to create an import request in the **sn\_devops.bitbucket\_default\_branch** property.

-   **[Additional scans for DevOps Health Scan Content pack](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with identifying configuration issues like plugin and version incompatibilities, or pipelines that chronically fail, have been added.

-   **[Import pull-request records for Bitbucket Server or Bitbucket Data Center](https://www.servicenow.com/docs/access?context=devops-wkspc-bitbucket-tool-conn&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Import pull-request records for Bitbucket Server or Data Center for improved insights and efficiency.

-   **[Change request creation with errors in DevOps data retrieval for Harness pipelines](https://www.servicenow.com/docs/access?context=change-request-creation-with-devops-data-retrieval-errors&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Enable change request creation even if there is an error in retrieving the DevOps data for a Harness pipeline.

-   **[Branch name filter](https://www.servicenow.com/docs/access?context=create-devops-change-request-manual&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Search for build numbers by the branch name while associating DevOps data to a change request in the Service Operations Workspace \(SOW\) or Classic UI.

-   **[Test summary name in GitHub Actions](https://www.servicenow.com/docs/access?context=servicenow-devops-custom-actions-from-github-marketplace&version=xanadu&pubname=xanadu-it-service-management&section=servicenow-devops-test-report-custom-action&ft:locale=en-US)**

The servicenow-devops-test-report custom action in GitHub now includes an optional test-summary-name parameter to specify the test summary results name.

-   **[Token based authentication for Rally](https://www.servicenow.com/docs/access?context=configure-webhooks-for-rally-manually&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Configure webhooks for Rally using token based authentication instead of using the integration username and password.

-   **[Renamed variables for Docker](https://www.servicenow.com/docs/access?context=servicenow-custom-actions-for-gitlab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The environmental variables in the Generic Docker actions for DevOps Change Velocity have been renamed by removing the CI prefix for better clarity.

-   **[Security scan results](https://www.servicenow.com/docs/access?context=dev-ops-change-acceleration&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Security scan results on the change record associated to a pipeline execution with a linked package are now displayed in the **Security Summaries** tab.

-   **[Source of commits in SOW](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

View the source of commits like pipeline execution, branch, repository, and so on for a change request in the DevOps data section of the Service Operations Workspace.

-   **[Track file changes](https://www.servicenow.com/docs/access?context=sc-github&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The **Track file changes** option is now disabled by default when a repository is configured to prevent any potential security risks.

-   **[Close code value for a change request](https://www.servicenow.com/docs/access?context=dev-ops-administration&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Two new properties have been added in DevOps Change Velocity, so that you can specify a close code value for a change request based on the change request completion state when the autoCloseChange parameter is enabled.

-   **[Support for MID Server cluster](https://www.servicenow.com/docs/access?context=playbook-enter-github-instance-details&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Improve load balancing and failover protection by selecting a MID Server cluster when connecting to a tool instance associated with a MID Server cluster. This configuration enables multiple MID Servers with relevant capabilities to be grouped.

-   **[Improved UX for DevOps Change health scans](https://www.servicenow.com/docs/access?context=run-health-scan-check&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Run health scans and analyze findings efficiently in the DevOps Change workspace with an intuitive and user-friendly interface.

-   **[Pipeline association for GitHub Actions](https://www.servicenow.com/docs/access?context=sc-github&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

When onboarding GitHub Actions pipelines through the App onboarding catalog or the onboarding APIs, now only the selected pipelines are associated with the DevOps app. If no pipeline is selected, all pipelines within the specified repository are associated.

-   **[Tool connection check status](https://www.servicenow.com/docs/access?context=devops-reference-error-messages&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

If a tool is marked as Disconnected because of a system-generated failure during an unsuccessful connection check, any subsequent successful check automatically updates the connection status to Connected. If you manually disconnect the tool, the tool status remains Disconnected even if there’s a subsequent successful connection check.

-   **[New roles for vulnerability integration](https://www.servicenow.com/docs/access?context=installed-with-dev-ops&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
    -   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.

</td></tr><tr><td>

Digital Portfolio Management

</td><td>

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

The Digital Portfolio Management configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For information about how to upgrade, see the [rn-summary-changes.md\#digital-portfolio-management-rn-accessibility](rn-summary-changes.md#digital-portfolio-management-rn-accessibility) that follows.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **[Updated references from questionnaire tables to intake tables in Card Operations](https://www.servicenow.com/docs/access?context=components-installed-with-dispute-rules-content-pack-for-mastercard&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Updated references from the old questionnaire tables to the new intake tables in Card Operations.


</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

-   **[Questionnaire and chargeback eligibility ruless](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Added new chargeback eligibility rules to reflect the latest dispute conditions from Visa.
    -   Updated the dispute questionnaire to support the following reason codes:
        -   10.3 \(Other fraud—card-present environment\)
        -   13.1 \(Merchandise/services not received\)
        -   13.5 \(Misrepresentation\)
-   **[Visa Resolve Online \(VROL\) 24.2 revision Alignment](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Updated chargeback reason codes and dispute questionnaire with VROL's latest release revision 24.2.
    -   Updated 12.1 chargeback rules to 11.3.
-   **[Visa Resolve Online \(VROL\) 25.2 revision Alignment](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

The chargeback eligibility rule under the 12.6 reason code that validates **Is the other transaction paid by other means? == N** has been removed,

-   **[Updated references in Card Operations tables](https://www.servicenow.com/docs/access?context=components-installed-with-dispute-rules-content-pack-for-visa&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Updated references from the old questionnaire tables to the new intake tables in Card Operations.

-   **[Updated data model](https://www.servicenow.com/docs/access?context=dispute-data-model&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**
    -   Enhanced Dispute Rules Content Pack for Visa to support the updated chargeback eligibility conditions and the fields used for validating disputed transactions.
    -   Moved the following tables as generic intake tables, from Dispute Rules Content Pack for Visa \[sn\_bom\_visa\_cp\] to Financial Services Card Operations \[sn\_bom\_credit\_card\]:
        -   Visa Dispute Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\] → Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
        -   Visa Dispute Cardholder Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_cardholder\_intake\] → Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

**Note:** These tables have been moved only for new customers, but they are still available in the Dispute Rules Content Pack for Visa for existing customers.


</td></tr><tr><td>

Document Services

</td><td>

-   **[Google Docs files on Google Drive](https://www.servicenow.com/docs/access?context=google-drive-spoke-document-services&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Manage Google Docs files on Google Drive using Multi Provider Document Services Framework.

-   **[Document viewer support for hyperlinks, attachments, and digital signature](https://www.servicenow.com/docs/access?context=Documentviewer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Document Viewer now supports using hyperlinks, downloading of PDF attachments, and viewing of digital signatures.

-   **[Accessibility feature for DOCX to PDF conversion](https://www.servicenow.com/docs/access?context=enable-accessibility-docx-to-pdf&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Accessibility support added for DOCX to PDF conversion. PDF accessibility tags are now available to help non-sighted users who rely on screen readers to navigate, understand, and interact with converted PDF documents.


</td></tr><tr><td>

Dynamic Translation

</td><td>

-   **[Character maximum has increased for MS translation requests](https://www.servicenow.com/docs/access?context=limitations-dynamic-translation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

For users of the Microsoft Azure Translator service: the maximum character limit for a translation request has increased to 50,000. The maximum character limit for a detection request remains 50,000.


</td></tr><tr><td>

Employee Center

</td><td>

-   **[Content Analytics](https://www.servicenow.com/docs/access?context=ecpro-content-automation-analytics&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Content Analytics is now part of the Platform Analytics Experience. When you navigate to **All** &gt; **Content Analytics** &gt; **Dashboards**, the Content Analytics dashboards are displayed alongside Platform Analytics dashboards.

-   **[Experience and Service Feedback](https://www.servicenow.com/docs/access?context=ex-fdback-ovrvw&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Access the following enhancements within the feedback functionality:

    -   Leverage three different types of feedback - Experience, Service, and Survey feedback to gain more insight from your users.
    -   Integrate the experience feedback response with the Success Dashboard indicators.
    -   Configure service feedback to keep it anonymous after feedback is submitted.
    -   Access Experience and Service Feedback in Virtual Agent assist.
-   **[SharePoint Online Search Connector](https://www.servicenow.com/docs/access?context=sharepoint-search-overview&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

Enhance your Microsoft SharePoint experience with the following upgrades:

    -   Streamline the site permissions and other granular access controls.
    -   Grant permission and provide access to specific personas.

</td></tr><tr><td>

Encryption Key Management

</td><td>

-   **[Changes to Code Signing requirements](https://www.servicenow.com/docs/access?context=code-signing-landing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

As a part of improving security around Root of Trust, signing of script and attachments records can only be done on your trusted non-production instance or using the standalone signing tool. The exception is notarization, which can still be performed in the protected production instance.

-   **[Enhancement requests for the Code Signing Standalone signing tool](https://www.servicenow.com/docs/access?context=sa-code-signing-tool&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Updates to Code Signing enable your administrators to work with keystores, signature records, and records to be signed outside of the local system.

-   **[Improved activation process for Code Signing](https://www.servicenow.com/docs/access?context=config-code-signing&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Activate Code signing with a new UI page that is designed to streamline the activation process.

-   **[Download All Button for Multiple Attachments is available when Edge Encryption is enabled](https://www.servicenow.com/docs/access?context=c_EdgeEncryptionOverview&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

By using the download all functionality, you can now download multiple documents into a zip file when you also enable Edge Encryption.

-   **[Edge Encryption jRobin dashboards have been migrated to NEXT Experience](https://www.servicenow.com/docs/access?context=code-signing-reference&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

View troubleshooting and performance on dashboards that were migrated from the deprecated jRobin framework. These dashboards display the same information that was available in previous versions.

-   **[Column Level Encryption Enterprise is installable by administrators after purchase](https://www.servicenow.com/docs/access?context=activate-platform-encryption&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

After purchasing Column Level Encryption Enterprise, your administrator can typically activate the product without needing technical assistance.

-   **[Support for full string UTF-8 in Column Level Encryption](https://www.servicenow.com/docs/access?context=set-encrypted-field-config&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

CLE supports encryption and decryption of the full range of UTF-8 characters, including emoji.

-   **[Improved readability for Column Level Encryption logging](https://www.servicenow.com/docs/access?context=code-signing-reference&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

With the improved system, node, application, and audit logging, your administrators can analyze and troubleshoot their CLE or CLEE implementation.


</td></tr><tr><td>

Event Management

</td><td>

-   **[Alert page performance enhancements](https://www.servicenow.com/docs/access?context=c_EMAlert&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Benefit from the enhanced load time of the alert forms and service dashboard.

-   **[Calculate impact during loop dependency](https://www.servicenow.com/docs/access?context=cross-business-service-impact&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Support for circular \(loop\) dependency between configuration items in the impact tree is enabled.

-   **[Automated alert groups perform tag-based alert clustering](https://www.servicenow.com/docs/access?context=c_SACorrelatedAlertGroups&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Tag-based alert group correlation is performed as part of automated alert groups.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **Capacity and Reservations Management**

Capacity and Reservations Management data model has been changed to accommodate the agent's start and end location.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Dispatcher Workspace and Workforce Optimization for Field Service support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [rn-summary-changes.md\#field-service-management-rn-accessibility](rn-summary-changes.md#field-service-management-rn-accessibility) section that follows.

-   **Google Maps APIs for Field Service Capabilities**

Upgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.

You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.

If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.

For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Updated data model](https://www.servicenow.com/docs/access?context=installed-with-card-operations&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Introduced the following two new tables for questionnaire intake:

    -   Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
    -   Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

-   **[Updated Card disputes transaction table](https://www.servicenow.com/docs/access?context=installed-with-card-operations&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

Removed the following fields from the Card disputes case table:

    -   Account status as of transaction date
    -   Dispute amount modification reason
    -   Reason code
    -   Reason code message
    -   Suggested reason code

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=card-operations-reference&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)**

The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.


</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Updated the following subflows to align with Visa Resolve Online \(VROL\) release 25.1 revision changes:

    -   Submit dispute questionnaire
    -   Submit fraud report

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

-   **[Flow generation configures action and flow logic inputs](https://www.servicenow.com/docs/access?context=create-flow-now-assist&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

Use the Now Assist for Creator flow generation skill to create and configure a flow from text directions. Flow generation uses data pills to set input values for actions and flow logic.


</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Directions for generative AI updates for Generative AI Controller](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

The prompts, which are the instructions to the large language model \(LLM\), for all four capabilities \(Generic Prompt, Generate Content, Summarization, and Sentiment Analysis\), semantic filtering, and recursive summarization have been updated.


</td></tr><tr><td>

Goal Framework

</td><td>

-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**
    -   The following fields on the Target form have been renamed:
        -   **Review frequency** to **Check-in frequency**
        -   **Base value** to **Start value**
        -   **Target value** to **Final target value**
        -   **Actual value** to **Actuals to date**
        -   **Review due date** to **Check-in due date**
    -   The Fortnightly option in the **Check-in frequency** field is no longer supported.
-   **[Goal Framework tables](https://www.servicenow.com/docs/access?context=goal-framework&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

The maximum number of characters allowed in the **Name** field has been increased from 80 to 255 for the Strategic Plan \[sn\_gf\_strategic\_plan\], Strategic Priority \[sn\_gf\_strategy\], Goal \[sn\_gf\_goal\], and Target \[sn\_gf\_goal\_target\] tables.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

On the Target form, the **Breakdown interval** and **Cumulative target** fields have been removed, and the **Review frequency** field has been renamed to **Check-in frequency**.


</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

</td><td>

-   **[Workspace performance enhancements](https://www.servicenow.com/docs/access?context=hcls-using-workspace&version=xanadu&pubname=xanadu-healthcare-life-sciences&ft:locale=en-US)**

The Healthcare Workspace has received performance enhancements to optimize loading times.


</td></tr><tr><td>

Hermes Messaging Service

</td><td>

-   **[Monitor topics in multiple cluster sets](https://www.servicenow.com/docs/access?context=view-messages-hermes-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

View messages from multiple cluster sets by selecting a service group in the Hermes Topic Inspector module.

-   **[Test connectivity to multiple cluster sets](https://www.servicenow.com/docs/access?context=run-hermes-messaging-service-diagnostics&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Verify that your instance can send messages to and receive messages from multiple cluster sets by selecting a service group in the Hermes Diagnostics module.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **Alert automation enhancements**

In Group automation, in the Simulation section, **Re-run test** has been renamed **Re-run simulation**.

The **Active** toggle switch has been replaced with a check box.

-   **[Enrich automation](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

A new section, **And finally**, featured two radio buttons, **Run other enrich alert automations** and **Don't run other enrich alert automations**, which replace the previous **Continue running automations of this type** toggle switch. Although this section is new, the functionality is unchanged. Selecting **Run other enrich alert automations** continues running automations with the same filter conditions, while **Don't run other enrich alert automations** halts additional automations after execution except for those owned by other assignment groups.

-   **[Associate services to use in Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-add-service&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

System admins can select any supported service and associate it to use in Service Reliability Management regardless of the owner or support group configurations.


</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

-   **Enhanced [Cloud Services Catalog](https://www.servicenow.com/docs/access?context=csc-home&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) Cloud Services Catalog experience**

Improved the hierarchical structure of multiple repositories with the support of Terraform Connector IaC discovery capabilities.

Support for integration of Google Cloud Platform \(GCP\) with Terraform Open Source.


</td></tr><tr><td>

ITOM Optimization

</td><td>

-   **[Cloud Admin Portal](https://www.servicenow.com/docs/access?context=cloud-admin-portal&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

The Cloud Admin Portal link to the user portal now points to Employee Center if you have installed and set up the Cloud Services Catalog application.


</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **[Use the enhanced Shazzam probe to collect data](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-insights&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

View the extended data collected by the Shazzam probe in the Discovery Admin Workspace **Insights** tab.

-   **[Revised Service Mapping roles](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Gain improved visibility of ML-powered candidates in Service Mapping with updated roles:

    -   service\_mapping\_admin replaces sm\_admin.
    -   service\_mapping\_user replaces sm\_user.
-   **[Use the enhanced Discovery and Service Mapping Patterns for extended discovery](https://www.servicenow.com/docs/access?context=r_SupportedApplications&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Note the following new Pattern extensions and improvements:

    -   [Pure Storage FlashArray](https://www.servicenow.com/docs/access?context=flasharray-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
    -   [Azure SQL license information](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
    -   [Google Cloud Platform \(GCP\) resource inventory discovery](https://www.servicenow.com/docs/access?context=gcp-resource-inventory-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
-   **[Scale up your Azure change processing](https://www.servicenow.com/docs/access?context=azure-change-processing&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Update your CMDB in real time with your Azure cloud resource changes. After upgrading to the enhanced November 2024 Patterns \(1.21.0\) version, run an Azure cloud discovery on all service accounts to ensure receiving all updates.

-   **[Stay informed about Cloud Discovery patterns updates](https://www.servicenow.com/docs/access?context=r_SupportedApplications&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Download and use the Cloud Discovery patterns spreadsheet with the latest up-to-date information on Cloud Discovery patterns, including REST-API permissions.

-   **[Run top-down discovery using Service Mapping integrated with Agent Client Collector](https://www.servicenow.com/docs/access?context=service-mapping-with-acc&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

Top-down Service Mapping and Automated Service Suggestions are supported with Agent Client Collector.


</td></tr><tr><td>

Impact

</td><td>

-   **[Accelerator catalog](https://www.servicenow.com/docs/access?context=accelerator-catalog&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**
    -   Updates to the  Accelerator
    -   The UX \(User Experience\) Design: Employee Center Accelerator name is changed to [UX: Design for Employee Center](https://www.servicenow.com/docs/access?context=ux-design-employee-center&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   The User Experience Review: Employee Center Accelerator name is changed to [UX: Portal Experience Review](https://www.servicenow.com/docs/access?context=ux-review-employee-center&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
-   **[HealthScan definitions updates: November release](https://www.servicenow.com/docs/access?context=healthscan-definitions-nov-store&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**

Some definitions have been deprecated or enhanced to improve performance, reduce false positives, and meet the latest coding practices.

-   **Accelerators with minor updates to the descriptions**
    -   The [Center of Excellence &amp; Innovation Design](https://www.servicenow.com/docs/access?context=CoEI-design&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [TuneUp Your Hardware Asset Management](https://www.servicenow.com/docs/access?context=tuneup-hw-asset-management&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [TuneUp Your Software Asset Management](https://www.servicenow.com/docs/access?context=tuneup-sw-asset-mgmt&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [UX: Design for Employee Center](https://www.servicenow.com/docs/access?context=ux-design-employee-center&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [UX: Portal Experience Review](https://www.servicenow.com/docs/access?context=ux-review-employee-center&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
    -   [Jumpstart Your Strategic Portfolio Management – Planning Workspace](https://www.servicenow.com/docs/access?context=jumpstart-spm-planning-workspace&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)
-   **[Objectives and outcomes](https://www.servicenow.com/docs/access?context=value-blueprint&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**

Value Blueprint is renamed to Objectives and outcomes.​

-   **[HealthScan definitions updates: August release](https://www.servicenow.com/docs/access?context=healthscan-definitions-aug-store&version=xanadu&pubname=xanadu-impact&ft:locale=en-US)**

Some definitions have been deprecated or enhanced to improve performance, reduce false positives, and meet the latest coding practices.


</td></tr><tr><td>

Incident Management

</td><td>

-   **[Email notification link redirection behavior](https://www.servicenow.com/docs/access?context=t_ViewIncidentNotification&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

In email notifications, you can now decide where the links to an incident record are redirected. Instead of an incident record automatically opening in the classic UI16 interface in Incident Management, the incident record can be opened in SOW. The incident record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) system property is set to true.
    -   The user selecting the incident record link has the sn\_sow.sow\_user role.
The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

To ensure consistency, the email notification template is updated to send the notification from SOW in the same format as sent from classic UI16 interface. Also, the template theme is updated to match the Next Experience theme.


</td></tr><tr><td>

Integration Hub

</td><td>

-   **[External Triggers framework to use new features provided by Platform Security](https://www.servicenow.com/docs/access?context=set-up-external-webhook-endpoints&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Upgrade the existing external triggers framework to use new features like Hash-based and Token-based authentication profiles with access policies.


</td></tr><tr><td>

Intelligence for CSM

</td><td>

-   **[Guided Decisions - Question field updated to type HTML](https://www.servicenow.com/docs/access?context=guided-decision-tree-node-types&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

The **Question** field has been updated from type=string to type=HTML. When adding a question to a decision node, decision tree authors can include the text, formatted text, and images in the **Question** field.


</td></tr><tr><td>

Knowledge Management

</td><td>

-   **[Enable AI Search on the Knowledge Management Service Portal](https://www.servicenow.com/docs/access?context=knowledge-service-portal-searching&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Displays AI-powered search results for a selected article through AI Search.

-   **[Default advanced plugin installation](https://www.servicenow.com/docs/access?context=activate-knowledge-advanced-plugin&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Article versioning, article subscriptions, article templates, and an article quality index are available through the Knowledge Management advanced plugin, which is installed by default for new customers. If you are an existing customer, you have the option to activate it.


</td></tr><tr><td>

MID Server

</td><td>

-   **[MID Server log enhancement](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637658)**

MID Server supports log file compression. The new log file handler settings are available as MID Server properties on the instance. The compression mode is not enabled in the base system.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Now Assist for Virtual Agent enhancements](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Deliver direct, relevant, and conversational responses to questions using generative AI, including the ability to give feedback to messages generated by AI in Virtual Agent.

-   **[Now Assist in AI Search on Mobile](https://www.servicenow.com/docs/access?context=now-assist-mobile-search&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Provide AI-generated or AI-selected answers to user searches with the ability for users to provide feedback on the relevancy of the curated answers.

-   **[Two new button instances](https://www.servicenow.com/docs/access?context=sg-studio-button-instances&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**
    -   Provide users with an additional shortcut to items or actions in record screens with the top icon function button instance, providing support for the agent-to-agent mobile Sidebar experience.
    -   Add shortcuts to the Indoor Wayfinding experience with the custom map bottom drawer function button instance.
-   **[Mobile client scripting enhancements](https://www.servicenow.com/docs/access?context=config-autofil-inputs-nptfrmscrn&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Streamline input form screen completion with auto-filled inputs based on one or many user inputs.

-   **[Navigation bar enhancement](https://www.servicenow.com/docs/access?context=config-badge-counts-nav-bars&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Add badging capability to navigation bar tabs, which enables badging on any navigation tab icons.

-   **[Configure mobile apps to use device date/time formats](https://www.servicenow.com/docs/access?context=config-apps2use-devicedatetimeform&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Set the **useDeviceSettingsForDateTimeFormats** mobile property to `True` to configure the date/time fields in mobile apps to use the date/time format that is used on the mobile device. This feature is available on the 18.2.0 mobile client release version and later.

-   **[Hide the seconds display in date/time fields](https://www.servicenow.com/docs/access?context=hide-secs-mobcds-recscreen-actstrem&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Use mobile properties to hide the display of seconds in mobile cards, record screen details pages, or activity streams. This feature is available on the 18.2.0 mobile client release version and later.

-   **[Configure an external authentication browser for iOS apps](https://www.servicenow.com/docs/access?context=config-ext-auth-browser-ios&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Configure an external browser on iOS apps that are used during authentication so external URLs that are opened by the same browser type can maintain sessions and cookies. This feature is available on the 18.3.0 mobile client release version and later.

-   **[Search in a ServiceNow instance with Siri shortcuts](https://www.servicenow.com/docs/access?context=siri-shortcuts&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Configure your ServiceNow instance to enable Siri voice search in your mobile app on the instance using global search. This feature is available on the 18.4.0 mobile client release version and later.

-   **[Notification tab enhancements](https://www.servicenow.com/docs/access?context=sg-mobile-tab-bar&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**

Use the following enhancements added to the Notification tab within the navigation bar:

    -   Option to mark all notifications as read, providing the ability to manage your notification entries.
    -   Highlighted display of critical alerts in the notification area.
-   **[Mobile Publishing enhancements and changes](https://www.servicenow.com/docs/access?context=mobile-publishing&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US)**
    -   Auto-populate instance URLs when new branded app builds are requested and when existing branded apps are updated.
    -   Support for unlisted iOS branded apps.
    -   New requirement for iOS Microsoft Intune apps to be registered with Microsoft Entra ID \(formerly Azure AD\).
    -   Add deep links when you make new Android branded app requests for both private and public distribution.

</td></tr><tr><td>

Next Experience

</td><td>

-   **[Select a theme in Next Experience](https://www.servicenow.com/docs/access?context=select-a-theme-in-next-experience&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

If multiple core themes have been created using Theme Builder, then those themes and their alternate color palettes are displayed in the Theme user preference group.


</td></tr><tr><td>

Next Experience Components

</td><td>

<table id="table_xfn_9mj_y5b"><thead><tr><th>

Component

</th><th>

Enhancements

</th></tr></thead><tbody><tr><td>

Appointment calendar

</td><td>

Reflow support in higher browser zoom levels of up to 400% in day and week view.

</td></tr><tr><td>

Badge

</td><td>

Option to enable partial number counts and additional characters, including the plus "+" symbol.

</td></tr><tr><td>

Breadcrumbs

</td><td>

Improved breadcrumb orientation experience with option to enable overflow menu.

</td></tr><tr><td>

Calendar

</td><td>

-   Extra content slot in the header to add buttons.
-   Column width control in the timeline view.

</td></tr><tr><td>

Checkbox

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Checklist

</td><td>

-   Additional configuration options like Disabled, Read Only, and Invalid.
-   Font size customization.
-   Option to configure mandatory field indicator.
-   Error notification appears when the user attempts to submit a form with an incomplete required field.

</td></tr><tr><td>

Contextual sidebar

</td><td>

Improved configuration with vertical tabs structure.

</td></tr><tr><td>

Date-time

</td><td>

-   Time zone displays for users.
-   Horizontal layout option for date-time input field.

</td></tr><tr><td>

Email composer

</td><td>

-   Improved draft management experience with email footer and side panel action buttons.
-   Improved drafting experience with larger compose area and enhancements to save vertical space.
-   Option to enable auto-load of most recent draft.
-   Option to suppress "Send email" button.
-   Support for international characters in email IDs.

</td></tr><tr><td>

Email composer \(mini\)

</td><td>

-   Improved draft management experience with email footer and side panel action buttons.
-   Improved drafting experience with larger compose area and enhancements to save vertical space.
-   Option to enable auto-load of most recent draft.
-   Option to suppress "Send email" button.
-   Support for international characters in email IDs.

</td></tr><tr><td>

Form

</td><td>

Support for 2 or more forms on a page. **Note:** If you want to add a form to a legacy page with an existing form, see the [Form UIB Setup documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-record-form-section-column-layout/uib-setu).

</td></tr><tr><td>

Highlighted value

</td><td>

Improved display of long text with text wrapping functionality.

</td></tr><tr><td>

Input

</td><td>

-   Customizable slot after the information button for inserting additional elements.
-   Added a caret slot that follows the user's text cursor.

</td></tr><tr><td>

Node map

</td><td>

In the hierarchical layout:-   Movable nodes in the map.
-   Customizable control panel.
-   Customizable node connections in new nodes.
-   Improved reflow in higher browser zoom levels.
-   Support for pausing node map layout refresh \(re-layout\).

</td></tr><tr><td>

Radio button

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Related items

</td><td>

-   Show or hide the heading.
-   Configure the background color.
-   Refresh a specific list along with all other lists in the container.

</td></tr><tr><td>

Select

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Text area

</td><td>

-   Customizable slot after the information button for inserting additional elements.
-   Added a caret slot that follows the user's text cursor.

</td></tr><tr><td>

Toggle

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Typeahead

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Typeahead multi

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr></tbody>
</table>

</td></tr><tr><td>

Notifications

</td><td>

-   **[New search and category filter in notification preferences](https://www.servicenow.com/docs/access?context=advanced-notification-prefrences&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Notification preferences now include the ability to search within custom notifications and filter by category in system notifications.

-   **[Email unsubscribe](https://www.servicenow.com/docs/access?context=email-unsubscribe&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Unsubscribe from emails using the unsubscribe capability in the email header.

-   **[Language preferences](https://www.servicenow.com/docs/access?context=multilingual-email-notifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

Honor sys\_user language preferences set by users for email translations.


</td></tr><tr><td>

Notify

</td><td>

-   **[Notify Twilio Direct driver](https://www.servicenow.com/docs/access?context=Notify-TwilioDirectDriver&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

When the Twilio messaging service is disconnected from a ServiceNow instance, you can choose to delete the messaging records according to your data management and security retention policies or retain the records for future reference. For more details, see the [Behaviour of Default Messaging Service when connecting to Twilio from ServiceNow instance \[KB1644265\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644265) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Now Assist

</td><td>

-   **[New conditions available in Define Availability step of guided setup for chat reply recommendation](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

When activating or editing the chat reply recommendation skill, you can now add conditions to determine who can use the skill.


-   **[__Get started__ step added to guided setup for resolution note generation](https://www.servicenow.com/docs/access?context=now-assist-rn-summarization&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

A step has been added to the guided setup for the resolution notes generation skill to remind you to update any customized code that is associated with the skill after a new release.


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

-   **[Enhancement in post-call summarization](https://www.servicenow.com/docs/access?context=summarize-a-call-by-using-now-assist-for-customer-service-management-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**
    -   You can now review a call that has been handed off from one live agent to another agent, and then provide a summary of the key topics that are covered during the conversation.
    -   Support for outbound calls from agents to the customers.
    -   Generate a call summary when the real-time transcript is not available.
-   **[Knowledge generation from multiple cases](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-csm-workspace&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

You can now select and gather insights and data from multiple similar cases to draft an article by using Now Assist for CSM.

-   **[Enhancements in chat summarization](https://www.servicenow.com/docs/access?context=now-assist-csm-summarize-chat&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Multiple Language Support via Digital technology \(DT\) support and a new step in the guided flow that allows the customization of how and when the skill capability will be available in the admin console.

-   **[Enhancements in Email recommendation](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Get recommendations for email responses when starting new emails, forwarding messages, or finalizing drafts. Help improve agent productivity by reducing the time taken to compose email and improve relevance of email reply recommendations. Also, get template recommendations while composing an email by leveraging AI search.

-   **[Enhancement in Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-csm-generate-resolution&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Generate resolution notes and then shorten or elaborate the content using the Now Assist context menu in the resolution notes field of the case form, in both Core UI \(UI16\) and Workspace.

-   **[Enhancements in Knowledge generation](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-csm-workspace&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

Revise the content in existing knowledge articles by using the Now Assist icon ![](../../common/image/icon-ai-sparkle.png), which is accessible as an inline capability, and create and refine knowledge articles. You can also generate knowledge articles in multiple languages.

-   **Xanadu Patch 7 Case summarization enhancement**

Extended the capabilities of the case summarization feature so it can now be used on custom tables.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

**Xanadu Patch 9**

-   **[System property to display knowledge article templates](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Display Knowledge article templates that you can use to create articles by using a system property. In earlier releases, the templates were displayed by default.

-   **[IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The Categorize incidents use case has been renamed to the Triage and categorize ITSM incidents agentic workflow.

The following AI agents have been added to the workflow:

    -   Link major incident AI agent
    -   Link incident to problem AI agent
The Incident categorize AI agent has been renamed to Categorize incident AI agent.

-   **[Xanadu Patch 3](../quality/xanadu-patch-3.md) [Resolution notes generation skill enhancements \(for upgrade customers\)](https://www.servicenow.com/docs/access?context=configure-now-assist-for-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Enhance your existing incident resolution notes generation skill to show the root cause and resolution steps taken. Enable this enhancement by using the toggle switch on the Configure response screen in the Now Assist Admin console.

**Note:** This option is available only when the incident resolution notes generation skill has been activated prior to upgrading.


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

-   **[Now Assist Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=now-assist-qna-genius-results&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The Now Assist Q&amp;A Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **[Now Assist Actions Genius Results](https://www.servicenow.com/docs/access?context=now-assist-catalog-ordering-gr&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The Now Assist Actions Genius Results feature is in maintenance mode. This feature will have no new enhancements but will have continued support. Similar and improved functionality is available in the newer Now Assist Multi-Content Response Genius Results feature. For more details on this feature, see [Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).


</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   **[Standard chat](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

The existing Now Assist in Virtual Agent LLM conversational behavior received a terminology update and is now referred to as standard chat.


</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   **[On-Call Scheduling new schedule engine](https://www.servicenow.com/docs/access?context=oncall-schedule-engine&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The new 2024 schedule engine offers a more efficient and improved experience for managing your schedules and shifts. On-Call Scheduling supports an automatic upgrade to the new schedule engine.

-   **[On-Call Scheduling new schedule engine](https://www.servicenow.com/docs/access?context=oncall-schedule-engine&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The new schedule engine introduces the following enhancement:

    -   Shift support to resolve gaps resulting from member placement.
    -   Resolve daily rotation gaps, caused by adding or removing members, holiday schedules, or extra time.
    -   Verifies user continuity based of the last on-call member from the previous schedule.
    -   Improved performance by reducing the time required to add, remove, or move members.

</td></tr><tr><td>

Operational Resilience

</td><td>

-   **[Reporting Operational vulnerability](https://www.servicenow.com/docs/access?context=reporting-operational-vul&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

The Operational vulnerability related list has been added to the following modules in the List view:

    -   Importance and impact tolerance assessment
    -   Scenario analyses
    -   Self attestations
    -   Services

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   **[ESG program manager role enhanced](https://www.servicenow.com/docs/access?context=components-installed-with-esg&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

The ESG program manager \(sn\_esg.program\_manager\) can now create, read, update, and delete emission factors.

-   **Changes in the metric tables**

Enhanced the following metric related tables with read access control lists \(ACLs\):

    -   Metric definition
    -   Metric
    -   Metric data
    -   Metric data task
    -   Metric data task url
With this change, the following changes are in effect:

    -   Metric level Approver user or Approver group: This means that the specified user or group designated as the approver can access only the particular metric and the tables specified for which they are the approver.
    -   Multi-level approval: This means that the specified user or group designated as the approver can access only those records in the metric related tables for which they are the approver.
    -   Enable enterprise owners to access metric records: This means that an enterprise owner can access any metric related record.

</td></tr><tr><td>

Operational Technology Change Management

</td><td>

-   **[Updated layout of the OT change record on the Industrial Workspace](https://www.servicenow.com/docs/access?context=create-ot-change-request&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The OT change record in the Industrial Workspace was updated so that all existing related lists are included under the **Related Records** tab.


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **[Updated layout of the OT incident record on the Industrial Workspace](https://www.servicenow.com/docs/access?context=report-ot-incident&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The OT incident record in the Industrial Workspace was updated to include all existing related lists under the **Related Records** tab.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[OT Devices tab data](https://www.servicenow.com/docs/access?context=ot-manager-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The following data available in the **OT Devices** tab of the OT Manager dashboard has been moved to the Operational Technology Visibility dashboard.

    -   New OT devices discovered
    -   Inactive OT devices
    -   OT Devices overview
        -   Total CMDB OT devices
        -   Unclassed OT devices
        -   Unassigned OT devices
        -   Unmapped OT devices
    -   OT devices by category
        -   Supervisory systems
        -   Control systems
        -   Field devices
        -   Computers and servers
        -   Network Gear
        -   Industrial IoT
    -   OT devices by Purdue level
    -   OT devices by type \(Top Level\)
    -   OT devices by manufacturer \(Top Level\)
    -   OT devices by criticality

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   **[OT Vulnerabilities tab data](https://www.servicenow.com/docs/access?context=operational-technology-vulnerability-response-dashboard&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The following data that was available in the **OT Vulnerabilities** tab of the OT Manager dashboard has been moved to the OTVR \(PA\) dashboard:

    -   Total OT Vulnerable Items
    -   New OT Vulnerable Items
    -   OT Unassigned Vulnerable Items
    -   OT Vulnerable Items by State
    -   OT Vulnerable Items by Risk Rating

</td></tr><tr><td>

Order Management

</td><td>

-   **[Add a sales agreement](https://www.servicenow.com/docs/access?context=som-add-sales-agreement-to-order&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

When an agent creates an order, the latest sales agreement associated with the account is automatically applied and the catalog is filtered to display the agreement's products and prices.

-   **[Update product locations at the order line level](https://www.servicenow.com/docs/access?context=order-mgt-copy-order-line-location&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Agents can create orders by location, which enables them to tailor orders for a customer location and streamline the ordering process by managing orders that have multiple locations.


</td></tr><tr><td>

Password Reset

</td><td>

-   **[Enhancing Password Reset Security URL](https://www.servicenow.com/docs/access?context=password-reset-global-properties&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

Control the expiration duration of a password reset URL by setting the `glide.pwd_reset.onetime.token.validity` property. By default, the URL is valid for one hour.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[Analysis cache for indicators on data visualizations](https://www.servicenow.com/docs/access?context=data-caching-pa&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

You can now cache indicator data as well as table data.

-   **[Prefetching cached data](https://www.servicenow.com/docs/access?context=data-caching-pa&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Cached data with an expiration time of 8 hours or more is refreshed automatically within the 30 minutes before it would expire. You therefore don't have to wait for the dashboard or visualization to load new data the first time you view it for the day.

-   **[Unloading Platform Analytics dashboards to update sets simplified](https://www.servicenow.com/docs/access?context=move-pae-db-with-update-set&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Unload Platform Analytics inline dashboards to update sets with one click.

-   **[Migration improvements](https://www.servicenow.com/docs/access?context=data-migration&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

Migration to the Platform Analytics Experience has added full migration of the following items in the Xanadu release:

    -   V1 Pivot reports and pivot reports with multiple columns
    -   Indicator scorecards with custom order and label names
    -   Top X elements for Performance Analytics widgets for time series breakdowns​
    -   Custom URL on-click behavior
    -   Act as filter capability
    -   Unconfigured reports, Performance Analytics widgets, and interactive filters: These objects are migrated to empty data visualizations and filter elements.
    -   Cascading filters
    -   Dashboard background colors
    -   Chart interactions: drilling down from chart to chart
-   **[Migration Center Improvements](https://www.servicenow.com/docs/access?context=data-migration&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**
    -   If you have migrated in an earlier version, previously unsupported visualizations are migrated on upgrade.
    -   Improved migration log UX.
-   **[Platform Analytics creation rights for specific scoped apps](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Using the ServiceNow AI Platform delegated development capability, a non-admin user can get the rights to create Platform Analytics objects for a specific scoped app.

-   **[Insights card grouping](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

When multiple insights of the same type are generated, they are aggregated into a single card.

Trend and target or threshold insights are also shown on a single card.

-   **[Insight notifications in data visualizations](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

If an insight is generated regarding the data source used in a data visualization, an alert appears in that visualization. This feature applies to data visualizations on both an in-line dashboard with insights activated and a UI Builder page.

-   **[Project does not need to be specified for process mining insights](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

If you have process mining insights activated, you no longer have to specify per dashboard which process mining projects to check for insights. All relevant projects are checked automatically.

-   **[Insight notifications in data visualizations](https://www.servicenow.com/docs/access?context=proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

If an insight is generated regarding the data source used in a data visualization, an alert appears in that visualization. This feature applies both to data visualizations on an in-line dashboard with insights activated and to individual data visualizations on a UI Builder page.

-   **[Auto sizing of single score visualizations](https://www.servicenow.com/docs/access?context=create-dv-sing-sc-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

The new Auto size option for single score visualizations fits the visualization dynamically into the available space, depending on targets or other information displayed in it.

-   **[Global filters apply to advanced dashboards](https://www.servicenow.com/docs/access?context=pass-global-filters-to-db&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

When opened, advanced dashboards are automatically filtered by the values of the global filter passed from the source page.

-   **[Saved data visualization on dashboard can be unlinked from library](https://www.servicenow.com/docs/access?context=editing-local-copy-saved-dv&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

If you have a shared data visualization on a dashboard that you can edit, you can unlink the local copy on the dashboard from the library and edit it without special roles and without impacting other dashboards.

-   **[Simple list follows filters](https://www.servicenow.com/docs/access?context=create-dv-simple-list-ac&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

A simple list on a dashboard can follow filters on that dashboard. You can also add borders to a simple list.


</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   **[Updated Roles](https://www.servicenow.com/docs/access?context=process-automation-designer-roles&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

The pd\_admin role is now playbook.admin.

-   **Activities trigger asynchronously**

To avoid slowing down the playbook runs, the first activities are triggered asynchronously.


</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Perform CRI tiering questionnaire to determine the tier value of entity](https://www.servicenow.com/docs/access?context=perform-cri-tier-pc-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

In addition to the Entity owner, the Corporate compliance manager \[sn\_compliance\_ws.corporate\_compliance\_manager\], Corporate compliance analyst \[sn\_compliance\_ws.corporate\_compliance\_analyst\], and IT compliance manager \[sn\_compliance\_ws.it\_compliance\_manager\] can trigger CRI tiering questionnaire and initiate CRI profile assessments.

    -   UI action button **Initiate CRI tiering assessment** has been renamed as **Initiate CRI tiering questionnaire**.
    -   UI action button **Initiate CRI assessment** has been renamed as **Initiate CRI profile assessment**.
-   **[Domain separation in GRC: Policy and Compliance Management](https://www.servicenow.com/docs/access?context=domain-separation-pol-comp&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Now both manually created records and auto-generated records created through scheduled jobs or scripts are domain separated based on their parent object or user domain for all Policy and Compliance Management objects.


</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), from Xanadu Patch 9.**

Five new advanced options are available for classification solutions, including new parameters and a new algorithm.

    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Customize training behavior by including a dictionary of parameters in the JSON format.

</td></tr><tr><td>

Problem Management

</td><td>

-   **[Re-assess a Problem Task from the Work in Progress state](https://www.servicenow.com/docs/access?context=assess-a-problem-task&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Additional flexibility for the workflow of a problem task analyst.

-   **[Email notification redirection behavior](https://www.servicenow.com/docs/access?context=configure-notifcations-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

When users select the problem record link in their email notifications, they can be redirected to the problem record in Service Operations Workspace instead of the classic UI16 experience. The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Known error articles available by default](https://www.servicenow.com/docs/access?context=create-known-error-from-problem&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Problem Knowledge Integration is activated by default for new customers.

-   **[Problem Management Migration Utility](https://www.servicenow.com/docs/access?context=migration-utility&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The Xanadu base problem files list is updated so the Problem Management Migration Utility can detect customizations.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Product catalog hierarchy visualization](https://www.servicenow.com/docs/access?context=som-catalog-hierarchy&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Toggle the view to show the specification hierarchy along with the offer hierarchy or show just the offer hierarchy using the Catalog Hierarchy tab for a product offering.

-   **Configuration UI changes**
    -   Sorting of product entities: Product catalog categories and categories are now displayed in alphabetic order. Characteristic options and child offers in the configuration UI are also displayed in alphabetical order, unless product catalog admins set a different display order when defining the associated product offerings.
    -   [Configurable products for sales agreements](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US): Agents can select from the different options for products and characteristics within a configurable bundle or product. These selections determine what product offerings are available as part of the sales agreement when creating orders from sales agreements.
    -   Improved the display and aggregation of alerts, error, and information messages in the Configuration UI to provide more context. Added visual indicators that indicate when a configuration is incomplete.
-   **[Configuration State Model API Framework enhancements](https://www.servicenow.com/docs/access?context=som-open-state-management-model&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Use the configuration state model to control various features in the product configurator. For example, you can define different default product configurations displayed to your agents, based on context, such as role or sales channel. You can also control the quantity values that agents can enter on a configuration node or optionally define info messages that are triggered for specific conditions that you set.


-   **Changing a published price list**

Starting with the Xanadu release, you can change only the **Description** and price list **End date** fields in a published price list. You can continue to add price list lines.

-   **[Copy a price list](https://www.servicenow.com/docs/access?context=copy-price-list&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Duplicate a published price list, its price list lines, and any related attribute adjustments and decision tables, without having to re-create the price list and its price list lines. For example, you can copy a published price list and its price list lines and use the price list copy for another account or location.

-   **[Cost book enhancements](https://www.servicenow.com/docs/access?context=pricing-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Create multiple cost books for a given currency and set a default cost book for a given currency. You can also do the following:

    -   [Copy a cost book](https://www.servicenow.com/docs/access?context=copy-cost-book&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).
    -   Manage the default cost books used and set cost book validation rules by using the [Cost Book Defaulting Matrix](https://www.servicenow.com/docs/access?context=som-control-default-costbook&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).
    -   Customize the default cost book logic called by other SOM applications by using the [DefaultCostBookExtensionPoint extension point](https://www.servicenow.com/docs/access?context=extension-points-som-pricing&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).
-   **[Matrix rule validations](https://www.servicenow.com/docs/access?context=configuring-rule-validations&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

Use predefined validation rules or create your own rules to validate the context variables, such as mandatory inputs, in pricing and product eligibility rule matrices. Each validation definition has a script that identifies the context variables to be validated and the corresponding error or warning messages that are displayed in the matrix decision table, depending on the validation results.

-   **Name change for Pricing Matrix Management application**

Starting with the Xanadu release, the Pricing Matrix Management application is renamed as the Product and Pricing Rules application \(sn\_csm\_price\_mtrx plugin\). The application includes the product catalog eligibility matrices introduced in this release as well as the pricing matrices.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Project Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

The new ServiceNow® Project Workspace application provides a more efficient, streamlined way for you to work. For information about how to upgrade, see [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US). Project Portfolio Management is still supported in this release.


</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Constituent Service Dashboard Migration to Platform Analytics](https://www.servicenow.com/docs/access?context=constituent-services-dashboard&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)**

The Constituent Service Dashboard has been migrated to Next Experience Platform Analytics. Next Experience is a ServiceNow AI Platform® feature that is active by default when the user loads or upgrades to the Xanadu release. The dashboard migration to Next Experience enables continuous visualization of historical and real-time process statistics in role-based dashboards, which enable individual stakeholders to make informed decisions. The new dashboard can be accessed by navigating to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

-   **[Enhancements to Social Benefits Playbook](https://www.servicenow.com/docs/access?context=psds-using-sb-playbooks&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)**

Use the enhanced Social Benefits Playbook to view an updated constituent card with more detailed information about the primary applicant. Cancel draft cases, bypass the initial eligibility screening, and skip playbook activities by using the updated process playbook in the Government Service Portal.


</td></tr><tr><td>

RPA Hub

</td><td>

-   **[Process job with no logs](https://www.servicenow.com/docs/access?context=rpa-studio-ui&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

In the RPA Desktop Design Studio, the following process job records aren’t displayed in the Attach log window:

    -   Process job records with no logs.
    -   Process job records that are stored in the robot machine.
-   **[Credential sets are replaced by credential groups](https://www.servicenow.com/docs/access?context=credential-management-rpa-hub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

In RPA Hub, the credential sets that were created for a bot process are now replaced with credential groups. You can now define the robot credentials, Time-based One-time Password \(TOTP\) authentication, and application credentials outside of the bot process and reuse them in multiple bot processes. By using credential groups, you don't have to create the same credentials for each bot process.

For upgrading customers, the existing credential sets and associated credentials are migrated seamlessly.

-   **[Changes in the Start Process UI action](https://www.servicenow.com/docs/access?context=start-bot-process&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

In RPA Hub, when you select the **Start Process** button, you can't view the robots that are in the **In Maintenance** life-cycle stage status.

When a bot process is either in the **In Maintenance** or **Build** life-cycle stage status and is using a robot pool, new robots aren’t deployed for dynamic allocation.

Dynamic allocation in the robot pool is only activated for published bot processes.

-   **[Changes in the Start Process action](https://www.servicenow.com/docs/access?context=rpa-hub-actions&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

When invoking the **Start Process** Workflow Studio action, the robots that are in the **In Maintenance** life-cycle stage status are treated as failed robots.

-   **[Changes in the Start Process subflow](https://www.servicenow.com/docs/access?context=rpa-hub-actions&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

If a process job isn’t in the **Running** status, the robot that is associated with the process job is treated as **Failed** in the **Start Process** subflow output.

-   **[Break component issue with loops](https://www.servicenow.com/docs/access?context=use-loop-break&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

An issue with the break components in the nested activities that failed to break their loops is now fixed. For more information, see [List of components compatible with latest version](https://www.servicenow.com/docs/access?context=list-components-upgrade&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **Microsoft Software Installer \(MSI\) compatibility**

Older MSIs that are related to Unattended Robot, Attended Robot, and RPA Desktop Design Studio from the RPA Hub store release versions 7.0.3 and 9.0.0 are compatible and can be used with the current store release version \(10.0.X\) of RPA Hub.

However, there are some limitations:

    -   Any new automation components available in the latest version aren’t available in the older versions. For example, the CreateFile component in the Zip category in version 10.0 doesn’t work in older versions.
    -   Components of the same name with different parameters aren’t backward compatible.
If robot machines are using older MSIs than the current version of the instance, any new features that are added in the later versions aren’t available for older MSIs. For example, the features released after version 7.0.3 don’t work in version 7.0.3 MSIs. Only those features that exist in version 7.0.3 work in that version.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **[Enhanced Task Management](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Enhanced the Task management feature to help the coordinator to change the ownership of change tasks and action tasks.

-   **[Next Experience Chat Collaboration and Discuss](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Enhanced the Next Experience Chat and Collaboration and Discuss feature.

-   **[Action Tasks](https://www.servicenow.com/docs/access?context=manage-reg-action-tasks&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Added action tasks that are segregated from the Regulatory Change Management or the Compliance Case Management application for differentiation and reporting in the **My Tasks** portal.


</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   **[Resource Management Workspace](https://www.servicenow.com/docs/access?context=rsrc-mgmt-wrkspc&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

The new Resource Management Workspace provides a more efficient, streamlined way for you to work. For information about how to upgrade, see [Resource Management Workspace](https://www.servicenow.com/docs/access?context=rsrc-mgmt-wrkspc&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US). [Resource Management classic](https://www.servicenow.com/docs/access?context=c_ResourceManagement&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) is still supported in this release.


</td></tr><tr><td>

Security Center

</td><td>

-   **[Scan checks](https://www.servicenow.com/docs/access?context=scan-checks&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Schedule security scans with the updated Auditor Suite to monitor access control configurations in the Security Scanner tool. The Auditor Scan suite has been streamlined to contain only access control checks and renamed to Access Control Auditor Suite. The updated access control checks generate a smaller, more focused number of findings that reflect potential security vulnerabilities according to ServiceNow security experts.

-   **[Legacy workflows have been converted to Flow Designer workflows](https://www.servicenow.com/docs/access?context=sec-center-v2&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Legacy base system Workflows have been converted to modern Flow Designer workflows to standardize ServiceNow flows onto the modern technology. The updated low-code flows are designed to be more scalable and make updating and troubleshooting easier.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Security Incident Response Orchestration](https://www.servicenow.com/docs/access?context=c_SecIncRespOrchestration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

<table id="table_ffd_4lh_fdc"><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[Security Incident Response Orchestration flows and actions](https://www.servicenow.com/docs/access?context=sec-inc-resp-orchestration-workflows&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Create Lookup Request for IoC Changes Flow](https://www.servicenow.com/docs/access?context=t_CreateScanRequestforIoCChanges&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Incident Response- Get Network Statistics Flow](https://www.servicenow.com/docs/access?context=obtain-network-statistics-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Incident Response - Get Running Services Flow](https://www.servicenow.com/docs/access?context=get-running-services-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

<table id="table_jr2_h4h_fdc"><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[Security Operations Integration- Block Request capability](https://www.servicenow.com/docs/access?context=block-request-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer flows in the following integrations:-   [Run Block Request](https://www.servicenow.com/docs/access?context=run-block-request&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations Integration - Block Request Flow](https://www.servicenow.com/docs/access?context=secops-integration-block-request-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Get Network Statistics capability](https://www.servicenow.com/docs/access?context=get-network-statistics-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Execution Tracking - Begin \(CIs\) Flow Action](https://www.servicenow.com/docs/access?context=execution-tracking-begins-cis-activity&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Incident Response- Get Network Statistics Flow](https://www.servicenow.com/docs/access?context=obtain-network-statistics-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Get Running Processes capability](https://www.servicenow.com/docs/access?context=get-running-processes-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Security Operations - Get Running Processes Flow](https://www.servicenow.com/docs/access?context=secops-integration-get-running-processes-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations Carbon Black Integration - Get Running Processes Flow](https://www.servicenow.com/docs/access?context=secops-integration-cb-get-running-processes-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Isolate Host capability](https://www.servicenow.com/docs/access?context=isolate-host-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Security Operations - Isolate Host Flow](https://www.servicenow.com/docs/access?context=secops-integration-isolate-host-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Run Isolate Host](https://www.servicenow.com/docs/access?context=run-isolate-host&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations Carbon Black Integration - Isolate Host Flow](https://www.servicenow.com/docs/access?context=secops-integration-cb-isolate-host-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Publish to Watchlist capability](https://www.servicenow.com/docs/access?context=pubish-to-watchlist-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following section:-   [Security Operations Integration - Publish to Watchlist Flow](https://www.servicenow.com/docs/access?context=secops-integration-publish-watchlist-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr><tr><td>

[Security Operations Integration- Sightings Search capability](https://www.servicenow.com/docs/access?context=sightings-search-capability&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following section:-   [Security Operations Integration - Sightings Search Flow](https://www.servicenow.com/docs/access?context=secops-integration-sightings-search-workflow&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Security Incident Response integrations](https://www.servicenow.com/docs/access?context=sir_integrations&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

<table id="table_wyv_zp3_fdc"><thead><tr><th>

Integration Name

</th><th>

Integration Changes

</th></tr></thead><tbody><tr><td>

[CrowdStrike Falcon Host integration](https://www.servicenow.com/docs/access?context=crowdstrike-falcon-host-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)

</td><td>

Workflow is migrated to the Flow Designer in following sections:-   [Get started with the CrowdStrike Falcon Host integration](https://www.servicenow.com/docs/access?context=activate-configure-crowdstrike-host&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Security Operations CrowdStrike Falcon Host - Publish to Watchlist Flow](https://www.servicenow.com/docs/access?context=secops-integration-crowdstrike-publish&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)


</td></tr></tbody>
</table>-   **[Review and assign your DLP incidents](https://www.servicenow.com/docs/access?context=using-dlp-ops-portal&version=xanadu&pubname=xanadu-security-management&section=review-and-assign-dlp-incidents&ft:locale=en-US)**

Providing a closure code when closing a DLP incident from the DLP IR analyst workspace is now mandatory.

-   **[DLP Incident Response Administration](https://www.servicenow.com/docs/access?context=data-loss-prevention-administration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

Adding users and groups is now accomplished through related lists rather than adding users from the respective configurations in the following Administration modules:

    -   DLP Default Configuration
    -   DLP Assignment Rules
    -   DLP Response Due Date Rules
    -   DLP Incident Assessment
    -   DLP User Instructions Templates
    -   DLP Record Level Restrictions
    -   DLP Field Level Restrictions
-   **[Install and configure the Netskope DLP integration for Data Loss Prevention](https://www.servicenow.com/docs/access?context=install-configure-netskope-dlp-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The Netskope integration now supports DLP incident ingestion.

-   **[Data Loss Prevention Incident Response Incident Management](https://www.servicenow.com/docs/access?context=data-loss-prevention-incident-management&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

View the forensic details of DLP Incidents in both the DLP IR Analyst workspace and DLP End user workspace.

-   **[Download evidence files](https://www.servicenow.com/docs/access?context=download-files-netskope&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The Netskope integration supports downloading the evidence file directly on demand.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Landing page configurations from Admin Center](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

All landing page configurations such as the landing page redirection, donut configurations, and so on are grouped under the **Landing Page Configurations** section of the **Configurations** tab.

-   **[Reordering of modules on the left navigation pane](https://www.servicenow.com/docs/access?context=reorder-left-navigation-pane-modules&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The left navigation pane modules, such as Inbox and Lists, are reordered for improved access to these modules.

-   **[Role to create a request from interaction and incident records](https://www.servicenow.com/docs/access?context=create-catalog-request-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

A user should now have either the itil role or sn\_request\_write role to create a request from interaction and incident records. Before Xanadu, users needed the interaction\_agent role to create the request.

-   **[DevOps data in change request](https://www.servicenow.com/docs/access?context=create-change-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**
    -   View, add, and edit DevOps data in a manually created change request in Service Operations Workspace for ITSM for a unified change request experience in the DevOps Change Workspace and Service Operations Workspace for ITSM.
    -   Starting in version 6.1, view, add, and edit work items data in a manually created DevOps change request in Service Operations Workspace for ITSM.
-   **[Creating change requests from problem records](https://www.servicenow.com/docs/access?context=work-on-problem-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

You can create additional change requests, because the action is no longer hidden after it has been used once.

-   **[Inline editing in the __Problem Tasks__ tab](https://www.servicenow.com/docs/access?context=lists-inline-edit&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Change a field in the problem tasks list instead of opening the record and changing it on the form.

-   **[Sidebar enhancements for incidents](https://www.servicenow.com/docs/access?context=using-sidebar&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

The sidebar will now display recommendations for users who can assist agents in resolving incidents or tasks. A standard set of recommendations are provided to enhance the support workflow.

ITSM Pro provides the customized recommendations using an AI-based algorithm, ensuring that the most appropriate users are suggested to assist with the task.

The group addition feature offers the ability to add entire groups to a conversation. By default, all members of a group will be included in the conversation. For groups with designated on-call members, only those members are added to the conversation, enabling for more focused and efficient communication.

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Service Operations Workspace for ITSM configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the Accessibility information section that follows.

-   **[Email notification redirection behavior in Problem Management](https://www.servicenow.com/docs/access?context=configure-notifcations-sow-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

When users select the problem record link in their email notifications, they can be redirected to the problem record in Service Operations Workspace instead of the classic UI16 experience. The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

-   **[Work notes in Compose section](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in version 6.1, the Work notes \(Private\) is displayed as default in the **Compose** section instead of the **Comments \(Customer visible\)** section for incident records.

-   **View the Close icon**

Starting in version 6.1, the “X” symbol of the Close icon is clearly visible on the SOW landing page.

-   **Complementary landmark for screen reader support**

Starting in version 6.1, the complementary landmark is available on the SOW landing page for the screen reader support.

-   **View the Problem and Change record information with incident granular roles**

Starting in version 6.1, when a user with incident granular roles \(sn\_incident\_read and sn\_incident\_write\) selects the preview info icon on the problem and change records from the related records section of the **Details** tab on an incident record, a pop up displays a message that they don’t have the permission to view the record.

-   **View impacted location for proposed major incident candidate**

Starting in version 6.1, you can view the impact locations for a proposed major incident candidate along with promoted major incident.

-   **Expansion of the compose section with activity stream**

Starting in version 6.1, when a file containing a lengthy name is attached to an incident record, and the activity stream is expanded to view the file name, the compose section also expands on the same level as the activity stream.

-   **Copy URL action for Incident list page**

Starting in version 6.1, you can copy and share the incident record on the Incident list page with the required stakeholders.

-   **Arrow orientation in record information panel**

Starting in version 6.1, the arrows next to the links in the Opened for card in the record information panel now point in the right direction, including for right-to-left languages.

-   **Access to form header links**

Starting in version 6.1, you can now select the form header links irrespective of the size of the browser.


</td></tr><tr><td>

Service Portal

</td><td>

-   **[Show the current user in the team members list of the User Profile widget](https://www.servicenow.com/docs/access?context=user-profile-widget&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Indicate whether to include the logged-in user in the team members list when viewing another team member's user profile from the User Profile widget.

-   **[Additional multi-factor authentication options](https://www.servicenow.com/docs/access?context=mfa-use&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

Log in to portals using a biometric authenticator or hardware security key with multi-factor authentication \(MFA\).


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Convert command uses module project type by default](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

The `projectType` parameter is set to `module` by default. By converting an application with the module project type, you can gradually migrate application metadata into ServiceNow Fluent code rather than converting all application metadata into code initially.


-   **[transpiledSourceDir parameter replaced with modulePaths parameter in now.config.json file](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US#application-structure)**

Use the `modulePaths` parameter in the `now.config.json` file for your application to map the source directory for modules to the output directory for modules instead of the deprecated `transpiledSourceDir` parameter. The `modulePaths` parameter is used to compile TypeScript source files into JavaScript modules.


-   **[Table API includes label object](https://www.servicenow.com/docs/access?context=table-api-now-ts&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Configure field labels \[sys\_documentation\] for tables and columns with the label object in the Table API.


-   **[Create and convert commands include template parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Specify whether to use JavaScript or TypeScript in modules with the `template` parameter on the `now-sdk create` and `now-sdk convert` commands. This parameter determines the configuration of the `package.json` and `now.config.json` files and adds a `tsconfig.json` file for TypeScript projects.


-   **[Default application structure](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US#application-structure)**

The default application structure includes some changes to directories and files, including the addition of a `.gitignore` file and moving the `now` object configuration in `package.json` to its own `now.config.json` file.

-   **[Create and convert commands include project-type parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

Specify the type of application to create or convert with the `project-type` parameter on the `now-sdk create` and `now-sdk convert` commands. This parameter determines the default application structure based on whether you want to use ServiceNow Fluent and JavaScript modules and third-party libraries in the application \(`fluent`\) or only use JavaScript modules and third-party libraries \(`module`\).

-   **Fetch command includes debug parameter**

Return debug logs generated during the fetch process by setting the `debug` parameter to true with the `now-sdk fetch` command.

-   **[Deploy command includes reinstall parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&section=now-sdk-deploy-command&ft:locale=en-US)**

Uninstall and reinstall the application on the instance by setting the `reinstall` parameter to true with the `now-sdk deploy` command. Reinstalling an application ensures that the metadata on the instance matches the metadata in the deployment package.

**Warning:** Metadata that is on the instance but not in your local application is removed.


</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **[SPO list page](https://www.servicenow.com/docs/access?context=procurement-specialist-list-page&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

All playbooks in SPO have been standardized to deliver a consistent look and feel, enhancing the overall user experience.

-   **[Configure conditions for merging purchase requisitions](https://www.servicenow.com/docs/access?context=config-pr-merge&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Set the conditions for merging purchase requisitions \(PRs\). Procurement administrators can define which fields must match for PR merges, ensuring flexibility to align with specific business processes.

-   **[Add a sourcing request to a negotiation event](https://www.servicenow.com/docs/access?context=add-a-sourcing-request-to-a-negotiation-event&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Introduced a unified logic for calculating supplier response close dates when adding sourcing requests to new or existing negotiation events. This ensures consistency in date calculations, regardless of whether the dates are system-generated or manually defined by procurement fulfillers.

-   **[Sourcing and Procurement Operations integration with third-party sourcing solutions](https://www.servicenow.com/docs/access?context=psm-integration-third-party-sourcing&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Enhanced the Source-to-Pay Integration Framework for integrations with third-party sourcing tools. You can now support negotiation-event-based integrations that consist of multiple sourcing requests.

Enhanced the purchase order cancellation flow when it's updated from the purchase order outbound table.

-   **[Inbound staging tables for Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=spo-inbound-staging-tables&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Made the following updates related to inbound staging tables:

    -   Introduced the following staging table and transform map:
        -   **Staging table**: Spend Shipment Import inbound \[sn\_spend\_intg\_imp\_shipment\]

        -   **Transform map**: Spend Shipment Import
    -   Transferred attachments from the Enterprise Resource Planning \(ERP\) system staging table to the main Purchase Order table. These attachments are also visible on the purchase order.
-   **[Source-to-Pay integration framework](https://www.servicenow.com/docs/access?context=sap-integration-overview-2&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Updated some fields and processes in the Source-to-Pay Integration Framework to build connection points and to work with other ERP systems, including the following fields and processes:

    -   Turned off the buttons to update purchase order when the integration status in the staging table is New or In Process.
    -   Disallowed purchase order lines to be created when purchase orders haven’t been brought in yet from the ERP system. Added a scheduled job to retry adding purchase order lines after a purchase order is created.
    -   Added missing columns and removed some columns in some staging and primary tables such as the outbound receipt, purchasing group primary and staging, cost center staging, and Fx currency tables. Updated the transform map logic for some of these tables to render these columns.
    -   Created the ERP plant address mapping staging table.

</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Break down work from a parent work item](https://www.servicenow.com/docs/access?context=breakdown-work-eap-epics-capabilities-child-work&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

Create child work items directly from the parent record page.

    -   The **Child items** tab on the work item record page is replaced with the tabs of each associated child item. For example, the full details page of an Epic shows separate tabs for its child work items, capabilities, features, and stories, based on the EAP configuration.
    -   New button is added to each tab to create work items directly from the parent work item record page.
-   **[Enhancements to the PI planning board in EAP](https://www.servicenow.com/docs/access?context=pi-planning-eap&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

The PI planning board displays all work assigned to the current Agile structure level as well as its child teams.

-   **[Feedback](https://www.servicenow.com/docs/access?context=product-feedback-landing&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)**

The Product Feedback application name is changed to Feedback.


</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Allocation charts reflect only active users](https://www.servicenow.com/docs/access?context=subscription-details-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

The Allocation summary and Allocation history charts on the subscription details page reflect only subscriptions allocated to active users for each month following the upgrade.


</td></tr><tr><td>

Talent Development Core

</td><td>

-   **[New Talent Development Core name](https://www.servicenow.com/docs/access?context=egd-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

The Talent Development Core name change enables easier alignment of growth and development goals across the enterprise. For information about the name change, see [Talent Development Core](https://www.servicenow.com/docs/access?context=egd-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).


</td></tr><tr><td>

Task Intelligence for ITSM

</td><td>

-   **[Classification model renaming](https://www.servicenow.com/docs/access?context=create-incident-prediction-model&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

The classification model available with the base system has been renamed from **ITSM OOTB TI Solution** to **Incident Categorization**.

-   **[Monitoring and Analytics](https://www.servicenow.com/docs/access?context=task-intel-monitor-analystics&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

You can now view the number of records predicted by the similarity models in the Task intelligence analytics page.


-   **[Updated Load Records icon](https://www.servicenow.com/docs/access?context=create-a-similar-records-prediction-model-in-task-intelligence-for-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

Starting in version 7.0.0, you can now viw the updated **Load Records** icon on Train the model screen.


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **[Visualization of a rack or cabinet](https://www.servicenow.com/docs/access?context=visualization-of-rack&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

The new rack visualization provides new power, weight, and capacity metrics.

-   **[Creating your inventory models](https://www.servicenow.com/docs/access?context=creating-your-inventory-models&version=xanadu&pubname=xanadu-telecom-network-inventory&ft:locale=en-US)**

The legacy product model tables are deprecated and they are migrated to Enterprise product model app.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[TISC Library Repository](https://www.servicenow.com/docs/access?context=tisc-ioc&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

New aliases can now be added directly from the form views of the threat intelligence library.


</td></tr><tr><td>

Vendor Management Workspace

</td><td>

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Vendor Management Workspace configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For information about how to upgrade, see the [Accessibility information section](rn-summary-changes.md#vendor-management-workspace-rn-accessibility) that follows.


</td></tr><tr><td>

Visa Spoke

</td><td>

-   **[Visa Resolve Online \(VROL\) version 24.2 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 24.2 revision changes:

    -   Submit Transaction Inquiry Request Builder
    -   Look up Queue Response Parser
    -   Look up Batch Queue Response Parser
    -   Submit Dispute Questionnaire
    -   Create Dispute Pre Arbitration
    -   Look up Dispute Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Pre Arbitration Response Details Response Parser

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.1 revision changes:

    -   Submit Fraud Report Request Builder
    -   Look up Fraud Report Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Details Response Parser
    -   Submit Dispute Questionnaire

</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **[Deprecated the privilege to delete a vulnerable item for the Admin role](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

As a vulnerability admin \[sn\_vul.vulnerability\_admin\], you can’t delete a vulnerable item. This privilege is now given to the sn\_vul.delete granular role.

-   **[Deprecated the privilege to delete source records for the sn\_vul.admin and sn\_vul.admin\_solutions roles](https://www.servicenow.com/docs/access?context=installed-with-vr&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

The privilege to delete the source records has been deprecated for the sn\_vul.admin and sn\_vul.admin\_solutions roles. This privilege is given to the sn\_vul\_cmn.delete granular role.


</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

-   **[Updates made for Claroty CTD v5.1](https://www.servicenow.com/docs/access?context=connect-to-claroty-ctd-vr-integration&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

The following updates were made to support Claroty CTD v5.1:

    -   There's no limit now on the number of Common Vulnerabilities and Exposures \(CVEs\) that you can import.
    -   The **Minimum CVSS Score** field was replaced with the **CVSS V3 Score** field.

</td></tr><tr><td>

Workflow Studio

</td><td>

-   **[Update Workflow Studio and all its dependencies](https://www.servicenow.com/docs/access?context=update-to-the-latest-version-of-workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

As of Washington DC patch 3, updating Workflow Studio automatically updates all of its application dependencies such as Workflow Studio, Playbook, and Decision Builder. You can no longer see or update the individual application dependencies of Workflow Studio from the ServiceNow Store or the list of plugins.


</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Dispatcher Workspace and Workforce Optimization for Field Service support reflow that enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For more information, see the [Accessibility information](../customer-service-management/workforce-optimization-csm-rn.md#workforce-optimization-csm-rn-accessibility) section that follows.


</td></tr><tr><td>

Workforce Optimization for ITSM

</td><td>

-   **[Reflow for configurable workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

Workforce Optimization for ITSM configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. For information about how to upgrade, see the [Accessibility information section](rn-summary-changes.md#workforce-optimization-itsm-rn-accessibility) that follows.

-   **[Renaming a published schedule](https://www.servicenow.com/docs/access?context=publish-schedule-wfo-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

You can edit the name of a schedule after it is published.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Xanadu features](../release-notes-summaries.md)

