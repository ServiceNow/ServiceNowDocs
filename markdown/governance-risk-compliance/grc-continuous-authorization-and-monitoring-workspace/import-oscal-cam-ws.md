---
title: Import OSCAL catalog
description: From the OSCAL Import landing page, import catalog OSCAL data into the CAM Workspace.
locale: en-US
release: yokohama
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Importing in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL catalog

From the OSCAL Import landing page, import catalog OSCAL data into the CAM Workspace.

## Before you begin

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, and sn\_irm\_cont\_auth.admin

**Note:**

-   The catalog file that you want to import must be in the JSON format and validated using the OSCAL-CLI tool for any validation error. For more information on the OSCAL-CLI tool, see [usnistgov/oscal-cli](https://github.com/usnistgov/oscal-cli) on GitHub.
-   When the import process is complete, recipients are notified through email.

The OSCAL catalog import is a synchronous process.

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the primary navigation, select the OSCAL import landing page icon \(![OSCAL import](../image/cam-oscal-import-icon.png)\).

3.  Select **Catalog** from the **OSCAL Model** drop-down list.

    By default, the Catalog model is selected.

4.  Enter the **Source** name.

    The source of control objective.

5.  Enter the **Import status recipients** name.

    You can list the users you want to be notified once the OSCAL import is complete. The recipient receives an email notification on the import status.

6.  In the Attachments section, attach the catalog file from your local repository by selecting **Attach File**.

7.  Verify the control objectives to be imported by selecting **Import**.

8.  In the **Catalog import** pop-up window, verify the control objectives to be created or skipped.

9.  Select **Import**.

    **Note:** The CAM OSCAL catalog import model doesn’t support test templates and assessment procedures if they’re included in the catalog JSON file.

10. Refresh the page.

    In the **Import status** section, you can view the import status report.

    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.


**Parent Topic:**[Importing in OSCAL format](../concept/import-oscal.md)

