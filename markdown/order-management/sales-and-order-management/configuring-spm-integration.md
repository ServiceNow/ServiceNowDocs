---
title: Configuring the Strategic Portfolio Management integration
description: Configure the Strategic Portfolio Management integration so that order delivery tasks in Order Management can be tracked as planned project tasks in SPM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/sales-and-order-management/configuring-spm-integration.html
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Configuring the Strategic Portfolio Management integration

Configure the Strategic Portfolio Management integration so that order delivery tasks in Order Management can be tracked as planned project tasks in SPM.

As an admin, follow these tasks to set up the SPM integration.

<table id="table_n2l_dcy_qxb"><thead><tr><th>

Configuration step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Activate PPM Standard \(Project Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/ppm-collaboration/t_ActivateProjectPortfolioSuiteWithFinancials.md)

</td><td>

Install the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin. If you're tracking customer projects, you must also activate the Customer Project Management \(com.snc.csm\_ppm\) plugin. For information on setting up Customer Project Management, see [Integrate with Customer Project Management using Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-ppm-configuration.md).

**Note:** If you installed the Order Management application before activating the PPM Standard or Customer Project Management plugins, you must repair the Order Management \(com.sn\_ind\_tmt\_orm\) plugin to get the plugin-dependent updates and demo data for the SPM integration.

</td></tr><tr><td>

[Create project templates and project template tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/creating-project-templates-orders.md)

</td><td>

Use the Project Portfolio Management application to create the project templates for order lines and project template tasks for domain orders and order tasks.

</td></tr><tr><td>

[Configure field mapping between orders and projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/configure-project-table-mapping.md)

</td><td>

Configure the CSM table maps to associate fields in order lines, domain orders, and order tasks to projects in SPM.

</td></tr><tr><td>

[Set up project oversight conditions and decision rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/setting-up-project-oversight.md)

</td><td>

Configure the conditions and decision rules for determining the order lines, domain orders, project offering with site locations, site project, and order tasks that qualify for project management oversight. You also specify the project templates to be used to create those projects.

</td></tr><tr><td>

[Configure project oversight for Product offering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/configure-site-project-product-offering.md)

</td><td>

Configure the conditions and decision rules that qualify product offering for site project oversight.

</td></tr><tr><td>

[Control the automatic closure of project tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/control-auto-closure-proj-tasks.md)

</td><td>

Manage the automatic closure of project tasks when related child tasks are completed or canceled.

</td></tr></tbody>
</table>