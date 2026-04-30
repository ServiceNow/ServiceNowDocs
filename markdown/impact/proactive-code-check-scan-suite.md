---
title: Proactive Code Check scan suite matrix for the Impact Store Application
description: Refer to the Proactive Code Check \(PCC\) scan suite matrix for details on the checks performed during a PCC scan.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Proactive Code Check, Platform Health, Using Impact, Impact]
---

# Proactive Code Check scan suite matrix for the Impact Store Application

Refer to the Proactive Code Check \(PCC\) scan suite matrix for details on the checks performed during a PCC scan.

**Note:** Starting with Impact Zurich version 6.0.8 ServiceNow Store release, Proactive Code Check is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

<table id="table_agy_hml_m2c"><thead><tr><th>

Category

</th><th>

Name

</th><th>

Short\_description

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Performance

</td><td>

HSD0001049 Avoid Global UI Scripts

</td><td>

Avoid Global UI Scripts

</td><td>

Global UI scripts are loaded on every single page/form in ServiceNow even if the code within them is not called.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001058 SCRIPT Scoped app uses logging utils or deprecated methods

</td><td>

Scoped app uses logging utils or deprecated method - gs.log

</td><td>

Scoped applications should use scoped logging APIs rather than legacy methods.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001058 XML Scoped app uses logging utils or deprecated methods

</td><td>

Scoped app uses logging utils or deprecated method - gs.log

</td><td>

Scoped applications should use scoped logging APIs rather than legacy methods.

</td></tr><tr><td>

Performance

</td><td>

HSD0001116 Client Scripts should not be defined against the Global table

</td><td>

Client Scripts should not be defined against the Global table

</td><td>

A global client script is any client script where the selected Table is Global. Global client scripts have no table restrictions; therefore they will load on every page in the system introducing browser load delay in the process. There is no benefit to loading this kind of scripts on every page.

</td></tr><tr><td>

Performance

</td><td>

HSD0001126 SCRIPT Unnecessary dot walking to sys\_id from current object

</td><td>

Unnecessary dot walking to sys\_id from current object

</td><td>

Reference fields already store the Sys ID of the referenced record. Using gr.fieldname.sys\_id is a dot-walk and instructs the platform to perform another query only to return the same value. This is an unnecessary overhead.

</td></tr><tr><td>

Performance

</td><td>

HSD0001126 XML Unnecessary dot walking to sys\_id from current object

</td><td>

Unnecessary dot walking to sys\_id from current object

</td><td>

Reference fields already store the Sys ID of the referenced record. Using gr.fieldname.sys\_id is a dot-walk and instructs the platform to perform another query only to return the same value. This is an unnecessary overhead.

</td></tr><tr><td>

Performance

</td><td>

HSD0001128 SCRIPT Client-side code should not use synchronous AJAX methods

</td><td>

Client-side code should not use synchronous AJAX methods

</td><td>

Code that uses synchronous AJAX can possibly cause delays in processing UI events. It can be detrimental to performance and negatively impact user experience. Wherever possible, we should try to employ asynchronous AJAX.

</td></tr><tr><td>

Upgradability

</td><td>

HSD0001142 SCRIPT Client-side code should not use DOM manipulation technique

</td><td>

Client-side code should not use DOM manipulation technique

</td><td>

This customization technique gives a lot of control, but does frequently cause upgrade challenges. It is recommended not to use jQuery, PrototypeJS, gel and other techniques.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001153 SCRIPT Hard coded instance URL

</td><td>

Hard coded instance URL

</td><td>

Raises a finding for hard coded instance URLs as their use can be detrimental to functionality across environments.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001153 XML Hard coded instance URL

</td><td>

Hard coded instance URL

</td><td>

Raises a finding for hard coded instance URLs as their use can be detrimental to functionality across environments.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001174 REST Scripted Web Services writing data directly

</td><td>

Scripted Web Services writing data directly

</td><td>

