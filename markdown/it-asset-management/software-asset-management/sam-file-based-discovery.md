---
title: File Signature Normalization
description: File-based discovery finds files on UNIX or Windows servers and processes them with an established set of rules that enhance the identification of installed software. Use the results to monitor specific file types on network servers for security purposes or to manage your software licenses with the File Signature Normalization plugin for Software Asset Management - Professional \(SAMP\).
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# File Signature Normalization

File-based discovery finds files on UNIX or Windows servers and processes them with an established set of rules that enhance the identification of installed software. Use the results to monitor specific file types on network servers for security purposes or to manage your software licenses with the File Signature Normalization plugin for Software Asset Management - Professional \(SAMP\).

For more information on the file-based discovery, see the [File-based Discovery](https://www.servicenow.com/docs/access?context=file-based-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

**Note:** The information provided in this page only covers the features available with the File Signature Normalization \(com.snc.file\_signature\_normalization\) plugin.

## Required plugins

The File Signature Normalization plugin is required to allow file information to be mapped to installed software. To enable this plugin, [Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md).

You can also enable file-based discovery with the File-Based Discovery \(com.snc.discovery.file\_based\_discovery\) plugin to filter file signatures. This plugin is included with a Discovery subscription, but you must request plugin activation. Normalization of products and publishers is available for file-based discovery with or without Software Asset Management.

## How File Signature Normalization works

File Signature Normalization uses discovered files and their attributes, such as file name, file sizes, and version, to find a signature match in the Content Data Service \(CDS\). Then, File Signature Normalization creates a normalized software installation record.

During regularly scheduled Discovery jobs, the file information is discovered at all the specified end points in a user environment and sent to the MID Server. The information from the MID Server is then sent back to the ServiceNow instance. Information is matched against the content library and the software installation records are created.

If a discovered file name does not match a predefined file signature rule in the CDS, an unidentified file set record is created in the unidentified file set \[cmdb\_unidentified\_file\_set\] table. Users with the sam\_admin role can create a custom file signature rule for the unidentified file set to normalize data manually.

If you opt in to the content service, these custom file signatures are sent back to the CDS for further analysis and inclusion in the content service for future discovery. You can also restrict some custom file signatures from being sent to the CDS by changing the value in the Exclude From CDS column to True.

**Note:** Software discovery models are stored in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table. Unlike pattern discovery normalization, discovery models created by File Signature Normalization do not go through the normalization process automatically and are ignored during scheduled normalization jobs.

File Signature Normalization also identifies duplicates. Software installations that are discovered on the same configuration item, but from different discovery sources, are considered duplicates. All installations that are identified are marked as inactive by default. Once the duplication has been deleted, the remaining installation is marked as active and the discovery model picks up all associated installs.

**Note:** By default, scheduled jobs are performed during specific times so they do not run heavy loads that could cause performance or stability issues. If these scheduled job times are changed, performance issues could occur.

Any software installs discovered during File-based discovery are updated to reflect any CDS changes in the software install attributes such as product or publisher name change. Stage product and Stage publisher are new columns in the File Set \[samp\_file\_set\] table.

## File Signature Normalization roles

File Signature Normalization adds the following role.

|Roles|Description|
|-----|-----------|
|file\_normalization\_admin|Users with this role can access file attribute and unidentified file information. Required to ensure that file signature normalization supports third-party software installation discovery sources.|

## Tables

File Signature Normalization adds the following tables.

|Table|Description|
|-----|-----------|
|samp\_file\_set|File set that maps to a software product. Multiple samp\_file\_map records can point to one samp\_file\_set record.|
|samp\_file\_map|File map record for each file hash discovered by the end-user device. The file hash is created based on the discovered file and its attributes.|
|samp\_file\_name|File names that are used to search on end-user devices.|
|samp\_custom\_file\_name|File names that entered by the user that can be discovered on end-user devices.|
|cmdb\_unidentified\_file\_set|Custom rules that are created if a software match is not found for the discovered file in the CDS.|

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

