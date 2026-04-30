---
title: Clustered application discovery on Windows
description: A process and its corresponding resource information can be used to determine whether the process is a clustered process.To detect Windows clustered applications, create a process classifier for that CI type.In the second step, relate the process classifier to the information that is in the Windows Cluster resources table.The value field defines two JavaScript objects, called resourceType and isMatch.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Clustered application discovery on Windows

A process and its corresponding resource information can be used to determine whether the process is a clustered process.

The **Microsoft SQL Server** process classifier that comes with your instance identifies clustered SQL Servers. You can leverage the same technique to detect other clustered applications on Windows using Discovery.

To detect Windows clustered applications with Discovery, you create a process classifier that detects whether a process is a clustered process. Perform the following steps:

**Parent Topic:**[Software discovery](c_Software.md)

## Create a classifier for clustered processes

To detect Windows clustered applications, create a process classifier for that CI type.

### Before you begin

Role required: discovery\_admin

### Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **Processes**.

2.  Click **New**.

3.  Fill out the form using the fields from the table.

4.  Click **Submit**.

    ![Process Classification form](../image/ProcessClassificationForm2.png "Process Classification form")

<table id="table_xf2_wcr_dr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the process classifier.

</td></tr><tr><td>

Table

</td><td>

Select **Application**.

</td></tr><tr><td>

Relation type

</td><td>

Select the CI relationship type for this classification. The relationship field is only available for Process and Scan Application classifications. Discovery process classifications typically use one of these relationship types: -   **Runs on::Runs**: Defines the relationship of an application to the host on which it runs. This relationship is expressed from the perspective of the host and the application. For example: My database application runs on server001::server001 runs my database application.
-   **Depends on::Used by**: Defines the relationship of an application that communicates with another application. This relationship is expressed from the perspective of each application. For example: The Tomcat application depends on the MySQL database:: The MySQL database is used by Tomcat.
-   **Virtualized by::Virtualizes**: Defines the relationship of a virtual machine to its host. This relationship is expressed from the perspective of the virtual machine and of the host. For example: server001 is virtualized by ServerESX::Server ESX virtualizes server001.
-   **Cluster of::Cluster**: Defines the relationship of a cluster node to the cluster to which it belongs. This relationship is expressed from the perspective of the cluster node and of the cluster.
-   **Hosted on::Hosts**: Defines the relationship of a cluster node and the Windows host. This relationship is expressed from the perspective of the cluster node and of the Windows host.


</td></tr><tr><td>

Active

</td><td>

Select this box to activate the process classification. Deselect to deactivate it.

</td></tr><tr><td>

Order

</td><td>

Enter the order in which Discovery should run this process classification when there are multiple classifications available for a table. Discovery runs process classifications from the lowest to the highest order.

</td></tr><tr><td>

Test with

</td><td>

Lists the host CI where an automatically generated process classification conditions were met. Use this field to test changes to the process classification to ensure that the updated classification behaves as expected.

</td></tr><tr><td>

Condition

</td><td>

Configure the appropriate condition. The example screenshot triggers this process classification when the process command contains the string `MSFT SQL Server 2000`.

</td></tr></tbody>
</table>
## Relate the process classifier to Windows cluster resources

In the second step, relate the process classifier to the information that is in the Windows Cluster resources table.

### Before you begin

Role required: admin

### About this task

The [Windows Cluster](../reference/r_WindowsServerClusterDiscovery.md) resources table is cmdb\_ci\_win\_cluster\_resource. This relationship is built through JavaScript.

### Procedure

1.  Navigate back to the process classification you just made.

2.  Select the **Parameters** tab.

3.  Select **New**.

4.  Fill out the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Name|Select a unique name.|
    |Application|Select **Global**.|
    |Type|Enter **Cluster**.|
    |Value|This field defines two JavaScript objects, called resourceType and isMatch. For more information, see [Populate the Value field on the Classifier Parameter form](c_ClusteredAppDiscoveryOnWindows.md#).|

5.  Select **Submit**.


## Populate the Value field on the Classifier Parameter form

The value field defines two JavaScript objects, called resourceType and isMatch.

### Before you begin

Role required: admin

### About this task

The resourceType value refers to the Resource Type column in the Windows Cluster Resources table \[cmdb\_ci\_win\_cluster\_resource\]. The resourceType value can not be empty or null.

### Procedure

1.  Navigate to a Windows cluster page to access the Windows Cluster Resources table.

2.  Click the **Windows Cluster Resources** tab.


### Example

The **isMatch** value evaluates whether the process is a clustered process.

-   An evaluation that returns **true** indicates the process is a clustered application, and the process is classified as a clustered application in the cluster.
-   An evaluation that returns **false** classifies the process as a regular application running on the cluster node.

The **isMatch** value is a function that contains two input variables, process and resource:

-   process: Process is the GlideRecord of the process application. It is determined by the **Table** field in the classifier. In this example, it is the GlideRecord entry of the Application table \(cmdb\_ci\_app\) for the process that is being classified. You have access to any field values for the CI type such as name or version.
-   resource: Resource is the GlideRecord entry in the Windows Cluster Resource table after the resourceType condition has been applied. In the example, it is the GlideRecord entry of the sixth row.

Examples of JavaScript for the Value field.

In the following example code: resourceType: "SQL Server" the query filters the Windows Cluster Resources table entry for the Resource Type field that has a value that is equal to SQL Server. In the following example table, the sixth record would be returned.

The following script indicates that if there is a resource of type SQL Server, the process is classified as a clustered application.

```
resourceType: "SQL Server" 
isMatch: function(process, resource) { 
    return true; 
}
```

The following script indicates that if if there is a resource of type SQL Server, and the application name is equal to the resource name, then the process is classified as a clustered application.

```
resourceType: "SQL Server" 
isMatch: function(process, resource) { 
    if (process.name == resource.name) 
        return true; 
}
```

If there are multiple matches to the resourceType condition, the matching function is called multiple times. For the following resourceType example, the matching function is called twice because there are two entries that have **Physical Disk** in the **Resource Type** column in the sample Windows Cluster Resources table.

```
resourceType: "Physical Disk" 
```