Scripted Web Services insert/update/delete data directly, whereas it is recommended to utilize Script Includes because it provides a structured and documented approach for managing data operations, ensuring consistency, security, and maintainability within the platform.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001174 SOAP Scripted Web Services writing data directly

</td><td>

Scripted Web Services writing data directly

</td><td>

Scripted Web Services insert/update/delete data directly, whereas it is recommended to utilize Script Includes because it provides a structured and documented approach for managing data operations, ensuring consistency, security, and maintainability within the platform.

</td></tr><tr><td>

Security

</td><td>

HSD0001235 XML Avoid Dynamic JEXL Expressions inside Jelly tag

</td><td>

Avoid Dynamic JEXL Expressions inside Jelly tag

</td><td>

When writing Jelly code, avoid using dynamic JEXL expressions inside the Jelly tag \(or &lt;g2:evaluate&gt; for phase two\). While the code appears to work, it affects a memory resource \(called PermGen\) in the Java Virtual Machine, which can lead to performance issues and even system outages over time. The exception to using JEXL expressions inside &lt;g:evaluate&gt; tags is with static values, including: $\{AMP\}\\, $\{AND\}, $\{GT\}, $\{LT\}, and $\{SP\} \(and their phase two counterparts: $\[AMP\], $\[AND\], and so on\).

</td></tr><tr><td>

Upgradability

</td><td>

HSD0001247 Use of deprecated API RESTMessage \(V1\)

</td><td>

Use of deprecated API RESTMessage \(V1\)

</td><td>

The API allowed to send outbound REST messages using JavaScript.

 However the version 1 of RESTMessage has been deprecated.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001275 Scripts should not contain hard-coded IDs

</td><td>

Scripts should not contain hard-coded IDs

</td><td>

Hard coding sys\_ids makes the system more difficult to manage, and less able to move functionality between instances.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001278 Before Business Rules should not update\(\) or insert\(\) on other tables

</td><td>

Before Business Rules should not update\(\) or insert\(\) records on other tables

</td><td>

Running an insert\(\) or update\(\) in a onBefore BR will cause updates to other tables, even though the update may be cancelled.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001281 getMessage\(\) called in Client Script without preloading message key

</td><td>

getMessage\(\) called in Client Script without preloading message key

</td><td>

getMessage used in a client script needs to have the message key added to the Messages field on the script record.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001312 SCRIPT Avoid console.log\(\) usage in code

</td><td>

Code should not contain the console.log\(\) debugging method

</td><td>

The client-side function console.log could cause errors in certain browser versions. Furthermore, there is a good chance that what's being logged is information you would not want publicly exposed, and that persons with malicious intent could manipulate the script to reflect PII. It is never a good idea to go to production with console logging enabled. Console.log is invalid server side and therefore should not be there either.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001312 XML Avoid console.log\(\) usage in code

</td><td>

Code should not contain the console.log\(\) debugging method

</td><td>

The client-side function console.log could cause errors in certain browser versions. Furthermore, there is a good chance that what's being logged is information you would not want publicly exposed, and that persons with malicious intent could manipulate the script to reflect PII. It is never a good idea to go to production with console logging enabled. Console.log is invalid server side and therefore should not be there either.

</td></tr><tr><td>

Performance

</td><td>

HSD0001338 Business Rules should not be defined on the Global table

</td><td>

Business Rules should not be defined on the Global table \(Global Business Rule\)

</td><td>

A Global Business Rule is any Business Rule where the selected table is Global. Any other script can call Global Business Rules. Global Business Rules have no condition or table restrictions and load on every page in the system.

</td></tr><tr><td>

Performance

</td><td>

HSD0001347 SCRIPT Client-side code should not use GlideRecord

</td><td>

Client-side code should not use GlideRecord

</td><td>

The client side GlideRecord object is often inefficent, because it returns lots of unecessary data. GlideRecord and g\_form.getReference are both involved.

</td></tr><tr><td>

Performance

</td><td>

