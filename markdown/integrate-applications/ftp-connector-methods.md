---
title: FTP connector methods
description: The FTP connector methods perform various actions on the File Transfer Protocol server as part of an automation. To enable the methods, you must provide appropriate parameters.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [FTP, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# FTP connector methods

The FTP connector methods perform various actions on the File Transfer Protocol server as part of an automation. To enable the methods, you must provide appropriate parameters.

## SetConfiguration

Sets the File Transfer Protocol server access details. You must execute this method first.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Url|URL of the File Transfer Protocol|Data in|String|None|Yes|
|Username|Username to access the File Transfer Protocol server.|Data in|String|None|Yes|
|Password|Password to access the File Transfer Protocol server.|Data in|String|None|Yes|

## CreateFolder

Creates a folder on the File Transfer Protocol server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|FolderName|Path in the File Transfer Protocol server where the folder will be created with the folder name.|Data in|String|None|Yes|
|Return|Returns True if the folder is created, else, returns False.|Data out|Boolean|None|Not applicable|

## DeleteFile

Deletes a file in the FTP server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|RemoteFilePath|Path to the file you want to remove in the File Transfer Protocol server.|Data in|String|None|Yes|
|Return|Returns True if the file is deleted, else, returns False.|Data out|Boolean|Not applicable|Not applicable|

## DeleteFolder

Deletes the specified folder in the File Transfer Protocol server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|RemoteFolderPath|Path to the folder in the File Transfer Protocol server including the folder name.|Data in|String|None|Yes|
|Return|Returns True if the folder is deleted, else, returns False.|Data out|Boolean|Not applicable|Not applicable|

## DownloadFile

Downloads a file from the File Transfer Protocol server to the local drive.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|RemoteFile|Path to the file in the File Transfer Protocol and the name of the file.|Data in|String|None|Yes|
|LocalFile|Path in the local drive where the file will be downloaded.|Data in|String|None|Yes|
|TimeOut|Time after which the request to the File Transfer Protocol server times out.|Data in|Integer|None|No|
|Return|Returns True if the file is downloaded, else, returns False.|Data out|Boolean|None|Not applicable|

## DownloadFolder

Downloads a folder from the File Transfer Protocol server to the local drive.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|RemoteFolderPath|Path to the folder in the File Transfer Protocol and the name of the folder.|Data in|String|None|Yes|
|LocalFolderPath|Path in the local drive where the folder will be downloaded.|Data in|String|None|Yes|
|TimeOut|Time after which the request to the File Transfer Protocol server times out.|Data in|Integer|None|No|
|Return|Returns True if the folder is downloaded, else, returns False.|Data out|Boolean|None|Not applicable|

## GetFileList

Returns the list of files in a folder in the File Transfer Protocol server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|RemoteFolderPath|Path to the folder in the File Transfer Protocol and the name of the folder.|Data in|String|None|Yes|
|Return|Returns the list of files in the folder.|Data out|String|Not applicable|Not applicable|

## RenameFile

Renames a file in the File Transfer Protocol server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|RemoteFilePath|Path to the file in the File Transfer Protocol server and the name of the file.|Data in|String|None|Yes|
|NewNameofFile|Path to the file in the File Transfer Protocol server and the new name of the file.|Data in|String|None|Yes|
|Return|Returns True if the name of the file is changed, else, it returns False.|Data out|Boolean|Not applicable|Not applicable|

## RenameFolder

Renames a folder in the File Transfer Protocol server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|RemoteFolder|Path to the folder in the File Transfer Protocol server and the name of the folder.|Data in|String|None|Yes|
|NewNameofFolder|Path to the folder in the File Transfer Protocol server and the new name of the folder.|Data in|String|None|Yes|
|Return|Returns True if the name of the folder is changed, else, it returns False.|Data out|Boolean|Not applicable|Not applicable|

## UploadFile

Uploads a file from the local drive to the File Transfer Protocol server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|LocalFilePath|Path to the file in the local drive.|Data in|String|None|Yes|
|RemoteFilePath|Path to the location in the File Transfer Protocol server.|Data in|String|None|Yes|
|Return|Returns True if the file is uploaded, else, returns False.|Data out|Boolean|Not applicable|Not applicable|

## UploadFolder

Uploads a folder from the local drive to the File Transfer Protocol server.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|LocalFolderPath|Path to the folder in the local drive.|Data in|String|None|Yes|
|RemoteFolderPath|Path to the location in the File Transfer Protocol server.|Data in|String|None|Yes|
|Return|Returns True if the folder is uploaded, else, returns False.|Data out|Boolean|Not applicable|Not applicable|

**Parent Topic:**[FTP](../concept/ftp-connector.md)

