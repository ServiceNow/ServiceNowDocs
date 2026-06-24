---
title: Installing Core Business Suite applications
description: Install Core Business Suite applications to be able to submit inquiries, create and track requests, and manage workflows. These applications support departments such as Legal, Human Resources, Workplace Services, Health and Safety, Procurement, Finance, Supplier Lifecycle Operations, and Accounts Payable Operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/core-business-suite/install-cbs-applications.html
release: zurich
topic_type: concept
last_updated: "2025-12-02"
reading_time_minutes: 2
breadcrumb: [Configure, Core Business Suite]
---

# Installing Core Business Suite applications

Install Core Business Suite applications to be able to submit inquiries, create and track requests, and manage workflows. These applications support departments such as Legal, Human Resources, Workplace Services, Health and Safety, Procurement, Finance, Supplier Lifecycle Operations, and Accounts Payable Operations.

Core Business Suite provides applications for various parts of your organization. You can install any or all of them.

Verify that the listed plugins are installed. If they aren’t, install them individually using the standard installation process.

<table id="table_fmt_rxg_qhc"><thead><tr><th>

Application

</th><th>

Description

</th><th>

Plugins

</th></tr></thead><tbody><tr><td>

Legal services

</td><td>

Submit and manage general legal requests. See [Install Legal Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/legal-request-management/install-legal-request-management.md).

</td><td>

-   Legal Request Management application \(sn\_lg\_ops\)
-   Legal Counsel Center application \(sn\_lg\_cf\_workspace\)

</td></tr><tr><td>

Human Resources \(HR\) services

</td><td>

Manage payroll inquiries, benefits questions, and general HR requests. See [Activate Case and Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/hr-service-delivery/activate-case-and-knowledge-management-scoped.md).

</td><td>

-   Human Resources Scoped App: Core \(com.sn\_hr\_core\)
-   Agent Workspace for HR Case Management \(sn\_hr\_agent\_ws\)
-   Advanced Work Assignment for HRSD \(com.sn\_hr\_awa\)
-   Document Templates \(sn\_doc\)
-   HR Taxonomy \(sn\_hr\_emp\_taxonomy\)
-   Human Resources Scoped App \(sn\_hr\_pa\)

</td></tr><tr><td>

Workplace Services Delivery

</td><td>

Handle general service requests and managing space arrangements efficiently.See [Install Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/workplace-case-management/install-workplace-case-mgmt.md).

</td><td>

-   Workplace Core \(sn\_wsd\_core\)
-   Workplace Case Management \(sn\_wsd\_case\)
-   Workplace Agent for mobile \(sn\_wsd\_agent\_mob\)
-   Workplace Central \(sn\_wsd\_central\)

</td></tr><tr><td>

Health and Safety services

</td><td>

Enable employees to make health and safety related inquiries. See [Install Health and Safety Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/health-and-safety-risk-management/install-hs-risk-mgmt.md).

</td><td>

-   Health and Safety Core \(sn\_ohs\_im\)
-   Health and Safety Case \(sn\_hs\_cm\)

</td></tr><tr><td>

Procurement services

</td><td>

Enable employees to make procurement related inquiries. See [Install Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-finance-spend-central.md).

</td><td>

-   Common Service Delivery \(sn\_spend\_sdc\)
-   Supplier Common Architecture \(sn\_slm\)
-   Finance Common Architecture \(sn\_fin\)
-   Source-to-Pay Workspace \(sn\_spend\_workspace\)
-   Procurement Case Management \(sn\_spend\_psd\)
-   Supplier Case Management \(sn\_supplier\_mgmt\)

</td></tr><tr><td>

Finance services

</td><td>

Enable employees to make finance related inquiries. See [Install Finance Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/finance-case-management/install-fin-case-mgmt.md).

</td><td>

-   Finance Case Management \(sn\_fin\_ops\)
-   Finance Common Architecture \(sn\_fin\) installed with \(sn\_fin\_ops\)
-   Common Service Delivery \(sn\_spend\_sdc\) installed with \(sn\_fin\_ops\)
-   Finance Operations Workspace \(sn\_fin\_ops\_ws\) installed with \(sn\_fin\_ops\)
-   Source-to-Pay Common Architecture \(sn\_shop\)
-   Advanced Work Assignment for Source-to-Pay Operations \(sn\_spend\_awa\)

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

Streamline procurement, supplier, and invoice requests from submission to fulfillment. See [Install Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-supp-mgmt.md).

</td><td>

-   Supplier Case Management \(sn\_supplier\_mgmt\)
-   Supplier Common Architecture \(sn\_slm\)
-   Source to Pay Workspace \(sn\_spend\_workspace\)
-   Supplier Collaboration Portal \(sn\_supplier\_sp\)

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

Enable suppliers to view purchase orders, invoices, and inquiry cases, and submit invoice-related questions. See [Install Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/accounts-payable-operations/install-acc-pay-mgmt.md).

</td><td>

-   Invoice Case Management \(sn\_ap\_cm\)
-   Source-to-Pay Common Architecture \(sn\_shop\)
-   Finance Common Architecture \(sn\_fin\_ops\)
-   Common Service Delivery \(sn\_spend\_sdc\)
-   Source to Pay Workspace \(sn\_spend\_workspace\)
-   Supplier Collaboration Portal \(sn\_supplier\_sp\)

</td></tr></tbody>
</table>What to do next:

Import Core Business Suite configuration files. For more information, see [Import Core Business Suite configuration files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/core-business-suite/cbs-import-update-sets.md).

