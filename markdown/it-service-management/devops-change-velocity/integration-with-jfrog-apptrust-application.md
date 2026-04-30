---
title: Integration with JFrog AppTrust application
description: Integrate DevOps Change Velocity with JFrog AppTrust applications to automate change request creation, approval, and evidence collection as application versions are promoted through life-cycle stages.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-02-25"
reading_time_minutes: 4
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Integration with JFrog AppTrust application

Integrate DevOps Change Velocity with JFrog AppTrust applications to automate change request creation, approval, and evidence collection as application versions are promoted through life-cycle stages.

Install the JFrog plugin \(x\_snc\_jfrog\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## JFrog AppTrust overview

JFrog AppTrust is an application risk governance solution containing applications. Within each application, administrators define a software development life-cycle as a sequential set of stages such as Development, QA, Staging, and Production, through which application versions are promoted. When a new version is built, it can be advanced from one life-cycle stage to the next through a process called promotion. Promotions can be subject to change control using DevOps Change Velocity.

## Tool record

-   **Connect**

    The JFrog tool must be connected using bearer token credentials. This connection enables the following capabilities:

    -   Discovery of JFrog projects within your instance.
    -   Re-configuration of webhooks that are already existing.
    -   Association of ServiceNow business applications with JFrog AppTrust applications to configure new webhooks for projects.
    -   Enabling of change control for application promotion.
    **Note:** For information on connecting a JFrog tool, see [Onboard JFrog to DevOps Change Velocity — Workspace](../task/devops-jfrog-connect-workspace.md).

-   **Permission checks**

    The bearer token must have the required permissions for seamless discovery and import of tool objects. The permission check verifies access to the following objects:

    |Object|Permissions Required|Impact|
    |------|--------------------|------|
    |Artifact repository|Read access to artifact repositories|Required to retrieve artifact details such as artifact name, version, and metadata|
    |Project|Read access to JFrog projects|Required to discover and list available projects in the JFrog instance|
    |Build|Read access to build information|Required to retrieve build details associated with artifacts for change request evidence|

-   **Discover Projects**

    Once the tool is connected and permissions are verified, ServiceNow discovers the JFrog projects available in your instance. During discovery, ServiceNow queries the JFrog API to retrieve the list of projects and imports them as DevOps tool objects.

-   **Configure webhooks at project level**

    To configure new webhooks for a project, you must associate the ServiceNow business application with the JFrog AppTrust application. For more information, see [Associate business application](../task/associate-business-application.md).

-   **Configure webhooks at tool level**

    Once the projects are configured, you can automatically re-configure webhooks for the configured projects by selecting the **Auto configure with new token** button in the tool record. This action configures all previously configured JFrog projects with a new token. Webhooks enable JFrog to send real-time event notifications to ServiceNow, such as when an application version is promoted to a new life-cycle stage.

-   **Project tab**

    Use the **Project** tab in the tool record to associate ServiceNow business applications with JFrog AppTrust applications. This association ensures that change requests created during promotions are linked to the correct business application in ServiceNow, enabling accurate tracking and governance.

    To associate a business application, select a discovered project and map it to the appropriate ServiceNow business application. For detailed instructions, see [Associate business application](../task/associate-business-application.md).


## Change creation

When an application version is promoted to a new stage in JFrog, the integration with DevOps Change Velocity \(DCV\) automatically creates a change request in ServiceNow, populated with the required evidences.![ServiceNow Change request added in JFrog stage](../image/jfrog-lifecycle-change.png)

In JFrog, change request creation can be enabled for a stage in the AppTrust Integrations page. ![Change request creation settings in JFrog](../image/jfrog-change-creation.png)

Once the change request is reviewed and approved in ServiceNow, the approval is passed back to JFrog, which then automatically promotes the application version to the new stage.

## Change policy

You can add change approval policies to the model you created for JFrog change requests. For information on creating change approval policies, see [Creating change approval policies](../../change-management/concept/using-change-approval-policies-cf.md).

In the change policy, to retrieve the evidence associated with a JFrog change request, you can use the JFrog Fetch evidences flow action. This flow action collects the relevant evidence data such as artifact promotion details from JFrog and attaches it to the corresponding change request. You can incorporate this flow action into your change policy's approval workflow to ensure that the required evidence is available before the change request is approved or moved forward.

## Digital signature verification

ServiceNow supports digital signature verification to ensure the integrity and authenticity of application artifacts. A public key is required to verify digital signatures associated with an AppTrust application in JFrog. This verification ensures that artifacts have not been tampered with during the promotion process. You must first generate a key with the sn\_kmf.cryptographic\_manager role. Perform the following steps to generate a key:

1.  Navigate to the **Key Management Framework \(KMF\)** module in your ServiceNow instance.
2.  Select the **x\_snc\_jfrog.signing\_key** module.
3.  Generate the key.
4.  Export the key from your JFrog instance.
    1.  In your JFrog instance, navigate to **Administration &gt; Security &gt; Keys Management**.
    2.  Look for the public key associated with your AppTrust configuration.
    3.  Export or copy the public key from this section.

-   **[Associate business application](../task/associate-business-application.md)**  
Associate a business application with a JFrog project in the JFrog tool record to create an AppTrust application in JFrog.

**Parent Topic:**[JFrog integration with DevOps Change Velocity](devops-jfrog-integration.md)

