---
title: Cloud credentials
description: Cloud credential types manage access to cloud-based applications, including Amazon Web Services and the Microsoft Azure cloud.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# Cloud credentials

Cloud credential types manage access to cloud-based applications, including Amazon Web Services and the Microsoft Azure cloud.

## AWS Identity and Access Management \(IAM\) roles

If you have a MID Server installed on Amazon EC2 in an AWS cloud, and if that MID Server is configured to discover resources within the cloud, you can use security credentials provided by AWS Identity and Access Management \(IAM\) roles rather than credentials managed on your instance. These AWS credentials grant permissions in the cloud through an instance profile, based on roles. These credentials are temporary and rotate automatically on a configurable interval. When an IAM role is defined on the MID server. For details, see [Configure the MID Server for AWS IAM roles](https://www.servicenow.com/docs/access?context=config-mid-iam-roles&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

Discovery ignores any credentials stored on the instance in favor of the credentials granted by the role in the instance profile. For more information on AWS instance profiles, see [IAM Roles for Amazon EC2](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html).

## AWS credentials

<table id="table_jsq_gxn_jw"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for the AWS credentials.

</td></tr><tr><td>

Active

</td><td>

Option to use the credential.

</td></tr><tr><td>

Access Key ID

</td><td>

The **Access key ID** that you generated on the AWS Management Console, such as: APIAIOSFODNN7EXAMPLE.

</td></tr><tr><td>

Secret access key

</td><td>

The **Secret access key** that you generated on the AWS Management Console, such as: wPalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY.

</td></tr></tbody>
</table>## Azure Service Principal credential form fields

<table id="table_ozx_ggc_lhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the service principal to register with the instance.

</td></tr><tr><td>

Tenant ID and

</td><td>

Paste the Azure **Directory ID** value from the Azure portal into the Cloud Management **Tenant ID** field.

</td></tr><tr><td>

Client ID

</td><td>

Paste the Azure **Application ID** value of the application that you registered in Azure into the Cloud Management **Client ID** field.

</td></tr><tr><td>

Authentication Method

</td><td>

Select **Client secret**.**Note:** **Client assertion** is not supported.

</td></tr><tr><td>

Secret key

</td><td>

Paste the secret key that was generated while creating the Azure Service Principal.This field appears when **Authentication method** is **Client secret**.

</td></tr></tbody>
</table>## Azure Enterprise Agreement credentials

Azure Enterprise Agreement credentials are necessary for the billing functionality that the Cloud Management application provides.

|Field|Description|
|-----|-----------|
|Name|Enter a descriptive name.|
|Enrollment number|Enter the enrolment number from Azure.|
|Access Key|Paste the access key that Azure provides.|

## Cloud Management credentials

This credential type is available for Orchestration.

<table id="table_CloudManagementCredentialsForm"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential. For example, you might call it **Cloud Atlanta**.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

Type

</td><td>

Specify **AWS**.

</td></tr><tr><td>

User name

</td><td>

Enter the CIM user name to create in the Credentials table. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name.

</td></tr><tr><td>

Password

</td><td>

Enter the CIM password.

</td></tr><tr><td>

SSH Passphrase

</td><td>

Enter a memorable phrase for key generation. For example, you might enter **Friday is a good day**.

</td></tr><tr><td>

SSH private key

</td><td>

Enter the SSH private key.

</td></tr><tr><td>

Authentication protocol

</td><td>

Select the **MD5**or **SHA** authentication protocol that was used to generate the **Authentication Key**.

</td></tr><tr><td>

Authentication Key

</td><td>

Enter a SSH-generated authentication key.

</td></tr><tr><td>

Privacy protocol

</td><td>

Enter one of the following privacy protocols that describes encryption for the **Privacy Key**: -   **3DES** for Triple Data Encryption Standard \(DES\)
-   **AES128** for Advanced Encryption Standard \(AES\) with 128 bit encryption
-   **AES192** for AES with 192 bit encryption
-   **AES256** for AES with 256 bit encryption
-   **DES** for legacy DES encryption

</td></tr><tr><td colspan="2">

Enter an additional privacy key.

</td></tr><tr><td>

Credential alias

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. Currently, the only supported external storage system is CyberArk.

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

Classification

</td><td>

Enter the Application Classification for CI discovery.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>## Cloud Management \(CMP\) node credentials

Cloud Management \(CMP\) node credentials associate credentials for a virtual server that Cloud Management provisions. The Cloud Management application automatically creates these credentials.

**Note:** You might need to deactivate these credentials if you no longer want them used, change the order precedence, or select a MID Server that is allowed to access them. Otherwise, you do not need to manually create or modify this type of credential.

<table id="table_ngl_y4j_kz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The automatically generated name based on the datacenter where the virtual machine is located.

</td></tr><tr><td>

Active

</td><td>

If the credentials are active.

</td></tr><tr><td>

Applies to

</td><td>

Choose whether this credential is available to a specific MID Server or a all MID Servers.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

User Name and Password

</td><td>

The virtual server user name and password.

</td></tr><tr><td>

SSH passphrase and SSH private key

</td><td>

The private key and the passphrase that protects the key if the virtual server requires it.

</td></tr><tr><td>

Authentication Protocol and Authentication Key

</td><td>

The private key and the passphrase that protects the key if the virtual server requires it.

</td></tr><tr><td>

Privacy Protocol and Privacy Key

</td><td>

The encryption protocol used with the virtual server and enter the privacy key.

</td></tr><tr><td>

Credential alias

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.

</td></tr></tbody>
</table>## Cloud Management \(CMP\) SSH key pair credentials

Cloud Management \(CMP\) SSH key pairs store the keys that the Cloud Management application automatically generates when users provision stack resources.

**Note:** You might need to deactivate these credentials if you no longer want them used. Otherwise, you do not need to manually create or modify this type of credential.

|Field|Description|
|-----|-----------|
|Name|The automatically generated name.|
|Active|If the credentials are active.|
|SSH Public Key|The public key.|
|SSH Private Key|A secure private key that can be used instead of a password for SSH logins.|

