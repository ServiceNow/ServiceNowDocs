---
title: Build a Cloud Provisioning blueprint
description: Use the blueprint designer to create custom blueprints for the Cloud Provisioning and Governance application. Blueprints are deprecated in the Orlando release.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Cloud Provisioning Blueprints, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Build a Cloud Provisioning blueprint

Use the blueprint designer to create custom blueprints for the Cloud Provisioning and Governance application. Blueprints are deprecated in the Orlando release.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

**Note:**

-   Starting with Orlando, Cloud Provisioning blueprints are available on instances upgraded from a previous release but you cannot create new blueprints. Existing blueprints and catalog items from those blueprints remain unaffected and continue to work.
-   Use Cloud Provisioning cloud templates to create catalog items in place of blueprints. Cloud Provisioning [cloud templates](create-cloud-template.md) allow you to ingest Azure ARM, AWS CFT, Google Deployment Manager \(GDM\) and Terraform specification syntax in cloud catalog items to run your cloud deployment orchestration.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Blueprints**.

2.  Click **New**, enter a unique and meaningful **Name** and **Description**, and then specify the service **Category**.

    Several categories are provided by default.

3.  Click **Submit**.

    The system creates the blueprint record and displays the Deployment Model tab of the blueprint designer. The Deployment Model tab is a visual canvas where you drop resource blocks. Each resource block represents a CI in a multi-tier application stack. The Deployment Model specifies the resources and connections between resources for the cloud items that you are defining.

    ![Blueprint operations](../image/blueprint-operationstab.png)

4.  To add a resource to the deployment model, click **Resources** and then select the resource from the list.

    The resources appear on the canvas. Move the resource to an appropriate location for the model that you have in mind. Add as many resources as needed.

5.  Connect the container resource to the first resource to deploy.

    To create a connection between resources, select the parent resource, click the connection pad in the resource, and then drop the connection in any resource with a dotted outline. The system does not allow certain connections \(for example, an AWS datacenter cannot host an ARM resource\).

6.  Add and connect all resources that make up the blueprint.

    You must add and connect all resources before you configure operations and attributes in the **Operations** section. As you update the resources in the Deployment Model tab, the system generates the Cloud Template: a complete representation of the blueprint in YAML script. You can export the Cloud Template representation of the deployment model and later import it into the Cloud Provisioning and Governance application on another instance.

7.  Configure the operations that the system performs on the resources and the attributes to use while performing the operations.

    By default, **Provision**, **Stop**, **Start** and **Deprovision** operations are provided. You can either select an existing operation or create a new blueprint operation.

    -   Select an existing operation: In the **Operations** section, select the **Provision** operation check box and click **Provision** to view a graph. You can rearrange the graph by deleting and adding operations. You can click **Optimize All Plans** for the Cloud Provisioning and Governance application to suggest an optimized plan for you. The Cloud Provisioning and Governance application looks at the blueprint you created and based on the attributes, the mappings, and the dependencies of each resource, suggests an optimized plan to execute. All the attributes for the **Provision** operation appear in the window. You can select or de-select any attribute. Once you configured the **Provision** operation, you can select the next operation and configure its attributes as needed.
    -   Create a new blueprint operation: Click **New** in the **Operations** section. The New Blueprint Operation dialog box appears. Enter a name, select an operation type, enter input parameters for the new operation, and click **Save**. The new blueprint operation appears in the **Operations** section.
8.  If you have completed the design of the blueprint and you do not want to configure the blueprint any further, click the **Draft** toggle button to publish the blueprint.

    A message appears saying that your blueprint has been published. To continue configuring the blueprint, then skip this step.

9.  To configure parameters such as variable sets, rules, life cycle operations for the blueprint catalog item, click the **Catalog** tab and then click the catalog.

    The Cloud Catalog Item screen appears.

10. Click **Update** if you made any changes to the form.

11. Click **Publish** to publish the blueprint.

    To view all published catalog items, click **Published** in the Blueprints landing page.


-   **[Add a resource operation to the execution plan](add-resource-operation-cmp.md)**  
The base system includes a large set of predefined resource operations. Rarely, you might add a custom operation for a resource.
-   **[Execute blueprint operations in parallel](execute-blueprint-operations-parallel.md)**  
You can execute your blueprint resource operations to run in a linear or in a parallel way.
-   **[Blueprint attributes](../reference/blueprint-attributes.md)**  
When you add a blueprint operation to a resource, the system adds the appropriate attributes. You can choose whether or not to make the attributes available as catalog properties on the form when the system performs the operation.
-   **[Configure a blueprint rule](configure-a-blueprint-rule.md#)**  
Configure a rule that contains actions the system can take on blueprint attributes.

**Parent Topic:**[Cloud Provisioning Blueprints](../concept/blueprints.md)

**Related topics**  


[Form configuration with blueprints](../concept/blueprint-form-configuration.md)

