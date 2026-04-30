---
title: Create a JavaScript function in Microsoft Azure using Visual Studio Code
description: To use Power Virtual Agents with Virtual Agent Bot Interconnect, you must create a JavaScript function in Microsoft Azure using the sample code files in Bot Interconnect.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a JavaScript function in Microsoft Azure using Visual Studio Code

To use Power Virtual Agents with Virtual Agent Bot Interconnect, you must create a JavaScript function in Microsoft Azure using the sample code files in Bot Interconnect.

## Before you begin

You will need a Microsoft Azure account.

Role required: admin

## Procedure

1.  Sign into Microsoft Azure and create a JavaScript function.

    This involves configuring your environment and creating a local project. Refer to the [Microsoft documentation](https://docs.microsoft.com/en-us/azure/azure-functions/create-first-function-vs-code-node) for details.

2.  Go to [Create an Azure Function for Microsoft Power Virtual Agents as Secondary bot with ServiceNow Bot Interconnect setup \(KB1112368\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1112368), and then do the following:

    1.  Copy the code in the attached `index.txt` file into the `index.js` file in your Azure project.

    2.  Copy the code in the attached `function.txt` file into the `function.json` file in your Azure project.

    3.  Save both files.

3.  Install the **request-promise** libraries.

    1.  In a command line window, change directories to the folder where you created the Azure project.

        For example, enter `cd DemoAzureFunction`.

    2.  At the prompt, enter: `npm install --save request`

    3.  At the prompt, enter: `npm install --save request-promise`

    The dependencies are added to the `package.json` file in your project.

    ![The request and request-promise libraries are included as dependencies in your project, as "request" and "request-promise."](../images/va-api-azure-libs-package-json.png)

4.  Deploy the project to Azure as described in the [Microsoft documentation](https://docs.microsoft.com/en-us/azure/azure-functions/create-first-function-vs-code-node).

5.  From the Azure portal, navigate to **All Resources**.

6.  Select the name of the function app that you've created.

7.  On the Overview page, select the function you've created in the Functions tab, and copy the function URL from the Get function URL option.

    The Azure function URL will be used as the secondary bot endpoint in your ServiceNow instance.

    ![Copy the function URL in the Get Function URL subtab of the selected function. The example reads, "https://appname.azurewebsites.net."](../images/va-api-azure-app-url.png)


**Parent Topic:**[Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ms-powerva.md)

**Previous topic:**[Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ms-powerva.md)

**Next topic:**[Locate and copy the Direct Line secret key in Microsoft Power Virtual Agents](get-dl-secret-key-mspva.md)