HSD0001358 SCRIPT Server-side code should not use GlideRecord.getRowCount\(\)

</td><td>

Server-side code should not use GlideRecord.getRowCount\(\) to count records

</td><td>

The GlideRecord.getRowCount\(\) works by getting the whole result set without using the build-in arithmetic functions of the database. GlideAggregate does use the database, therefore is often drastically faster. The exception to this recommendation is if you intend to loop through the records and process them anyway.

</td></tr><tr><td>

Performance

</td><td>

HSD0001358 XML Server-side code should not use GlideRecord.getRowCount\(\)

</td><td>

Server-side code should not use GlideRecord.getRowCount\(\) to count records

</td><td>

The GlideRecord.getRowCount\(\) works by getting the whole result set without using the build-in arithmetic functions of the database. GlideAggregate does use the database, therefore is often drastically faster. The exception to this recommendation is if you intend to loop through the records and process them anyway.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001392 Scripts should not use the eval\(\) method

</td><td>

Scripts should not use the eval\(\) method

</td><td>

The eval\(\) function evaluates or executes an argument. Improper use of eval\(\) opens up your code for injection attacks and debugging can be more challenging, as no line numbers are displayed with an error.

</td></tr><tr><td>

Performance

</td><td>

HSD0001554a JDBC Data Srcs with "Use last run datetime" disabled for update sets

</td><td>

JDBC Data Sources should have the "Use last run datetime" option check

</td><td>

Repeatedly importing data that has not changed leads to many skipped rows and unnecessarily bounds system resources.

</td></tr><tr><td>

Performance

</td><td>

HSD0001560 Use 'track by' in ngRepeat loops

</td><td>

Use 'track by' in ngRepeat loops

</td><td>

When using the ngRepeat directive without a 'track by' clause, the DOM elements are destroyed and rebuilt every time the source data is updated. Adding a 'track by' clause with a unique key \(such as a sys\_id\) allows the DOM elements to be reused rather than rebuilt, which significantly improves the performance of pages with large, complex lists.

</td></tr><tr><td>

Manageability

</td><td>

HSD0001578 Business Rules should not use the SOAP getResponse\(\) method

</td><td>

Business Rules should not use the SOAP getResponse\(\) method

</td><td>

getResponse blocks the transaction, waiting until a response is received. This is better done asynchronously.

</td></tr><tr><td>

Performance

</td><td>

HSD0001623 Read ACLs \(Security rules\) should not have GlideRecord/GlideAggregate

</td><td>

Read ACLs \(Security rules\) should not have GlideRecord/GlideAggregate

</td><td>

Read ACLs are frequently executed. Having complex database lookups can harm performance.

</td></tr><tr><td>

Security

</td><td>

HSD0002016 Server scripts in widgets should use GlideRecordSecure

</td><td>

Server scripts in widgets should use GlideRecordSecure instead of GlideRecord

</td><td>

The best practice should be that server scripts in widgets should use GlideRecordSecure rather than GlideRecord. This is to ensure that security ACLs are considered in all server interactions. To detect deviation from this, any instantiation of GlideRecord should be marked as a finding.

 Note that $sp.getRecord\(\) currently returns a GlideRecord object. This call should actually return a GlideRecordSecure object to be as secure as possible. While that is a separate enhancement outside of the HealthScan tool, it does pose a challenge in that it will be harder for HealthScan to detect the use of the GlideRecord object returned by $sp.getRecord.

</td></tr><tr><td>

Performance

</td><td>

HSD0002144 Leverage c.server.get\(\) for better widget performance

</td><td>

Leverage c.server.get\(\) for better widget performance

</td><td>

On the client script, c.server.get\(\) allows you to pass specific data to the server script. Doing this can have performance improvements over c.server.update\(\), which sends the entire data object.

</td></tr><tr><td>

Performance

</td><td>

HSD0002150 Remove unused services from widget client script.

</td><td>

Remove unused services from widget client script.

</td><td>

