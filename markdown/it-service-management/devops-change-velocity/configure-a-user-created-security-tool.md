---
title: Configure user-created security tool
description: Connect your custom security tool that is integrated with your CI/CD pipelines to DevOps Change Velocity to retrieve security scan results.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [DevOps user-created security tool integration, User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure user-created security tool

Connect your custom security tool that is integrated with your CI/CD pipelines to DevOps Change Velocity to retrieve security scan results.

## Before you begin

You must create the application vulnerability integration by following the step-by-step instructions in the [Configure DevOps with Application Vulnerability Response for better visibility into CI/CD pipeline \[KB1441741\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1441741) enablement guide. This is a required pre-requisite setup to onboard your custom security tool from DevOps Change Velocity.

Role required:

-   Developer role for the scoped app
-   DevOps admin role

**Note:** When creating an integration as a scoped app, the system admin must assign these roles to the integration developer, so the integration developer is able to create tool integration and integration capability records for the specific scope.

## Procedure

1.  Navigate to **DevOps &gt; Integrations &gt; Tool Integrations** and create a record to define the tool you are integrating.

2.  Select **Create manually**, and enter the following values in the form fields.

    |Field|Value|
    |-----|-----|
    |Tool label|Name of the tool integration.|
    |Integration version|Version of the tool integration.|

    ![Tool integration record for custom security tool integration](../image/custom-sec-tool-01.png)

3.  Select **Submit**.

4.  Open the newly created tool integration and navigate to the Tool Integration Capability Mappings related list.

5.  Select **New**, and enter the following values in the form fields.

    |Field|Value|
    |-----|-----|
    |Tool integration|Sample tool|
    |Tool type capability|Security|

    ![Tool Integration Capability Mapping record for custom security tool integration](../image/custom-sec-tool-02.png)

6.  Select **Submit**.

7.  Navigate to the Integration Capabilities related list, and select **New**.

8.  Create the **Connect** and **Validate** records by entering the following values in the form fields.

<table id="simpletable_qll_1nf_cyb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Tool integration

</td><td>

Sample Code Tool

</td></tr><tr><td>

Capability mapping

</td><td>

Capability mapping record created in step 6.

</td></tr><tr><td>

Action

</td><td>

Connect**Note:** Do not edit tool action records.

</td></tr><tr><td>

Active

</td><td>

Selected

</td></tr><tr><td>

Timeout \(ms\)

</td><td>

Timeout for the corresponding subflow. If execution of the subflow exceeds this value, a timeout exception occurs. Value is in milliseconds \(ms\). Default is 45,000 \(45 seconds\).

</td></tr><tr><td>

Subflow name

</td><td>

-   For Connect: sn\_devops\_vul\_ints.security\_tool\_connect
-   For Validate: sn\_devops\_vul\_ints.security\_tool\_validate


</td></tr><tr><td>

Domain

</td><td>

global

</td></tr></tbody>
</table>    ![Integration capability record for connect action](../image/custom-sec-tool-03.png)![Integration capability record for validate action](../image/custom-sec-tool-04.png)

9.  Open the newly created tool integration record and add the **SecOps source integration** and **Integration handler** name fields to the form by navigating to **Configure &gt; Form layout**.

    In the tool integration form, enter the following values for these fields.

    -   SecOps source integration: Select the source integration that is created in the Third Party Integrations \(sn\_sec\_int\_integration\) table as described in the **Configuration page &gt; Steps to create a configuration** section in the [Configure DevOps with Application Vulnerability Response for better visibility into CI/CD pipeline \[KB1441741\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1441741) enablement guide.
    -   Integration handler name: sn\_devops\_vul\_ints.DevOpsSecurityToolIntegrationHandler
10. Ensure that "Tool Integration name" DevOps Integration \(example: Veracode DevOps Integration\) is created in the Application Vulnerability Integration \(sn\_vul\_app\_integration\) table and mapped to the source integration that is created in the Third Party Integrations \(sn\_sec\_int\_integration\) table as described in the **Configuration page &gt; Steps to create a configuration** section in the [Configure DevOps with Application Vulnerability Response for better visibility into CI/CD pipeline \[KB1441741\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1441741) enablement guide.


## What to do next

By default, when you onboard your tool from workspace, you have to enter the mandatory fields as defined in the Configuration Page section in the [Configure DevOps with Application Vulnerability Response for better visibility into CI/CD pipeline \[KB1441741\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1441741) enablement guide. Not all the mandatory fields are credential fields. In the base system, all the mandatory fields are displayed while updating credentials. If you want to update the credentials for this tool when the credentials have expired, you may not want to enter all the mandatory fields. To configure the mandatory fields that you want to show in the Update credentials page, perform the following steps.

1.  Navigate to **Now Experience Framework &gt; Experiences**.
2.  Select **DevOps Change Workspace**.
3.  On the UX Page Properties related list, select **securityToolsUIConfig**.
4.  Add the following entry to the JSON.

    ```
    <tool_integration_sys_id> : { 
       "CREDENTIAL_PAGE": { 
          "FIELDS_TO_SHOW": [ 
             "<parameter_1>", 
             "<parameter_2>"     
                        ] 
      } 
    } 
    ```

    ![JSON entry in the securityToolsUIConfig UX page property](../image/cus-sec-tool-05.png)


**Parent Topic:**[DevOps user-created security tool integration](../concept/devops-security-tool-integration.md)

