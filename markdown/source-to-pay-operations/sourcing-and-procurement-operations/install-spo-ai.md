---
title: Install Sourcing and Procurement Operations
description: Install Sourcing and Procurement Operations \(SPO\) on your instance from the Product Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/install-spo-ai.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 4
breadcrumb: [Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Install Sourcing and Procurement Operations

Install Sourcing and Procurement Operations \(SPO\) on your instance from the Product Hub.

## Before you begin

-   The ServiceNow Otto for Setup application \(sn\_ia\) must be installed on your instance. See [Set up ServiceNow Otto with ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-setup-now-assist.md).
-   Your instance must be entitled to at least one SPO resource for the SPO tile to display on admin Home.

Role required: admin

## About this task

Sourcing and Procurement Operations applications, plugins, and dependencies are bundled into a single installable resource. Selecting install starts a single-select installation of the full set of SPO applications your instance is entitled to, instead of installing each application individually.

## Procedure

1.  From the header of your ServiceNow instance, navigate to **Admin** &gt; **Admin Home**.

2.  From the **Manage your products** section, select Sourcing and Procurement Operations.

    \[Omitted image "spo-config-hub.png"\] Alt text: Sourcing and Procurement Operations tile in the Manage your products section on admin Home.

    The Product Hub page for Sourcing and Procurement Operations is displayed.

3.  In the **Apps and plugins** section, from the **Not installed** tab, select **Install** for Sourcing and Procurement Operations.

    The **Select applications and versions to be installed** page is displayed \(step 1 of 2\), with all entitled applications and their latest versions preselected.

4.  Review the preselected applications and versions, and select **Load demo data** if you want to install sample records along with the applications.

    Load demo data when you first install Sourcing and Procurement Operations on a development or test instance.

5.  Select **Proceed**.

    The **Review Installation Details** page is displayed \(step 2 of 2\), confirming the number of applications selected.

6.  Under **Installation schedule**, select **Install now** or **Install later**, and then select **Install**.

    An **Installation Progress** window opens. All entitled SPO applications, plugins, and dependencies install together. Select **Run in background** to continue working while installation completes.

    **Important:** Admins can access Application Manager directly through a link during installation. The **Included Applications** count on the Application Manager product page displays as 0 during installation, then updates to reflect the accurate application count after installation completes. For more information, see [Sourcing and Procurement Operations tile temporarily disappears from Admin Home during installation \[KB3153465\]](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=0a303c69474bc710d1a5ab29736d4361).

7.  After installation completes, confirm Sourcing and Procurement Operations in the **Installed** tab.

    \[Omitted image "spo-product-hub-configure.png"\] Alt text: Sourcing and Procurement Operations Product Hub with the Installed tab selected and the Helpful resources section.

    The **Helpful resources** section is always visible and provides the following resources:

    -   Product overview video
    -   Link to configure with ServiceNow Otto
    -   Configuration guidance
    -   Release notes
    -   Product documentation
    -   Community link
8.  Start configuring Sourcing and Procurement Operations.

    1.  Select **Configure** to open the SPO Configuration Console.

        \[Omitted image "spo-config-console.png"\] Alt text: Configure Sourcing and Procurement Operations Configuration Console showing configuration summary and setup status.

        The SPO Configuration Console is displayed.

    2.  In the **Get started with configuration** pop-up window, review the configuration instructions and select **Got it**.

        \[Omitted image "spo-config-console-got-it.png"\] Alt text: Getting started with Sourcing and Procurement Operations configuration.


## Result

Sourcing and Procurement Operations is installed and ready for configuration.

-   **[Components installed with Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/installed-with-FSC.md)**  
Several types of components are installed with the activation of Sourcing and Procurement Operations, including tables, user roles, and scheduled jobs.

**Parent Topic:**[Configuring Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configuring-spo.md)

**Related topics**  


[Sourcing and Procurement Operations product tile]()

[Sourcing and Procurement Operations Product Hub]()

[Sourcing and Procurement Operations Configuration Console]()

[Configure Sourcing and Procurement Operations]()

[Setting up primary data for ShoppingHub]()

[Configure punchout for third-party site purchases]()

[Configuring work prioritization]()

[Add a button in Shopping Hub]()

[Add a footer link in Shopping Hub]()

[Customize your top suppliers on Shopping Hub]()

[Configure conditions for merging purchase requisitions]()

[Service portal configuration for ShoppingHub]()

[Install ShoppingHub Mobile]()

[Advanced Work Assignment for Source-to-Pay Operations]()

[Install Universal Request for Sourcing and Procurement Operations]()