If injected services are not used in a widget's client controller script, consider removing them. Services which are injected and not used will be instantiated, which may have a performance impact. It is also good practice from a code readability perspective to only inject services that are required.

</td></tr><tr><td>

Performance

</td><td>

HSD0002154 Don't use $rootScope.$on in a widget's client script.

</td><td>

Don't use $rootScope.$on in a widget's client script.

</td><td>

$rootScope.$on should only be used in a service. Using event listeners on $rootScope in a widget's client controller script can cause memory leaks if the listeners are not manually destroyed. Every time a widget is loaded, the controller is initialized, and every listener initialized on the $rootScope will not be destroyed with the controller, unless done so manually.

 Services have no other alternative but to fire events on $rootScope, and the listen for events on $rootScope. This is because services are initialized once across the app and do not have their own scope. It is okay to use $rootScope.$on in a service.

</td></tr><tr><td>

Manageability

</td><td>

HSD0002808 Client Scripts without description

</td><td>

Client Scripts without description

</td><td>

Client Scripts where the description is either empty, very short or the same as the script name.

</td></tr><tr><td>

Manageability

</td><td>

HSD0002808 Script Includes without description

</td><td>

Script Includes without description

</td><td>

Script Includes where the description is either empty, very short or the same as the script name.

</td></tr><tr><td>

Manageability

</td><td>

HSD0002827 All events should have a description

</td><td>

All events should have a description

</td><td>

All custom events in the event registry should have the "description" field populated. This will ensure that the event's purpose is easily identifiable by administrators who did not create the registry entry and improve maintainability of the instance.

</td></tr><tr><td>

Manageability

</td><td>

HSD0002828 All events should have the "fired by" field populated

</td><td>

All events should have the "fired by" field populated

</td><td>

All custom events in the event registry should have the "fired\_by" field populated. This will ensure that the event's trigger is easily identifiable by administrators who did not create the registry entry and improve maintainability of the instance.

</td></tr><tr><td>

Manageability

</td><td>

HSD0003076 Basic authentication credentials on SOAP Message definition

</td><td>

Basic authentication credentials on SOAP Message definition

</td><td>

Basic Authentication for outbound SOAP Messages should use Basic Auth Profiles instead of putting the credentials on the function definition itself.

</td></tr><tr><td>

Manageability

</td><td>

HSD0003081 Basic authentication credentials on REST Message definition

</td><td>

Basic authentication credentials on REST Message definition

</td><td>

Basic Authentication for outbound REST Messages should use Basic Auth Profiles instead of putting the credentials on the function definition itself.

</td></tr><tr><td>

Upgradability

</td><td>

HSD0003307 Change Request table should not be extended

</td><td>

Change Request table should not be extended

</td><td>

At least one child table extending Change Request has been created.

 Extending Change Request with custom child tables should not be done:

-   To support a custom Change Request table a high amount of customization to the other ITSM processes is required
-   New functionality in future releases might not work on extended tables or would require further customization

</td></tr><tr><td>

Manageability

</td><td>

HSD0003625 Business Rule script should be encapsulated in executeRule function

</td><td>

Script code in Business Rules should be encapsulated in the executeRule function

</td><td>

The code should check if there is any business rule that have some code that is not encapsulated in the executeRule function.

</td></tr><tr><td>

Upgradability

</td><td>

HSD0004147 Use of GlideDialogWindow and GlideOverlay

</td><td>

Use of GlideDialogWindow and GlideOverlay

</td><td>

Checks for the use of GlideDialogWindow and GlideOverlay, which cannot be tested by ATF.

</td></tr><tr><td>

Performance

</td><td>

HSD0004365 SCRIPT Cache flushed as part of scripts

</td><td>

Cache flushed as part of scripts

</td><td>

If a cache flush is triggered as part of a non-ootb script execution this will require the platform to rebuild the cache before returning to its BAU state. This activity has a significant performance impact.

</td></tr><tr><td>

Performance

</td><td>

HSD0004726 SCRIPT Debugger should not be used in scripts

