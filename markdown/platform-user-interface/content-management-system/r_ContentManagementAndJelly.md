---
title: Content Management and the Apache Jelly engine
description: Apache Jelly is a Java-based and XML-based scripting and processing engine for turning XML into executable code.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Content Management and the Apache Jelly engine

Apache Jelly is a Java-based and XML-based scripting and processing engine for turning XML into executable code.

The Apache Jelly engine closely resembles XML and should be comfortable for developers familiar with JavaScript, XML, XHTML, or HTML. In the ServiceNow instance, the Apache Jelly engine renders items such as forms, lists, and UI Pages. Apache Jelly code renders well within a dynamic content block, but can have issues when used in static blocks. You can use Jelly tags, calls, and statements, but HTML acts just like XHTML.

```
<?xml version= "1.0" encoding= "utf-8" ?>
<j:jelly trim = "false" xmlns:j = "jelly:core" xmlns:g = "glide" xmlns:j2 = "null" xmlns:g2 = "null" >
 
	<j:if test = "${current_page.getName()=='Solutions'}" >
	<h1 class = "page_name" > <b> <a href = "solutions.do?" title = "${gs.getMessage('Solutions')}" >${gs.getMessage('Solutions')}</a> </b> </h1>
	<p class = "page_description" >
	 	    ${current_page.getDescription()}
	</p> <br />
	</j:if>
	<j:if test = "${current_page.getName()=='IT 3.0'}" >
	   <h1 class = "page_name" > <b> <a href = "solutions.do?" title = "${gs.getMessage('Solutions')}" >${gs.getMessage('Solutions')}</a> </b> | ${current_page.getName()}</h1>
	   <p class = "page_description" >
	 	    ${current_page.getDescription()}
		</p> <br />
		</j:if>
		</j:jelly>
```

Ensure that all tags are closed. If the tag is not a naturally closing tag, then place a forward slash before the end bracket. For example, a `<BR />` or an `<IMG src="cms.png" />`.

If you are unfamiliar with Jelly scripting, review these topics:

-   [Jelly tags](https://www.servicenow.com/docs/access?context=r_JellyTags&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)
-   [Extensions to Jelly syntax](https://www.servicenow.com/docs/access?context=c_ExtensionsToJellySyntax&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)
-   [Jelly escaping types](https://www.servicenow.com/docs/access?context=r_JellyEscapingTypes&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

Include the following tag with all Apache Jelly scripts.

```
<j:jelly trim= "false" xmlns:j= "jelly:core" xmlns:g= "glide" xmlns:j2= "null" xmlns:g2= "null" >
```

The tag looks complex, but keep the following information in mind.

-   Apache Jelly script uses multiple namespaces.
-   There are two types of prefixes in tags: j and g. The j prefix is used for tags that are natively part of Apache Jelly. The g prefix is used for tags that the ServiceNow platform created and is using for platform purposes.

The j2 and g2 prefixes are just like j and g, except that they are processed in a second phase. The Apache Jelly script parser runs through each j and g tag respectively. For example:

```
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
	<j:set var="jvar_phase1" value="Hello" />
	<j2:set var="jvar_phase2" value="World" />
	${jvar_phase1} $[jvar_phase2]
</j:jelly>
```

In phase 1, the parser runs through all the j and g tags. It then caches the result. Before it runs the second phase, it takes the j and g namespaces and moves the namespaces to the second phase. It looks something like the following code.

```
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="jelly:core" xmlns:g2="glide">
	<j2:set var="jvar_phase2" value="World" />
	Hello $[jvar_phase2]
</j:jelly>
```

For subsequent calls of this script, only phase 2 is parsed.

**Note:** If you plan to use phase 2 Jelly tags \(g2 and j2\) on the Content Type \[content\_type\] or Dynamic Content \[content\_block\_programmatic\] tables, select the **Two phase** option on the content form.

Another example is to create a report of all open incidents assigned to each group. For this purpose, you could use a report and save time, but it is a good example for learning Jelly. Start with the Jelly tag:

```
<j:jelly trim= "false" xmlns:j= "jelly:core" xmlns:g= "glide" xmlns:j2= "null" xmlns:g2= "null" >
</j:jelly>
```

First, you need a list of open incidents. Use a `g2:evaluate` tag. The evaluate tag runs the script. Anything inside the tag is parsed like a business rule, so, for example, you can call global business rules, script includes, and gliderecord.

```
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
	<g:evaluate var="jvar_groups" object="true">
		var now_GR = new GlideRecord("sys_user_group");
		gr.orderBy('name');
		gr.query();
		gr;
	</g:evaluate>
</j:jelly>
```

This script is in phase 1 because frequent changes to incident assignment groups are not expected. Also notice the `var` attribute on the evaluate tag. This attribute specifies what variable is set from this block. At the end of the script, there is a `gr` on a line by itself. That last line is what sets the variable.

You can omit the `jvar_groups` variable, but then all the variables in the evaluate tag become Apache Jelly variables. The `object=true` specifies that the variable is not a primitive data type. If `object=true` is omitted, the script would break because `jvar_groups` would only be able to hold items like integers and strings.

After the evaluate tag, loop through these groups and find the incidents for each one.

```
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
	<g:evaluate var="jvar_groups" object="true">
		var now_GR = new GlideRecord("sys_user_group");
		gr.orderBy('name');
		gr.query();
		gr;
	</g:evaluate>
	<table>
		<tr>
			<th>Name</th>
			<th>Incidents</th>
		</tr>
		<j:while test="${jvar_groups.next()}">
			<tr>
				<td>${HTML:jvar_groups.getValue('name')}</td>
				<td></td>
			</tr>
		</j:while>
	</table>
</j:jelly>
```

You can include normal XML in the Apache Jelly script at any time. Since there is no namespace, the Apache Jelly script does not try to parse the XML tags. Notice the `j:while` loop. It is a normal while loop and can iterate through a GlideRecord object. Also notice that you output a value with `${HTML:jvar_groups.getValue('name')}`. Here are the important elements:

-   The outer brackets, `${}`, specify the output of the variable and the phase in which the variable is output: `${}` means first phase, `$[]` means second phase.
-   HTML before the expression is for escaping the output. The expression `jvar_groups.getValue('name')` is being escaped for HTML. For other types of escaping, there are JS \(Javascript\), NS \(No Script\), and some other options.

To select only one record and not iterate through many records, the code looks like the following example:

```
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
	<g:evaluate var="jvar_groups" object="true">
		var now_GR = new GlideRecord("sys_user_group");
		gr.orderBy('name');
		gr.query();
		gr;
	</g:evaluate>
	<j:if test="${jvar_groups.next()}">
		We found ${HTML:jvar_groups.getValue('name')}
	</j:if>
</j:jelly>
```

-   **[Content management and Jelly code examples](r_CodeExamples.md)**  
Code examples

**Parent Topic:**[Content blocks](../concept/c_ContentBlocks.md)

**Related topics**  


[Configure a content block](../task/t_CreateAContentBlock.md)

[View CMS block tags](../task/t_CMSBlockTag.md)

[Types of content blocks](r_TypesOfContentBlocks.md)

