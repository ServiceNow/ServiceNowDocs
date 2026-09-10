---
title: Skills Foundation release notes
description: The ServiceNow Skills Foundation application provides an overview of skills-related data and enables admins to work on Job architecture data from a single location. Skills Foundation was enhanced and updated in the Zurich release.The ServiceNow Skills Foundation application provides an overview of skills-related data and enables admins to work on Job architecture data from a single location. Skills Foundation was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Skills Foundation release notes

The ServiceNow® Skills Foundation application provides an overview of skills-related data and enables admins to work on Job architecture data from a single location. Skills Foundation was enhanced and updated in the Zurich release.

## About Skills Foundation

-   The Skills Intelligence application name has been changed to Skills Foundation.
-   The skills ontology, which contained skill structure with categories and definition, is no longer provided. Supply your own skills data and import it into the Skills Foundation application.
-   Efficient skill search mechanism is provided by replacing machine learning models with AI search and AI search with RAG configuration for Pro Plus License \(i.e. LLM Integration\) customers.
-   Automatic HR job profile and Talent job profile synchronization when a new employee joins the organization, or​ an existing employee changes position. You must have Human Resources Scoped App \(sn\_hr\_core\) installed for this feature to work.
-   Integration between SAP SuccessFactors and ServiceNow enables customers to import skills and user skills into ServiceNow, unlocking Growth Experiences features and driving higher adoption​. The integration feature will only work for the customers who are using Job Profile Builder and will not work for those who are using Talent Intelligence Hub.

See  for more information.

## Activation and other requirements

**Important:** Skills Foundation is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Skills Foundation by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    You cannot download industry skills data as part of the guided setup.

-   **Additional requirements**
    -   The Human Resources Scoped App \(sn\_hr\_core\) plugin on Australia family release must be installed for HR profile and Talent job profile synchronization.

        **Note:** For earlier releases, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request. Approve the message and re-import the plugin manually.

    -   The Skills foundation \(sn\_skills\_int\) v 10.0 for the skills foundation features.
    -   The Skills Workspace plugin \(sn\_skills\_int\_ws\) v 6.1 must be installed to access the workspace experience.
    -   HRSD integration for SAP SuccessFactors \(sn\_hr\_sf\) Plugin which depends on SuccessFactors \(sn\_successfactors\) spoke v 4.6.1-7 to fetch skills and user skills data.

**Parent Topic:**[Growth Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/employee-growth-development-landing.md)

## Zurich

The ServiceNow® Skills Foundation application provides an overview of skills-related data and enables admins to work on Job architecture data from a single location. Skills Foundation was enhanced and updated in the Zurich release.

### What's changed

-   ****

    Skills search is powered by AI Search capability instead of machine learning models. You can configure the skill search to be indexed based on the skill name or description or both. For Pro Plus License \(i.e. LLM Integration\) customers, AI search with RAG configuration is provided to power skill search.Multilingual skill support is limited to the languages supported by AI Search, which is fewer than the previously supported 23 languages.Resume parsing is done using Now Assist.ITSM skills previously stored in the CDS plugin were moved back to the seed data plugin.


-   ****

    The application name Skills Intelligence Workspace has been changed to Skills Workspace.Role group skill recommendations will not be readily available unless you load your own ontology data to the industry plugin.In Skill Harmonization, duplicate skills identification relies on AI search instead of ML models, which will have some quality impact in identifying duplicates.In Skills Import, two new integration options are added for SAP SuccessFactors and skills and user skills imported go through harmonization pipeline.


-   ****

    In the Career tab, the recommended skills source is now derived both from skills that are tagged to activities that employees has been pursuing and from similar user skills.


### What's deprecated or removed

-   The LinkedIn Parsing capability is not supported because it is based on ML models.
-   The skills ontology, which contained skill structure with categories and definition, is no longer provided. Supply your own skills data and import it into the Skills Foundation application.
-   Legacy Data Science algorithms from Talent Development applications.

