---
title: CIM probe
description: The CIM probe uses WBEM protocols to query a particular CIM server, the CIM Object Manager, for a set of data objects and properties. CimIQL syntax consists of several elements, including a query and different tokens.The CimIQL probe requires operation tokens.The CimIQL probe requires component tokens, which are sub-components of operational tokens.This is a tutorial by example where each example builds on the previous example.CIM Probe results are passed to the probe sensor as an XML document embedded within the &lt;output&gt; element.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# CIM probe

The CIM probe uses WBEM protocols to query a particular CIM server, the CIM Object Manager, for a set of data objects and properties.

For instructions on configuring probe parameters, see [Set probe parameters](../task/t_SetProbeParameters.md).

The following parameters may be passed to the CIM probe:

|Parameter|Description|Default Value|
|---------|-----------|-------------|
|source|\[Required\] The initial host to connect to.|None|
|port|The port to connect to. If empty, the value is determined by the "schema" parameter: http = 5988, https = 5989.|5988 or 5989|
|schema|\[Required\] The schema to use: '"http"' or '"https"'.|http|
|namespace|\[Required\] The CIM namespace. May be overridden by a query.|None|
|queries|\[Required\] A semicolon-delimited list of CIM probe queries to process and return results for.|None|
|retries|The number of times to retry a query if it fails due to network connectivity issues.|2|
|connection\_timeout|The number of milliseconds the probe has to connect to a server.|5000|
|socket\_timeout|The number of milliseconds the probe has to read data.|5000|

The CIM Intermediate Query Language \(CimIQL\) uses keys, filters, and dot-walking to traverse the CIM schema.

## Parameter Expansion

The CIM query language supports standard SNC preprocessed probe parameter expansion. Place variables in queries by encapsulating their names like this:

```
${foobar}.CIM_RunningOS[0].Name
CIM_ComputerSystem.${barfoo}
```

The text $\{foobar\} is replaced with the contents of the foobarprobe parameter passed to the CIM probe; likewise for barfoo.

## CIMIQL

The CIM Intermediate Query Language \(CimIQL\) is an intermediate language designed to simplify the process of querying CIM providers.

CimIQL currently supports the standard Web-Based Enterprise Management \(WBEM\) protocol stack, but others, such as Web Services-Management \(WS-MAN\), may be added in the future. The query language syntax borrows from elements of Microsoft's WMI query language and UNIX's wbemcli command. The CimIQL library is a pure Java implementation.

**Note:** CimIQL is pronounced "simicle".

**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

## CimIQL syntax

CimIQL syntax consists of several elements, including a query and different tokens.

