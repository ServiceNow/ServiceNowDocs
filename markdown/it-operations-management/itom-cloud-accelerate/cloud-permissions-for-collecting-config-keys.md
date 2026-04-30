---
title: Cloud permissions required to collect the base system Cloud Configuration Governance configuration keys
description: The Cloud Configuration Governance requires appropriate cloud permissions to collect the base system configuration keys from the cloud. Therefore, you must set the appropriate permissions in the cloud to suit the needs of your organization.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud permissions required to collect the base system Cloud Configuration Governance configuration keys

The Cloud Configuration Governance requires appropriate cloud permissions to collect the base system configuration keys from the cloud. Therefore, you must set the appropriate permissions in the cloud to suit the needs of your organization.

**Note:** Starting with Cloud Configuration Governance version 1.3.7, the base system contents are moved to the CCG Content Pack. Install the CCG Content Pack to access the base system Cloud Configuration Governance contents.

## Amazon Web Services \(AWS\) datacenter

Cloud Configuration Governance uses the following items to collect the configuration key for the AWS datacenter configuration keys:

-   Resource collector: Cloud Service Account
-   Cloud API used: Action: DescribeRegions
-   Cloud permission: **ec2: DescribeRegions**

|Configuration key|Data type|
|-----------------|---------|
|**AWS:EC2:VM:DescribeRegions**|**String**|

## AWS Identity and Access Management \(IAM\) users

Cloud Configuration Governance uses the following items to collect the configuration key for the AWS IAM user configuration keys:

-   Resource collector: AWS IAM User Data Collector
-   Cloud API used:
    -   Action: GetCredentialReport and GenerateCredentialReport
    -   Service: **AWS IAM service**
-   Cloud permission: **Iam:GetCredentialReport** and **Iam:GenerateCredentialReport**

|Configuration key|Data type|
|-----------------|---------|
|**AWS:IAM:Policy:ARN**|**String**|
|**AWS:IAM:Policy:AttachmentCount**|**String**|
|**AWS:IAM:Policy:CreateDate**|**String**|
|**AWS:IAM:Policy:PolicyName**|**String**|
|**AWS:IAM:Policy:UpdateDate**|**String**|
|**AWS:IAM:User:AccessKey1.active**|**Boolean**|
|**AWS:IAM:User:AccessKey1.lastRotated**|**Date**|
|**AWS:IAM:User:AccessKey1.lastUsedDate**|**Date**|
|**AWS:IAM:User:AccessKey1.lastUsedRegion**|**String**|
|**AWS:IAM:User:AccessKey1.lastUsedService**|**String**|
|**AWS:IAM:User:AccessKey2.active**|**Boolean**|
|**AWS:IAM:User:AccessKey2.lastRotated**|**Date**|
|**AWS:IAM:User:AccessKey2.lastUsedDate**|**Date**|
|**AWS:IAM:User:AccessKey2.lastUsedRegion**|**String**|
|**AWS:IAM:User:AccessKey2.lastUsedService**|**String**|
|**AWS:IAM:User:Certificate1.active**|**Boolean**|
|**AWS:IAM:User:Certificate1.lastRotated**|**Date**|
|**AWS:IAM:User:Certificate2.active**|**Boolean**|
|**AWS:IAM:User:Certificate2.lastRotated**|**Date**|
|**AWS:IAM:User:CreationTime**|**Date**|
|**AWS:IAM:User:LoginProfile.active**|**Boolean**|
|**AWS:IAM:User:MfaEnabled**|**Boolean**|
|**AWS:IAM:User:PasswordEnabled**|**Boolean**|
|**AWS:IAM:User:PasswordLastChanged**|**String**|
|**AWS:IAM:User:PasswordLastUsed**|**Date**|
|**AWS:IAM:User:PasswordNextRotation**|**String**|

## AWS object storage

Cloud Configuration Governance uses the following items to collect the configuration key for the AWS IAM user configuration keys:

-   Configuration collector: AWS S3 Encryption Metric Collector
-   Resource collector: AWS S3 Resource Collector
-   Cloud API used: Action: ListBuckets and GetBucketEncryption on S3 service
-   Cloud permission: **s3:ListBucket** and **s3:GetEncryptionConfiguration**

|Configuration key|Data type|
|-----------------|---------|
|**AWS:S3:Encryption:BucketKeyEnabled**|**Boolean**|
|**AWS:S3:Encryption:KMSMasterKeyID**|**String**|
|**AWS:S3:Encryption:ServerSideEncryptionEnabled**|**Boolean**|
|**AWS:S3:Encryption:SSEAlgorithm**|**String**|

-   Configuration collector: AWS S3 ACL Permission Metric Collector
-   Resource collector: AWS S3 Resource Collector
-   Cloud API used: Action: GetBucketAcl
-   Cloud permission: **s3:GetBucketAcl**

