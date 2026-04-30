---
title: Classifying licenses and resolving component licenses in the Software Bill of Materials workspace
description: Classify licenses and resolve \(match\) them to components, or create licenses in the License administration module in the SBOM workspace. Classifying and matching licenses to your components permits you determine your license compliance for the proprietary, open-source, and vendor-supplied software components you upload in your SBOM files.
locale: en-US
release: yokohama
product: SBOM Core
classification: sbom-core
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Uploading and viewing your SBOM files in the SBOM Workspace, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Classifying licenses and resolving component licenses in the Software Bill of Materials workspace

Classify licenses and resolve \(match\) them to components, or create licenses in the License administration module in the SBOM workspace. Classifying and matching licenses to your components permits you determine your license compliance for the proprietary, open-source, and vendor-supplied software components you upload in your SBOM files.

## License data and third-party software

As organizations build more of their own software applications, they are using open-source components and vendor-supplied software. Using third-party and open-source components provide you with many advantages for the rapid creation and release of your software projects, however, using these components comes with licensing risks:

-   Open-source and vendor-supplied software components at times have dependencies on other components, and each component might have its own licensing requirements.
-   If you’re not compliant with the terms of your licenses for the components and software in your applications, you might inadvertently ship code that violates your internal policies and regulatory licensing requirements.

## The License administration module

The License administration module in the SBOM Workspace permits you to perform the following tasks.

-   Classify licenses that require it for the components you upload with your SBOM files.
-   Resolve each license you classify to a specific component.
-   See what percentage of the components you are using are out of compliance on a data visualization on the Home page. You can use this information to help you determine your overall security posture and potential risk exposure.

If the SBOM files you upload include license information, the license database grows automatically as unique licenses are observed on each SBOM upload. With each SBOM upload, you can build a database of uploaded licenses and then classify them if necessary with the License administration module in the SBOM Workspace. You build an inventory of licenses so that you can assign them to components after you classify them in one of the following categories:

-   Permitted
-   Restricted
-   Banned
-   Unclassified

Legal personnel, license managers, compliance, and regulatory managers perform tasks in the License administration module.

## Viewing uploaded license data

You have the following options to view any license information you've uploaded with your components in the SBOM Workspace.

-   Navigate to **Workspaces** &gt; **SBOM Workspace** &gt; **Components**.

    On the Components page the License classification of components card displays a visualization of your overall license compliance with the following categories.

    |Category|Description|
    |--------|-----------|
    |Banned|Licensed usage is not permitted.|
    |Classification required|License is not yet classified and requires a review.|
    |Permitted|Licensed usage is permitted without restriction.|
    |Restricted|Licensed usage is not permitted in specific use cases.|

    This snapshot uses the classifications and resolved license information you enter in the License administration module to calculate your over-all license compliance.

    If you select a component record from this list, you can view the component's license information along with other information in the State field.

-   Alternatively, navigate to **Workspaces** &gt; **SBOM Workspace** &gt; **License administration** &gt; **License classification**.

    This page tracks the total number of unique licenses that have been detected from the SBOM files you’ve uploaded. It also filters them in cards along the top of the page in the following categories.

    -   Unclassified - License requires review and classification.
    -   Banned - License usage is not permitted.
    -   Restricted - License is not permitted in specific use cases.
    -   Permitted - License usage is permitted without restriction.
    -   All licenses - Total count of licenses.
    All the components in your organization are using one of the licenses that is listed on this page. When a new license is detected from an SBOM upload, a record is created and stored in the SBOM license \[sn\_sbom\_license\] table and added to this list. It’s classification by default is, **Classification Required**. License records in this state must be reviewed and classified before you can resolve \(match\) them to components so your overall license compliance is accurately calculated.

    For information on how to classify licenses, see [Classify imported licenses in the Software Bill of Materials Workspace](../task/vr-sbom-classify-license.md).


## Roles

New licenses must be classified by a user with the sn\_sbom\_response.managelicense role. This user views uploaded license information and determines which licenses are permitted and which are banned. Users with this role cannot view the Component license resolution module unless they have the sn\_sbom\_response.licenseresolver role.

After classification, licenses must be resolved by a user with the sn\_sbom\_response.licenseresolver role so that your over-all license compliance can be determined. This user resolves licenses to components. Users with this role cannot view the License Classification module unless they have the sn\_sbom\_response.managelicense role.

Classifying new license information is an ongoing process. You might prefer to keep the total number displayed on the Unclassified card low. As a license manager, you might prefer to check for licenses that need classification every few days and after you upload SBOM files.

As a license resolver, you might prefer to check for updated classified licenses every few days.

