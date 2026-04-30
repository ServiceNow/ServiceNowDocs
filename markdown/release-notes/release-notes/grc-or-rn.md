---
title: Operational Resilience release notes
description: The ServiceNow Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Operational Resilience release notes

The ServiceNow® Operational Resilience application supports organizations to help keep business services running during adverse events like pandemics, severe weather, or cyber attacks. Operational Resilience was enhanced and updated in the Yokohama release.

## Operational Resilience highlights for the Yokohama release

-   Align with the CSDM model to set up configurable main node configurations, which are used to retrieve CSDM and their dependency data.
-   Add the primary origin to an operational vulnerability, and the impacted areas are automatically included. The vulnerability can then be viewed from any impacted area.
-   All CSDM objects, dependencies, and their red flags can be rolled up based on the entity hierarchy.
-   Use Smart Assessment for evaluating an Operational vulnerability.

See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Operational Resilience is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Measure resilience metrics using the CSDM model](https://www.servicenow.com/docs/access?context=using-csdm-v5&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Define the entity types and pillars in Operational Resilience and generate the entities. Establish relationships between CSDM objects, including business services, service offerings, business processes, and application services. Specify the type of main node configuration that you want to use by setting the **sn\_oper\_res.opres\_csdm\_main\_node\_config** property.

    After generating the entities and setting up the main node configurations, you can import CMDB data into Operational Resilience for reporting. CSDM and their dependencies are updated weekly while the red flags data is calculated daily. The outcome is displayed on the Homepage or in the related list of the CSDM objects.

-   **[Specify the primary origin of an operational vulnerability](https://www.servicenow.com/docs/access?context=add-impacted-area-to-vul&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Identify the primary origin of an operational vulnerability in its record. Once the primary origin is specified, its upstream dependencies are automatically included in the impacted areas, enabling you to view the operational vulnerability from all affected perspectives.

-   **[Using Digital resilience incident reporting](https://www.servicenow.com/docs/access?context=drir-module&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Assess whether any critical services are affected and classify the reported incident as a major incident if necessary. Notify regulators of major incidents, categorized by their severity and security ratings.

    The Digital resilience incident reporting module, accessible from the Operational Resilience Workspace, is integrated with Incident Management and Security Incident Response to generate and share reports in the format that is specified by the regulators.

    You can generate an initial report within 24 hours, an intermediate report within 72 hours, and a final report within 1 month. All of these reports are automatically triggered by the application from the time that the incident is classified as a major incident.


## UI changes

-   **[Business services dashboard](https://www.servicenow.com/docs/access?context=opres-ws-homepage-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Business services dashboard has been added to display business services data.

-   **[New modules for services and processes](https://www.servicenow.com/docs/access?context=using-csdm-v5&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Services, Business Services, Service Offerings, and Business Processes modules have been added to the Operational Resilience Workspace. Operational Resilience managers use these modules to manage the services, business services, service offerings, and business processes used in Operational Resilience reporting.

-   **[Entity Types and Pillars modules](https://www.servicenow.com/docs/access?context=manage-entity-types-pillars-from-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Entity Types and Pillars modules have been added to the Operational Resilience Workspace. These modules enable Operational Resilience managers to update the entity types and pillars directly from the Workspace.

-   **[Primary origin tab](https://www.servicenow.com/docs/access?context=add-impacted-area-to-vul&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The **Primary origin** tab has been added to the Operational vulnerability record to identify the main source and report the upstream entities of the vulnerability.

-   **[Addition of classes to the assessment form](https://www.servicenow.com/docs/access?context=submit-an-assessment-in-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Business Service and Offering classes have been added to the **Scope** tab of the assessment form, enabling you to assess the business services and service offerings alongside services. Once the assessment is complete, the importance and impact tolerance of these items are displayed in the Importance and Impact Tolerance columns on the **Scope** tab.

-   **[Addition of classes to the scenario analysis form](https://www.servicenow.com/docs/access?context=scenario-analysis-in-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Business Service and Offering classes have been added to the **Scope** tab of the scenario analysis form, enabling you to analyze the business services and service offerings alongside services.

-   **[Addition of classes to the self-attestation form](https://www.servicenow.com/docs/access?context=self-attestation-in-ws&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Business Service and Offering classes have been added to the **Scope** tab of the self-attestation form, enabling you to self-attest the business services and service offerings alongside services.

-   **[Digital resilience incident reporting module](https://www.servicenow.com/docs/access?context=drir-module&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    The Digital resilience incident reporting module is used to report the Information and Communication Technology \(ICT\) related incidents to the regulators.


## Activation information

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Business Continuity Management requires the following browsers:

-   Google Chrome
-   Firefox and Firefox Extended Support Release \(ESR\)
-   Microsoft Edge Chromium
-   Safari 12.0 and later versions

## Related ServiceNow applications and features

-   **[Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the Risk Management application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce the reaction time from days to minutes.

-   **[Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the Advanced Risk application to identify, measure, and track risks. The application includes the workflows for risk assessments and events, ensuring efficient management of your organization's risk profile.

-   **[Policy and Compliance Management](https://www.servicenow.com/docs/access?context=r_PolicyComplianceMgmt&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the Policy and Compliance Management application to create and manage policies, standards, and internal control procedures that are mapped to external regulations and general guidelines.

-   **[Business Continuity Management](https://www.servicenow.com/docs/access?context=risk-workspace&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use the Business Continuity Management application to ensure that your organization can keep delivering products and services at an acceptable level even when faced with disruptive events.

-   **[Vulnerability Response](https://www.servicenow.com/docs/access?context=avr-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Use the Vulnerability Response application to enable security users to analyze security data, implement changes, and generate security incidents.

-   **[Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use the Incident Management application to restore normal service operation while minimizing impact to business operations and maintaining quality.

-   **[Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    Use the Security Incident Response application to manage the life cycle of your security incidents from initial analysis to containment, eradication, and recovery.

-   **[Digital Operational Resilience Management](https://www.servicenow.com/docs/access?context=conf-dg-resi-party-regi&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use this application for uploading and downloading of all individual DORA tables. It is automatically installed when the Digital Resilience Third-party Information Register is activated.

-   **[Data registry](https://www.servicenow.com/docs/access?context=grc-360-deg-rel-vis&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)**

    Use this application to visually explore the relationships between the different types of critical data that affect your business, such as controls, risks, and issues.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

