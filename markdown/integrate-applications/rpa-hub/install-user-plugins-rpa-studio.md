---
title: Create user plugins for RPA Desktop Design Studio
description: Create user plugins by using Microsoft Visual Studio to enable RPA developers to use complex .NET components or libraries in RPA Desktop Design Studio in a seamless way.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Building automations, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Create user plugins for RPA Desktop Design Studio

Create user plugins by using Microsoft Visual Studio to enable RPA developers to use complex .NET components or libraries in RPA Desktop Design Studio in a seamless way.

## Before you begin

Use either Microsoft Visual Studio Pro, Community, or Enterprise version to perform this task.

Role required: none

## About this task

The following procedure describes how to create a user plugin using C\#.NET.

## Procedure

1.  Open Microsoft Visual Studio and click **Create a new project**.

2.  In the Create a new project dialog box, select the Class Library \(.NET Framework\) template.

    ![Class library DOT NET Framework.](../image/rpa-user-plugin-class-library.png "Select a project type of Class Library DOT NET Framework")

3.  Click **Next**.

4.  In the Configure your new project dialog box, fill in the following fields:

<table id="table_e51_l1h_5rb"><thead><tr><th>

Field

</th><th>

Description and action

</th></tr></thead><tbody><tr><td>

Project name

</td><td>

Name of your project.For example, `MyFirstPlugin`.

</td></tr><tr><td>

Location

</td><td>

Location of your project.Select a disk location.

</td></tr><tr><td>

Solution name

</td><td>

Name of your project's solution.

</td></tr><tr><td>

Framework

</td><td>

Select a framework version.Select **.NET Framework 4.7** version.

</td></tr></tbody>
</table>5.  Click **Create**.

    The Class1.cs file opens.

6.  In the Solution Explorer pane, right-click **References** and select **Add Reference**.

7.  In the Reference Manager dialog box, navigate to **Assemblies** &gt; **Framework**.

8.  Select the **System.AddIn** assembly to add an annotation of this addin.

    ![Select System.AddIn assembly.](../image/rpa-user-plugin-system-addin.png "Select System.AddIn assembly")

9.  Click **OK**.

10. In the Class1.cs file, add the `System.AddIn.AddIn("MyFirstPlugin", Description = "Learning to create custom components", Version = "1.0")` code snippet above the class.

11. In the Class1.cs file, create one or more public static methods to your code.

    In this example, two methods are added to the code:

    -   **SayHello** method: The name is taken as the input and returns "Hello" with a name and followed by an exclamation mark. For example, if the input is `User`, it returns "Hello User!".
    -   **Sum** method: Two numbers are taken as the input and returns the sum of these two numbers. For example, if the inputs are `5` and `12`, it returns "17".
    ![Public static methods.](../image/rpa-user-plugin-code.png "Public static methods")

12. Click **Save**.

13. In the Solution Explorer pane, right-click your project and select **Build**.

14. After the build is successful, do the following actions to copy and paste the .dll files:

    1.  In the Solution Explorer pane, right-click your project and select **Open Folder in File Explorer**.

    2.  Navigate to **bin** &gt; **Debug** and copy the .dll files.

    3.  Go to your RPA Desktop Design Studio automation project folder and create a new folder as **UserPlugins**.

        **Important:** Ensure that the spelling of this folder is entered correctly.

    4.  In the UserPlugins folder, create a folder and enter a name for the folder.

        For example, `My First Plugin`.

    5.  Paste the .dll files in this folder.

15. In the RPA Desktop Design Studio, do the following actions to add the plugin to your automation project:

    1.  In the Project Explorer pane, right-click **User Plugins** and select **Add User Plugin**.

    2.  In the Available User Plugins dialog box, select the plugin.

    3.  Click **OK**.

    In the Toolbox pane, the user plugin you created appears.

16. Do the following actions to use the user plugin:

    1.  In the Toolbox pane, navigate to the user plugin component category to select a method.

        ![Two methods that appear in the user plugin component category.](../image/rpa-user-plugin-toolbox.png "Two methods that appear in the user plugin component category")

    2.  Drag a method to the Design surface.

    3.  To provide the input parameter value manually, double-click the input parameter field under the method, and enter the value.

    4.  To provide the input parameter value from another method or component, connect the Data In port of the method to the Data Out port of another method or component.

    5.  Connect the control ports of the method to the corresponding ports of another method or component.

    6.  On the Design surface, right-click the title bar of the component from where you want to start the execution and select **Run From Here**.

        ![Output of the SayHello method that appears as "Hello User!".](../image/rpa-user-plugin-example1.png "Output of the SayHello method")

        ![Output of the Sum method that appears as "17".](../image/rpa-user-plugin-example2.png "Output of the Sum method")


**Parent Topic:**[Building automations](../concept/rpa-studio-build.md)

