---
title: Organization codes and paths
description: An organization code is a unique identifier for a business organization, while an organization path establishes the organization hierarchy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-bo-code-bo-path.html
release: brazil
topic_type: concept
last_updated: "2026-09-09"
reading_time_minutes: 1
breadcrumb: [Import business organizations with guided setup, Create a business organization, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Organization codes and paths

An organization code is a unique identifier for a business organization, while an organization path establishes the organization hierarchy.

## Organization codes

An organization code must be unique that identifies a business organization in a ServiceNow instance. Attempting to insert a new record with previously existing organization code in the Organization Core \[sn\_customer\_service\_organization\] table, the value for the code results in the following error:

`java.sql.BatchUpdateException: Duplicate entry for key service_organization_path`

## Organization paths

An organization path establishes the hierarchy among different business organizations. This path is stored in the **Business Organization Path** on the Business Organization form.

An organization path is a combination of the organization codes for each business organization in the hierarchy. For example, let's use the following business organizations to demonstrate business organization paths.

\[Omitted image "bo-codes-paths.png"\] Alt text: Business organization hierarchy example with three levels of parent and child companies

<table id="table_mxm_dst_jyb"><thead><tr><th>

Business Organization

</th><th>

Organization code

</th><th>

Organization path

</th></tr></thead><tbody><tr><td>

Manhattan Main

</td><td>

~~~~1

</td><td>

~~~~1

 Manhattan main is the parent company. The business organization path for Manhattan main is the same as the organization code, which indicates that it’s the first element in the hierarchy.

</td></tr><tr><td>

Manhattan Upper

</td><td>

~~~~2

</td><td>

~~~~1/~~~~2

 Manhattan upper is a child company of Manhattan main. The structure of the business organization path is interpreted as Manhattan main/Manhattan upper.

</td></tr><tr><td>

Manhattan Upper East

</td><td>

~~~~3

</td><td>

~~~~1/~~~~2/~~~~3

 Manhattan upper east is a child company of Manhattan upper and the structure of the business organization path is interpreted as Manhattan main/Manhattan upper/Manhattan upper east.

</td></tr><tr><td>

Manhattan Upper West

</td><td>

~~~~4

</td><td>

~~~~1/~~~~2/~~~~4

 Manhattan Upper West is a child company of Manhattan Upper. The structure of this business organization path is interpreted as Manhattan main/Manhattan upper/Manhattan upper west.

</td></tr></tbody>
</table>## Importing business organization records

If you create your business organization records by importing the data from some source system through a transform map, make sure that you execute the business rules. The organization Path is added, updated, and deleted based on the insertion, updating, and deletion of records in the Organization Core \[sn\_customer\_service\_organization\] table through the business rules. If the business rules aren’t executed, it can result in empty organization paths, which can then result in data access issues.

**Note:** If you don’t execute the business rules during import, run the script in the **Update Organization Path** business rule for the newly imported records to set the organization paths correctly.

