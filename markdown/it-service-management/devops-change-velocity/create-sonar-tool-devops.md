---
title: Onboard SonarQube to DevOps Change Velocity — Classic
description: Connect to your Sonar instance to retrieve scan results.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [SonarQube, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard SonarQube to DevOps Change Velocity — Classic

Connect to your Sonar instance to retrieve scan results.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  In the Create DevOps tool form, enter the tool details:

<table id="table_lfh_tr1_fwb"><tbody><tr><td>

Tool name

</td><td>

Name for the tool you're integrating.

</td></tr><tr><td>

Tool integration

</td><td>

Tool to integrate. Select SonarQube.

</td></tr><tr><td>

Tool URL

</td><td>

SonarQube/SonarCloud instance URL.For example,https://sonarcloud.io

 **Note:** Don’t enter the slash \(/\) character at the end of your Sonar tool URL.

</td></tr><tr><td>

Tool password / Access token

</td><td>

SonarQube user token

</td></tr><tr><td>

Use MID Server

</td><td>

MID Server is optional. Select MID Server for an on-premises tool that is attached to a MID Server. The Application value is automatically set to DevOps and the Capability value is set to REST. For more information, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>3.  Click **Submit** to connect to your Sonar instance.

4.  On successful tool creation, you're taken to the tool record page.
5.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.


## What to do next

-   [Configure SonarQube scans on Azure DevOps pipelines](config-sonarqube-azure-devops.md)
-   [Configure SonarQube scans on Jenkins pipelines](config-sonarqube-jenkins-devops.md)

**Parent Topic:**[SonarQube integration with DevOps Change Velocity](../concept/sonarqube-devops-integration-devops.md)