|Element|Description|
|-------|-----------|
|Statement|The most basic element of CimIQL is a valid . A statement contains multiple queries delimited by a period . character.|
|Query|A represents a single high-level protocol-independent request. Each query is comprised of nested language components and sub-components known as tokens.|
|Token|A describes a specific lexical aspect of the CimIQL syntax.|
|[Operation Token](r_CIMProbe.md#)|The first token of each query must be an , which represents the overall logical operation to be performed.|
|[Component Token](r_CIMProbe.md#)|A is a sub-component of an operation token.|
|Result|Each query is paired with a result, which is then provided as input to the next query in the statement. A is comprised of a set of objects and their properties.|

## CimIQL operation tokens

The CimIQL probe requires operation tokens.

Each of the following core operations has a counterpart in the [CIM Operations over HTTP](http://www.dmtf.org/sites/default/files/standards/documents/DSP0200_1.3.1.pdf) standard.

<table id="table_rk1_jzc_lp"><thead><tr><th>

Return Value

</th><th>

Details

</th><th>

Equivalent CIM Operation over HTTP

</th></tr></thead><tbody><tr><td>

class object

</td><td>

[Get Object](r_CIMProbe.md#GetObjectToken) Retrieves a single object of a specific class by specifying all of its unique keys \(as [key tokens](r_CIMProbe.md#KeyToken)\) and any optional [parameter tokens](r_CIMProbe.md#ParameterToken), separated by commas.

</td><td>

GetInstance

</td></tr><tr><td>

class object

</td><td>

[Enumerate Objects](r_CIMProbe.md#EnumerateObjectsToken) Retrieves objects that match a set of [condition tokens](r_CIMProbe.md#ConditionToken) and [parameter tokens](r_CIMProbe.md#ParameterToken).

</td><td>

EnumerateInstances

</td></tr><tr><td>

class object

</td><td>

[Enumerate Associated Objects](r_CIMProbe.md#EnumerateAssociatedObjectsToken) Retrieves objects associated with each result from the preceding query.

</td><td>

Associators

</td></tr><tr><td>

statement results

</td><td>

[Substitution](r_CIMProbe.md#SubstitutionToken) A no-op token that feeds the results of a previous named statement as input into the next query of its own statement.

</td><td>

Reference the results of a named statement

</td></tr></tbody>
</table>### Get Object Token

&lt;classname&gt;\{&lt;key token&gt;,&lt;parameter token&gt;,...\}

-   Retrieves a single object of a specific class by specifying all of its unique keys \(as key tokens [key tokens](r_CIMProbe.md#KeyToken)\) and any optional [parameter tokens](r_CIMProbe.md#ParameterToken), separated by commas. This token is also known as the .
-   The &lt;classname&gt; is the case-sensitive CIM class name of the desired object. By default, objects of the specified class and of any extended classes are retrieved.
-   The key and parameter tokens are enclosed by a single pair of curly brackets \{ ... \}.
-   This token must only be used as the first query in a statement.
-   Returns: class object
-   Example:

    ```
    CIM_ComputerSystem{CreationClassName='Linux_ComputerSystem',Name='runtime'}.*
    ```


### Enumerate Objects Token

&lt;classname&gt;\{\{&lt;condition token&gt;,&lt;parameter token&gt;,...\}\}&lt;array index token&gt; OR &lt;classname&gt;&lt;array index token&gt;

-   Retrieves objects that match a set of [condition tokens](r_CIMProbe.md#ConditionToken) and [parameter tokens](r_CIMProbe.md#ParameterToken). This token is also known as the .
-   The condition tokens and parameter tokens are enclosed by two pairs of curly brackets \{\{ ... \}\}. The curly brackets are optional if there are no conditions or parameters necessary.
-   The &lt;classname&gt; is the case-sensitive CIM class name of the desired objects. By default, objects of the specified class and of any extended classes are retrieved.
-   The [index token](r_CIMProbe.md#IndexToken) is optional.
-   This token must only be used as the first query in a statement.
-   Returns: class object
-   Example:

    ```
    CIM_ComputerSystem{{Name!='runtime'}}.*
    ```


### Enumerate Associated Objects Token

&lt;association classname&gt;\{\{&lt;property filter token&gt;,&lt;parameter token&gt;,...\}\}&lt;array index token&gt; OR &lt;association classname&gt;&lt;array index token&gt;

-   Retrieves objects associated with each result from the preceding query.
-   The [condition tokens](r_CIMProbe.md#ConditionToken) and [parameter tokens](r_CIMProbe.md#ParameterToken) are enclosed by two pairs of curly brackets \{\{ ... \}\}. The curly brackets are optional if there are no properties filters or parameters necessary.
-   The &lt;association classname&gt; is the name of the many-to-many or one-to-many class that associates two objects together. By default, objects of the specified class and of any extended classes are retrieved.
-   The &lt;parameter token&gt;, ResultClass, may be specified to filter results based on the resulting object's classname.
-   The [index token](r_CIMProbe.md#IndexToken) is optional.
-   This token must not be used as the first query in a statement.
-   Returns: class object
-   Example:

    ```
    CIM_ComputerSystem{{Name='runtime'}}[2].*
    ```


### Substitution Token

$\{&lt;statement name&gt;\}

-   A no-op token that feeds the results of a previous named statement as input into the next query of its own statement.
-   Returns: void
-   Example:

    ```
    $(lastComputer).ElementName
    ```


## CimIQL component tokens

The CimIQL probe requires component tokens, which are sub-components of operational tokens.

The following tokens are sub-components of [operation tokens](r_CIMProbe.md#).

<table id="table_rk1_jzc_lp"><thead><tr><th>

Token

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Properties token

</td><td>

\* OR &lt;property name&gt;,&lt;property name&gt;,...Specifies which properties are to be returned for each object of the final result set.

</td></tr><tr><td>

Query Delimiter Token

</td><td>

. \(Period\)Separates queries.

</td></tr><tr><td>

Index Token

</td><td>

\[index\]Reduces a preceding query's results to a single object at the specified integer index.

</td></tr><tr><td>

Key Token

</td><td>

&lt;key name&gt;='&lt;value&gt;'Matches an object property designated as a key by exact value.

</td></tr><tr><td>

Condition Token

</td><td>

&lt;property name&gt;&lt;conditional operator&gt;&lt;enclosed value&gt;Matches a single property of an object based on the condition specified.

</td></tr><tr><td>

Parameter Token

</td><td>

&lt;parameter name&gt;:'&lt;value&gt;'Passes a parameter by &lt;parameter name&gt; to the operation being called. The parameter may be consumed during CimIQL pre-processing or by the CIMOM via request, depending on the parameter.

</td></tr></tbody>
</table>### Properties Token

\* OR &lt;property name&gt;,&lt;property name&gt;,...

-   Specifies which properties are to be returned for each object of the final result set.
-   The wildcard \* returns all properties available. Otherwise, each property name desired is provided within a comma-separated list.
-   This token is required at the end of each statement.
-   Example:

    ```
    CIM_ComputerSystem[0].*
    ```


### Query Delimiter Token

. \(Period\)

-   Separates queries.
-   Example:

    ```
    CIM_ComputerSystem.PrimaryOwnerContact
    ```


### Index Token

\[index\]

-   Reduces a preceding query's results to a single object at the specified integer index.
-   This token is always optional.
-   Example:

    ```
    CIM_ComputerSystem[0].*
    ```


### Key Token

&lt;key name&gt;='&lt;value&gt;'

-   Matches an object property designated as a key by exact value.
-   The &lt;key name&gt; is the name of the property used as a key.
-   Example:

    ```
    CIM_ComputerSystem{CreationClassName='Linux_ComputerSystem',Name='runtime'}.*
    ```


### Condition Token

&lt;property name&gt;&lt;conditional operator&gt;&lt;enclosed value&gt;

-   Matches a single property of an object based on the condition specified.
-   The &lt;property name&gt; is the name of the property to match against.
-   The &lt;conditional operator&gt; determines how the property's actual value is compared to its expected value. The operators available are equality \(=\) and inequality \(!=\).
-   The &lt;enclosed value&gt; should be one of the following:
    -   Literal value enclosed in single-quotes ' ... '. For example, foo='bar'
    -   Regular expression, enclosed by a pair of slashes / ... /. For example, foo=/bar.\*/
-   Example:

    ```
    CIM_ComputerSystem{{Name!='runtime'}}.*
    ```


### Parameter Token

&lt;parameter name&gt;:'&lt;value&gt;'

-   Passes a parameter by &lt;parameter name&gt; to the operation being called. The parameter may be consumed during CimIQL pre-processing or by the Common Information Model Object Manager \(CIMOM\) via request, depending on the parameter.
-   Example:

    ```
    CIM_ComputerSystem.CIM_RunningOS{{ResultClass:'Win32_ComputerSystem'}}.*
    ```


## CimIQL tutorial

This is a tutorial by example where each example builds on the previous example.

<table id="table_e4t_35d_lp"><thead><tr><th>

Order

</th><th>

CimIQL Statement

</th><th>

Result

</th></tr></thead><tbody><tr><td>

1

</td><td>

CIM\_ComputerSystem\[0\].\*

</td><td>

Retrieves the [first result](r_CIMProbe.md#IndexToken) of all instances of CIM\_ComputerSystem and its descendants. Retrieves all [properties](r_CIMProbe.md#PropertiesToken).

</td></tr><tr><td>

2

</td><td>

CIM\_ComputerSystem.PrimaryOwnerContact

</td><td>

Retrieves all instances of CIM\_ComputerSystem and their descendants. Retrieves only one [property](r_CIMProbe.md#PropertiesToken), PrimaryOwnerContact.

</td></tr><tr><td>

3

</td><td>

CIM\_ComputerSystem\{CreationClassName='Linux\_ComputerSystem',Name='runtime'\}.\*

</td><td>

Retrieves a single unique instance of CIM\_ComputerSystem and its descendants. All [key tokens](r_CIMProbe.md#KeyToken) must be specified within the \{ \} [identity token](r_CIMProbe.md#GetObjectToken).

</td></tr><tr><td>

4

</td><td>

CIM\_ComputerSystem\{\{Name!='runtime'\}\}.\*

</td><td>

Retrieves all instances and descendants of CIM\_ComputerSystem that do not have a Name [property](r_CIMProbe.md#PropertiesToken) of 'runtime'.

 The [filter token](r_CIMProbe.md#EnumerateObjectsToken) \{\{ \}\} filters out instances that do not contain all of the properties/keys specified.

</td></tr><tr><td>

5

</td><td>

CIM\_ComputerSystem\{\{Name=/^run.\*$/\}\}.\*

</td><td>

Retrieves all instances and descendants of CIM\_ComputerSystem that have a value matching the regular expression contained within the / / characters.

**Note:** The regular expression does not require single quotations.

 The [filter token](r_CIMProbe.md#EnumerateObjectsToken) \{\{ \}\} filters out instances that do not contain all of the properties/keys specified.

</td></tr><tr><td>

6

</td><td>

CIM\_ComputerSystem\{\{Name='runtime'\}\}\[2\].\*

</td><td>

Retrieves the [second result](r_CIMProbe.md#EnumerateAssociatedObjectsToken) of all instances of CIM\_ComputerSystem and its descendants [where](r_CIMProbe.md#EnumerateObjectsToken) the instances have a property Name of 'runtime'.

 The order of operations follows the query syntax.

1.  [Query](r_CIMProbe.md#GetObjectToken) server for all CIM\_ComputerSystem and descendants.
2.  [Filter](r_CIMProbe.md#EnumerateObjectsToken) results based on Name property.
3.  [Retrieve the second](r_CIMProbe.md#EnumerateAssociatedObjectsToken) instance that passed the filter.

</td></tr><tr><td>

7

</td><td>

CIM\_ComputerSystem.CIM\_RunningOS\[0\].Name

</td><td>

Retrieves the Name [property](r_CIMProbe.md#PropertiesToken) for the first CIM\_OperatingSystem instance of each CIM\_ComputerSystem instance.

 The middle-token, CIM\_RunningOS, is the name of the [Associator class](r_CIMProbe.md#EnumerateAssociatedObjectsToken), not the end-result.

</td></tr><tr><td>

8

</td><td>

CIM\_ComputerSystem.CIM\_RunningOS\{\{Name=/CentOS/\}\}\[0\].Name

</td><td>

Retrieves the Name [property](r_CIMProbe.md#PropertiesToken) for the first CIM\_OperatingSystem instance of each CIM\_ComputerSystem instance, [where](r_CIMProbe.md#EnumerateObjectsToken) each CIM\_OperatingSystem instance has a Name property containing 'CentOS'.

</td></tr></tbody>
</table>## CimIQL results

CIM Probe results are passed to the probe sensor as an XML document embedded within the &lt;output&gt; element.

The following is a commented example of a CimQuery batch result.

```
<!-- document root -->
 <cimqueryset>
 <!-- A single query and query result. Multiple <cimquery> tags may be provided. -->
 <cimquery>
   <!-- The original query, enclosed by CDATA. -->
   <query><!CDATA[[>CIM_ComputerSystem[0].PrimaryOwnerContact<! ]]></query>
   <!-- The resulting data is enclosed within a single <result> tag. -->
   <result>
     <!-- A single class instance result. Multiple <instance> tags may be provided.
          Special tags are prefixed with an underscore character. -->
     <instance>
       <!-- The instance's CIM classname -->
       <_classname>Linux_ComputerSystem</_classname>
       <!-- A set of this instances identifying keys. Always provided, regardless of property filters.
            Within here, each key is provided as <KeyName>VALUE</KeyName> with the VALUE enclosed as CDATA. -->
       <_key>
         <CreationClassName><![CDATA[Linux_ComputerSystem]]></CreationClassName>
         <Name><![CDATA[runtime]]></Name>
       </_key>
       <!-- Each property that matches the query's property filter will be provided here, in the same format as keys;
            As <PropertyName>VALUE<PropertyName> where VALUE is enclosed as CDATA -->
       <PrimaryOwnerContact><![CDATA[root@runtime]]></PrimaryOwnerContact>
     </instance>
   </result>
 </cimquery>
 </cimqueryset>
```

