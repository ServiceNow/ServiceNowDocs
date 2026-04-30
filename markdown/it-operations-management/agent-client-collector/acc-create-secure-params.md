---
title: Create secure parameters for a check
description: When creating a check definition or check instance, you can configure the parameters you want to be secured when the agent executes the check. During check execution, the secured parameters are obfuscated, securing their information. Only credential information is obfuscated.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Collect data from your system devices, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Create secure parameters for a check

When creating a check definition or check instance, you can configure the parameters you want to be secured when the agent executes the check. During check execution, the secured parameters are obfuscated, securing their information. Only credential information is obfuscated.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Check Definitions**.

2.  Select a check definition from the displayed list.

    The **Check Definition** page for the selected check appears.

3.  Scroll to the bottom of the page and select the **Check Secure Parameter Definitions** tab.

4.  Click **New**.

    The **Check Secure Parameter Definition New Record** page appears.

    ![Check Secure Parameter Definition New Record page](../image/ACC-Check-Secure-Parameter.png)

5.  Configure the fields on the page.

<table id="choicetable_jz2_g32_1mb"><thead><tr><th align="left" id="d589138e112">

Field Name

</th><th align="left" id="d589138e115">

Description

</th></tr></thead><tbody><tr><td id="d589138e121">

**Name**

</td><td>

The name of the parameter, formatted as a reference prefix. For example, `cred_` is a reference prefix for the credentials table.

</td></tr><tr><td id="d589138e133">

**Check Definition**

</td><td>

The name of the check definition connected to the parameter.

</td></tr><tr><td id="d589138e142">

**Order**

</td><td>

A number indicating the order in which the parameter is sent to the check command/script. For example, if you configure the following parameters:-   Name=**cred\_user\_name**, Order=**1**
-   Name=**cred\_password**, Order=**2**
 The **username** parameter is sent first to the standard input, and the **password** parameter is sent second to the standard input.

 The `READ` command is performed first on the **username** parameter and then on the **password** parameter. You can then use **$username** and **$password** in your Bash script.

</td></tr><tr><td id="d589138e202">

**Active**

</td><td>

Select the check box to activate the secure parameter.

</td></tr></tbody>
</table>6.  Click **Submit**.

    The configured parameter appears in the table on the **Check Secure Parameter Definitions** tab.

    Repeat this procedure to enter multiple secure parameters.

7.  Enter the secure parameters into the **Command prefix** field of the check definition.


