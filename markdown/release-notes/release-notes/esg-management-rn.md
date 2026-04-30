---
title: Operational Sustainability Management release notes
description: The ServiceNow ESG Management application helps you to manage all your environmental, social, and governance \(ESG\) commitments. ESG Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Operational Sustainability Management release notes

The ServiceNow® ESG Management application helps you to manage all your environmental, social, and governance \(ESG\) commitments. ESG Management was enhanced and updated in the Yokohama release.

## ESG Management highlights for the Yokohama release

-   Model and prepare for potential outcomes with what-if scenario analysis tools that can help with your strategic planning.
-   Review the calculated metric definition data by using a formula tree so that you can access detailed information on the operands, metric definitions, metrics, and emission factors.
-   Streamline ESG metric tracking and enable trend analysis with enhanced Metric data tasks that support choice and HTML response formats and table improvements.
-   Import your historical metric data by using an import template to update and manage metric data within your organization.
-   Assign data owners dynamically for metrics that are based on configurations.

See [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US) for more information.

**Important:** ESG Management is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Forecast planning and analysis](https://www.servicenow.com/docs/access?context=scenario-analysis-forecast&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    Model and prepare for potential outcomes by using forecast planning analysis. With these tools, you can create, save, or visualize multiple scenarios.

-   **[Formula tree](https://www.servicenow.com/docs/access?context=reviewing-formula-tree&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    Explore the calculated metric definitions by reviewing a structured and visual representation of the entire calculation chain. By using a formula tree, you can access the calculation details and view how the different metrics and emission factors are interconnected.

-   **[Historical metric data](https://www.servicenow.com/docs/access?context=importing-metric-data&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    Import the historical metric data by using a pre-defined import template with instructions. With this process, you can update and manage the metric data within your organization and help to ensure that all data complies with the established business rules.

-   **[Dynamic filtering for Microsoft 365 for ServiceNow Reporting](https://www.servicenow.com/docs/access?context=add-related-fields-0365&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    Filter the fields dynamically and set up dependencies by using related fields. In the Microsoft 365 add-in, you can configure fields so that cascading filters are supported dynamically. You can select a value in a field and have the related fields automatically update to show the relevant options. This process helps you to streamline data entry and improve efficiency.


## UI changes

-   **[Forecast planning and analysis](https://www.servicenow.com/docs/access?context=scenario-analysis-forecast&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    The forecast planning analysis module is now included in the List view of the Operational Sustainability Workspace.


## Changed in this release

-   **[Result types](https://www.servicenow.com/docs/access?context=create-manual-metric-definition&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    If you have the ESG manager \[sn\_esg.metric\_manager\] role, you can now configure either text, choice, or HTML format options for responses to qualitative metric data tasks that are related to manual metric definitions, including both initial and overridden responses. These options help you achieve more precision and detail in your data collection process.

-   **[Metric data table filters and side panel enhancements](https://www.servicenow.com/docs/access?context=metric-data-table&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    If you have the ESG data owner \[sn\_esg.data\_owner\] role, you can now apply filters by using the filter menu and reject or approve tasks from the metric data table side panel. Data owners can now multi-submit and assign approvers to multi-approve or reject tasks, with the option to use choice and HTML response formats.

-   **[Data owner assignment types](https://www.servicenow.com/docs/access?context=create-manual-metric-definition&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)**

    If you have the ESG Manager \[sn\_esg.metric\_manager\] role, you can now configure the Data Owner Assignment type to be either simple or advanced for manual metric definitions. When you select the Simple option, the system assigns the specified Data Owner or Data Owner Group to the Metric Data Task. If you choose the Advanced assignment option, which is available with the GRC: Approver Configurator application, you can set custom configuration conditions, tables, or data owners to dynamically assign data owners.

-   **Table added to the GRC: Metrics application**

    The following tables were added to the GRC: Metrics application:

    -   sn\_grc\_metric\_import\_job
    -   sn\_grc\_metric\_data\_import
    -   sn\_grc\_metric\_st\_import\_log
    -   sn\_grc\_metric\_st\_transform\_history
    -   sn\_grc\_metric\_import\_template
-   **Table added to the ESG content accelerator application**

    The sn\_esg\_content\_issb\_citation table was added to the ESG content accelerator application.

-   **Table added to the Forecast planning analysis application**

    The following tables were added to the Forecast planning analysis application:

    -   sn\_grc\_forecast\_analysis
    -   sn\_grc\_forecast\_context
    -   sn\_grc\_forecast\_data
    -   sn\_grc\_forecast\_parameter\_data
-   **Database view added to the Scope 3 emissions management application**

    The sn\_esg\_scope3\_asset\_emissions database view was added to the Scope 3 emissions management application.

-   **Changes made to the sn\_grc\_metric\_data\_task table**

    In the sn\_grc\_metric\_data\_task table, the job\_submitted, job\_errors, choice, overridden\_choice, html, and overridden\_html columns were added. The type="string" attribute was added to the state column.

-   **Changes made to the sn\_grc\_metric\_metric table**

    In the sn\_grc\_metric\_metric table, the period\_date, data\_owner\_type, data\_owner, and data\_owner\_group columns were added. The type="string" attribute was added to the domain\_area column.

-   **Changes made to the sn\_grc\_metric\_parent\_data table**

    In the sn\_grc\_metric\_parent\_data table, the formula\_operands columns, and html columns were added.

-   **Changes made to the sn\_grc\_metric\_base\_definiton table**

    In the sn\_grc\_metric\_base\_definiton table, the formula\_tree, result\_type, choice\_table, choice\_field, choice\_condition, data\_owner\_assignment\_type, source columns were added. The type="string" attribute was added to the frequency column.

-   **Changes made to the sn\_grc\_metric\_data\_by\_entity table**

    In the sn\_grc\_metric\_data\_by\_entity table, the html column was added.

-   **Attributes modified in the sn\_grc\_metric\_collector\_data table**

    In the sn\_grc\_metric\_collector\_data table, the display="true" attribute was removed from the collector\_definition column.

-   **Attributes modified in the sn\_grc\_metric\_data\_process\_queue table**

    In the sn\_grc\_metric\_data\_process\_queue table, the reference\_cascade\_rule="delete" attribute was added to the metric\_definition column.

-   **Attributes modified in the sn\_grc\_metric\_definition table**

    In the sn\_grc\_metric\_definition table, the type="string" attribute was added to the type, method\_type columns.

-   **Changes made to the sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\_filter table**

    In the sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\_filter table, the related\_fields column was added. The display="true" attribute was added to the field\_name column in the sn\_esg\_msoff\_intg\_o365\_reporting\_configuration\_filter table.

-   **System properties are added to the GRC: Metrics application**

    The following properties were added to the GRC: Metrics application:

    -   com.glide.event\_manager.grc\_metrics\_queue.even.load.distribution.enabled
    -   com.glide.event\_manager.grc\_metrics\_queue.claim\_limit

## Deprecations

Business rules were deactivated and moved to common script include methods as part of GRC Metrics. For more information, see the KB article: [KB1734660](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3De92f82dd476a9610b8a4aa25126d4356).

## Activation information

Install ESG Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

