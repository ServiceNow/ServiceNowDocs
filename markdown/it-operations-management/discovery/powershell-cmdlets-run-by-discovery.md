---
title: PowerShell commands run by Discovery
description: These are the PowerShell cmdlets and their parameters that Discovery runs to control and automate the administration of Windows servers and applications. Included are the probe parameters and MID Server scripts that contain the commands.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 15
breadcrumb: [PowerShell for Discovery and Service Mapping, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# PowerShell commands run by Discovery

These are the PowerShell cmdlets and their parameters that Discovery runs to control and automate the administration of Windows servers and applications. Included are the probe parameters and MID Server scripts that contain the commands.

<table id="table_xgb_4hp_pgb"><thead><tr><th>

Cmdlet/Parameters

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add-Content-   Path
-   Encoding
-   Value

</td><td>

Appends content to a specified item or file. You can specify the content by typing the content in the command or by specifying an object that contains the content.-   **Probe**

Windows - File discovery \(filebaseddiscovery.ps1\)

-   **MID Server script**

CollectConnectionsAndProcessesInfo.ps1


</td></tr><tr><td>

Add-Member-   NotePropertyName
-   NotePropertyValue
-   MemberType
-   Name
-   Value

</td><td>

Lets you add properties and methods to an instance of a Windows PowerShell object. For instance, you can add a NoteProperty member that contains a description of the object or a ScriptMethod member that runs a script to change the object.-   **Probe**

Windows - File discovery \(filebaseddiscovery.ps1\)

-   **MID Server script**

CollectConnectionsAndProcessesInfo.ps1


</td></tr><tr><td>

Add-Type-   TypeDefinition
-   AssemblyName
-   MemberDefinition
-   Name
-   Namespace
-   PassThru

</td><td>

Adds a Microsoft .NET Framework class in your Windows PowerShell session. You can then use the New-Object cmdlet to instantiate objects and use those objects, just as you would use any .NET Framework object. If you add an Add-Type command to your Windows PowerShell profile, the class is available in all Windows PowerShell sessions.-   **Probes**
    -   Windows - MSSQL \(sqlinfo.ps1\)
    -   Windows - Azure \(is.azure.ps1\)
-   **MID Server script**
    -   Credentials.psm1
    -   RegistryAPI.psm1
    -   LaunchProc.psm1

</td></tr><tr><td>

Compare-Object-   Property
-   PassThru

</td><td>

Compares two sets of objects. One set of objects is the reference set, and the other set is the difference set. The result of the comparison indicates whether a property value appeared only in the object from the reference set or, if the IncludeEqual parameter is specified, in both objects.-   **MID Server script**

DiagnosticsUtil.psm1


</td></tr><tr><td>

ConvertTo-SecureString-   String
-   AsPlainText
-   Force

</td><td>

Converts encrypted standard strings into secure strings. It can also convert plain text to secure strings. It is used with ConvertFrom-SecureString and Read-Host. The secure string created by the cmdlet can be used with cmdlets or functions that require a parameter of type SecureString.-   **Probes**

Windows - Storage 2012 - PS \(storage.2012.ps1\)

-   **MID Server script**

Credentials.psm1


</td></tr><tr><td>

ConvertTo-Json

</td><td>

Converts any object to a string in JavaScript Object Notation \(JSON\) format. The properties are converted to field names, the field values are converted to property values, and the methods are removed.-   **MID Server script**

CollectConnectionsAndProcessesInfo.ps1


</td></tr><tr><td>

Copy-Item-   Path
-   Destination
-   Force
-   Recurse
-   PassThru

</td><td>

Copies an item from one location to another location in the same namespace. For instance, it can copy a file to a folder, but it cannot copy a file to a certificate drive.-   **MID Server script**
    -   ADMELauncherWMI.psm1
    -   ExecuteRemote.psm1
    -   LaunchProc.psm1
    -   NmapInstallation.ps1

</td></tr><tr><td>

ForEach-Object - process

</td><td>

Performs an operation against each item in a collection of input objects. The input objects can be piped to the cmdlet or specified by using the InputObject parameter.-   **Probes**
    -   Windows - JBoss Find web.xml List \(indwebxml.ps1\)
    -   Windows - MSSQL \(sqlinfo.ps1\)
-   **MID Server script**
    -   CollectConnectionsAndProcessesInfo.ps1
    -   DiagnosticsUtil.psm1
    -   PSScript.ps1

</td></tr><tr><td>

Format-List

</td><td>

Formats the output of a command as a list of properties in which each property is displayed on a separate line. You can use Format-List to format and display all or selected properties of an object as a list.-   **MID Server script**

RegistryAPI.psm1


</td></tr><tr><td>

Get-ChildItem-   Path
-   File
-   Recurse
-   Filter
-   Directory
-   Include

</td><td>

Gets the items in one or more specified locations. If the item is a container, it gets the items inside the container, known as child items. You can use the Recurse parameter to get items in all child containers.-   **MID Server script**
    -   CollectConnectionsAndProcessesInfo.ps1
    -   DiagnosticsUtil.psm1
    -   ExecuteRemote.psm1
    -   LaunchProc.psm1
    -   NmapInstallation.ps1
    -   PSScript.ps1
    -   RegistryAPI.psm1

</td></tr><tr><td>

Get-Content-   Raw
-   Path

</td><td>

Gets the content of the item at the location specified by the path, such as the text in a file. It reads the content one line at a time and returns a collection of objects, each of which represents a line of content.-   **Probes**

Windows - ADM Enhanced

-   **MID Server script**
    -   ADMELauncherWMI.psm1
    -   ADMELauncherWinRM.psm1
    -   ScriptAPI.psm1

</td></tr><tr><td>

Get-Date - Uformat

</td><td>

Gets a DateTime object that represents the current date or a date that you specify. It can format the date and time in several Windows and UNIX formats. You can use Get-Date to generate a date or time character string, and then send the string to other cmdlets or programs.-   **Probes**

Windows - File Discovery \(filebaseddiscovery.ps1 \)

-   **MID Server script**
    -   DiagnosticsUtil.psm1
    -   LaunchProc.psm1

</td></tr><tr><td>

Get-Item

</td><td>

Gets the item at the specified location. It does not get the contents of the item at the location unless you use a wildcard character \(\*\) to request all the contents of the item.-   **Probes**

Windows - ADM Enhanced

-   **MID Server script**
    -   ExecuteRemote.psm1
    -   ADMELauncherWinRM.psm1
    -   ADMELauncherWMI.psm1

</td></tr><tr><td>

Get-ItemProperty-   Path
-   Name
-   ErrorAction

</td><td>

Gets the properties of the specified items. For example, you can use this cmdlet to get the value of the LastAccessTime property of a file object. You can also use this cmdlet to view registry entries and their values.-   **MID Server script**
    -   RegistryAPI.psm1
    -   ScriptAPI.psm1
    -   NmapInstallation.psm1

</td></tr><tr><td>

Get-Member - MemberType

</td><td>

Gets the members, the properties and methods, of objects. To specify the object, use the InputObject parameter or pipe an object to Get-Member. To get information about static members, the members of the class, not of the instance, use the Static parameter. To get only certain types of members, such as NoteProperties, use the MemberType parameter.-   **Probes**

Windows - ADM Enhanced

-   **MID Server script**

CollectConnectionsAndProcessesInfo.ps1


</td></tr><tr><td>

Get-Process-   Id
-   ErrorVariable \(alias EV\)
-   PSProvider

</td><td>

Gets the processes on a local or remote computer. Without parameters, this cmdlet gets all of the processes on the local computer. You can also specify a particular process by process name or process ID \(PID\) or pass a process object through the pipeline to this cmdlet.-   **Probes**

Windows - File Discovery \(filebaseddiscovery.ps1 \)

-   **MID Server script**
    -   CollectConnectionsAndProcessesInfo.ps1
    -   Get-PEB.psm1

</td></tr><tr><td>

Get-PSDrive-   Name
-   ErrorAction
-   PSProvider

</td><td>

Gets the drives in the current session. You can get a particular drive or all drives in the session.-   **Probes**

Windows - ADM Enhanced

-   **MID Server script**
    -   ADMELauncherWMI.psm1
    -   Credentials.psm1

</td></tr><tr><td>

Get-PSSession

</td><td>

Gets the user-managed Windows PowerShell sessions \(PSSessions\) on local and remote computers.-   **MID Server script**

Credentials.psm1


</td></tr><tr><td>

Get-Variable - Name

</td><td>

Gets the Windows PowerShell variables in the current console. You can retrieve just the values of the variables by specifying the ValueOnly parameter, and you can filter the variables returned by name.-   **MID Server script**
    -   ExecuteRemote.psm1
    -   PSScript.ps1
    -   DiagnosticsUtil.psm1

</td></tr><tr><td>

Get-WmiObject-   ComputerName
-   Filter
-   Credential
-   Impersonation
-   Authentication
-   ErrorAction \(alias EA\)
-   List
-   Namespace
-   Class

</td><td>

Gets instances of Windows Management Instrumentation \(WMI\) classes or information about the available WMI classes. To specify a remote computer, use the ComputerName parameter. If the List parameter is specified, the cmdlet gets information about the WMI classes that are available in a specified namespace. If the Query parameter is specified, the cmdlet runs a WMI query language \(WQL\) statement.-   **Probes**
    -   Windows - MSSQL \(sqlinfo.ps1\)
    -   Windows - Storage 2008 - PS \(storage.ps1\)
-   **MID Server script**
    -   ExecuteRemote.psm1
    -   ADMELauncherWinRM.psm1
    -   ADMELauncherWMI.psm1

</td></tr><tr><td>

Get-WSManInstance - ResourceURI

</td><td>

Retrieves an instance of a managemenet resource that is specified by a resource Uniform Resource Identifier \(URI\). The information that is retrieved can be a complex XML information set, which is an object, or a simple value.-   **MID Server script**

ScriptAPI.psm1


</td></tr><tr><td>

Group-Object - NoElement

</td><td>

Displays objects in groups based on the value of a specified property. Group-Object returns a table with one row for each property value and a column that displays the number of items with that value.-   **MID Server script**

RegistryAPI.psm1


</td></tr><tr><td>

Import-Module-   Name
-   DisableNameChecking
-   Global

</td><td>

Adds one or more modules to the current session. The modules that you import must be installed on the local computer or a remote computer.-   **Probes**

Windows - Storage 2012 - PS \(storage.2012.ps1\)

-   **MID Server script**
    -   Credentials.psm1
    -   PSScript.ps1

</td></tr><tr><td>

Invoke-Command-   Session
-   ScriptBlock
-   ErrorAction
-   ErrorVariable
-   ArgumentList \(alias is args\)
-   FilePath

</td><td>

Runs commands on a local or remote computer and returns all output from the commands, including errors. By using a single Invoke-Command command, you can run commands on multiple computers.-   **Probes**

Windows - Storage 2012 - PS \(storage.2012.ps1\)

-   **MID Server script**
    -   ADMELauncherWinRM.psm1
    -   Credentials.psm1
    -   ExecuteRemote.psm1
    -   LaunchProc.psm1
    -   Get-PEB.psm1
    -   WMIFetch.psm1

</td></tr><tr><td>

Invoke-Expression

</td><td>

Evaluates or runs a specified string as a command and returns the results of the expression or command. Without Invoke-Expression, a string submitted at the command line would be returned \(echoed\) unchanged.-   **MID Server script**
    -   NmapInstallation.ps1
    -   ScriptAPI.psm1

</td></tr><tr><td>

Invoke-WmiMethod-   Name
-   ComputerName
-   Argumentlist
-   Credential
-   ErrorAction

</td><td>

Calls the methods of Windows Management Instrumentation \(WMI\) objects. -   **MID Server script**
    -   LaunchProc.psm1
    -   ADMELauncherWinRM.psm1
    -   ADMELauncherWMI.psm1

</td></tr><tr><td>

Measure-Object - Sum

</td><td>

Calculates the property values of certain types of object. Measure-Object performs three types of measurements, depending on the parameters in the command.-   **MID Server script**

CollectConnectionsAndProcessesInfo.ps1


</td></tr><tr><td>

New-Item-   ItemType
-   Path
-   Force
-   ErrorAction

</td><td>

Creates a new item and sets its value. The types of items that can be created depend on the location of the item. For example, in the file system, New-Item creates files and folders. In the registry, New-Item creates registry keys and entries.-   **MID Server script**
    -   CollectConnectionsAndProcessesInfo.ps1
    -   ExecuteRemote.psm1
    -   LaunchProc.psm1
    -   NmapInstallation.ps1
    -   ADMELauncherWinRM.psm1
    -   ADMELauncherWMI.psm1

</td></tr><tr><td>

New-Object-   TypeName
-   Property
-   ArgumentList

</td><td>

Creates an instance of a Microsoft .NET Framework or COM object.-   **Probes**
    -   Windows - AWS Relationship \(AWS\_InstanceID.ps1\)
    -   Windows - Azure \(is.azure.ps1\)
    -   Windows - MSSQL \(sqlinfo.ps1\)
    -   Windows - File Discovery \(filebaseddiscovery.ps1\)
    -   Windows - Storage 2012 - PS \(storage.2012.ps1\)
-   **MID Server script**
    -   ADMELauncherWMI.psm1
    -   CollectConnectionsAndProcessesInfo.ps1
    -   Credentials.psm1
    -   Get-PEB.psm1
    -   LaunchProc.psm1
    -   WMIFetch.psm1 XMLUtil.psm1
    -   ExecuteRemote.psm1

</td></tr><tr><td>

New-PSDrive-   PSProvider
-   Root
-   ErrorAction
-   Credential
-   Name
-   Scope

</td><td>

Creates temporary and persistent drives that are mapped to or associated with a location in a data store, such as a network drive, a directory on the local computer, or a registry key, and persistent Windows mapped network drives that are associated with a file system location on a remote computer.-   **MID Server script**
    -   ADMELauncherWMI.psm1
    -   ScriptAPI.psm1

</td></tr><tr><td>

New-Variable-   Namer
-   Value
-   Force

</td><td>

Creates a new variable in Windows PowerShell. You can assign a value to the variable while creating it or assign or change the value after it is created.-   **MID Server script**

PSScript.ps1


</td></tr><tr><td>

New-PSSession-   Credential
-   SessionOption

</td><td>

Creates a Windows PowerShell session \(PSSession\) on a local or remote computer. When you create a PSSession, Windows PowerShell establishes a persistent connection to the remote computer.-   **MID Server script**

PSRemoteSession.psm1


</td></tr><tr><td>

New-PSSessionOption

</td><td>

Creates an object that contains advanced options for a user-managed session. You can use the object as the value of the SessionOption parameter of cmdlets that create a PSSession, such as a New-PSSession, Enter-PSSession, and Invoke-Command.-   **MID Server script**

PSRemoteSession.psm1


</td></tr><tr><td>

New-Timespan-   Start
-   End

</td><td>

Creates a timespan object which represents an interval. You can use to add or subtract time from a DateTime object.-   **Probes**

Windows - File Discovery \(filebaseddiscovery.ps1\)


</td></tr><tr><td>

Out-File - FilePath

</td><td>

Sends output to a file. You can use this instead of &gt; operator when you need to use its parameters.-   **Probes**

Windows - File Discovery \(filebaseddiscovery.ps1\)


</td></tr><tr><td>

Out-Null

</td><td>

Sends output to NULL, in effect, deleting it.-   **MID Server script**

Get-PEB.psm1


</td></tr><tr><td>

Out-String

</td><td>

Converts the objects that Windows PowerShell manages into an array of strings. By default, Out-String accumulates the strings and returns them as a single string, but you can use the stream parameter to direct Out-String to return one string at a time. This cmdlet lets you search and manipulate string output as you would in traditional shells when object manipulation is less convenient.-   **MID Server script**

Get-PEB.psm1


</td></tr><tr><td>

Receive-Job

</td><td>

Gets the results of Windows PowerShell background jobs, such as those started by using the Start-Job cmdlet or the AsJob parameter of any cmdlet. You can get the results of all jobs or identify jobs by their name, ID, instance ID, computer name, location, or session, or by submitting a job object.-   **MID Server script**

LaunchProc.psm1


</td></tr><tr><td>

Remove-Item-   Recurse
-   Path
-   Force

</td><td>

Deletes one or more items. Because it is supported by many providers, it can delete many different types of items, including files, folders, registry keys, variables, aliases, and functions.-   **MID Server script**
    -   ExecuteRemote.psm1
    -   NmapInstallation.ps1
    -   LaunchProc.psm1
    -   CollectConnectionsAndProcessesInfo.ps1

</td></tr><tr><td>

Remove-Job

</td><td>

Deletes Windows PowerShell background jobs. You can start jobs by using the Start-Job or the AsJob parameter of any cmdlet. You can use this cmdlet to delete all jobs or delete jobs based on their name, ID, instance ID, command, or state, or by passing a job object to Remove-Job. Without parameters or parameter values, Remove-Job has no effect.-   **MID Server script**

LaunchProc.psm1


</td></tr><tr><td>

Remove-PSDrive - Name

</td><td>

Deletes temporary Windows PowerShell drives that were created by using the New-PSDrive cmdlet.-   **MID Server script**
    -   ADMELauncherWMI.psm1
    -   ScriptAPI.psm1

</td></tr><tr><td>

Remove-PSSession - Session

</td><td>

Closes Windows PowerShell sessions \(PSSessions\) in the current session. It stops any commands that are running in the PSSessions, ends the PSSession, and releases the resources that the PSSession was using. If the PSSession is connected to a remote computer, this cmdlet also closes the connection between the local and remote computers.-   **Probes**

Windows - Storage 2012 - PS \(storage.2012.ps1\)

-   **MID Server script**

Credentials.psm1


</td></tr><tr><td>

Remove-Variable-   Name
-   Value

</td><td>

Deletes a variable and its value from the scope in which it is defined, such as the current session. You cannot use this cmdlet to delete variables that are set as constants or those that are owned by the system.-   **MID Server script**

PSScript.ps1


</td></tr><tr><td>

Rename-Item-   Path
-   NewName

</td><td>

Changes the name of a specified item. This cmdlet does not affect the content of the item being renamed. You cannot use Rename-Item to move an item, such as by specifying a path together with the new name. To move and rename an item, use the Move-Item cmdlet.-   **Probes**

Windows - File Discovery \(filebaseddiscovery.ps1 \)


</td></tr><tr><td>

Select-Object-   ExpandProperty \(alias Expand\)
-   Property
-   ExcludeProperty

</td><td>

Selects specified properties of an object or set of objects. It can also select unique objects, a specified number of objects, or objects in a specified position in an array. Alias is "Select".-   **Probes**

Windows - MSSQL \(sqlinfo.ps1\)

-   **MID Server script**
    -   CollectConnectionsAndProcessesInfo.ps1
    -   RegistryAPI.psm1

</td></tr><tr><td>

Select-String-   Pattern
-   NotMatch

</td><td>

Searches for text and text patterns in input strings and files. You can use it like Grep in UNIX and Findstr in Windows. You can type Select-String or its alias, sls.-   **MID Server script**

CollectConnectionsAndProcessesInfo.ps1


</td></tr><tr><td>

Select-XML-   Xpath
-   Content
-   Namespace

</td><td>

Allows you to use XPath queries to search for text in XML strings and documents. Enter an XPath query, and use the Content, Path, or Xml parameter to specify the XML to be searched.-   **MID Server script**

ScriptAPI.psm1


</td></tr><tr><td>

Set-Content-   Path
-   Value
-   Force
-   Encoding

</td><td>

Writes or replaces the content in the specified item, such as a file. You can type the content in the command or send content through the pipeline to Set-Content.-   **MID Server script**
    -   ADMELauncherWinRM.psm1
    -   CollectConnectionsAndProcessesInfo.ps1
    -   ExecuteRemote.psm1

</td></tr><tr><td>

Set-Location - Path

</td><td>

Sets the working location to a specified location. That location could be a directory, a sub-directory, a registry location, or any provider path.-   **MID Server script**

Credentials.psm1


</td></tr><tr><td>

Set-StrictMode - Version

</td><td>

Configures strict mode for the current scope and all child scopes, and turns it on and off. When strict mode is on, Windows PowerShell generates a terminating error when the content of an expression, script, or script block violates basic best-practice coding rules.-   **MID Server script**

Get-PEB.psm1


</td></tr><tr><td>

Set-Variable-   Name
-   Value
-   Option
-   Scope

</td><td>

Assigns a value to a specified variable or changes the current value. If the variable does not exist, the cmdlet creates it.-   **MID Server script**
    -   PSScript.ps1
    -   CollectConnectionsAndProcessesInfo.ps1
    -   ExecuteRemote.psm1

</td></tr><tr><td>

Sort-Object - Property

</td><td>

Sorts objects in ascending or descending order based on the values of properties of the object. You can specify a single property or multiple properties \(for a multi-key sort\), and you can select a case-sensitive or case-insensitive sort. You can also direct Sort-Object to display only the objects with a unique value for a particular property.-   **Probes**

Windows - MSSQL \(sqlinfo.ps1\)

-   **MID Server script**

DiagnosticsUtil.psm1


</td></tr><tr><td>

Split-Path-   Leaf
-   Path
-   Parent

</td><td>

Returns only the specified part of a path, such as the parent folder, a subfolder, or a file name. It can also get items that are referenced by the split path and tell whether the path is relative or absolute.-   **Probes**
    -   Windows - Weblogic - Find \(findconfig.ps1\)
    -   Windows - Storage 2012 - PS \(storage.2012.ps1\)
-   **MID Server script**
    -   Credentials.psm1
    -   LaunchProc.psm1
    -   PSScript.ps1
    -   ExecuteRemote.psm1

</td></tr><tr><td>

Start-Sleep-   S \(alias for seconds\)
-   M \(alias for millisecond\)

</td><td>

Suspends the activity in a script or session for the specified period of time. You can use it while waiting for an operation to complete or pausing before repeating an operation.-   **Probes**

Windows - Active Connections Multiple \(WMI\_ActiveConnections.ps1\)

-   **MID Server script**
    -   CollectConnectionsAndProcessesInfo.ps1
    -   LaunchProc.psm1
    -   NmapInstallation.ps1

</td></tr><tr><td>

Stop-Job

</td><td>

Stops Windows PowerShell background jobs that are in progress. You can use this cmdlet to stop all jobs or stop selected jobs based on their name, ID, instance ID, or state, or by passing a job object to Stop-Job.-   **MID Server script**

LaunchProc.psm1


</td></tr><tr><td>

Test-Path-   Path
-   PathType

</td><td>

Determines whether all elements of the path exist. It returns $True if all elements exist and $False if any are missing. It can also tell whether the path syntax is valid and whether the path leads to a container or a terminal or leaf element.-   **MID Server script**
    -   ExecuteRemote.psm1
    -   LaunchProc.psm1
    -   NmapInstallation.ps1
    -   PSScript.ps1
    -   RegistryAPI.psm1
    -   ADMELauncherWinRM.psm1
    -   ADMELauncherWMI.psm1
    -   CollectConnectionsAndProcessesInfo.ps1

</td></tr><tr><td>

Test-WSMan-   Computer
-   Port

</td><td>

Submits an identification request that determines whether the WinRM service is running on a local or remote computer. If the tested computer is running the service, the cmdlet displays the WS-Management identity schema, the protocol version, the product vendor, and the product version of the tested service.-   **MID Server script**

ScriptAPI.psm1


</td></tr><tr><td>

Where-Object

</td><td>

Selects objects that have particular property values from the collection of objects that are passed to it. For example, you can use the Where-Object cmdlet to select files that were created after a certain date, events with a particular ID, or computers that use a particular version of Windows.-   **MID Server script**
    -   CollectConnectionsAndProcessesInfo.ps1
    -   DiagnosticsUtil.psm1
    -   WMIFetch.psm1

</td></tr><tr><td>

Write-Error-   Message
-   Category

</td><td>

Declares a non-terminating error. By default, errors are sent in the error stream to the host program to be displayed, along with output.-   **Probes**
    -   Windows - MySQL Configuration \(mysqlconfig.ps1ps1\)
    -   Windows - MySQL Version \(mysqlinfo.ps1\)
    -   Oracle - Instance Pfile \(oraclepfile.ps1\)
    -   Oracle - Instance Version \(oracleversion.ps1\)
    -   Windows - MSSQL \(sqlinfo.ps1\)
-   **MID Server script**
    -   ADMELauncherWinRM.psm1
    -   ADMELauncherWMI.psm1
    -   ExecuteRemote.psm1
    -   LaunchProc.psm1
    -   NmapInstallation.ps1

</td></tr><tr><td>

Write-Host - NoNewLine

</td><td>

Writes customized output to a host. You can specify the color of text by using the ForegroundColor parameter, and you can specify the background color by using the BackgroundColor parameter. The Separator parameter lets you specify a string to use to separate displayed objects. The particular result depends on the program that is hosting Windows PowerShell.-   **Probes**
    -   Windows - Network ARP Table \(arpTable.ps1\)
    -   Windows - Weblogic - Find \(findconfig.ps1\)
    -   Windows - JBoss Get \(findjbossservicexml.ps1\)
    -   Windows - WebSphere - Web Services \(\)
    -   Windows - JBoss Find \(findwebxml.ps1\)
    -   Windows - Weblogic - Get \(\)
    -   Windows - WebSphere - Cell \(getcellxml.ps1\)
    -   Windows - WebSphere - Web Applications \(getserverindexxml.ps1\)
    -   Oracle - Instance PFile \(oraclepfile.ps1\)
    -   Oracle - Instance Version \(oracleversion.ps1\)
    -   Windows - MSSQL \(sqlinfo.ps1\)
    -   Windows - Storage 2012 - PS \(storage.2012.ps1\)
    -   Windows - Storage 2008 - PS \(storage.ps1\)
    -   Windows - Active Connections Multiple \(WMI\_ActiveConnections.ps1\)
-   **MID Server script**
    -   ADMELauncherWinRM.psm1
    -   ADMELauncherWMI.psm1
    -   PSScript.ps1
    -   RegistryAPI.psm1
    -   ScriptAPI.psm1
    -   WMIFetch.psm1
    -   DiagnosticsUtil.psm1
    -   NmapInstallation.ps1

</td></tr><tr><td>

Write-Output

</td><td>

Sends the specified objects to the next command in the pipeline. If the command is the last command in the pipeline, the objects are displayed in the console.-   **Probes**
    -   Windows - Azure \(is.azure.ps1\)
    -   ExecuteRemote \(testExecuteRemote.ps1\)
    -   Windows - File Discovery \(filebaseddiscovery.ps1\)
-   **MID Server script**

Get-PEB.psm1


</td></tr><tr><td>

Write-Verbose - Message

</td><td>

Writes text to the verbose message stream in Windows PowerShell. Typically, the verbose message stream is used to deliver information about command processing that is used for debugging a command.-   **MID Server script**
    -   Get-PEB.psm1
    -   LaunchProc.psm1
    -   ExecuteRemote.psm1

</td></tr></tbody>
</table>**Parent Topic:**[PowerShell for Discovery and Service Mapping](r_PowerShellForDiscovery.md)

