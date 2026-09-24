---
title: SAP publisher pack integration architecture
description: The SAP publisher pack integration architecture defines how licensing, user, engine, and database usage data flows from SAP systems to ServiceNow for software reconciliation and compliance reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/sap-integration-architecture.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 8
keywords: [SAP integration, SAP publisher pack, RFC, WSDL, OData, satellite systems, FUE, Private Cloud]
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management, Asset Management]
---

# SAP publisher pack integration architecture

The SAP publisher pack integration architecture defines how licensing, user, engine, and database usage data flows from SAP systems to ServiceNow for software reconciliation and compliance reporting.

ServiceNow communicates exclusively with one central SAP system. That central system reaches one or more satellite SAP systems such as Solution Manager, S/4HANA, GRC, or ECC over RFC \(Remote Function Call\). ServiceNow never connects to satellite systems directly.

## Connection types

The integration supports two interchangeable connection types: SOAP/WSDL with Basic Authentication and OData with OAuth 2.0. Both connection types perform the same refresh and pull operations; the difference is in the entry point and response format.

**Important:** Basic Auth \(SOAP/WSDL\) will be deprecated by SAP after November 2026. OAuth 2.0 is the recommended connection type for all new integrations, including SAP S/4HANA Cloud, Private Edition.

|Area|Basic — SOAP/WSDL|OData / OAuth 2.0|
|----|-----------------|-----------------|
|Entry point|RFC Function Module|SAP Gateway Service|
|SAP layer|Function module called directly|Gateway → DPC\_EXT → Function module|
|Refresh|Refresh FM \(via `I_REQUEST_TYPE`\)|OData Action → `/NOW/SAMP_USER_DETAILS_REFRESH`|
|Data pull|Pull FM \(via `I_REQUEST_TYPE`\)|OData Action → `/NOW/SAMP_USER_DETAILS_PULL`|
|Response format|XML only|XML or JSON|
|Status|Deprecation planned in November 2026|Recommended|

## Integration architecture

The following diagram shows the four layers of the integration:

-   The software asset management layer
-   The connection layer
-   The central system, which contains the three processing phases and the staging layer
-   The satellite systems

\[Omitted image "sam-sap-integration.svg"\] Alt text: SAM SAP integration architecture diagram showing all the three phases

## How the integration works

The integration operates in the following three phases:

**Note:** All three phases run automatically. No manual action is required during data collection or retrieval operations.

1.  Phase 1 — Refresh and job scheduling: When the Software Asset Management application sends a refresh request, the central SAP system receives it through either the SOAP/WSDL endpoint or the OData/OAuth gateway. The entry function module evaluates the request type and triggers class `/NOW/SAMP_CL_USER_DETAILS`, which schedules a background job \(`JOB_OPEN → SUBMIT → JOB_CLOSE`\). The dispatcher program `/NOW/SAMP_USER_PROG_BCKJOB_RUN` then calls `GET_*_DATA_THR_RFC` for each active RFC destination.
2.  Phase 2 — RFC extraction: The central system loops through each configured RFC destination and calls `RFC_READ_TABLE` and RFC-enabled function modules or BAPIs on the satellite system. This reads standard SAP tables such as `USR02`, `AGR_USERS`, `ADRP`, `TUPL`, and `AGR_FLAGS`, and writes the results into 12 custom `/NOW/*` staging tables on the central system.
3.  Phase 3 — Data pull and retrieval: When the Software Asset Management application sends a pull request, the central system reads the staging tables using `GET_DATA_FROM_*_TABLE`. The SAP system applies filters by RFC name, system ID, client, offset, and limit for pagination. It converts the records to XML or JSON payload in `ET_XML_TABLE` and returns the SOAP or OData response. ServiceNow processes the response and updates its internal tables.

## Staging layer

Phases 2 and 3 both interact with a set of intermediate tables on the central SAP system. Phase 2 writes into these tables and Phase 3 reads from them. This staging layer decouples the RFC collection step from the data transfer step, preventing long-running synchronous calls to ServiceNow.

The following table lists all staging tables and their content.

|Table|Content|
|-----|-------|
|`/NOW/M_USER_DATA`|User data including Named User Type and, for Cloud Private deployments, target FUE classification|
|`/NOW/M_SAP_ROLES`|SAP role definitions|
|`/NOW/M_USER_ROLE`|User-to-role assignments|
|`/NOW/M_USR_ACTIT`|User activity data|
|`/NOW/M_USR_TCODE`|Transaction codes used per user|
|`/NOW/SAP_TCODES`|SAP transaction code definitions|
|`/NOW/M_ENGINES`|SAP engine usage data \(collected from S/4HANA via Special Scenario 1\)|
|`/NOW/USMM_DATA`|USMM-based license measurement data|
|`/NOW/SAMP_PRICE`|Price list data for license cost calculation|
|`/NOW/SAMP_RFC`|RFC destination configuration data, including deployment type \(Cloud Private or on-premises\) for each connected system|
|`/NOW/DIGITAL_ACC`|Digital Access document count data for indirect access licensing|
|`/NOW/WEB_ACTIVITY`|Web activity data from connected SAP systems|

## Special scenarios

Two special scenarios exist where standard SAP tables do not hold the required data. In these cases, custom function modules on the satellite systems collect the data separately and write it into dedicated staging tables.

-   **Special Scenario 1 — Engine data \(Satellite 2: S/4HANA only\)**

    A custom function module on the S/4HANA satellite writes engine usage data to `/NOW/HANA_DB`. The central system reads this table and stages the data into `/NOW/M_ENGINES`. This special case applies only to S/4HANA satellite systems and collects HANA database usage metrics for engine license measurement.

-   **Special Scenario 2 — FUE user classification \(all satellites\)**

    A custom function module on each satellite triggers the SAP user classification program \(`SLIM_USER_CLF_HELP`, also referred to as the STAR report\). The program applies the uploaded license ruleset to classify each user into a Named User Type — Developer \(GA\), Advanced \(GB\), Core \(GC\), or Self-Service \(GD\). It writes the results to `/NOW/M_USER_CLF` on the satellite. The central system reads this staging table over RFC and updates `/NOW/M_USER_DATA` with the License classification values. This special case applies to all satellite systems and is required for Full Usage Equivalent \(FUE\) license calculation.


## Design principles

-   ServiceNow communicates only with the central SAP system. Satellite systems are never accessed directly.
-   The central SAP system exposes the WSDL endpoint and SAP Gateway. Satellite systems are reached exclusively over RFC.
-   Multiple satellite systems can send data to one central system. The RFC loop in Phase 2 repeats for each configured RFC destination.
-   Background jobs in Phase 1 prevent long-running synchronous calls between the central system and satellites.
-   Supported satellite system types include ECC, S/4HANA, GRC, and Solution Manager.

**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack]()

[Set up SAP integration to establish a connection with SAP]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create software models for SAP]()

[Create entitlements for SAP]()

[Create a custom SAP named user type]()

[Map a role to a named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[Import custom SAP price lists]()

[SAP USMM-based optimization]()

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

[Set up SAP integration to establish a connection with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/setup-sap-integration.md)

[Deploy the ABAP program for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-abap-program-sap.md)

[Upload the license ruleset for SAP S/4HANA Private Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/upload-license-ruleset-sap-private-cloud.md)

[Export the Root CA certificate from SAP for Private Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/export-root-ca-cert-sap-private-cloud.md)

[Tables installed with the SAP publisher pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/component-installed-sap-plugin.md)

