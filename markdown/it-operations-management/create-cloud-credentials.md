---
title: Create cloud credentials
description: Create cloud credentials to manage access to cloud-based applications, including Amazon Web Services, Microsoft Azure, and Google Cloud. Discovery uses these credentials to connect to your cloud provider accounts and discover cloud resources.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 4
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console for Discovery, Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Create cloud credentials

Create cloud credentials to manage access to cloud-based applications, including Amazon Web Services, Microsoft Azure, and Google Cloud. Discovery uses these credentials to connect to your cloud provider accounts and discover cloud resources.

## Before you begin

Verify the following:

-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Now Assist for Setup](install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](install-now-assist-itom.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](access-itom-config-console-disco.md).

Role required: discovery\_admin

## About this task

Cloud credentials store the authentication information that Discovery needs to access your cloud provider accounts. Before you create cloud credentials, verify that you have the required access and permissions configured in your cloud provider environment. The specific configuration requirements vary by cloud provider.

For more information about cloud provider setup and permissions, see [Discovery for cloud environment](../../discovery/concept/cloud-discovery-wizard.md).

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Discovery Setup**.

2.  Select **Cloud credentials**.

3.  From the **Credential type** drop-down list, select a credential type.

    The following credential types are available for Cloud credentials.

    |Credential type|Description|
    |---------------|-----------|
    |[Alibaba Cloud API](../../discovery/task/create-alibaba-cloud-api-credentials.md)|API credentials for discovering Alibaba Cloud resources. Requires an AccessKey ID and AccessKey secret from the Alibaba Cloud Console.|
    |[AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_CloudManagementCredentialsForm.md)|Credentials for discovering Amazon Web Services cloud resources.|
    |[AWS SSM Instance User](../../discovery/task/configure-custom-user-credentials.md)|User credentials for AWS Systems Manager \(SSM\) Agent discovery on EC2 instances. Requires only a user name for the alternate user credential configured on the EC2 instance.|
    |[Azure Enterprise Agreement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_CloudManagementCredentialsForm.md)|Credentials for Azure Enterprise Agreement enrollments.|
    |Azure SAS|Credentials that use a shared access signature token for Azure storage access.|
    |[Azure Service Principal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_CloudManagementCredentialsForm.md)|Service principal credentials for Azure cloud discovery. Requires a tenant ID, client ID, and secret key from the Azure portal.|
    |[Azure SSH Certificate](../../discovery/task/azure-cloud-disc-ssh.md)|SSH certificate credentials for discovering Azure Linux virtual machines. Requires a linked Azure Service Principal credential.|
    |[Cloud Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_CloudManagementCredentialsForm.md)|General credentials for cloud management operations.|
    |[CloudFoundry](../../service-mapping/concept/pivotal-cloud-foundry.md)|Credentials for Cloud Foundry environments.|
    |[Google API](../../discovery/reference/google-api-credentials-form.md)|API credentials for Google Cloud services.|
    |Google Cloud|Credentials for discovering Google Cloud Platform resources.|
    |[IBM](../../service-mapping/reference/ibm-cloud-platform-discovery.md)|Credentials for discovering IBM Cloud Platform resources. Requires a SoftLayer API user and key, or a Bluemix API key.|
    |[OpenStack](../../service-mapping/reference/openstack-discovery.md)|Credentials for OpenStack cloud environments.|
    |[Oracle API](../../it-operations-management/task/create-oracle-api-credentials.md)|API credentials for Oracle Cloud Infrastructure discovery.|
    |[oVirt](../../service-mapping/reference/red-hat-virtualization-discovery.md)|Credentials for oVirt virtualization environments.|
    |[VMWare](../../discovery/concept/vmware-cloud-discovery.md)|Credentials for VMware vCenter cloud environments.|

4.  Select **Create new**.

5.  Complete the form.

    The fields in the form vary based on the credential type that you selected. The following fields appear in most credential types.

<table id="table_lxx_t5x_bjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for the credential.

</td></tr><tr><td>

User name

</td><td>

Enter the user name for this credential. Avoid leading or trailing spaces in user names.

</td></tr><tr><td>

Active

</td><td>

Select this check box to make the credential available for Discovery.

</td></tr><tr><td>

Credential alias

</td><td>

Select a credential alias to associate with this credential. Credential aliases enable you to define a credential once and reference it across multiple configurations.

</td></tr><tr><td>

Order

</td><td>

Enter the sequence in which Discovery tries this credential when it attempts to log in to devices. The smaller the number, the higher the priority. If all credentials have the same order number, Discovery tries them in a random order.**Note:** Establish credential order when you use large numbers of credentials or when security policies lock out users after failed login attempts.

</td></tr></tbody>
</table>6.  Select **Submit**.

    You're returned to the Cloud credentials page.

7.  To complete the setup, select **Mark as configured**.


**Related topics**  


[Get started with credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/credentials-getting-started.md)