</td><td>

Debugger should not be used in scripts

</td><td>

The debugger statement is used to tell the executing JavaScript environment to stop execution and start up a debugger at the current point in the code. This has fallen out of favor as a good practice with the advent of modern debugging and development tools. Production code should definitely not contain debugger, as it will cause the browser to stop executing code and open an appropriate debugger.

</td></tr><tr><td>

Performance

</td><td>

HSD0006666 Check if current.update\(\) is used in a business rule

</td><td>

Check if current.update\(\) is used in a business rule

</td><td>

Current.update\(\) used in a business rule causes recursive updates and can significantly impact performance.

</td></tr><tr><td>

Manageability

</td><td>

HSD0013213 SCRIPT Detecting hard-coded strings in addInfoMessage\(\) usage

</td><td>

Detecting hard-coded strings in addInfoMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addInfoMessage\(\) on both the client and server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0013213 XML Detecting hard-coded strings in addInfoMessage\(\) usage

</td><td>

Detecting hard-coded strings in addInfoMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addInfoMessage\(\) on both the client and server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0013215 SCRIPT Detecting hard-coded strings in alert\(\) usage

</td><td>

Detecting hard-coded strings in alert\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in alert\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0013215 XML Detecting hard-coded strings in alert\(\) usage

</td><td>

Detecting hard-coded strings in alert\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in alert\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014228 SCRIPT Detecting hard-coded strings in addErrorMessage\(\) usage

</td><td>

Detecting hard-coded strings in addErrorMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addErrorMessage\(\) on both the client and server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014228 XML Detecting hard-coded strings in addErrorMessage\(\) usage

</td><td>

Detecting hard-coded strings in addErrorMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addErrorMessage\(\) on both the client and server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014229 SCRIPT Detecting hard-coded strings in setError\(\) usage

</td><td>

Detecting hard-coded strings in setError\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in setError\(\) on the server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014229 XML Detecting hard-coded strings in setError\(\) usage

</td><td>

Detecting hard-coded strings in setError\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in setError\(\) on the server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014231 SCRIPT Detecting hard-coded strings in confirm\(\) usage

</td><td>

Detecting hard-coded strings in confirm\(\) usage - SCRIPT

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in confirm\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014231 XML Detecting hard-coded strings in confirm\(\) usage

</td><td>

Detecting hard-coded strings in confirm\(\) usage - XML

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in confirm\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014232 SCRIPT Detecting hard-coded strings in prompt\(\) usage

</td><td>

Detecting hard-coded strings in prompt\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in prompt\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014232 XML Detecting hard-coded strings in prompt\(\) usage

</td><td>

Detecting hard-coded strings in prompt\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in prompt\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014233 SCRIPT Detecting hard-coded strings in addMessage\(\) usage

</td><td>

Detecting hard-coded strings in addMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addMessage\(\) on the server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014233 XML Detecting hard-coded strings in addMessage\(\) usage

</td><td>

Detecting hard-coded strings in addMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addMessage\(\) on the server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014234 SCRIPT Detecting hard-coded strings in addFormMessage\(\) usage

</td><td>

Detecting hard-coded strings in addFormMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addFormMessage\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014234 XML Detecting hard-coded strings in addFormMessage\(\) usage

</td><td>

Detecting hard-coded strings in addFormMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addFormMessage\(\) on the client side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014544 SCRIPT Detecting hard-coded strings in addWarningMessage\(\) usage

</td><td>

Detecting hard-coded strings in addWarningMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addWarningMessage\(\) on both the client and server side.

</td></tr><tr><td>

Manageability

</td><td>

HSD0014544 XML Detecting hard-coded strings in addWarningMessage\(\) usage

</td><td>

Detecting hard-coded strings in addWarningMessage\(\) usage

</td><td>

Hard-coded messages/strings in the code will not be localized. Detecting such occurrences in addWarningMessage\(\) on both the client and server side.

</td></tr></tbody>
</table>