|Configuration key|Data type|
|-----------------|---------|
|**AWS:S3:ACL:AuthnUsersListing**|**Boolean**|
|**AWS:S3:ACL:AuthnUsersReadACL**|**Boolean**|
|**AWS:S3:ACL:AuthnUsersWrite**|**Boolean**|
|**AWS:S3:ACL:AuthnUsersWriteACL**|**Boolean**|
|**AWS:S3:ACL:OwnerFullControl**|**Boolean**|
|**AWS:S3:ACL:OwnerId**|**String**|
|**AWS:S3:ACL:OwnerListing**|**Boolean**|
|**AWS:S3:ACL:OwnerName**|**String**|
|**AWS:S3:ACL:OwnerReadACL**|**Boolean**|
|**AWS:S3:ACL:OwnerWrite**|**Boolean**|
|**AWS:S3:ACL:OwnerWriteACL**|**Boolean**|
|**AWS:S3:ACL:PublicListing**|**Boolean**|
|**AWS:S3:ACL:PublicReadACL**|**Boolean**|
|**AWS:S3:ACL:PublicWrite**|**Boolean**|
|**AWS:S3:ACL:PublicWriteACL**|**Boolean**|

## AWS virtual machine instance

Cloud Configuration Governance uses the following items to collect the configuration key for the AWS virtual machine instance configuration keys:

-   Resource collector: AWS VM Data Collector
-   Cloud API used: Action: DescribeInstances and AWS EC2 resource
-   Cloud permission: **ec2:DescribeInstances**

|Configuration key|Data type|
|-----------------|---------|
|**AWS:EC2:VM:CapacityReservationPreference**|**String**|
|**AWS:EC2:VM:CpuOptionsCoreCount**|**Numeric**|
|**AWS:EC2:VM:CpuOptionsThreadsPerCore**|**Numeric**|
|**AWS:EC2:VM:EbsOptimized**|**Boolean**|
|**AWS:EC2:VM:HardwareType**|**String**|
|**AWS:EC2:VM:ImageId**|**String**|
|**AWS:EC2:VM:InstanceState**|**String**|
|**AWS:EC2:VM:KeyName**|**String**|
|**AWS:EC2:VM:LaunchTime**|**Date**|
|**AWS:EC2:VM:MonitoringState**|**String**|
|**AWS:EC2:VM:Platform**|**String**|
|**AWS:EC2:VM:PrivateDnsName**|**String**|
|**AWS:EC2:VM:PrivateIpAddress**|**String**|
|**AWS:EC2:VM:PublicDnsName**|**String**|
|**AWS:EC2:VM:PublicIPAddress**|**String**|
|**AWS:EC2:VM:SecurityGroups**|**String**|
|**AWS:EC2:VM:SubnetId**|**String**|
|**AWS:EC2:VM:Tags**|**Map**|
|**AWS:EC2:VM:UsageOperation**|**String**|
|**AWS:EC2:VM:VpcId**|**String**|

