---
title: Manage information objects of a business application in EA Workspace
description: Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object, which can be used to leverage the business application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-associate-info-obj-ba.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with an application portfolio, Working with Portfolio list view, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage information objects of a business application in EA Workspace

Relate a business application to an information object using the CI relationship \[cmdb\_rel\_ci\] table of type Uses::Used by. Use this suggested relationship to get the logical data of the information object, which can be used to leverage the business application.

## Before you begin

Role required: sn\_apm.apm\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon \(\[Omitted image "portfolio-icon.png"\] Alt text: Portfolio icon\).

3.  Select the expand row icon \(\[Omitted image "ExpandIcon.png"\] Alt text: Expand Row icon\) next to **Application Portfolio**.

4.  Select **Business Applications**.

5.  Select the name of a business application to view the associated artifacts.

6.  Select the **Information Objects** tab.

    A list of information objects associated with the business application is displayed.

7.  To relate an existing information object to the business application, select **Add**.

8.  On the form, fill in the fields.

    For field information, see [Add relationship form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/add-relationship-form.md).

9.  Select **Save**.

10. To delete a relationship between a business application and an information object, select an information object then select **Delete Relationship**.

    The relationship between the business application and the information object, and the attributes of the relationship gets deleted.

11. To edit an existing relationship details, select an information object then select **Edit**.

    Edit the details in the **Manage Relationship** form and select **Update**.


**Parent Topic:**[Working with an application portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-work-with-application-portfolio.md)

