---
title: Client software distribution extension points
description: The client software distribution \(CSD\) extension points create the customization code for the specific provider and the extension keys.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client software distribution extension framework, Client Software Distribution, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Client software distribution extension points

The client software distribution \(CSD\) extension points create the customization code for the specific provider and the extension keys.

The purpose of the extension points is to associate extension keys with a specific provider, and then create a script that sets input variables for your custom deployment and revocation workflows. Another extension point script tells CSD if the provider has the capability to revoke software. If this is the case, CSD enables the UI action that triggers revocation from the provider.

## SetDeploymentData

The script associated with this extension key must set the **csdExtensionResult** object with these attributes:

-   **deploymentWorkflowInputs**: Object that specifies the deployment workflow input variables.
-   **softwareModel**: Software model sys\_id.
-   **deploymentType**: An integer. Use **1** for deployment to a user and **2** for deployment to a device.
-   **softwareApplication**: Software application sys\_id.

## CheckRevocable

The script associated with this extension key gets the input parameter **csdExtensionInputs.softwareConfiguration**, which is a Client Software Distribution record in the Software Configuration \[sn\_client\_sf\_dist\_software\_config\] table. All providers' software configurations are extended from this table, but may have different attributes.

This script must set the **csdExtensionResult** object to **true** or **false**, depending on whether the software configuration specifies uninstallation.

## SetRevocationData

The script associated with this extension key gets the input parameter **csdExtensionInputs.softwareConfiguration**, which is a Client Software Distribution record in the Software Configuration \[sn\_client\_sf\_dist\_software\_config\] table. All providers' software configurations are extended from this table, but may have different attributes.

The script must set the **csdExtensionResult** object with these attributes:

-   **revocationWorkflowInput**: Object that specifies the revocation workflow input variables.
-   **softwareModel**: Software model sys\_id.
-   **deploymentType**: An integer. Use **1** for deployment to a user and **2** for deployment to a device.

**Parent Topic:**[Client software distribution extension framework](../concept/c_CSDExtensionFramework.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