AWS profile with minimal permissions

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "iam:GenerateCredentialReport",
                "s3:GetEncryptionConfiguration",
                "ec2:DescribeInstances",
                "s3:ListBucketVersions",
                "ec2:DescribeRegions",
                "s3:ListBucket",
                "iam:GetCredentialReport"
            ],
            "Resource": "*"
        }
    ]
}
```

## Microsoft Azure virtual machine instance

Cloud Configuration Governance uses the following items to collect the Azure virtual machine instance configuration keys:

-   Resource collector: Azure VM Data Collector
-   Cloud API used: Microsoft.ResourceGraph/resources
-   Cloud permission: **Microsoft.ResourceGraph/resources**

|Configuration key|Data type|
|-----------------|---------|
|**Azure:VM:HardwareType**|**String**|
|**Azure:VM:NICID**|**String**|
|**Azure:VM:OSDiskCaching**|**String**|
|**Azure:VM:OSDiskCreateoption**|**String**|
|**Azure:VM:OSDiskDeleteoption**|**String**|
|**Azure:VM:OSDiskId**|**String**|
|**Azure:VM:OSDiskName**|**String**|
|**Azure:VM:OSDiskOSType**|**String**|
|**Azure:VM:OSDiskSizeGB**|**String**|
|**Azure:VM:OSProfileAllowExtensionOperations**|**Boolean**|
|**Azure:VM:OSProfileComputerName**|**String**|
|**Azure:VM:OSProfileLinuxConfigurationDisablePasswordAuthentication**|**Boolean**|
|**Azure:VM:OSProfileLinuxConfigurationPatchSettingsAssessmentMode**|**String**|
|**Azure:VM:OSProfileLinuxConfigurationPatchSettingsPatchMode**|**String**|
|**Azure:VM:OSProfileLinuxConfigurationProvisionVmAgent**|**Boolean**|
|**Azure:VM:OSProfileLinuxConfigurationSSHKeyData**|**Map**|
|**Azure:VM:OSProfileLinuxConfigurationSSHPath**|**Map**|
|**Azure:VM:OSProfileRequireGuestProvisionSignal**|**Boolean**|
|**Azure:VM:OSWindowsConfigurationEnableAutomaticUpdates**|**Boolean**|
|**Azure:VM:OSWindowsConfigurationPatchSettingsAssessmentMode**|**String**|
|**Azure:VM:OSWindowsConfigurationPatchSettingsEnableHotpatching**|**Boolean**|
|**Azure:VM:OSWindowsConfigurationPatchSettingsPatchMode**|**String**|
|**Azure:VM:OSWindowsConfigurationProvisionVMAgent**|**Boolean**|
|**Azure:VM:PowerState**|**String**|
|**Azure:VM:ProvisioningState**|**String**|
|**Azure:VM:ResourceGroup**|**String**|
|**Azure:VM:StorageProfileDataDisksCaching**|**String**|
|**Azure:VM:StorageProfileDataDisksCreateOption**|**String**|
|**Azure:VM:StorageProfileDataDisksDeleteOption**|**String**|
|**Azure:VM:StorageProfileDataDisksDetachOption**|**String**|
|**Azure:VM:StorageProfileDataDisksDiskIopsReadWrite**|**String**|
|**Azure:VM:StorageProfileDataDisksDiskMBpsReadWrite**|**String**|
|**Azure:VM:StorageProfileDataDisksDiskSizeGb**|**Numeric**|
|**Azure:VM:StorageProfileDataDisksImage**|**String**|
|**Azure:VM:StorageProfileDataDisksLun**|**Numeric**|
|**Azure:VM:StorageProfileDataDisksManagedDiskDiskEncryptionSet**|**String**|
|**Azure:VM:StorageProfileDataDisksManagedDiskId**|**String**|
|**Azure:VM:StorageProfileDataDisksManagedDiskResourceGroup**|**String**|
|**Azure:VM:StorageProfileDataDisksManagedDiskStorageAccountType**|**String**|
|**Azure:VM:StorageProfileDataDisksManagedStorageAccountType**|**String**|
|**Azure:VM:StorageProfileDataDisksName**|**String**|
|**Azure:VM:StorageProfileDataDisksToBeDetached**|**Boolean**|
|**Azure:VM:StorageProfileDataDisksVhd**|**String**|
|**Azure:VM:StorageProfileDataDisksWriteAcceleratorEnabled**|**Boolean**|
|**Azure:VM:StorageProfileImageReferenceExactVersion**|**String**|
|**Azure:VM:StorageProfileImageReferenceId**|**String**|
|**Azure:VM:StorageProfileImageReferenceOffer**|**String**|
|**Azure:VM:StorageProfileImageReferencePublisher**|**String**|
|**Azure:VM:StorageProfileImageReferenceSharedGalleryImageId**|**String**|
|**Azure:VM:StorageProfileImageReferenceSku**|**String**|
|**Azure:VM:StorageProfileImageReferenceVersion**|**String**|
|**Azure:VM:Tags**|**Map**|
|**Azure:VM:VMId**|**String**|

-   Resource collector: Azure VM Data Collector
-   Configuration collector: Azure VM Metric Collector
-   Cloud API used: Microsoft.ResourceGraph/resources
-   Cloud permission: **Microsoft.ResourceGraph/resources**

|Configuration key|Data type|
|-----------------|---------|
|**Azure:VM:PublicIPAddress**|**String**|
|**Azure:VM:PublicIPId**|**String**|

-   Resource collector: Azure VM Data Collector
-   Configuration collector: Azure VM Monitoring Metric Collector
-   Cloud API used: Microsoft.Compute/virtualMachines/\{vmName\}/instanceView
-   Cloud permission: **Microsoft.Compute/virtualMachines/\{vmName\}/instanceView**

|Configuration key|Data type|
|-----------------|---------|
|**Azure:VM:MonitoringState**|**String**|

**Note:** Use **scope=https://graph.microsoft.com/.default** and**scope=https://management.azure.com/.default** to fetch the oAuth token for the Azure resources.

Azure profile with minimal permissions

```json
{
    "properties": {
        "roleName": "CCGAzureMinimalPermission",
        "description": "Grants access to scan compute resources from azure subscription",
        "assignableScopes": [
            "/subscriptions/${subscription_id}"
        ],
        "permissions": [
            {
                "actions": [
                    "Microsoft.ResourceGraph/resources/read",
                    "Microsoft.Compute/virtualMachines/instanceView/read"
                ],
                "notActions": [],
                "dataActions": [],
                "notDataActions": []
            }
        ]
    }
}
```

**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

