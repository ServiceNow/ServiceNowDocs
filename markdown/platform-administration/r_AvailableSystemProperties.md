---
title: Available system properties
description: Some properties are available on a system properties form, but some lesser-used properties are available only from the System Property \[sys\_properties\] table. Sometimes, the property does not exist in a base instance, but can be added if you change the value.Add or create a property to control system behavior.You can add a module in the application navigator to access the list of system properties. This module makes it easy to add properties to the System Properties table.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 141
breadcrumb: [Basic system configuration, Get started, Administer the ServiceNow AI Platform]
---

# Available system properties

Some properties are available on a system properties form, but some lesser-used properties are available only from the System Property \[sys\_properties\] table. Sometimes, the property does not exist in a base instance, but can be added if you change the value.

**Note:** The Instance Security Hardening Settings content contains detailed descriptions, and compliance values, for the security-related system properties and plugins in the ServiceNow AI Platform. To learn more about each of these properties, see [Instance Security Hardening Settings](https://www.servicenow.com/docs/access?context=update-security-hardening-params&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **cdu.record.watcher.timeout**

    Maximum waiting period for the Cloud Discovery schedule configuration wizard to stop watching the record watchers while validating account, member account Discovery, and logical database Discovery.

    -   Type: integer
    -   Default value: 120,000 milliseconds
    -   Location: System properties
-   **com.cmdb.baseline.max\_changes**

    Maximum number of changes and relationships for a CI that can appear in the baseline diff for the CI.

    -   Type: integer
    -   Default value: 100
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Baseline Properties**
-   **com.glide.attachment.max\_size**

    Sets the maximum file attachment size in megabytes. An empty value in this field allows attachments up to a maximum of 1 KB.

    -   Type: integer
    -   Default value: 1024
    -   Location: **System Properties** &gt; **Security**
-   **com.glide.cs.collab.event\_queue.enabled**

    Switch to enable the event queue for badge count calculation and publish.

    **Note:** If you set com.glide.cs.collab.event\_queue.enabled to **true**, you must manually enable the Sidebar notification events process schedule record \("sys\_trigger"\) by changing its *trigger\_type* value.

-   **com.glide.cs.collab.event\_queue.threshold**

    Calculates the unread count for each member of a chat. If the chat has too many members, this responder thread will be slow so offload this to the event queue. Default value: 50.

-   **com.glide.cs.collab.notify\_all\_members**

    If Sidebar is unable to deliver messages to a Microsoft Teams user, this property determines who a "message not sent" notification is sent to. If this property is **true**, then a notification is sent to all Sidebar users in the discussion. If **false**, then the notification is sent only to the sender of the message.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.glide.cs.collab.teams\_outage\_timer**

    Length of time the "message not sent" notification \(see com.glide.cs.collab.notify\_all\_members\) displays.

    -   Type: integer
    -   Default value: 5
    -   Location: System Property \[sys\_properties\] table
-   **com.glide.cs.conversation\_history\_cross\_channel.enabled**

    Enables \(**true**\) or disables \(**false**\) the display of cross-channel conversation history in the chat panel when an agent is having a conversation with a requester.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.cs.field.boolean.show.choice\_picker**

    Enables \(**false**\) or disables \(**true**\) a Boolean option to requesters whenever a dynamic choice node only has a single value associated. When set to **true**, the dynamic choice node displays to requesters with only the single value selection option and no Boolean option.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **com.glide.cs.gen\_ai.enable\_mid\_topic\_ai\_search**

    Enables or disables AI Search result in Mid Topic Discovery using this flag.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.glide.cs.instance\_uri\_override**

    Enables Virtual Agent to use this URL value to override the instance URL for link generation. The value entered must be a direct, full URL such as http://www.example.com to work correctly.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **com.glide.cs.notification.create\_llm\_actions\_after\_topic\_migration**

    Enables \(`true`\) or disables \(`false`\) whether actions for Virtual Agent notifications and Proactive Triggers are created after LLM topics are published during the NLU to LLM topic migration workflow.

    -   Type: true \| false
    -   Default: true
    -   Location: System Property \[sys\_properties\] table
-   **com.glide.cs.proactive\_trigger.create\_llm\_actions\_after\_topic\_migration**

    Enables \(true\) or disables \(false\) whether actions for Proactive Triggers are created after LLM topics are published during the NLU to LLM topic migration workflow.

    -   Type: true \| false
    -   Default: true
    -   Location: System Property \[sys\_properties\] table
-   **com.glide.csv.loader.ignore\_non\_parseable\_lines**

    Enables \(`true`\) or disables \(`false`\) ignoring one or more lines \(rows\) in an import set that contains bad data, such as a row that is missing a column of data.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.csv.loader.max\_errors\_allowed**

    Sets the maximum number of lines \(rows\) that an import can ignore before failing. If the import succeeds, the import lists the number of rows ignored due to errors.

    -   Type: integer
    -   Default value: 100
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.email.max\_read**

    Specifies the maximum number of emails a POP3 reader should process concurrently.

    -   Type: integer
    -   Default value: 20
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.event\_handler.CollabNotificationEventHandler**

    Specifies the event handler for the sidebar\_notification queue.

-   **com.glide.event\_manager.sidebar\_notification.claim\_limit**

    Specifies the number of sidebar\_notification events the job on each node polls each time.

-   **com.glide.interaction.autocreate\_relationships**

    Specifies whether auto-logging of records in the interaction\_related\_record table is turned on or off during active interactions.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.loader.verify\_target\_field\_size**

    Enables dynamic resizing of import set fields. With the default setting of **false**, up to 20 records of the source data are sampled to determine the import set field length. If the field is empty in all the sampled records, the default length of 40 is used. Any data loaded that exceeds the import set table field length is truncated. Set this property to **true** to allow any import set field to increase the column size by 100 to match the length of the data. For example, if the incoming source data has a length of 60, the system sets the length of the column to 160.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.script.fencing.secure\_child\_tables**

    Controls whether to apply cross-scope access rules when querying application-administered child tables with GlideRecord from a parent table. When false, administrators can view child table data from the parent table, even if the child table scoping configuration is set to avoid this. If you set this property to true, you can change it back to false only by contacting Customer Service and Support.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.script.scoped\_evaluator.allow\_dynamic\_cross\_scope\_eval\_scoped\_administration**

    Controls whether to allow scripts in applications with Scoped Administration enabled to be modified and executed by scripts in the global scope. When false, scripts in applications with Scoped Administration can't be modified or executed by scripts in the global scope.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.scripting.module.use\_module\_sandbox**

    Separates the JavaScript module runtime environment from scripts​. Setting this property to false may improve performance.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.soap.include\_non\_db\_fields**

    Controls whether non-database fields, such as the sys\_tags field, are included in WSDLs and SOAP responses \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.ssl.read.timeout**

    Sets the time-out value in seconds for SSL connections during read operations. Typically, this setting is used as part of LDAPS. If you enter timeout values for both this system property and the LDAP **Read timeout** field, the lowest timeout value takes precedence.

    -   Type: integer
    -   Default value: 10
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.glide.ui.virtual\_host**

    Specifies Guided Tour Designer callout icons. When set, callout icons appear in the designer instead of letters.

    -   Type: String
    -   Value: pa,html,script,include scripts,glide,custprefix,\_sn
    -   Location: System Property \[sys\_properties\] table
-   **com.glideapp.canvas**

    Enables \(**true**\) or disables \(**false**\) responsive canvas for dashboards. When enabled, all new dashboards use responsive canvas.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.apps.publish.include\_inactive\_choices**

    Specifies whether choice table selections marked as inactive \(`sys_choice inactive attribute = true`\) should be included when publishing an application \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.apps.publish.maxrows**

    Defines the maximum number of data records to include when publishing an application.

    -   Type: integer
    -   Default value: 1,000
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.assessment.decision\_matrix\_filter\_max\_entries**

    Defines the maximum number of items to show for a decision matrix field filter.

    -   Type: integer
    -   Default value: 1,000
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.assessment.signature\_authentication**

    Requires authentication for a user signature.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.dd.publish\_to\_app\_repo\_enabled**

    Enables \(**true**\) or disables \(**false**\) display of the **Publish To App Repo** permission in Manage Developers.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.dd.publish\_to\_app\_store\_enabled**

    Enables \(**true**\) or disables \(**false**\) display of the **Publish To App Store** permission in Manage Developers.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.dd.publish\_to\_update\_set\_enabled**

    Enables \(**true**\) or disables \(**false**\) display of the **Publish To Update Set** permission in Manage Developers.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.dd.upgrade\_app\_enabled**

    Enables \(**true**\) or disables \(**false**\) display of the **Update App** permission in Manage Developers.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.hr.core.impersonateCheck**

    Allows a user to have identical permissions/access as the person they are impersonating. If **true**, access and restrictions apply when impersonating another user. If **false**, the user has identical permissions/access as the person they are impersonating.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.iam.log\_level**

    Logging level for the business rule MapUpstreamImpactedCI. Debug is the most detailed option with full trace of how the Impacted CI List is calculated. Error is the minimal logging option with only severe errors being logged.

    -   Type: string
    -   Default value: info
    -   Possible values: debug, info, error
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.on\_call\_rotation.reminders.showtz**

    Specifies whether to show the user time zone \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.snc.pa.activate\_kpi\_signals**

    Create this property and set to 'false' to deactivate the KPI Signals feature.

    -   Type: Boolean true \| false
    -   Default value: Does not exist but is treated as 'true'
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.snc.pa.correlation.enable\_insights**

    Enables the generation of key contributor insight cards.

    -   Type: true/false \(Boolean\)
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.snc.pa.dc.batch\_score\_insert**

    When true, Performance Analytics [data collection jobs](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-data-collector&ft:locale=en-US) insert indicator scores to the database in batches. When false, indicator scores are inserted one by one. Even when true, batch score insertion is performed only as a fallback when nested data collection \(com.snc.pa.dc.nested\_collection\) has been disabled.

    -   Type: Boolean true \| false
    -   Default value: true
    -   Location: System Properties \[sys\_properties\] table
-   **com.snc.pa.dc.flush\_snapshot\_count**

    Maximum number of Performance Analytics [snapshots](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-snapshot&ft:locale=en-US) to store in the memory during data collection. When this number is reached, the snapshots are offloaded to the database, freeing memory.

    -   Type: integer
    -   Default value: 1000
    -   Location: System Properties \[sys\_properties\] table
-   **com.snc.pa.dc.nested\_collection**

    Activates a hierarchical approach to score collection, where Indicator &gt; level 1 breakdown &gt; level 2 breakdown. This approach is more resource efficient than a flat hierarchical approach, which creates redundant objects.

    -   Type: Boolean true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.snc.pa.dc.max\_breakdown\_elements\_limit**

    Maximum number of [breakdown elements](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-breakdown-element&ft:locale=en-US) retrieved by data collection for each [breakdown source](https://www.servicenow.com/docs/access?context=breakdown-sources&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US). This property is handled differently depending on whether nested collection is enabled. If nested collection is enabled, only those elements that have non-null scores count against this limit. If nested collection is disabled, such as under optimized data collection, all elements on the breakdown source count against the limit. When a breakdown source exceeds this limit, breakdown scores are not collected from that source.

    -   Type: integer
    -   Default value: 10000
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.dc.max\_error\_count**

    Maximum errors that may occur before data collection is stopped.

    -   Type: integer
    -   Default value: 500
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.dc.max\_records**

    Maximum number of records that are stored during a data collection.

    -   Type: integer
    -   Default value: 5000
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.dc.max\_row\_count\_indicator\_source**

    Maximum number of rows that are allowed to be fetched from an [indicator source](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-indicator-source&ft:locale=en-US). This property only applies to jobs that do not use [Optimized data collection](https://www.servicenow.com/docs/access?context=optimized-data-collection&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

    -   Type: integer
    -   Default value: 50000
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.dc.hsql.max\_row\_count\_indicator\_source**

    Maximum number of rows that are allowed to be fetched from an Indicator Source. This property only applies to jobs that use [Optimized data collection](https://www.servicenow.com/docs/access?context=optimized-data-collection&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

    -   Type: integer
    -   Default value: 1 million
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.dc.script\_timeout**

    Maximum time in seconds that a script is allowed to run during a data collection cycle.

    -   Type: integer
    -   Default value: 30
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.dc.use\_hashcode\_for\_distinct**

    Sets whether Count Distinct aggregations are stored as separate values in memory or as a HashCode. When the value of this property is True, a HashCode is used, which consumes less memory than storing individual values.

    -   Type: Boolean true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.snc.pa.insight.max\_days\_in\_past**

    By default, retrieve insights created within the number of days in the past that this property specifies.

    -   Type: Integer
    -   Default value: 14
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **com.snc.pa.insights.query\_limit**

    Limit the number of rows when querying the par\_computed\_insight table in the GET response to the Insights API.

    -   Type: Integer
    -   Default value: 1000
    -   Location: The System Properties \[sys\_properties\] table
-   **com.snc.pa.target\_batch\_operation\_limit**

    Applies only to KPI Details: The maximum number of targets that can be inserted or updated in one bulk action on the Targets Configuration page.

    -   Type: integer
    -   Default value: 100
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.dc.script.use.sandbox**

    Controls whether Performance Analytics data collection scripts use the sandbox. Only users with the security\_admin role can modify this property.

    **Important:** Exercise caution when turning off this property. When set to false, unauthorized users may be able to execute malicious actions on your instance.

    -   Type: Boolean true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.formula\_indicator\_valid\_breakdown**

    Controls whether users can apply a breakdown to a [formula indicator](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-formula-indicator&ft:locale=en-US) when not all [contributing indicators](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=contributing-indicator&ft:locale=en-US) in the formula use that breakdown. When true, all contributing indicators must use the formula. When false, a breakdown can be applied when at least one of the contributing indicators uses it.

    -   Type: Boolean true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.pa.xmr.processes.limit**

    The maximum number of KPI Signals Configurations \(pa\_xmr\_processes\) that can be evaluated by the KPI Signals Insight Job. After this number of processes have been evaluated, the remaining processes are ignored.

    -   Type: Integer
    -   Default: 1000
    -   Maximum: 10,000
-   **com.snc.pdf.whitelisted\_urls**

    Stores a list of URLs allowed to be rendered in a PDF generated by the [PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). This list is only verified if the glide.pdf.url.whitelisting.enabled property is set to true.

    -   Type: string
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.project.default\_schedule**

    Stores the sys\_id of the default schedule attached to projects.

    -   Type: string
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.project.loglevel**

    Automatically resubmits timed-out Ajax requests.

    -   Type: choice list
    -   Default value: 0 \(debugging disabled\)
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.project.wbs\_gantt**

    Automatically resubmits timed-out Ajax requests.

    -   Type: true \| false
    -   Default value: false
    -   Location: **Project** &gt; **Administration** &gt; **Properties**
-   **com.snc.task.associate\_ci**

    List of all task types where user wants to associate CIs using a List system.

    -   Type: string
    -   Default: incident,problem,change\_request
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.task.refresh\_impacted\_services**

    List of all task types where **Refresh Impacted Services** UI action is enabled.

    -   Type: string
    -   Default value: incident,change\_request
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.time\_card.default\_rate**

    \(Cost Management plugin\) Sets a default hourly rate to use if no labor rate cards apply to the user.

    -   Type: integer
    -   Default value: 50
    -   Location: System Property \[sys\_properties\] table
-   **com.snc.time\_worked.update\_task\_timer**

    Enables \(**true**\) or disables \(**false**\) updating the task timer value based on changes to the task time worked records. Uses the Update task time business rule.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **csm\_auto\_account\_domain\_generation**

    When new account in Customer Service application is created, domain is created and placed under TOP domain. If parent field on account form is populated, and new record is inserted, it creates that account as a subdomain of the parent.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **css.assessment.caption.background.color**

    Sets the background color of the caption on assessment and survey questionnaires.

    -   Type: color
    -   Default value: \#eee
    -   Location:
        -   **Assessments** &gt; **Admin** &gt; **Assessment Properties**
        -   **Survey Management** &gt; **Administration** &gt; **Properties**
-   **css.assessment.caption.font.color**

    Sets the font color of the caption text on assessment and survey questionnaires.

    -   Type: color
    -   Default value: \#ffffff
    -   Location:
        -   **Assessments** &gt; **Admin** &gt; **Assessment Properties**
        -   **Survey Management** &gt; **Administration** &gt; **Properties**
-   **css.assessment.question.header.background.color**

    Sets the background color of question headers on assessment and survey questionnaires.

    -   Type: color
    -   Default value: \#767676
    -   Location:
        -   **Assessments** &gt; **Admin** &gt; **Assessment Properties**
        -   **Survey Management** &gt; **Administration** &gt; **Properties**
-   **css.$nav-highlight-main**

    Sets the color for the navigation expanded items highlight background.

    -   Type: color
    -   Default Value: \#3D4853
    -   Location: System Property \[sys\_properties\] table
-   **css.$nav-hr-color**

    Sets the color for the navigation separator.

    -   Type: color
    -   Default Value: \#303A46
    -   Location: System Property \[sys\_properties\] table
-   **css.$navpage-header-bg**

    Sets the color for the header background.

    -   Type: color
    -   Default Value: \#303A46
    -   Location: System Property \[sys\_properties\] table
-   **css.$navpage-header-color**

    Sets the color for the banner text.

    -   Type: color
    -   Default Value: \#FFFFFF
    -   Location: System Property \[sys\_properties\] table
-   **css.$navpage-nav-bg-sub**

    Sets the color for the background for navigator and sidebars.

    -   Type: color
    -   Default Value: \#455464
    -   Location: System Property \[sys\_properties\] table
-   **css.$navpage-nav-border**

    Sets the color for the border for Core UI.

    -   Type: color
    -   Default Value: \#DDD
    -   Location: System Property \[sys\_properties\] table
-   **css.$navpage-nav-color-sub**

    Sets the color for module text in Core UI.

    -   Type: color
    -   Default Value: \#BEC1C6
    -   Location: System Property \[sys\_properties\] table
-   **css.$navpage-nav-selected-bg**

    Sets the color for navigator selected tab background.

    -   Type: color
    -   Default Value: \#4B545F
    -   Location: System Property \[sys\_properties\] table
-   **css.$navpage-nav-selected-color**

    Sets the color for the currently selected navigation tab icon color for Core UI.

    -   Type: color
    -   Default Value: \#FFFFFF
    -   Location: System Property \[sys\_properties\] table
-   **css.tablet.gradient.start**

    Start color of the gradient for the tablet UI header.

    -   Type: color
    -   Default value: \#666
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **css.tablet.gradient.end**

    End color of the gradient for the tablet UI header.

    -   Type: color
    -   Default value: \#111
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **css.tablet.headerfooter.text.color**

    Color of the text and icons in the tablet UI header and footer.

    -   Type: color
    -   Default value: \#ffffff
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **glide.allow.new.cert\_follow\_on\_task**

    Allow Desired State audit to create a new follow-on task for the same failure at each audit run. Applies only to audits that aren't scripted.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.amb.session.logout.overlay.style**

    Specifies a cascading style sheet \(css\) that defines an overlay. The overlay masks all onscreen data on timeout, and the login screen appears on top of the overlay.

    ![Overlay](../image/screen-w-overlay.png)

    Limited to core ServiceNow AI Platform functions, not applications.

    -   Type: string

        Example: `background-color: #000; opacity: 0.5`

    -   Default value: empty \(no overlay\)
    -   Location: System Property \[sys\_properties\] table
-   **glide.analytics.cache.enabled**

    When true, caching capability is turned on for data visualizations and Platform Analytics dashboards. Caching still needs to be turned on for individual dashboard and data visualizations in UI Builder and the inline dashboard editor, respectively.

    -   Type: true \| false \(Boolean\)
    -   Default value: true
    -   Location: System property \[sys\_properties\] table
-   **glide.analytics.cache.enable\_dashboard\_default**

    When true, caching is enabled by default on dashboards newly created in the inline editor.

    -   Type: true \| false \(Boolean\)
    -   Default: false
    -   Location: System property \[sys\_properties\] table
-   **glide.analytics.cache.expiration.age.in.seconds**

    Value in seconds of the expiration\_time field in analytics cache records. Applies only when glide.analytics.cache.enabled is true.

    -   Type: integer
    -   Default value: 86400 \(24 hours\)
    -   Minimum value: 3600 \(1 hour\)
    -   Location: System property \[sys\_properties\] table
-   **glide.analytics.cache.dashboard\_default\_value**

    Default expiration time in hours for caches on dashboards created in the inline editor.

    -   Type: choice
    -   Choices: 1, 2, 4, 8, 12, 24 \(hours\)
    -   Default value: 24
    -   Location: System property \[sys\_properties\] table
-   **glide.analytics.cache.prefetch.max\_refresh\_counter**

    Number of times a cache entry can be re-fetched after expiring.

    -   Type: integer
    -   Default value: 10
    -   Location: System property \[sys\_properties\] table
-   **glide.analytics.cache.prefetch.min\_age\_in\_seconds**

    Minimum cache entry age that allows cache prefetching, in seconds. Decreasing this value may impact instance performance.

    -   Type: integer \(seconds\)
    -   Default value: 28800 \(8 hours\)
    -   Location: System property \[sys\_properties\] table
-   **glide.angular.legacy**

    When true, enables legacy AngularJS behavior. When false, integrates AngularJS sanitizeUri and $http security patches. If you set this property to false, existing JSONP requests with cross-domain endpoints will fail. You can address this issue in your scripts by doing one of the following:

    1.  Add the domains of any newly failing requests to the **angular.jsonp.inclusion\_list.urls** system property.
    2.  Opt out of this behavior by changing **angular.jsonp.inclusion\_list.enabled** to false.
    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.apps.hub.current**

    URL of the team development parent instance.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.attachments.allow\_html\_in\_ics**

    It governs the handling of .ics files with embedded HTML content. When set to **true**, the system permits the attachment of .ics files containing HTML content. This enhancement provides greater flexibility in managing calendar event attachments, ensuring that files with HTML content can be included when necessary, while maintaining MIME type integrity.

    -   Type: text/html
    -   Default value: null
    -   Location: System Properties \[sys\_properties\] table
-   **glide.attachment.extensions**

    Comma-separated list of file extensions that can be attached. No value means that there are no restrictions.

    -   Type: string
    -   Default value: none
    -   Location: **System Properties** &gt; **Security**
-   **glide.attachment.role**

    Comma-separated list of roles that can create attachments.

    -   Type: string
    -   Default value: public
    -   Location: **System Properties** &gt; **Security**
-   **glide.authenticate.multisso.login\_locate.user\_field**

    Identifies a common login identifier.

    -   Type: string
    -   Default value: user\_name
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.authenticate.sso.saml2.require\_signed\_authnrequest**

    Enables the Identity Provider Single sign-on service to receive a signed AuthnRequest.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.banner.image.url**

    URL used when clicking the banner image.

    -   Type: string
    -   Default value: home.do
    -   Location: System Property \[sys\_properties\] table
-   **glide.banner.image.url\_target**

    Target frame used when clicking the banner image. Use `gsft_main` for the main frame, `_top` to replace the current browser window,`_blank` for a new window or tab.

    -   Type: string
    -   Default value: gsft\_main
    -   Location: System Property \[sys\_properties\] table
-   **glide.basicauth.update\_last\_login\_time**

    Controls whether the Last login and Last login time fields in a user record \[sys\_user\] are updated when an integration user sends a web request to an instance using basic authentication. If true, the Last login and Last login time fields in the user's record are updated with web requests. To turn off this functionality, set this property and the **glide.oauth.update\_last\_login\_time** system property to false.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.bsm.color.affect\_neighbors**

    Color of an affected neighbor node. When a node has a service issue, all nodes that depend on that node are considered affected nodes. In the map, the affected nodes are parents or grandparents of the node with the service issue.

    -   Type: color
    -   Default value: Beige
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.map.style.font\_family**

    Font family name used in the map text. If you designate a font that is not on the user system, the browser substitutes another font and the text may not render as you expect.

    -   Type: font name
    -   Default value: Arial
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.map.style.font\_size**

    Font size of the text that appears with a CI node. The default size is magnified for nodes with more connections and reduced for downstream nodes.

    -   Type: integer
    -   Default value: 14
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.map.style.selection\_background\_color**

    Background color of a selected CI node. This color is also used with a node's Highlight Hierarchy option.

    -   Type: color
    -   Default value: RoyalBlue
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.map.style.selection\_text\_color**

    Color of the text that appears under a selected CI node.

    -   Type: color
    -   Default value: White
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.map.style.text\_color**

    Color of the text that appears under an unselected CI node.

    -   Type: color
    -   Default value: Black
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.max\_levels**

    Maximum level depth from the root CI that can be initially displayed in business service maps. Level depth is the graph distance between the root CI and a node. This value must be an integer.

    -   Type: integer \(1-10\)
    -   Default value: 5
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.new\_node\_color**

    Color for nodes that became viewable from the last expand operation.

    -   Type: color
    -   Default value: PaleGreen
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.max\_nodes**

    Maximum number of downstream nodes to retrieve from the database for a CI. If more nodes exist in the database, they are not displayed in the map.

    -   Type: integer
    -   Default value: 1000
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.refresh\_interval**

    Seconds between each automatic reloading of troubles and tasks.

    -   Type: integer
    -   Default value: 30
    -   Range of possible values: 1 to 3600
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.task\_threshold**

    Change the CI glyph color from orange to red when the number of tasks reaches this threshold.

    -   Type: integer
    -   Default value: 3
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.bsm.too\_many\_children**

    Maximum number of child nodes to display. Nodes are collapsed for the map to meet this limit.

    -   Type: integer, valid values 1 or greater
    -   Default value: 10
    -   Location: **BSM Map** &gt; **Map Properties**
-   **glide.businessrule.async\_condition\_check**

    Specifies whether the instance checks the condition statement of async business rules \(the **When** field is set to async\) prior to running the business rule. If **true**, the instance evaluates the async business rule conditions a second time before running the rule. If **false** or missing, the instance does not evaluate the conditions a second time.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.businessrule.callstack**

    Specifies whether business rule executions are logged in the daily log when they start and finish \(**true**\) or are not logged \(**false**\). Logging is useful for troubleshooting a problem where you must know which business rules are running and in which order.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.cache.size.service\_cache**
    -   Type: integer
    -   Default value: 20
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.canvas.grid.widget\_render\_concurrent\_max**

    Defines the maximum number of widgets that can render simultaneously on a dashboard. With smaller values, individual widgets load more quickly. With larger values, fewer Ajax requests to the server are needed. Set the value of this property to half of the number of widgets that are visible when your most-used dashboard loads. For example, if six widgets are visible on the dashboard set the value to 3.

    **Note:** This system property applies to responsive dashboards only.

    Two is the minimum value, and 1 is interpreted as 2. For values of zero or lower, all widgets load simultaneously.

    -   Type: integer
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.cmdb.query.batch\_time\_limit\_in\_sec**

    Time limit \(in seconds\) for running one batch to get one batch of query results \(100 results\).

    -   Type: integer
    -   Default value: 300
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**
-   **glide.cmdb.query.max\_results\_limit**

    Limits the number of results for a scheduled query and in the results section in the Query Builder when you click **Load All Results**.

    -   Type: integer
    -   Default value: 10,000
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**
-   **glide.cmdb.query.non\_cmdb.black\_listed\_tables**

    Exclusion list of non-CMDB tables that appear in the CMDB Query Builder when creating a CMDB query.

    -   Type: string
    -   Default value: empty
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**
-   **glide.cmdb.query.query\_time\_limit\_in\_sec**

    Time limit \(in seconds\) for running an entire query to get all results.

    -   Type: integer
    -   Default value: 1,800
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Query Builder Properties**
-   **glide.cmdb.statemgmt.max\_bulk\_count**

    Maximum number of CIs that CI Lifecycle Management can process in a bulk update operation.

    -   Type: integer
    -   Default value: 1000
    -   Location: System Property \[sys\_properties\] table
-   **glide.cmdb.statemgmt.max\_lease\_expired\_days**

    Maximum number of days that lease expiration can be set with for CI Actions.

    -   Type: integer
    -   Default value: 15
    -   Location: System Property \[sys\_properties\] table
-   **glide.cms.dashboards.sharing\_with\_secure\_search**

    When enabled, the list of users, user groups, and roles that are visible in the sharing panel is restricted. The restriction is based on the configuration of the sys\_user, sys\_user\_group, and sys\_user\_role ACLs. For more information, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

    There is a performance penalty associated with enabling this property. Performance degradation may be based on the number and complexity of business rules and ACLs on your instance.

    -   Type: true \| false
    -   Default value: false
    -   Location: **System Properties** &gt; **Dashboard Properties**
-   **glide.cms.share\_dashboards.role**

    When this property is empty, all users can share their own dashboards.

    **Note:** This property does not apply to users with the admin and dashboard\_admin roles. Users with these roles can always share any dashboard.

    -   Type: string
    -   Default value: empty
    -   Location: **System Properties** &gt; **Dashboard Properties**
-   **glide.chart.decimal.precision**

    Controls the rounding precision of non-currency numeric values displayed on reports. A **Decimal Precision** value specified in a report's style options overrides this property. Currency values always have a precision of 2.

    -   Type: integer
    -   Default value: 2
    -   Maximum value: 4
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.chat.invite\_fields**

    \(Chat plugin\) Comma-separated list of fields \(glide\_list or references to sys\_user or sys\_group\) used to generate the invitations when creating a chat room from a task. Users can select a check box for each of the specified fields to invite to the chat room users that are referenced by the fields.

    -   Type: string
    -   Default value: none
    -   Location: **Social IT** &gt; **Chat Administration** &gt; **Properties**
-   **glide.chat\_room.create\_roles**

    \(Chat plugin\) Comma-separated list of roles that are allowed to create chat rooms.

    -   Type: string
    -   Default value: none
    -   Location: **Social IT** &gt; **Chat Administration** &gt; **Properties**
-   **glide.chat.show\_emoticons**

    \(Chat plugin\) Enables \(**true**\) or disables \(**false**\) rendering text emoticons as images.

    -   Type: true \| false
    -   Default value: true
    -   Location: **Social IT** &gt; **Chat Administration** &gt; **Properties**
-   **glide.class.downgrade.enabled**

    Flag for allowing class downgrade during identification and reconciliation.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Properties \[sys\_properties\] table
-   **glide.class.switch.enabled**

    Flag for allowing class switching during identification and reconciliation.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Properties \[sys\_properties\] table
-   **glide.class.upgrade.enabled**

    Flag for allowing class update during identification and reconciliation.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Properties \[sys\_properties\] table
-   **glide.cmdb.health.metricProcessor.maxRunningTime**

    Max time in minutes for which individual metric processor runs in each scheduled cycle.

    -   Type: integer
    -   Default value: 120
    -   Location: Navigate to **All** &gt; **Configuration** &gt; **Health Preference**, and then click **System Properties** in the right hand-side navigator.
-   **glide.cmdb.health.src.cmdb\_health\_audit\_only**

    When set to **true**, disables health results from sources other than CMDB Health audit \(such as cloud discovery\). Only results generated by CMDB Health audit appear in the CMDB dashboard.

    For example, by default, if a CI is determined to be stale by Discovery, then that CI appears as stale in the CMDB dashboard even though CMDB Health audit did not determine that CI to be stale. To disable these stale CI health results, set the property to **true**.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.cmdb.health.staleness\_exclude\_dependent\_cis**

    Exclude dependent CIs for the staleness CMDB Health metric.

    When enabled, dependent CIs are not checked for staleness, regardless of any staleness or inclusion rules that are defined for the respective CI types.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.cmdb.logger.source.identification\_engine**

    Enable and configure what type of details the system logs when using IRE outside the scope of identification simulation. For example, when using an API, ECC queue or scheduled jobs.

    -   Type: string
    -   Default value: info, warn, error, debug, or debugVerbose
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    **Note:** Depending on the setting, the system can generate large amounts of data that might affect overall system performance. Set the value with caution, limiting the level of details and use time to the minimum necessary for testing or debugging.

-   **glide.cmdb.logger.use\_syslog.CMDBHealth**

    A comma-separated list that controls the level of logging of CMDB Health jobs. Logging creates entries in the system logs to capture messages generated by the health auditing process each time they run. This logging helps debugging if there is a failure.

    -   Type: string
    -   Default value: error
    -   Location: System Property \[sys\_properties\] table
-   **glide.cmdb\_model.display\_name.shorten**

    If **true**, generates shorter display names for product models if the name of the product model contains the manufacturer name.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.cookies.http\_only**

    Enables \(**true**\) or disables \(**false**\) the generation of HTTP-only cookies. Set this property to **false** to use Approval with E-Signature.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.cost\_mgmt.calc\_actual\_cost**

    \(Cost Management plugin\) When an expense line is created for any task with a **Type** of **Planned task**, sums all task expense lines and adds the total to the **Work cost** field on the task record.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.cost\_mgmt.debug**

    \(Cost Management plugin\) Enables debugging of cost management processing. All logging events are recorded in the Financial Management Log \[fm\_log\] table.

    **Note:** This feature can generate a large number of log records. Enable the feature only during initial testing or when troubleshooting.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.cost\_mgmt.process\_task\_cis**

    \(Cost Management plugin\) Creates expense lines affected configuration items when creating a task expense line.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.cost\_mgmt.service\_allocation.method**

    \(Cost Management plugin\) Defines whether business service to cost center allocation costs should be calculated based on total units or allocated units.

    For example, if the service supports 100 units but only has 50 units allocated, and cost center ABC is allocated 25 units. Using the **All units** method results in an allocation cost of 25/100, or 25% of the total cost of the service. In this case, we track unallocated costs separately. Using **Allocation units** method results in an allocation cost of 25/50, or 50% of the total cost of the service. In this case, all costs are allocated \(recovered\).

    -   Type: choice list
    -   Default value: all\_units
    -   Location: System Property \[sys\_properties\] table
-   **glide.csv.export.line\_break**

    Enables the user to control how exported CSV data appears in Notepad. Valid values are LF for a line feed between records and CRLF for a carriage return followed by a line feed.

    -   Type: string
    -   Default value: LF
    -   Location: System Property \[sys\_properties\] table
-   **glide.csv.use\_row\_currency**

    If false, exports currency and price field values in the user's currency. If true, exports currency and price field values in the currency of the row.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.custom.ip.authenticate.allow**

    Comma-separated list or dash-separated range of IP addresses that are allowed access to view the stats.do, threads.do, and replication.do pages.

    -   Type: string
    -   Default value: none
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    -   Instance Security Hardening Settings: [Restrict performance monitoring access](https://www.servicenow.com/docs/access?context=sc-performance-monitoring-acl&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   **glide.db.aggregates.trend.use\_iso\_week**

    If set to true, reports weekly trend by data according to ISO weeks. If false, data trended per week reports according to the first day of the week set by glide.ui.date\_format.first\_day\_of\_week.

    -   Type: true \| false
    -   Default value: none
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.db.audit.ignore.delete**

    Specifies the tables where the sys\_audit\_delete file is not updated when records are deleted.

    -   Type: string — comma-separated list of tables
    -   Location: System Property \[sys\_properties\] table
-   **glide.db.forced.chunk.threshold**

    Sets the threshold above which to forces chunk record deletions and updates. Chunking helps to prevent non-primary key deletions on huge tables from causing replication problems. Use this property to set a force chunk threshold when using the [GlideRecord – DeleteMultiple](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=yokohama&pubname=yokohama-api-reference&section=r_ScopedGlideRecordDeleteMultiple&ft:locale=en-US) and [GlideRecord – UpdateMultiple](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=yokohama&pubname=yokohama-api-reference&section=r_ScopedGlideRecordUpdateMultiple&ft:locale=en-US) methods.

    -   Type: integer
    -   Default value: 100000000 \(100 million\)
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.db.clone.allow\_clone\_target**

    Enables \(**true**\) or disables \(**false**\) use of a non-production instance as the target for a system clone.

    -   Type: true \| false
    -   Default value: **false** for production instances, **true** for non-production instances
    -   Location: System Property \[sys\_properties\] table
-   **glide.db.impex.XMLLoader.max.file.size.mb**

    Controls the maximum file size allowed when importing an XML file, in megabytes. Attempting to import an XML file larger than this limit results in an error.

    **Warning:** Use caution when modifying this property. Uploading a large XML file may impact performance and can cause an instance outage.

    -   Type: integer
    -   Default value: 100
    -   Location: **System Properties** &gt; **Import Export**
-   **glide.db.large.threshold**

    Sets the number of rows above which a table is considered large and uses a different method of querying for results. When this property is absent, the instance uses the default query method.

    -   Type: integer
    -   Default value: none
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.db.loguser**

    Display \(**true**\) or suppress display \(**false**\) of database errors \(such as `Unique Key violation detected by database (Duplicate entry 'ABC' for key 'name') to user.)` to logged-in user.

    -   Type: true \| false
    -   Default value: none
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.db.max.aggregate.size**

    Sets the maximum number of groups that a grouped report or list renders. Larger values may affect system performance.

    -   Type: integer
    -   Default value: 100
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.db.max\_view\_records**

    Sets the maximum number of records returned when running a GlideRecord query in a script. Do not use values larger than the default because they may cause queries to consume excessive memory on the application server and can, in extreme cases, cause a system outage. This property does not control the maximum number of records that appear in a list, report, or exported file.

    -   Type: integer
    -   Default value: 10000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.db.table.update\_inactive\_choices\_enabled**

    Specifies whether choice table selections marked as inactive \(`sys_choice inactive attribute = true`\) should be loaded into client databases when applications are installed \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.debug.log\_point**

    Specifies whether the log points feature should be enabled or not.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.debugger.log.ui**

    Specifies whether logs should be displayed under forms and lists and in the Session Log tab, or only in the Session Log tab.

    -   Type: choice list
    -   Default value: Page
    -   Location: System Property \[sys\_properties\] table
-   **glide.discovery.application\_mapping**

    Enables or disables the Application Dependency Mapping \(ADM\) feature.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.discovery.log\_debug\_info**

    An optional property to populate debug information in Discovery log. If this property is set to **true**, the Discovery sensor extracts the debug information from ECC input message and writes this information to the Discovery log table, so that it is visible when inspecting discovery status.

    -   Type: true \| false
    -   Default: false
-   **glide.discovery.log\_message\_chars**

    When a log message is longer than this value, ServiceNow creates a preview of the message with an ellipsis at the end of the message to indicate that there is content that is not shown. The preview size prevents any one list row from taking up the entire screen.

    -   Type: integer
    -   Default value: 200 \(characters\)
    -   Location: **Discovery Definition** &gt; **Properties**
-   **glide.discovery.multi\_page\_serial\_mode**

    This property controls the processing of multi-page pattern input records. **false** sets the pages to process in parallel and **true** sets the pages to process serially.

    -   Type: true \| false
    -   Default value: false
-   **glide.discovery.sam\_batch\_update\_size**

    Enables batching the updates to table cmdb\_sam\_sw\_install when only the field last\_scanned in the table has changed. This optimizes the overall discovery execution as it reduces the multiple single update queries on the database. The default value is 100 which means 100 records at a time in the table are batched and updated. By setting this property to 1, this switches to sequential updates.

    -   Type: integer
    -   Default value: 100
-   **glide.discovery.use\_cmdb\_identifiers**

    Controls whether Discovery uses the CMDB Identification and Reconciliation Framework \(introduced with the Geneva release\) or the legacy identifiers from previous releases.

    -   Type: true \| false
    -   Default value: true
    -   Location: **Discovery Definition** &gt; **Properties**
-   **glide.domain.notify\_change**

    Displays a notification message telling the user that the domain picker automatically changed.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.domain.notify\_record\_change**

    Displays a notification message telling the user that the domain picker automatically changed because the record that the user is viewing changed the domain of the user.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.duplicate\_ci\_remediator.dry\_run**

    Determines whether the Duplicate CI Remediator actually remediates CI duplication by updating records in the CMDB, or not.

    -   Type: true \| false
    -   Default value: false
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Duplicate CI Remediator Properties**
-   **glide.duplicate\_ci\_remediator.max.cis**

    Threshold for the number of duplicate CIs, which if exceeded, support for reconciliation in the Duplicate CI Remediator is limited \(1,000 by default\).

    -   Type: integer
    -   Default value: 1000
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Duplicate CI Remediator Properties**
    **Note:** This threshold never exceeds 5,000, even if you set the property to a value greater than 5,000.

-   **glide.duplicate\_ci\_remediator.max.field\_length**

    Attributes in which max\_length exceeds this property value \(4000 by default\) are excluded from the **Select Main CI**, **Merge Attribute Values**, and **Determine Duplicate CI Actions** tabs in the Duplicate CI Remediator wizard.

    -   Type: integer
    -   Default value: 4000
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Duplicate CI Remediator Properties**
    **Note:** This property impacts the performance of de-duplication tasks, therefore be cautious about setting this value.

-   **glide.eccprobe.longrunner.class**

    Identifies the name of a script include that manages long running commands.

    -   Type: string
    -   Default value: LongRunner
    -   Location: System Property \[sys\_properties\] table
-   **glide.eccprobe.longrunner.retry\_minutes**

    Allows bursts of polling errors up to specified minutes in duration.

    -   Type: integer
    -   Default value: 10
    -   Location: System Property \[sys\_properties\] table
-   **glide.eccprobe.longrunner.interval.initial\_seconds**

    Initial polling period for long running commands in seconds.

    -   Type: integer
    -   Default value: 20
    -   Location: System Property \[sys\_properties\] table
-   **glide.eccprobe.longrunner.interval.backoff\_percent**

    Percentage that polling period grows per poll.

    -   Type: integer
    -   Default value: 15
    -   Location: System Property \[sys\_properties\] table
-   **glide.eccprobe.longrunner.interval.max\_seconds**

    Maximum polling period. As the polling period decays, it gets longer until it reaches this maximum.

    -   Type: integer
    -   Default value: 300
    -   Location: System Property \[sys\_properties\] table
-   **glide.eccprobe.longrunner.debug**

    Allows LongRunner logs status on successful polls in addition to the usual messages on unsuccessful ones when set to **true**.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.eccprobe.longrunner.max\_poll\_count**

    Maximum number of polls that is executed per 5- second polling period. This number is generally not relevant, but may be used to contain polling under extreme loading conditions.

    -   Type: integer
    -   Default value: unlimited
    -   Location: System Property \[sys\_properties\] table
-   **glide.ecmdb.all\_relationship\_role**

    An example value is: itil,asset,configuration.

    -   Type: string
    -   Default value: none
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.element.use\_object\_display\_value**

    It ensures that the display value for GlideElementGlideObject fields like glide\_date\_time is calculated correctly.

    -   Type: true\|false
    -   Default value: true
    -   Location: System Properties
-   **glide.element.reference.use\_actual\_display\_value**

    It controls the display value of GlideElementGlideObject fields like glide\_date\_time on Forms and Lists, and you would need to opt-in \(set property value to true\) to see the correct display value in these views.

    -   Type: true\|false
    -   Default value: false
    -   Location: System Properties
-   **__glide.email\_address\_filter.max\_domains__**

    Sets the maximum number of domains that can be associated with a single email address filter.

    -   Type: integer
    -   Default value: 100
-   **__glide.email\_address\_filter.max\_exceptions__**

    Sets the maximum number of exceptions that can be associated with a single email address filter.

    -   Type: integer
    -   Default value: 1000
-   **glide.email.append.timezone**

    Specifies whether to append the time zone to all dates and times in outbound emails \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **Email**
-   **__glide.email\_client.quick\_message.insert__**

    Controls how quick messages are inserted in the email client. If the property is set to **true**, quick message content is inserted at the place of the cursor. If **false**, quick message content replaces existing content in an email draft.

    -   Type: true \| false
    -   Default value: true
-   **glide.email.forward\_subject\_prefix**

    Specifies the comma-separated list of prefixes in the subject line that identify a forwarded email.

    -   Type: string
    -   Default value: fw:,fwd:
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.email.journal.lines**

    Specifies the number of entries from a journal field \(such as Additional comments and Work notes\) included in email notifications. A value of **-1** includes all journal entries.

    -   Type: integer
    -   Default value: 3
    -   Location: **System Properties** &gt; **Email**
-   **glide.email.mail\_to**

    Specifies the email address to send notifications that use the *$\{mailto:\}* variable.

    -   Type: string
    -   Default value: SMTP email address that is active by default
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.email.name\_split**

    Delimiter between the first and last name in an email address to identify users from incoming emails. For example, a delimiter of "." in the email address john.smith@company.com tells the system to look for a user record for John Smith.

    -   Type: string
    -   Default value: period \(.\)
    -   Location: **System Properties** &gt; **Email**
-   **glide.email.notification.save\_when\_no\_recipients**

    Controls whether \(**true**\) or not \(**false**\) a notification-generated sys\_mail record is saved even if there are no recipients. Used in conjunction with other notification recipient logging properties, this property enables troubleshooting problems with notifications.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.email.override.url**

    Sets the URL to use in emailed links in place of the instance URL. The URL should end with nav\_to.do. An example value is: https://servicenow.customerdomain.com/production/nav\_to.do.

    -   Type: string
    -   Default value: Instance URL
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.email.read.active**

    Enables \(**true**\) or disables \(**false**\) the inbound mail server.

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **Email**
-   **glide.email.reply\_subject\_prefix**

    Specifies the comma-separated list of prefixes in the subject line that identify an email reply.

    -   Type: string
    -   Default value: re:aw:,r:
    -   Location: System Property \[sys\_properties\] table
-   **glide.email.smtp.active**

    Specifies whether to enable \(**true**\) or disable \(**false**\) the outgoing mail server.

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **Email**
-   **glide.email.smtp.max\_recipients**

    Specifies the maximum number of recipients the instance can list in the To: line for a single email notification. Notifications that would exceed this limit instead create duplicate email notifications addressed to a subset of the recipient list. Each email notification has the same maximum number of recipients.

    -   Type: integer
    -   Default value: 100
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.email.smtp.max\_send**

    Specifies how many emails to send through each new SMTP connection. The instance establishes a new SMTP connection if there are more emails to send than the specified value.

    -   Type: integer
    -   Default value: 100
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **__glide.email\_system\_address\_filter.max\_address\_filters__**

    Sets the maximum number of email filters that can be associated with a single system address filter.

    -   Type: integer
    -   Default value: 100
-   **glide.email.test.user**

    Specifies the comma-separated list of email addresses to which the instance sends all email messages. Typically used in non-production instances for testing purposes.

    -   Type: string
    -   Default value: none
    -   Location: **System Properties** &gt; **Email**
-   **glide.email.text\_plain.strip\_xhtml**

    Indicates whether both outbound and inbound emails that are shown in comments convert the XML to plain text \(**true**\) or preserve the XML \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.email.watermark.visible**

    Indicates whether the watermark in email notifications is visible \(**true**\) or is wrapped in a hidden div tag \(**false**\).

    **Note:** Email clients that use the plain text version of the email show the watermark.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.email\_client.show\_sms\_option**

    Specifies whether a check box appears in the email client for sending the message to the user's SMS device \(**true**\) or not \(**false**\). If no SMS device exists, the email client sends the message to the primary email device.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.entry.loggedin.page\_ess**

    Specifies the page that an ESS user, who by definition has no roles, is redirected to when the user logs in.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.excel.boolean.display\_value**

    If true, translates columns of type boolean to the user's language when exporting records in Excel format. If false, exports the values in English, regardless of the user language.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.excel.max\_cells**

    Sets the maximum number of cells in an Excel export.

    -   Type: integer
    -   Default value: 500000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.excel.use\_user\_date\_format**

    Specifies whether Excel exports use the date/time format specified in a user's profile \(**true**\) or not \(**false**\). If **false**, exports the instance date/time format defined by the glide.sys.date\_format property.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.export.csv.charset**

    Specifies the character set used to export CSV files. See [Supported Character Encodings](https://docs.oracle.com/javase/8/docs/technotes/guides/intl/encoding.doc.html) for a list of supported character encoding options.

    -   Type: string
    -   Default value: windows-1252
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.export.csv.raw.value**

    When **true**, raw database values are exported instead of the display values when you export to CSV. When **false**, display values are exported.

    -   Type: true \| false
    -   Default value: false
    -   Location: **System Properties** &gt; **Import Export**
-   **glide.export.escape\_formulas**

    When **true**, string values that start with the characters +, -, =, or @ are prepended with a single apostrophe when you export to CSV, XLS, or XLSX files.

    -   Type: true \| false
    -   Default value: **true** for new instances starting with Istanbul
    -   Location: System Property \[sys\_properties\] table for new instances starting with Istanbul. For upgraded instances, [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.export.excel.general\_formatting**

    When **true**, values in cells in exported Excel files have the general format. When **false**, the cells in exported Excel files have the text format.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.export.excel.wrap\_cells**

    When **true**, values in cells in exported Excel files are wrapped automatically. When **false**, the width of exported Excel columns is resized to fit 256 characters and values are not wrapped.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.fdih.retry.max\_count**

    Specifies the maximum number of retry attempts when no value is specified in **Count** for a retry policy.

    -   Type: Integer
    -   Default value: 0
    -   Location: System Property \[sys\_properties\] table
-   **glide.glidesoap.proxy\_host**

    Specifies the proxy server hostname or IP address for SOAP clients.

    -   Type: string
    -   Default value: value of glide.http.proxy\_host
    -   Location: System Property \[sys\_properties\] table
-   **glide.glidesoap.proxy\_port**

    Specifies the port number for the proxy server for SOAP clients.

    -   Type: string
    -   Default value: value of glide.http.proxy\_port
    -   Location: System Property \[sys\_properties\] table
-   **glide.guest.active.session.life\_span**

    Sets the maximum session time for a guest session regardless of user activity, in minutes.

    -   Type: integer
    -   Default value: 0
    -   Location: System Property \[sys\_properties\] table
-   **glide.guest.session\_timeout**

    Sets the inactive session timeout for a guest session, in minutes.

    **Note:** This setting decouples a guest session timeout from the **glide.ui.session\_timeout** property. Any changes to the **glide.ui.session\_timeout** property do not affect a guest session timeout.

    -   Type: integer
    -   Default value: 30
    -   Location: System Property \[sys\_properties\] table
-   **glide.hd.payload\_multi\_page.device\_history.mutex\_expires**

    Total time the thread waits to update the Discovery history before giving up.

    -   Type: integer
    -   Default value: 1 minutes
    -   Location: System Properties
-   **glide.hd.payload\_multi\_page.device\_history.mutex\_spin\_wait**

    The time between when we check if the Discovery history database is free.

    -   Type: integer
    -   Default value: 100 ms
    -   Location: System Properties
-   **glide.hd.payload\_multi\_page.device\_history.mutex\_max\_spins**

    The number of times the Discovery history is checked before giving up.

    -   Type: integer
    -   Default value: 600
    -   Location: System Properties
-   **glide.hd.payload\_multi\_page.discolog.mutex\_expires**

    Total time the thread waits to update the Discovery log before giving up.

    -   Type: integer
    -   Default value: 1 minutes
    -   Location: System Properties
-   **glide.hd.payload\_multi\_page.discolog.mutex\_spin\_wait**

    The time between when we check if the Discovery log database is free.

    -   Type: integer
    -   Default value: 100 ms
    -   Location: System Properties
-   **glide.hd.payload\_multi\_page.discolog.mutex\_max\_spins**

    The number of times the Discovery log is checked before giving up.

    -   Type: integer
    -   Default value: 600
    -   Location: System Properties
-   **glide.help.default.page**

    Sets the overall help URL for the system if you are using context-sensitive help. This URL is used when there is not any context-sensitive help available for the form, list, or record.

    -   Type: string
    -   Default value: http://wiki.servicenow.com/
    -   Location: System Property \[sys\_properties\] table
-   **glide.history.max\_entries**

    Sets the number of characters to display as a preview of journal input fields.

    -   Type: integer
    -   Default value: 250
    -   Location: System Property \[sys\_properties\] table
-   **glide.history\_set.pull\_journal\_entries\_from\_journal\_table**

    Determines whether journal field values in history sets are retrieved from the journal table \(**true**\) or the audit table \(**false**\). If auditing is disabled for a GlideRecord by setting `setWorkflow(false)`, journal entries will be missing from history sets unless set to **true**.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.home.page**

    Specifies which page to load when a user selects a homepage from the banner.

    -   Type: string
    -   Default value: `home_splash.do?sysparm_direct=true`
    -   Location: System Property \[sys\_properties\] table
-   **glide.home.refresh\_disabled**

    Enables \(**true**\) or disables \(**false**\) homepage refresh.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.home.refresh\_intervals**

    Comma-separated list of refresh intervals available on homepages.

    -   Type: string
    -   Default value: 300,900,1800,3600
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    **Important:**

    The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Center dashboards take over homepage functionality.

    Use the [Homepage deprecation help tool](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) to convert the homepages on your instance to responsive dashboards.

    For more information, see:

    -   [Dashboards in the Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).
    -   [Working with responsive dashboards](https://www.servicenow.com/docs/access?context=c_ResponsiveDashboards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).
-   **glide.hosts.allowlist**

    Enables control over what hosts that a Fetch action can access. This affects HTTP APIs, like [RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) and Fetch [Fetch - Scoped, Global](https://www.servicenow.com/docs/access?context=FetchAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). Features of `glide.hosts.allowlist`:

    -   Supports a comma-separated list of URLs or IPs.
    -   Allows "\*" for all.
    -   Allows subdomains via \*.example.com.
    -   Has a global and a per-scope setting \(prefix with the scopename to specify an entry is for a specific scope\).
    -   Default value is an empty string, which is interpreted as no hosts are allowed for Fetch. For existing HTTP APIs, like RestMessageV2, empty is interpreted as all hosts are allowed \(other than those restricted by the existing deny list\).
    -   Type: string
    -   Default value: "" \(empty string\)
    -   Location: System Property \[sys\_properties\] table
-   **glide.html.enable\_media\_sites**

    Enables a URL option for media in the HTML Editor. The media attaches, but doesn't load in the HTML Editor.

    -   Type: string
    -   Default value: youtube.com,player.vimeo.com,vimeo.com
    -   Location: System Property \[sys\_properties\] table
-   **glide.html.escape\_script**

    Enables \(**true**\) or disables \(**false**\) JavaScript tags in HTML fields.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.html.sanitize\_all\_fields**

    Specifies whether all HTML fields are sanitized to remove unwanted code \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
    -   Instance Security Hardening Settings: [HTML sanitizer \(instance security hardening\)](https://www.servicenow.com/docs/access?context=sc-html-sanitizer&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   **glide.http.connection\_timeout**

    Specifies the maximum number of milliseconds an outbound HTTP request \(such as Web Services\) waits to establish a connection.

    -   Type: integer
    -   Default value: 10000 \(10 seconds\)
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.outbound.max\_timeout**

    Specifies the number of seconds that RESTMessageV2 and SOAPMessageV2 APIs wait for a response from a synchronous call. The maximum value is 30 seconds.

    To define a timeout longer than 30 seconds, set the **glide.http.outbound.max\_timeout.enabled** system property to **false** and use the waitForResponse\(\) method to set the timeout. For example, see [Asynchronous SOAPMessageV2 example](https://www.servicenow.com/docs/access?context=r_AsyncronousSOAPMessageV2Example&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). If**glide.http.outbound.max\_timeout.enabled** is set to true and a value is passed in the waitForResponse\(\) method, the system uses the smallest value from either the waitForResponse\(\) method or the **glide.http.outbound.max\_timeout** system property.

    -   Type: integer
    -   Default value: 30
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.http.outbound.max\_timeout.enabled**

    Enables setting a timeout in the **glide.http.outbound.max\_timeout** system property.

    To define a timeout longer than 30 seconds, set the **glide.http.outbound.max\_timeout.enabled** system property to **false** and use the waitForResponse\(\) method to set the timeout. For example, see [Asynchronous SOAPMessageV2 example](https://www.servicenow.com/docs/access?context=r_AsyncronousSOAPMessageV2Example&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). If**glide.http.outbound.max\_timeout.enabled** is set to true and a value is passed in the waitForResponse\(\) method, the system uses the smallest value from either the waitForResponse\(\) method or the **glide.http.outbound.max\_timeout** system property.

    -   Type: boolean
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.http.proxy\_bypass\_list**

    Specifies the semicolon-separated list of addresses that bypass the proxy server. Use an asterisk \(\*\) as a wildcard character to specify all or part of an address.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_host**

    Specifies the proxy server hostname or IP address.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_ntdomain**

    Specifies the domain used to authenticate the proxy server with NTLM authentication.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_nthost**

    Specifies the hostname used to authenticate the proxy server with NTLM authentication.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_ntpassword**

    Specifies the password used to authenticate the proxy server with NTLM authentication.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_ntusername**

    Specifies the user name used to authenticate the proxy server with NTLM authentication.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_port**

    Specifies the port number for the proxy server.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_password**

    Specifies the password used to authenticate the proxy server.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.proxy\_username**

    Specifies the username used to authenticate the proxy server.

    -   Type: string
    -   Default value: none
    -   Location: System Property \[sys\_properties\] table
-   **glide.http.timeout**

    \(Web service Consumer Plugin\) Specifies the maximum number of milliseconds to wait before an outbound transaction times out.

    -   Type: integer
    -   Default value: 175000 \(175 seconds\)
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.i18n.force\_index**

    Enables \(**true**\) or disables \(**false**\) indexing all translated fields, regardless of the value of the table attribute text\_index\_translations.

    -   Type: true \| false
    -   Default value: true
-   **glide.identification\_engine.batch\_update\_last\_discovered**

    Controls batch update of last\_discoveredfield in CIs that are being processed by the identification engine.

    Set to **false** if there are business rules that apply to last\_discovered field, and you want to trigger these rules when calling Identification and Reconciliation API.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.identification\_engine.dependent\_items\_local\_cache\_count**

    For optimization, a custom number of locally cached query result entries of dependent CIs.

    -   Type: integer
    -   Default value: 10000
    -   Location: [Add a system property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    **Note:** If there is a memory issue due to optimization related to using local cache, set the **glide.identification\_engine.related\_items\_local\_cache\_count** and the **glide.identification\_engine.dependent\_items\_local\_cache\_count** properties to 0.

-   **glide.identification\_engine.granular\_insert\_locking**

    Determines whether to use multiple granular insert locks or single global insert lock.

    Set to **false** if there are performance issues associated with the usage of multiple granular insert locks.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.identification\_engine.independent\_items\_local\_cache\_count**

    For optimization, a custom number of locally cached query result entries of independent CIs.

    -   Type: integer
    -   Default value: 100000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    **Note:** Setting the value to 0 avoids using local cache for independent CIs and might affect performance.

-   **glide.identification\_engine.related\_items\_local\_cache\_count**

    For optimization, a custom number of locally cached query result entries of related/lookup items.

    -   Type: integer
    -   Default value: 15000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    **Note:** If there is a memory issue due to optimization related to using local cache, set the **glide.identification\_engine.related\_items\_local\_cache\_count** and the **glide.identification\_engine.dependent\_items\_local\_cache\_count** properties to 0.

-   **glide.identification\_engine.skip\_duplicates**

    Controls how identification processes a small set of duplicate CIs.

    -   When **true**: If the number of duplicate CIs is less than the threshold specified by **glide.identification\_engine.skip\_duplicates.threshold**, then one of the duplicate CIs is picked as a match and gets updated. The rest of the duplicate CIs are tagged as duplicates.
    -   When **false**: Matching a CI fails, and an error is logged.
    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.identification\_engine.skip\_duplicates.threshold**

    Maximum number of CIs that can be in a set of duplicate CIs to allow identification to process the duplicate CIs according to the setting of **glide.identification\_engine.skip\_duplicates**.

    If the number of duplicate CIs exceeds the threshold, then identification processes the duplicate CIs as if **glide.identification\_engine.skip\_duplicates** is set to **false**, regardless of the setting.

    -   Type: integer
    -   Default value: 5
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.identification\_logs.max\_run\_ids**

    Maximum number of log runs that can be displayed when navigating to **Configuration** &gt; **Identification Logs**.

    -   Type: integer
    -   Default value: 1000
    -   Location: **Configuration** &gt; **CMDB Properties** &gt; **Identification/Reconciliation Properties**.
-   **glide.image\_provider.security\_enabled**

    Controls the security settings for images. If **true**, images are visible only to authenticated and authorized users. If **false**, images are visible to anyone with a URL to the attachment.

    -   Type: true \| false
    -   Default value: true
        -   New/zbooted instances: property is present and set to **true**
        -   Upgraded instances: **false** if property is not present, unchanged if property is present
    -   Location: System Property \[sys\_properties\] table
-   **glide.imap.secure**

    Enables \(**true**\) or disables \(**false**\) SSL encryption for connections to the IMAP server.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.imap.secure\_port**

    Specifies the communications port for IMAP secure connections.

    -   Type: string
    -   Default value: 995
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.imap.tls**

    Enables \(**true**\) or disables \(**false**\) starting the IMAP server in Transport Layer Security \(TLS\) mode.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.import.debug**

    Enables \(**true**\) or disables \(**false**\) debug logging for all import processes.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.import.error\_message.generic**

    Enables \(**true**\) or disables display \(**false**\), failed imports to display a generic error instead of a verbose SQL message. This property should be enabled.

    -   Type: true \| false
    -   Default value:
        -   New/zbooted instances: **true** for starting with Istanbul
        -   Upgraded instances: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.import\_excel.use\_only\_user\_session\_date\_format**

    If true, any Date or Date/Time value in an Excel spreadsheet is converted to a user session date format in the staging table upon Excel file import.

    If false, any Date/Time explicit cell type in Excel is imported into a staging table with the user session date format, and any date value that is not explicitly in a Date/Time cell type in Excel is imported into a staging table using the system date format.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table if you want to change the value to false.
-   **glide.import.sftp.debug**

    Enables \(**true**\) or disables \(**false**\) additional debug logging for SFTP imports. Enabling this property causes the instance to log all outgoing and incoming messages during the SSH session.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.import.scp.debug**

    Enables \(**true**\) or disables \(**false**\) additional debug logging for SCP imports. Enabling this property causes the instance to log all outgoing and incoming messages during the SSH session.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.import\_set.preserve.leading.spaces**

    Specifies whether the import process preserves leading spaces in Excel data cells \(**true**\) or not \(**false**\). When **false**, the import process removes leading spaces from Excel data cells.

    **Note:** The import process always removes trailing spaces from Excel data cells.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.import\_set\_row.dynamically\_add\_fields**

    Specifies whether an import set can add new columns to the staging table \(**true**\) or not \(**false**\). Instances that contain large numbers of import sets can sometimes become unresponsive when an import adds a column because the instance must alter every row in the staging table. Sometimes the database alter table action causes an outage. Setting this property to **false** prevents an import set from adding columns to the staging table and produces a log message. As a workaround, administrators can manually add a column to the staging table by creating a new dictionary entry and then reimporting the import set.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ir.query\_method**

    Sets the query method for global text search. Only the **Simple query** method is supported.

    -   Type: choice list
    -   Default value: simple
    -   Location: **System Properties** &gt; **Global Text Search**
-   **glide.active.session.timeout.invalidate.session**

    Specifies whether integration sessions can be invalidated by configuring a maximum active session time.

    -   Type: Boolean true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.integration.session\_timeout**

    Sets the inactive session timeout for integration sessions, in minutes.

    -   Type: integer
    -   Default value: 1
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.integration.update\_last\_login\_time.window.seconds**

    Controls the frequency of updates to integration user records.

    -   Type: integer
    -   Default value: 60
    -   Minimum value: 5
    -   Maximum value: 86400 \(one day in seconds\)
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.integrations.active.session.life\_span**

    Sets the maximum session time for a integration session regardless of activity, in minutes.

    -   Type: integer
    -   Default value: 0
    -   Location: System Property \[sys\_properties\] table
-   **glide.invalid\_query.returns\_no\_rows**

    Controls how invalid GlideRecord queries are handled with respect to invalid or undefined field names. When this property is **true**, invalid queries containing invalid or undefined field names always return no rows. When this property is **false** \(default\), if a query is incorrect, and includes invalid or undefined field names, the invalid part of the query condition is ignored and results are based on the valid part of the query.

    To override this logic at the session level, execute `gs.getSession().setStrictQuery(false)`. To restore strict query, execute `gs.getSession().setStrictQuery(true)`. To use this property, change the line `gr.addQuery('table', arguments.length == 1 ? record.getRecordClassName() : tableName);` in the Workflow script include to `gr.addQuery('table', (tableName) ? tableName : record.getRecordClassName() );`.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.itil.assign.number.on.insert**

    Controls whether \(**true**\) or not \(**false**\) a task number is generated and assigned on load \(**Create New**\) or when the task is submitted. This feature helps prevent unused task numbers.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.jdbcprobeloader.retry**

    Sets the number of times a JDBC probe attempts to connect to a JDBC data source.

    -   Type: integer
    -   Default value: 60
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.jdbcprobeloader.retry\_millis**

    Sets the number of milliseconds a JDBC probe waits between retry attempts to a JDBC data source.

    -   Type: integer
    -   Default value: 5000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.jquery.legacy**

    When true, enables legacy JQuery behavior. When false, integrates the JQuery 1.12.3 and 2.2.3 security patches. If you set this property to false, UI pages with incorrect HTML markup may render incorrectly. You can address this issue in your scripts by closing any html element tags that are self-closing and not in the valid list. For example, change `<div />` to `<div></div>`.

    -   Valid self-closing elements that do not need to be updated include:
        -   `<area />`
        -   `<base />`
        -   `<br />`
        -   `<col />`
        -   `<embed />`
        -   `<hr />`
        -   `<img />`
        -   `<input />`
        -   `<link />`
        -   `<meta />`
        -   `<param />`
        -   `<source />`
        -   `<track />`
        -   `<wbr />`
    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.knowman.search.apply\_role\_based\_security**

    If **true**, honors read access of knowledge bases or articles specified for roles. If **false**, enables specified user criteria to override read access specified for roles.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.knowman.search\_character\_limit**

    Minimum number of characters required for knowledge search. Search terms with fewer than this number of characters return no results.

    -   Type: integer
    -   Default value: 3
    -   Location: System Property \[sys\_properties\] table
-   **glide.knowman.search.default\_language**

    \(Knowledge Management Internationalization Plugin v2\) Default language for knowledge articles. If empty, defaults to the language of the logged-in user.

    -   Type: string
    -   Default value: empty
    -   Location: System Property \[sys\_properties\] table
-   **glide.knowman.serviceportal.seo\_portals**

    Value contains a comma-separated list of service portal record sys\_ids. The SEO indexing of knowledge articles is enabled on the portals mentioned in the list and is blocked by the noindex metatag for other portals. If at least one portal is listed, SEO suggestions display when users author or edit knowledge articles.

    -   Type: string
    -   Default value: empty
    -   Location: System Property \[sys\_properties\] table
    **Note:** If the property value is empty, the indexing is enabled for all portals.

-   **glide.knowman.show\_language\_option**

    \(Knowledge Management Internationalization Plugin v2\) Specifies whether the **Language** box appears \(**true**\) or is hidden \(**false**\) on articles with multiple translations.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.knowman.show\_language\_option.roles**

    \(Knowledge Management Internationalization Plugin v2\) Comma-separated list of roles that can see the Language box on articles with multiple translations.

    -   Type: string
    -   Default value: none
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.knowman.show\_links**

    Specifies whether the **Link** line appears \(**true**\) or is hidden \(**false**\) in a knowledge article.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ldap.allow\_empty\_group**

    Specifies whether all members can be removed from an Active Directory security group \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ldap.binary\_attributes**

    Comma-separated list of LDAP attributes that should be converted from binary format to encoded64 strings. If you set this property, only the values listed are converted. The most common attributes are **objectSID** and **objectGUID**. These converted values are unique and can be used as the coalesce field on the LDAP import mapping. If this property is blank, ServiceNow tries to map these binary attributes without the conversion and they are not guaranteed to be unique since they are not properly converted to string values.

    -   Type: string
    -   Default value: objectsid,objectguid
    -   Location: System Property \[sys\_properties\] table
-   **glide.ldap.paging**

    Enables \(**true**\) or disables \(**false**\) LDAP paging query support. LDAP paging is a more efficient LDAP querying method for environments with more than 1000 users.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.legacy.excel.export**

    Enables \(**true**\) or disables \(**false**\) exporting to XLS format when exporting to an Excel file. By default, only XLSX export is enabled. This property does not affect the Excel web service. When **true**, this property also allows users to select XLS or XLSX as the Easy Import template format.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.list.filter\_max\_length**

    Sets a maximum character limit for the condition builder query.

    -   Type: integer
    -   Default value: 0
    -   Location: System Property \[sys\_properties\] table
-   **glide.lists.live\_list\_enabled**

    Enables a list refresh prompt.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.live\_feed.company\_feed\_exclude\_groups**

    Controls whether messages posted to a public group appear \(**true**\) or are omitted \(**false**\) on the Company Feed.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.live\_services**

    \(Chat plugin\) Enables \(**true**\) or disables \(**false**\) Live Services, such as chat support.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.login.no\_blank\_password**

    Prevents \(**true**\) or allows \(**false**\) logins from users with blank passwords. Often, importing lists of users creates many users with blank passwords. By default, this property is set to **true** on production instances.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.login.home**

    Sets the default homepage that users see after login. If blank, the last page visited is used. The format is *&lt;page&gt;.do*.

    -   Type: string
    -   Default value: home.do
    -   Location: System Property \[sys\_properties\] table
-   **glide.max\_journal\_list\_size**

    Sets the maximum size, in megabytes, of journal input fields.

    -   Type: integer
    -   Default value: 10
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.messaging.reassign.enabled**

    Sets property that automatically reassigns messaging if the current agent is unavailable.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.notification.recipient.include\_logging**

    Master switch to enable/disable logging all reasons a recipient was included. If **false**, no include logging is performed.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.notification.recipient.exclude\_logging**

    Master switch to enable/disable logging all reasons a recipient was excluded. If **false**, no exclude logging is performed.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.notification.recipient.exclude\_logging.device\_inactive**

    Logs recipients who are excluded because their chosen notification device record is marked as inactive.

    -   Type: true \| false
    -   Default value: true
    The glide.notification.recipient.exclude\_logging property in the **System Properties** &gt; **Email** module must be enabled to modify this property.

-   **glide.notification.recipient.exclude\_logging.device\_schedule**

    Logs recipients who are excluded because the chosen notification device record’s schedule field excludes it.

    -   Type: true \| false
    -   Default value: true

        The glide.notification.recipient.exclude\_logging property in the **System Properties** &gt; **Email** module must be enabled to modify this property.

-   **glide.notification.recipient.exclude\_logging.event\_creator**

    Logs recipients who are excluded because they initiated the notification event, such as updating an incident record, and the **Send to Event Creator** check box is cleared on the notification record.

    -   Type: true \| false
    -   Default value: true
    The glide.notification.recipient.exclude\_logging property in the **System Properties** &gt; **Email** module must be enabled to modify this property.

-   **glide.notification.recipient.exclude\_logging.invalid\_email**

    Logs recipients who are excluded because the email address for that user is invalid, for example the @ is missing, or empty.

    To modify this property, you must enable the glide.notification.recipient.exclude\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.exclude\_logging.user\_calendar\_integration\_disabled**

    Logs recipients of calendar invitations who are excluded because the **Calendar Integration** field is set to **None** on the user record.

    -   Type: true \| false
    -   Default value: true
    The glide.notification.recipient.exclude\_logging property in the **System Properties** &gt; **Email** module must be enabled to modify this property.

-   **glide.notification.recipient.exclude\_logging.user\_inactive**

    Logs recipients who are excluded because the **Active** check box is cleared on the user record.

    -   Type: true \| false
    -   Default value: true
    The glide.notification.recipient.exclude\_logging property in the **System Properties** &gt; **Email** module must be enabled to modify this property.

-   **glide.notification.recipient.exclude\_logging.user\_notification\_disabled**

    Logs recipients who are excluded because the **Notification** field is set to **Disabled** on the user record.

    To modify this property, you must enable the glide.notification.recipient.exclude\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.include\_logging**

    Enables or disables logging all reasons that a recipient was included. This property is a main switch. If **true**, the subsequent properties dealing with the inclusion of logging are enabled. If **false**, none of the subsequent properties relating to the inclusion of logging are enabled.

-   **glide.notification.recipient.include\_logging.delegate**

    Logs recipients who are included because they are delegates of another user.

    -   Type: true \| false
    -   Default value: true
    The glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module must be enabled to modify this property.

-   **glide.notification.recipient.include\_logging.event\_parm**

    Logs recipients who are included because they are in the **parm1** or **parm2** fields of the event record.

    To modify this property, you muse enable the glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.include\_logging.recipient\_fields**

    Logs recipients who are included via a notification target record, such as an incident record, specified in the **Users/Groups in Field** field for the notification record. The recipient\_fields are fields in the target record that contain a recipient to add. For example, if the record that triggered the notification is an incident, and the **assigned\_to** field for the incident is listed in recipient\_fields, that user is included as a recipient.

    To modify this property, you must enable the glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.include\_logging.recipient\_groups.group\_email**

    Logs recipients who are included in a group email for any group provided in the notification record’s recipient\_groups or the event **parm1** or **parm2** field.

    To modify this property, you must enable the glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.include\_logging.recipient\_groups.manager**

    Logs recipients who are included because they manage any group provided in the notification record’s recipient\_groups or the event **parm1** or **parm2** field.

    To modify this property, you must enable the glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.include\_logging.recipient\_groups.membership**

    Logs recipients who are included via membership in any group provided in the notification record recipient\_groups or the event **parm1** or **parm2** field.

    To modify this property, you must enable the glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.include\_logging.recipient\_users**

    Logs recipients who are included via notification record’s **Users** field \(recipient\_users\).

    To modify this property, you must enable the glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.notification.recipient.include\_logging.subscription**

    Logs recipients because they are subscribed via User Notification Preferences.

    To modify this property, you must enable the glide.notification.recipient.include\_logging property in the **System Properties** &gt; **Email** module.

    -   Type: true \| false
    -   Default value: true
-   **glide.oauth.update\_last\_login\_time**

    Controls whether the Last login and Last login time fields in a user record \[sys\_user\] are updated when an integration user sends a web request to an instance using OAuth authentication. If true, the Last login and Last login time fields in the user's record are updated with web requests. To turn off this functionality, set this property and the **glide.basicauth.update\_last\_login\_time** system property to false.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.par.export.ppt.max\_visualizations\_allowed**

    For the Now Assist Platform skill "dashboard and visualization export," this property sets the maximum number of visualizations, and thus slides, that you can export from a Platform Analytics dashboard to Microsoft PowerPoint.

    -   Type: integer
    -   Default value: 150
    -   Location: System Property \[sys\_properties\] table
-   **glide.pdf\_export\_from\_form\_list.show\_report\_attrs**

    Enables or disables displaying the PDF page header for all PDFs generated from a list.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.pdf.max\_rows**

    Sets the maximum number of rows in an exported PDF file.

    -   Type: integer
    -   Default value: 1000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.pdf.font.size**

    Sets the font size for exported PDF files.

    -   Type: integer
    -   Default value: 8
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.pdf.url.whitelisting.enabled**

    Enables or disables whether external URLs provided should be rendered in the PDF output generated by the [PDFGenerationAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=PDFGenerationAPIBothAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US). Verifies against the allowed URLs listed in the com.snc.pdf.whitelisted\_urls property.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.pg.any\_rejection\_rejects**

    Controls the default process guide rejection handling. If **true**, the first rejection rejects the entity. If **false**, all users must reject the approval.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.phone\_number\_e164.allow\_national\_entry**

    When **true**, users can enter phone numbers in the local format listed in the territory selector. When **false**, users must enter phone numbers in the international format listed in the territory selector.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.phone\_number\_e164.display\_national**

    When set to **true** or **form**, a Phone Number \(E164\) field displays phone numbers in a local format on forms but as an international format on lists. When set to **all**, a Phone Number \(E164\) field always displays phone numbers in a local format. When set to user, a Phone Number \(E164\) field only displays phone numbers in a local format when the phone number matches the locale setting of the current user.

    -   Type: string
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.phone\_number\_e164.display\_territory\_selector**

    Specifies whether to display \(**true**\) or hide \(**false**\) the territory selector. Hiding the territory selector restricts users to entering only local or national phone numbers.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.phone\_number\_e164.display\_territory\_text**

    When set to all, a Phone Number \(E164\) always displays the territory label. When set to national, a Phone Number \(E164\) displays the territory label only if the phone number is in local format. When set to read-only, a Phone Number \(E164\) displays the territory label in read-only mode regardless of whether the number is in local or global format. When set to read-only-national, a Phone Number \(E164\) displays the territory label in read-only mode only if the number is in local format. When set to list, a Phone Number \(E164\) displays the territory label in a list. When set to list-national, a Phone Number \(E164\) displays territory label in a list if the number is in national format. When set to none, a Phone Number \(E164\) does not display the territory label.

    -   Type: string
    -   Default value: read-only
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.phone\_number\_e164.display\_users\_idd**

    Specifies whether to display the international direct dialing prefix between the territory selector and the input box on forms \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.phone\_number\_e164.strict**

    Specifies whether all phone number fields must match the display format of the field's select territory. When **true**, the phone number input box displays a red line underneath phone numbers that do not match the territory format listed in the territory selector. Users cannot save an invalid phone number. When **false**, the phone number input box displays a green line underneath phone numbers that do not match the territory format listed in the territory selector. Users can save an invalid phone number, and the territory selector offers the option to select an **Other / Unknown** territory format.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.pop3.ignore\_headers**

    Specifies the comma-separated list of email headers that cause the instance to ignore an email message. Use the format name:value to specify email header types and values. You can use a wildcard \(\*\) for the subtype. For example, `Content-Type:multipart/*; report-type=delivery-status;` ignores emails containing a type of multipart and a parameter of **report-type=delivery-status**. For syntax specifications, see [http://www.w3.org/Protocols/rfc1341/4\_Content-Type.html](http://www.w3.org/Protocols/rfc1341/4_Content-Type.html).

    -   Type: string
    -   Default value: Auto-Submitted:auto-replied,X-FC-MachineGenerated:true,Content-Type:multipart/report; report-type=delivery-status;
    -   Location: **System Properties** &gt; **Email**
-   **glide.pop3.ignore\_senders**

    Specifies the comma-separated list of senders that cause the instance to ignore an email message. Enter only the name before the at \(@\) sign.

    -   Type: string
    -   Default value: mailer-daemon, postmaster
    -   Location: **System Properties** &gt; **Email**
-   **glide.pop3.ignore\_subjects**

    Specifies the comma-separated list of strings that cause the instance to ignore an email message if they are present at the start of a subject line. Values are case-insensitive.

    -   glide
    -   Type: string
    -   Default value: out of office autoreply, undeliverable:, delivery failure:,returned mail:,autoreply
    -   Location: **System Properties** &gt; **Email**
-   **glide.pop3.parse\_end**

    \[Legacy\] Text indicating the end of the email body section where the instance should parse name:value pairs to change field values when processing inbound email actions. This property is no longer required to set field values from the email body.

    -   Type: string
    -   Default value: none
    -   Location: **System Properties** &gt; **Email**
-   **glide.pop3.parse\_start**

    \[Legacy\] Text indicating the beginning of the email body section where the instance should parse name:value pairs to change field values when processing inbound email actions. This property is no longer required to set field values from the email body.

    -   Type: string
    -   Default value: none
    -   Location: **System Properties** &gt; **Email**
-   **glide.pop3.process\_locked\_out**

    Enables \(**true**\) or disables \(**false**\) the ability for locked out users to trigger inbound actions.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.pop3.reply\_separators**

    Comma-separated list of separators that cause the instance to disregard everything below the text string in the message body. This list is case-sensitive.

    -   Type: string
    -   Default value: \\n\\n-----Original Message-----,\\n\\n \_\_\_\_\_ \\n\\nFrom:
    -   Location: **System Properties** &gt; **Email**
-   **glide.pop3readerjob.create\_caller**

    Controls the behavior when an instance receives an email from an email address not associated with a user record. If **true**, the instance creates a new user record for the email address and places that new user in the **Caller** field of any created tickets. If **false**, the instance associates the new ticket to the **Guest** user record.

    -   Type: true \| false
    -   Default value: false
    -   Location: **System Properties** &gt; **Email**
-   **glide.processor.json.row\_limit**

    Specifies the maximum number of rows a JSON query returns.

    -   Type: integer
    -   Default value: 250
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.product.description**

    The value of this property is displayed as text in the banner next to the company logo.

    -   Type: string
    -   Default value: Service Management
    -   Location: **System Properties** &gt; **Basic Configuration UI16**
-   **glide.product.help\_url**

    Global setting for the URL that the help icon goes to. Value must be empty for context-sensitive help to work.

-   **glide.product.help\_show**

    Controls whether the help icon, help.gifx, appears in \(**true**\) or is omitted from \(**false**\) the welcome banner.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.product.image.light**

    The Banner image displayed for Core UI Interface.

    -   Type: uploaded image
    -   Default value: none
    -   Location: **System Properties** &gt; **Basic Configuration UI16**
-   **glide.product.icon**

    Stores the favicon image displayed in bookmarks, tabs, and the browser address bar.

    -   Type: image
    -   Default value: favicon.ico?v=4
    -   Location: **System Properties** &gt; **System**
-   **glide.product.name**

    Specifies text to use in place of Service-now.com in the browser top title bar \(and in browser tabs\). This text is duplicated in the banner to the right of the logo unless you add display: none; to the end of the value field within the glide.product.name.style property.

    ![Glide Product Name](../image/GlideProductName1.png)

    -   Type: string
    -   Default value: ServiceNow
    -   Location: System Property \[sys\_properties\] table
-   **glide.product.name.style**

    Specifies the CSS properties used to display the glide.product.name text in the banner to the right of the logo. To not display the text, add `display: none;` to the end of the value field in this property.

    -   Type: string
    -   Default value: padding-bottom: 0px; padding-top: 0px;
    -   Location: System Property \[sys\_properties\] table
-   **glide.quota.manager.debug**

    Controls whether to display \(**true**\) or hide \(**false**\) additional information related to the Quota Manager, such as running transactions, canceled transactions, and which quotas are matched to transactions.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.quota.manager.heartbeat**

    Sets the number of seconds between the start of each Quota Manager heartbeat. This value determines how often the Quota Manager checks for transactions exceeding a quota and how often the Quota Manager writes status in the log file.

    -   Type: integer
    -   Default value: 1
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.quota.manager.minimum\_transaction\_time**

    Sets the minimum number of seconds that a transaction must run before the Quota Manager matches it to a transaction quota. You should set this value to at least 1 second because smaller values decrease performance, and because transactions shorter than 1 second are probably not worth canceling. For optimal performance, set this value to the value of your most restrictive quota. For example, if your most restrictive quota cancels transactions longer than 1 minute, set the minimum transaction time to 60 seconds.

    -   Type: integer
    -   Default value: 1
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.reconciliation.override.null**

    Flag for allowing or disallowing the update of an empty field by a lower priority data source.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Properties \[sys\_properties\] table
-   **glide.remote\_glide\_record.max\_count**

    Control the maximum number of records that the GlideRecord query method returns when using the SOAP web service. The instance primarily uses this property to control the records returned when using a Perl API GlideRecord query.

    **Warning:** If you set this property to a large value, such as 10000, socket timeout errors might occur with MID Servers. Keep the value of this property less than 1000.

    -   Type: integer
    -   Default value: 250
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.report.add\_to\_list\_supported**

    Sets whether to support the add\_to\_list ACL for reporting on specified columns from the Available columns list when creating or sharing a list report.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.report.calendar.max\_more\_events\_per\_day**

    Specifies the maximum number of calendar events that can appear in the **+ &lt;number&gt;** pop-up for:

    -   A calendar day when calendar is in month or year view
    -   The top 'full day' section of a calendar day when a calendar is in day or week view
    When this number is exceeded, a **+ many** link appears, which opens a list of events instead of a pop-up. For more information about the maximum number of events that can be displayed in a calendar day, see system property **glide.report.calendar.max\_events\_displayed\_per\_cell**.

    -   Type: integer
    -   Default value: 30
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.report.calendar.max\_events\_displayed\_per\_cell**

    Defines the maximum number of events that can appear in calendar report for:

    -   A calendar day when calendar is in month or year view
    -   The top 'full day' section of a calendar day when a calendar is in day or week view
    Events that exceed this value are visible via a link in the calendar cell. See **glide.report.calendar.max\_more\_events\_per\_day** for more information.

    -   Type: integer
    -   Default value: 3
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.report.new\_calendar**

    Enables \(**true**\) or disables \(**false**\) new calendar reports. Internet Explorer 7 and 8 do not support new calendars. If you open a calendar report in one of these browsers, the old version of calendar reports is always used.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.report\_home.group\_report.show\_usr\_grp**

    Enables \(**true**\) or disables \(**false**\) the Reporting preferences link in the user profile.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.required.attribute.enabled**

    Flag for enforcing required attributes \(cannot be null\) during identification and reconciliation.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Properties \[sys\_properties\] table.
-   **glide.rest.apis.disabled**

    Controls which REST APIs are available on the instance, along with glide.rest.apis.enabled. The value for this property is a comma-separated list of API names, such as Table API or Aggregate API. If neither this property nor glide.rest.apis.enabled is set, all REST APIs are available. If a particular API is specified in both properties, that API is disabled. If you disable specific APIs without explicitly enabling any APIs, all REST APIs except the disabled APIs are available.

    -   Type: string
    -   Default value: all REST APIs are enabled by default
    -   Location: System Property \[sys\_properties\] table
-   **glide.rest.apis.enabled**

    Controls which REST APIs are available on the instance, along with glide.rest.apis.enabled. The value for this property is a comma-separated list of API names, such as Table API or Aggregate API. If neither this property nor glide.rest.apis.disabled is set, all REST APIs are available. If a particular API is specified in both properties, that API is disabled. If you enable specific APIs, only those APIs are available.

    -   Type: string
    -   Default value: all REST APIs are enabled by default
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.rest.choice.allow\_non\_existing\_value**

    Enables passing non-existing values to a choice field. Does not apply to Change REST API /api/sn\_chg\_rest/change.

    -   Type: true \| false
    -   Default value: false

        If **true**, the choice field is set to a passed value, even if the passed value does not exist in the choice field.

    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.rest.debug**

    Logs all stages of REST processing, including processing times.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.rest.replace\_request\_host\_with\_property**

    Ensures that generated links in an API payload, such as links to more pages and reference fields, are based off of the instance address not the request host address.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.rollback.version**

    Controls whether rollback behavior is used \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.rss.max\_rows**

    Controls the maximum number of records returned by the RSS Feed Generator.

    -   Type: integer
    -   Default value: 1000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.sc.reset\_cascade**

    If **true**, forces variable cascading when navigating between pages in an order guide.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.schedules.repeat\_nth**

    Controls how a schedule entry with **Repeats** set to **Monthly** and **Monthly Type** set to **Day of the Week** is defined. Choices are **Week** or **Day**. The **Week** option is defined as choosing a day of the month in the nth week selects the nth day of the month. The **Day** option is defined as choosing the nth day of the month selects the nth day of the month.

    -   Type: choice list
    -   Default value: day
    -   Location: System Property \[sys\_properties\] table
-   **glide.schedules.fifth**

    Controls how a schedule entry that selects the fifth occurrence of a day in month behaves in a month containing only four occurrences of the day. Choices are **Last**, **Next**, and **Strict**. The **Last** option selects the last \(fourth\) occurrence of the day. The **Next** option selects the first day of the next month. The **Strict** option skips the day completely. This property is valid only when the glide.schedules.repeat\_nth property is set to **Day**.

    -   Type: choice list
    -   Default value: last
    -   Location: System Property \[sys\_properties\] table
-   **glide.script.ccsi.ispublic**

    Provides privacy control over client-callable script includes that are accessed by public pages. If **false**, all client-callable script includes are private.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.script.log\_level**

    Controls the behavior of gs.log. Set this property to **none** to disable Glide script logging, or to **print** to save log data to the file system instead of the database. Use the default value **all** to save all Glide script logs to the database.

    -   Type: string
    -   Default value: all
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.script\_processor.admin**

    Specifies the user role necessary to access the Scripts - Background module. To require administrators to elevate privileges to access the module, set the value to **security\_admin**.

    -   Type: string
    -   Default value: admin
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.script.vtable.log.debug**

    Enables use of debug logs for remote table script definitions. Set this property to **true**. Prolonged use of this property can affect performance, so it is best to set its value to **false** when you finish a debugging session.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.search.suggestions.enabled**

    Set it to **true** \(default\) to enable search suggestions, or set it to **false** to disable search suggestions everywhere. For more information about search suggestions, see [Enable search suggestions](../../search-administration/task/enable-search-suggestions.md).

-   **glide.secondary.query.sysid**

    Controls whether a secondary sort using sys\_id as a sort key is automatically applied when sorting requested database records on a list. This property is useful when sorting records that have multiple records found for a single value of the primary sort key. Use this property to ensure that the **Next / Previous** buttons on forms display the proper record. If **false**, there is no secondary sort, therefore records with the same primary sort value are returned as they are found in the database and may be inconsistent.

    **Note:** Setting this property to **true** may impact the load and sort processes. It is not supported by the Elasticsearch document store plugin.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.security.auto.resubmit.ajax**

    Automatically resubmits timed-out Ajax requests.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.security.checkacl.before.setvalue**

    Controls how the high security setting glide.security.strict.updates processes ACLs. When **true**, the instance checks ACL rules for all columns before applying any updates to a row. When **false**, the instance applies ACL rules as each column is processed in alphabetical order. This behavior may result in one update preventing another update from occurring. For example, suppose that you create a custom ACL rule to prevent updates after a record is closed. If you attempt to close an incident and also add information to a custom resolution code field in the same update, the close action is applied first because it is controlled by the \[incident.state\] column and the custom field by the \[incident.u\_resolution\_code\] column. After the instance applies the close action, the custom ACL rule prevents further write updates to the row.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.security.csrf.handle.ajax.timeout**

    Handles errors for timed out Ajax requests.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.security.csrf.strict.validation.mode**

    Enforces strict validation on CSRF tokens so that users cannot resubmit a request if the CSRF token does not match.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
    -   Instance Security Hardening Settings: [CSRF strict validation \(instance security hardening\)](https://www.servicenow.com/docs/access?context=sc-csrf-strict-validation&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   **glide.security.diag\_txns\_acl**

    Controls who can view the stats.do, threads.do, and replication.do pages. If **true**, only administrators or users from a known IP address are allowed to view the pages. If **false**, all users have access to the pages.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    -   Instance Security Hardening Settings: [Performance monitoring \(ACL\) \(instance security hardening\)](https://www.servicenow.com/docs/access?context=sc-performance-monitoring-acl&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   **glide.security.disable\_ui\_pages\_sysparm\_client\_script**

    The system does not evaluate client scripts that are passed in URL parameters in UI pages. If you use URL parameters to load client scripts, you can add and disable this system property. Use this property only while you change the implementation to no longer depend on clients being passed in by URL parameters. Do not keep the system property disabled.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.security.mime\_type.aliasset**

    Creates customized mime type alias sets. For example, `image/png=image/x-png`.

    -   Type: string
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.security.granular.create**

    Requires users to have write access on all individual fields on a table before they can create a record in that table.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.security.file.mime\_type.validation**

    Enables \(**true**\) or disables \(**false**\) MIME type validation for file attachments.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
    -   Instance Security Hardening Settings: [Restrict uploaded MIME types](https://www.servicenow.com/docs/access?context=sc-upload-mime-type-restriction&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   **glide.security.strict\_elevate\_privilege**

    Forces all elevated roles to be treated equally for users with the administrator role. When enabled, administrators must explicitly, manually elevate themselves to any roles that are marked as elevated.

    When disabled, administrators need only to manually elevate to the security\_admin role. Other roles are automatically granted to administrators.

    -   Type: true \| false
    -   Default value: **true** for new instances, **false** for upgraded instances
    -   Location: For new instances, this property is available on the System Property \[sys\_properties\] table. For upgrades, [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.service\_portal.search\_as\_you\_type\_behavior**

    Select search suggestions \(Suggestions\) or type-ahead functionality \(Typeahead\). For more information about search suggestions, see [Enable search suggestions](../../search-administration/task/enable-search-suggestions.md).

-   **glide.set\_x\_frame\_options**

    Enables \(**true**\) or disables \(**false**\) the X-Frame-Options response header to SAMEORIGIN for all UI pages. The X-Frame-Options HTTP response header can be used to indicate whether a browser should be allowed to render a page in a &lt;frame&gt; or &lt;iframe&gt;. Set this property to **true** to avoid clickjacking attacks, by ensuring that CMS content cannot be embedded into other sites.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
    -   Instance Security Hardening Settings: [Implement the x-frame-options: SAMEORIGIN security header](https://www.servicenow.com/docs/access?context=sc-x-frame-options-sameorigin&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   **glide.short\_poll\_delay**

    \(Chat plugin\) Sets the short polling delay, in milliseconds, for XMPP requests. Polling is the method by which the browser gets information from the server to send instant messages in chat.

    -   Type: integer
    -   Default value: 1000 \(1 second\)
    -   Location: **Social IT** &gt; **Chat Administration** &gt; **Properties**
-   **glide.shortened\_journal\_length**

    Sets the number of characters to display as a preview of journal input fields.

    -   Type: integer
    -   Default value: 512000
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.smtp.dateformat**

    Specifies the date format to use for outgoing email notifications

    -   Type: string
    -   Default value: date format \[sys\_user.date\_format\] listed in the user record of the email sender.
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.smtp.default\_retry**

    Enables \(**true**\) or disables \(**false**\) resending email when an unknown SMTP error code is encountered. The instance recognizes only the SMTP error codes defined in the glide.smtp.defer\_retry\_ids property.

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **Email**
-   **glide.smtp.defer\_retry\_ids**

    Specifies the comma-separated list of SMTP error codes that force the instance to resend email.

    -   Type: string
    -   Default value: 421,450,451,452
    -   Location: **System Properties** &gt; **Email**
-   **glide.smtp.fail\_message\_ids**

    Specifies the comma-separated list of SMTP error codes that prevent the instance from resending email.

    -   Type: string
    -   Default value: 500,501,502,503,504,550,551,552,553,554
    -   Location: **System Properties** &gt; **Email**
-   **glide.smtp.timeformat**

    Specifies the time format to use for outgoing email notifications.

    -   Type: string
    -   Default value: time format listed in email sender's user record \[sys\_user.time\_format\].
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.soap.allow\_null\_numeric\_output**

    When **true**, SOAP XML responses return an empty element for numeric fields with no value. When **false**, numeric fields with no value return a value of `0` in the SOAP response.

    **Note:** The property **glide.wsdl.show\_nillable** must be **true** to allow null values in SOAP responses.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.soap.default\_security\_policy**

    Specifies the name of SOAP security policy the instance uses when enforcing Web Services Security \(WSS\) for inbound requests.

    -   Type: string
    -   Default value: default security policy
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.soap.import\_set\_insert\_serialized**

    Controls the processing of web service inserts. If **true**, the instance processes multiple simultaneous inserts one at a time \(serially across nodes\) to ensure an accurate transform. Serialized processing slows the speed at which the instance processes inserts. If **false**, multiple simultaneous inserts into an import set table result in simultaneous transforms that may produce duplicate target records due to the coalesce value being created at the same time.

    **Note:** Set this value to **false** only to optimize performance when the related transform map does not have a coalesce value that may be present simultaneously.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.soap.request\_processing\_timeout**

    Sets the maximum number of seconds that a SOAP request has to finish processing before the connection times out. This property computes a default value from the value of the property glide.http.timeout divided by 1000. There might be network infrastructure \(such as proxy servers\) in place that implements a shorter timeout. In this case, a socket timeout may occur unless this property is set to a shorter value. In general, you should set this property to a value several seconds less than the shortest socket inactivity timeout in effect anywhere in the network path between the client application and the ServiceNow instance.

    -   Type: integer
    -   Default value: 175 \(value of glide.http.timeout divided by 1000\)
    -   Location: System Property \[sys\_properties\] table
-   **glide.source\_control.checksum\_required**

    This property allows you to enable optional checksum validations and sanitizations. When set to **true**, continues to throw an error if the checksum validation of application files fails. This action prevents application developers on your instance from importing application files from source control that have been modified outside of an instance.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.source\_control.checksum\_quick\_install**

    When set to **true**, bypasses the sanitization step\(s\) if the checksum matches. This action prevents an application developer from waiting for validation/sanitization steps to be processed if application files linked to a source control repository outside of your instance weren't modified.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.source\_control.default\_branch\_name**

    Sets the default GIT repository branch to work in for application files linked to source control.

    -   Type: string
    -   Default value: sn\_instances/&lt;instance\_name&gt;
    -   Location: System Property \[sys\_properties\] table
-   **glide.spell.dictionary.en**

    Sets the spell checker dictionary used in the system for English users. Dictionaries are available for Brazilian Portuguese \(pb.dic\), Czech \(cs.dic\), Dutch \(nl.dic\), English US \(en.dic\), English UK \(en\_uk.dic\), Estonian \(et.dic\), Finnish \(fi.dic\), French \(fr.dic\), German \(de.dic\), Hebrew \(he.dic\), Hungarian \(hu.dic\), Italian \(it.dic\), Polish \(pl.dic\), Portuguese \(pt.dic\), Russian \(ru.dic\), Spanish \(es.dic\), and Thai \(th.dic\).

    -   Type: choice list
    -   Default value: en.dic \(English US\)
    -   Location: System Property \[sys\_properties\] table
-   **glide.spell.dictionary.max\_matches**

    Specifies the maximum number of spelling errors that the spell-check should detect. By default, spell-check finds only 10 spelling errors. The instance ignores any additional errors after reaching the maximum value.

    -   Type: integer
    -   Default value: 10
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.split\_journal\_audit\_records**

    When set to **true**, ensures one-to-one mapping between \[sys\_journal\_field\] table and \[sys\_audit\] table records for consistent synchronization. If **glide.history\_set.pull\_journal\_entries\_from\_journal\_table** is set to **true** and there are missing or duplicate comments in the activity stream, setting **glide.split\_journal\_audit\_records** to **true** might resolve the issue. For more details, see [Duplicate/Missing Comments in Activity Stream \(UI 16\) \[KB2122007\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2122007).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add a system property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.sys.activity\_using\_audit\_direct**

    \[Not Supported\] Controls whether the record's history is generated using the Audit table \(**true**\) or not \(**false**\).

    \[Required\] Set the value to **false** to generate history with History Sets.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.sys.audit\_inserts**

    Specifies whether the Audit table audits inserts \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.sys.date\_format**

    System date format for all users unless overridden in the user record.

    -   Type: date format
    -   Default value: yyyy-MM-dd
    -   Location: **System Properties** &gt; **Basic Configuration U116**
-   **glide.sys.default.tz**

    System timezone for all users unless overridden in the user's record.

    -   Type: timezone
    -   Default Value: none
    -   Location: **System Properties** &gt; **Basic Configuration UI16**
-   **glide.sys.domain.domain\_change\_notify**

    Domain legacy

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.sys.domain.no\_change\_roles**

    Domain legacy

    -   Type: string
    -   Default value: This field should be left empty.
    -   Location: System Property \[sys\_properties\] table
-   **glide.sys.domain.use\_record\_domain**

    Domain legacy

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.sys.domain.use\_record\_domain\_for\_client\_scripts**

    Domain legacy

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.sys.time\_format**

    System time format for all users unless overridden in the user's record.

    -   Type: time format
    -   Default Value: HH:mm:ss
    -   Location: **System Properties** &gt; **Basic Configuration UI16**
-   **glide.sys\_reference\_row\_check**

    Specifies whether the script conditions of Access Control Rules apply to a table's reference fields \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
    **Note:** If the **glide.sys\_reference\_row\_check** system property is not present, or has been set to false, script conditions for Access Control Rules are not applied. This means an ACL containing scripted conditions will pass it's check as long as the other ACL criteria are met \(such as role requirements\).

-   **glide.template.max\_context**

    Specifies the maximum number of templates displayed in a form's context menu. If more than this number are available, users can click **Apply Template** on the context menu to open the reference list of templates.

    -   Type: integer
    -   Default value: 15
    -   Location: System Property \[sys\_properties\] table
-   **glide.transform.reuse\_coalesce\_field\_value**

    If **true**, avoid re-evaluation of coalesce scripts to get the values.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ts.index.attachment.debug**

    If **true**, enables log messages for exceptions that occur when indexing attachments. You can leave this property enabled during normal operations to capture stack trace information about any exceptions.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ts.index.attachment.list\_terms.debug**

    If **true**, the system logs all indexed terms when an attachment is indexed.

    For optimal performance, set this property to **false** during normal operations. Only enable this property when you are actively debugging an issue.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ts.reindex.sys\_metadata.after.upgrade**

    If **true**, the system automatically reindexes the sys\_metadata table after an upgrade, without noticeable performance impact. To disable automatic reindexing, set the value to **false**.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.activity.displayname**

    Specifies whether the activity formatter shows **name** values \(true\) or **user\_name** values \(false\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.activity.email\_roles**

    Specifies the list of roles \(comma-separated\) that can view email in the Activity Formatter.

    -   Type: string
    -   Default value: itil
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.activity.email.use\_display**

    Specifies whether to display the email address or the user IDs \(display value of the User table\) in email headers \(**true**\) or not \(**false**\). If **true**, the instance searches for a user record with a matching email address. If the instance cannot find a matching user record, it displays the email address.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.activity\_stream.form\_button**

    Removes the activity stream button from forms.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.activity\_stream.list\_button**

    Removes the activity stream button from lists.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.activity\_stream.page\_size**

    Size of pages for Core UI form activity stream. A value of `0` means no paging.

    -   Type: integer
    -   Default value: 0
    -   Location: Still appears in the System Properties \[sys\_properties\] table, but is no longer available.
-   **glide.ui.activity\_stream.scale\_animated\_gifs**

    Creates a thumbnail of animated `.gif` files. The maximum dimensions are 525 px width and 350 px height. The animation is not preserved in the thumbnail, but previewing the image displays the animation at its original size.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.activity\_stream.scale\_images**

    Creates a thumbnail of large images to display in the activity stream. The maximum dimensions are 525 pixels wide and 350 pixels high. If the user clicks the image or attachment, the preview is at full size.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.activity\_stream.style.comments**

    Changes the color of the left bar in activity stream comments in Core UI.

    -   Type: color entry, either a name, such as **blue** or a code, such as **\#0000FF**.
    -   Default value: transparent
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.activity\_stream.style.work\_notes**

    Changes the color of the left bar in activity stream work notes in Core UI.

    -   Type: color entry, either a name, such as **blue** or a code, such as **\#0000FF**.
    -   Default value: gold
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.activity.style.comments**

    Changes the background color of the activity stream comments in UI15.

    -   Type: string
    -   Default value: background-color: background-color: WhiteSmoke
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.activity.style.work\_notes**

    Changes the background color of the activity stream work notes in UI15.

    -   Type: string
    -   Default value: background-color: LightGoldenRodYellow
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.allow.field.dependency.for.templates**

    Checks dependency for choice fields at the time of applying template, preventing invalid values to be set to the dependent field. For example, a subcategory field which depends on category field.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.allow\_deep\_html\_validation**

    Allows administrators to prevent users from saving invalid HTML in a journal field.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.attachment.force\_download\_all\_mime\_types**

    Forces download of all MIME attachment files.

    -   Type: true \| false
    -   Default value: true for new instances, false for upgraded instances
    -   Location: System Property \[sys\_properties\] table
    -   Instance Security Hardening Settings: [Restrict Downloadable MIME types](https://www.servicenow.com/docs/access?context=sc-downloadable-mime-type-denylist&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)
-   **glide.ui.audit\_deleted\_tables**

    Comma-separated list of system tables for which the audit history tracks deletions.

    -   Type: string
    -   Default value: sys\_user, sys\_user\_group, sys\_user\_role, sys\_user\_has\_role, sys\_user\_grmember, sys\_group\_has\_role, sys\_security\_acl\_role
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.auto.recovery**

    Allows users to recover unsaved changes while working in the Studio.

    -   Type: true \| false
    -   Default value: true
    -   Location: **Auto Recovery** &gt; **Properties**
-   **glide.ui.auto.recovery.exclude.field.types**

    Comma-separated list of field types to exclude from automatic recovery.

    -   Type: string
    -   Default value: none
    -   Location: **Auto Recovery** &gt; **Properties**
-   **glide.ui.auto.recovery.unsupported.field.types**

    Comma-separated list of field types no supported for automatic recovery.

    -   Type: string
    -   Default value: password,password2,glide\_encrypted,video,user\_image,image
-   **glide.ui.auto.recovery.unsupported.tables**

    Comma-separated list of tables to exclude from automatic recovery.

    -   Type: string
    -   Default value: v\_ws\_editor
    -   Location: **Auto Recovery** &gt; **Properties**
-   **glide.ui.auto\_req.extend.session**

    If **true**, enables the user to extend their user session by selecting a homepage refresh time. If **false**, it enforces session timeout. The session timeout value is ignored when the user specifies an automatic refresh value.

    For example, if the user selects **5 minutes** for automatic homepage refresh, the session is renewed every five minutes. By adding this property and setting the value to **false**, administrators can force the user session to time out even if the user page refreshes every **x** number of minutes. The user session times out after the value specified in the session timeout, plus the selected refresh value. This property takes effect when the **Remember me** check box is not selected for the user. Tablet and mobile devices do not support this feature.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.breadcrumb\_max\_entries**

    Specifies how many choices will be shown in the condition builder breadcrumb.

    -   Type: integer
    -   Default value: 10
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.buttons\_bottom**

    Controls whether UI actions appear at both the bottom and top of the form \(**true**\) or only at the top \(**false**\). This property only works in a deprecated version of the UI.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.cert\_task\_activity.fields**

    Defines which journal field is the task activity field.

    -   Type: string
    -   Default value: work\_notes
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.chart.bar.horiz.max\_col\_slant\_labels**

    Sets the maximum number of columns in a horizontal bar chart before slanting \(angling\) the labels.

    -   Type: integer
    -   Default value: 5
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.chart.height**

    Specifies the height of a chart in pixels.

    -   Type: integer
    -   Default value: 300
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.chart.pie.labels**

    Enables \(**true**\) or disables \(**false**\) labels on pie chart slices.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.chart.pie.labels.max\_items**

    Sets the maximum number of pie chart slice values that can be returned to display their labels.

    -   Type: integer
    -   Default value: 8
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.clickthrough.popup**

    -   For reference fields, enables \(**true**\) or disables \(**false**\) display of the pop-up diamond icon for reference fields, and opening a new window when clicking the icon.
    -   For document ID fields, enables \(**true**\) or disables \(**false**\) displaying the information icon and opening a pop-up window with the document's form. To learn more [Document ID field](../../field-administration/task/t_CreatingADocumentIDField.md).
    **Note:** Related lists do not appear on forms opened in the pop-up window.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.clickthrough.replace**

    Enables \(**true**\) or disables \(**false**\) both the pop-up and click-through icons for reference fields.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.date\_format.first\_day\_of\_week**

    Specifies which day of the week that weeks start on for calendar reports \(1=Sunday, 2=Monday...\).

    -   Type: integer
    -   Default value: 1
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.date\_picker.first\_day\_of\_week**

    Specifies the first \(leftmost\) day of the week for the date and date/time picker \(1=Sunday, 2=Monday...\).

    -   Type: integer
    -   Default value: 1
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.default.applications**

    Comma-separated list of application names that open by default in the navigation pane when nothing is opened via user preferences. If the property is specified and is blank, no applications are opened in the navigation pane when no applications are opened via user preferences. If the property is not specified, the first application that is authorized for the user opens if no applications are opened via user preferences.

    -   Type: string
    -   Default value: first authorized application for the user
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.dirty\_form\_support**

    Enables \(**true**\) or disables \(**false**\) display of a confirmation message when a form has unsaved changes and the user leaves the form through any means except a submit \(such as using the green back arrow, any form button, or other\). This property is not supported in Safari.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.email.composer.enabled\_plugins**

    These plugin options are for Seismic Email Client. Removing plugins could cause undesirable side effects.

    -   Type: string
    -   Default values: link lists advlist table powerpaste searchreplace preview fullscreen placeholder readonlynoborder code image align\_listitems emoticons anchor charmap media
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.email.composer.toolbar**

    These toolbar options are for Seismic Email Client.

    -   Type: string
    -   Default values: newdocument bold italic underline \| strikethrough alignleft aligncenter alignright alignjustify \| blocks fontfamily fontsize table cut copy paste \| pastetext searchreplace bullist numlist outdent indent blockquote \| undo redo link unlink code forecolor backcolor removeformat \| hr visualblocks preview subscript superscript charmap image media fullscreen
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.encode\_module\_uri**

    Enables \(**true**, the default\) or disables \(**false**\) encoding of module URIs in the navigation pane. For information about how ServiceNow encodes module URIs, see [Encoding module URIs](https://www.servicenow.com/docs/access?context=test-steps-app-navigator-category&version=yokohama&pubname=yokohama-application-development&section=encoding-module-uris&ft:locale=en-US).

-   **glide.ui.escape\_form\_message**

    Specifies whether strings in GlideForm functions are sanitized to remove unwanted code \(true\) or not \(false\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.escape\_gwindow\_message**

    Specifies whether strings in GlideWindow functions are sanitized to remove unwanted code \(true\) or not \(false\).

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.export.choice\_list\_max\_characters**

    Sets the maximum number of characters that will be included from a condition field type in an export to Microsoft Excel, as well as the maximum number of characters displayed in the list view condition builder in Core UI. \(Note: This property has no effect on the length of condition field values in tables.\)

    -   Type: integer
    -   Default value: 80
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.filter.first\_day\_of\_week**

    Identifies the first day of the calendar week for the company. By default, the start of the week is Monday, meaning that the calendar week begins with Monday and ends with Sunday. To change this behavior, add the property **glide.ui.filter.first\_day\_of\_week** to the instance as an integer property. Set the value to the integer corresponding with the day of the week that the calendar begins on, where 1 is Sunday, 2 is Monday, and so on. The function impacts all charts and calculations where the day of the week is used as a parameter.

    -   Type: integer
    -   Default value: 2
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.first.field.reference**

    Enables \(**true**\) or disables \(**false**\) having the first column in a list always link to the underlying record, even if it is a reference field. For example, if the first column on an Incident list is **Assigned to**, that value links to the Incident if this property is set to **true**.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.form\_annotations**

    Enables \(**true**\) or disables \(**false**\) form annotations, which allow you to add Custom, Section Separator, and Line Separator to a form.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.form\_multiple\_splits**

    Enables \(**true**\) or disables \(**false**\) multiple splits and end splits in the form layout configuration slushbucket.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.gauge.view**

    Defines which view you want to be the default for homepage gauges.

    -   Type: string
    -   Default value: portal
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.glide\_list.start.locked**

    Controls whether a glide\_list \(like the watch list\) starts out locked \(**true**\) or unlocked \(**false**\) on a form.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.goto\_use\_contains**

    Controls whether the **Go to** navigation performs a "contains" query \(**true**\) or a "greater than" query \(**false**\) by default.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.homepage.parallel**

    Enables \(**true**\) or disables \(**false**\) use of parallel rendering.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.homepage.parallelism**

    Sets the maximum number of threads that should cooperate on rendering any given homepage.

    -   Type: integer
    -   Default value: 2
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.homepage.preview**

    Enables \(**true**\) or disables \(**false**\) displaying the preview icon for lists on the homepage.

    ![Preview icon](../image/HomepagePreviewIcon.png)

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.html.editor**

    Specifies which HTML field editor to use, TinyMCE or htmlArea \(legacy\).

    -   Type: string
    -   Default value: tinymce
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.html.editor.default\_target\_link**

    Enables you to set a default target value for links in the TinyMCE.

    -   Type: string
    -   Default value: ''
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.html.editor.extended\_valid\_elements**

    Defines which elements remain in the TinyMCE text when the editor saves. This functionality can be useful to add or override specific elements that should be kept.

    -   Type: string
    -   Default value: blank
    -   Location: System property \[sys\_properties\] table
-   **glide.ui.html.editor.toolbar.line1**

    Configures the editing toolbar \(first line\) for HTML fields when TinyMCE is enabled. The **spellchecker** tool is not supported in Core UI or UI15.

    -   Type: string
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.html.editor.toolbar.line2**

    Configures the editing toolbar \(second line\) for HTML fields when TinyMCE is enabled. The **spellchecker** tool is not supported in Core UI or UI15.

    -   Type: string
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.html.editor.v4.paste.html\_import**

    Controls how content being pasted from sources other than Microsoft Word is filtered. This includes content copied from TinyMCE itself.

    -   Type: choice list
    -   Default value: clean
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.html.image.allow\_url**

    Enables \(**true**\) or disables \(**false**\) uploading an image via URL from HTML Fields.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.html.editor.remove\_trailing\_brs**

    Specifies whether an empty line containing a `<br>` tag is converted to a `<div>&nbsp;</div>` tag for TinyMCE HTML fields. If **true**, the tag is converted. If **false**, the tag is left as `<br>`.

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.html.toolbar**

    Configures the editing toolbar for HTML fields.

    -   Type: string
    -   Default value: list of buttons
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.incident\_activity.fields**

    Defines what fields are visible in the activity formatter. If the activities are customized, the system updates this property automatically.

    -   Type: string
    -   Default value: list of fields
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.incident\_activity.max\_addresses**

    Specifies the maximum number of addresses to list in an email audit record. If the number of addresses exceeds this limit, the instance truncates the list after the maximum value and displays an ellipsis character \(...\).

    -   Type: string
    -   Default value: 5
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.incident\_alert\_activity.fields**

    Incident communication plan activity formatter fields — the list of fields tracked from the Incident Communication Plan form in the activity formatter.

    -   Type: string
    -   Default value: opened\_by, work\_notes, comments, severity, estd\_distruption\_time, actual\_disruption\_time
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.journal.use\_html**

    Specifies whether TinyMCE is available for journal fields \(**true**\) or not \(**false**\).

    -   Type: true \| false
    -   Default value: false
-   **glide.ui.js\_error\_notify**

    Displays client script errors to users with the **client\_script\_admin** role. Also displays a generic error message to other users who encounter a client script error.

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **All Properties**
-   **glide.ui.label.enable**

    Enables \(**true**\) or disables \(**false**\) using labels, such as Most Active, Most Recent, or user-created.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.m.clear\_pasteboard\_when\_backgrounded**

    Clears the copy/paste clipboard when the application enters the background.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table. In Categories, add the mobile\_post\_auth category.
-   **glide.ui.max\_calendar\_duration**

    Maximum number of days that a single calendar report entry can display.

    -   Type: integer
    -   Default value: 90
    -   Range of possible values: 90 to 400
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.max\_calendar\_records**

    Maximum number of records saved in a calendar report.

    -   Type: integer
    -   Default value if the property is not configured: 10,000
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.m\_agents**

    Comma-separated list of browser agents considered as mobile browsers for the Smartphone Interface. These browsers are directed to the mobile pages instead of the full browser pages.

    -   Type: string
    -   Default value: iphone,android\_phone,IEMobile,Windows Phone,iPod,Windows CE,BlackBerry,BB10
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.max\_ref\_dropdown**

    Maximum number of records for a reference field that is displayed as a choice list. If the number of available records is greater than this value, the field appears as a reference field, not as a choice list.

    -   Type: integer
    -   Default value: 25
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.mentions.default\_limit**

    Number of users with same name displayed in Activity Stream Compose editor. When set to true, the default limit takes in a number which determines how many users with the same name are displayed.

    -   Type: string
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.mobile\_agents**

    Comma-separated list of browser agents considered as mobile browsers for the Legacy Smartphone Interface. These browsers are directed to the mobile pages instead of the full browser pages.

    -   Type: string
    -   Default value: iPod,Windows CE,BlackBerry,Android,Opera Mini,IEMobile,Windows Phone,iphone
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.nav.stripe.select.maxchars**

    Numerical character limit for list menu choices within the nav stripe. The nav stripe appears at the top of the page when using UI11.

    -   Type: integer
    -   Default value: none
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.polaris.experience**

    Enables the Next Experience user interface, landing page, and Unified Navigation. For more information, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    This property does not affect anything in workspaces, such as Platform Analytics Components. Workspaces, UI Builder, and related features are always enabled.

    -   Type: true \| false
    -   Default value: true on new instances, false on upgrades from Tokyo or earlier.
    -   Location: The System Property \[sys\_properties\] table
-   **glide.ui.polaris.global\_search**

    Toggles the Next Experience search function.

    -   Type: true \| false
    -   Default value: true when **glide.ui.polaris.experience** is true.
    -   Location: The System Property \[sys\_properties\] table
-   **glide.ui.polaris.history.url.param\_blocklist**

    URL parameters that are excluded when the system identifies and clears duplicate URLs from the history. This property applies only to the Next Experience Unified Navigation, which is enabled when **glide.ui.polaris.experience** is true.

    -   Type: string
    -   Default value: \["tinyId"\]
    -   Location: The System Property \[sys\_properties\] table
-   **glide.ui.polaris.list\_style.enable\_highlighted\_value\_style**

    Enables highlighted value style on list cells. This property applies only when **glide.ui.polaris.experience** is true.

    -   Type: true \| false
    -   Default value: true when **glide.ui.polaris.experience** is true.
    -   Location: The System Property \[sys\_properties\] table
-   **glide.ui.polaris.login.show\_illustrations**

    Enables display of illustrative graphics on the stylized login page. This property applies only when **glide.ui.polaris.experience** is true.

    -   Type: string
    -   Default value: true when **glide.ui.polaris.experience** is true.
    -   Location: The System Property \[sys\_properties\] table
-   **glide.ui.polaris.menus**

    Toggles the Unified Navigation menus in the header. This property applies only when **glide.ui.polaris.experience** is true, meaning that Next Experience Unified Navigation is enabled.

    -   Type: true \| false
    -   Default value: true when **glide.ui.polaris.experience** is true.
    -   Location: The System Property \[sys\_properties\] table
-   **glide.ui.reference.readonly.clickthrough**

    Enables \(**true**\) or disables \(**false**\) reference pop-ups on read-only reference fields. Reference pop-ups and click-throughs are hidden by default if a client script, UI policy, or ACL makes the field read-only. Being able to see or click through to the target record is unrelated to the reference field being writable.

    If **false**, the administrator can override the system setting for a specific field by adding the **readonly\_clickthrough=true** attribute to the dictionary entry.

    -   Type: true \| false
    -   Default value: false
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.remember\_view**

    Enables \(**true**\) or disables \(**false**\) use of user preferences for the last view.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.remember.me.default**

    Controls whether the **Remember me** check box is selected \(**true**\) or cleared \(**false**\) by default.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.report.extend\_calendar\_choices**

    Controls which field styles are applied during calendar highlighting. If **false**, field styles in only the Task table are used. If **true**, the calendar first uses field styles from the table that the report is based on. If no applicable styles exist in that table, the calendar uses field styles from the Task table.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.report.old\_report\_builder**

    Enables \(**true**\) or disables \(**false**\) use of the old report builder UI.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.section508**

    Enables \(**true**\) or disables \(**false**\) rendering of alternate text in place of images.

    -   Type: true \| false
    -   Default value: false
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.show\_live\_feed\_activity**

    Enables \(**true**\) or disables \(**false**\) live feed for a record in the activity formatter.

    -   Type: true \| false
    -   Default value: false
    -   Location: **System Properties** &gt; **UI Properties**
-   **glide.ui.show\_template\_bar**

    Controls whether the template bar can be displayed on the specified table. For example: `glide.ui.show_template_bar.incident = false`.

    -   Type: true \| false
    -   Default value: true
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.session\_timeleft**

    Sets how much time, in minutes, users have to extend a session before it times out due to inactivity.

    -   Type: integer
    -   Default value: 2
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.active.session.life\_span**

    Sets the maximum session time for sessions regardless of activity, in minutes.

    -   Type: integer
    -   Default value: 0
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.session\_timeout**

    Sets the inactive session timeout, in minutes.

    -   Type: integer
    -   Default value: 30
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.stream\_icon**

    Toggles the displaying of the activity stream button on the specified table. For example: `glide.ui.stream_icon.hr_case = true`.

    -   Type: true \| false
    -   Default value: false
-   **glide.ui.syntax\_editor.context\_menu**

    Enables disables the context menu in script editor.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.syntax\_editor.linter.eslint\_config**

    Defines linting configurations using the ESLint utility.

    -   Type: string
    -   Default value: All recommended ESLint rules are enabled, except no-undef, no-unused-vars, no-empty, and semi.
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.table.labels**

    Controls whether the system uses verbose labels for table names \(**true**\) or literal table names \(**false**\).

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.tablet\_enabled**

    Enables \(**true**\) or disables \(**false**\) the tablet UI.

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **glide.ui.tablet\_agents**

    Uses the tablet UI if one of the specified strings \(comma-separated\) appears in the browser user\_agent header.

    -   Type: string
    -   Default value: ipad,android\_tablet
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **glide.ui.tablet.title**

    Displays the specified text as a brief page title for tablet UI.

    -   Type: string
    -   Default value: ServiceNow
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **glide.ui.tablet.title.ios\_webapp**

    Displays the specified text as the default home screen icon label used in iOS version 6 and later.

    -   Type: string
    -   Default value: ServiceNow
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **glide.ui.task.insert**

    Enables \(**true**\) or disables \(**false**\) the use of **Insert** and **Insert and Stay** options on tables derived from Task \(such as Incident, Change, and Problem\).

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.textarea.character\_counter**

    When **true**, displays a count of available characters for journal and multi-line text fields.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.textarea\_initial\_rows**

    Sets the number of rows initially displayed for multiline form elements. When the element is selected for editing, it is expanded. Set this value to `0` or blank to ignore this property. This functionality is used to conserve space on a form when multiline elements take up too much space.

    -   Type: integer
    -   Default value: 0
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.update\_on\_iterate**

    Controls whether updates are saved \(**true**\) or discarded \(**false**\) when a user clicks the blue arrows on a form.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.ui\_policy\_debug**

    Enables \(**true**\) or disables \(**false**\) logging of UI policy processing in the JavaScript debug window

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ui.user\_cookie.life\_span\_in\_days**

    Sets the expiration time period for the 'remember me' cookie.

    **Note:** When a user accesses an instance with 'remember me' enabled, the access resets the cookie expiration period until the maximum \(glide.ui.user\_cookie.max\_life\_span\_in\_days\) life span limit is reached.

    -   Type: integer
    -   Default value: 15 \(days\)

        **Note:** Maximum value 30.

    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.user\_cookie.max\_life\_span\_in\_days**

    Sets a maximum cap for the **glide.ui.user\_cookie.life\_span\_in\_days** cookie to expire before forcing a user to re-authenticate into the instance.

    -   Type: integer
    -   Default value: 30 \(days\)

        **Note:** Maximum value 365 days.

    -   Location: System Property \[sys\_properties\] table
-   **glide.ui.welcome.profile\_link**

    Enables \(**true**\) or disables \(**false**\) allowing users to click their name in the welcome message and see their user profile.

    -   Type: true \| false
    -   Default value: In new instances **true**. In existing instances **false**.
    -   Location: System Property \[sys\_properties\] table
-   **glide.ui11.show\_switch\_link**

    This property only affects a deprecated version of the UI. It is no longer supported. Displays \(**true**\) or hides \(**false**\) a banner link for switching between the UI11 and legacy interfaces.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **glide.update.suppress\_update\_version**

    Comma-separated list of tables for which updates are not tracked in the Versions \[sys\_update\_version\] table. You cannot compare and revert versions for tables in this list.

    -   Type: string
    -   Default value: sys\_user,sys\_import\_set\_row
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.user.default\_password**

    Default password for new users created from incoming email. Users must reset the password at first login.

    -   Type: string
    -   Default value: password
    -   Location: **System Properties** &gt; **Email**
-   **glide.userauthgate.extauth.check**

    Enables \(**true**\) or disables \(**false**\) the **UserAuthenticationGate** checks for both external and internal authentication mechanisms.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **glide.user.trusted\_domain**

    Comma-separated list of trusted domains for which the instance automatically creates a guest user based on incoming emails. Use an asterisk \(\*\) to trust all domains. If an email is not from a trusted domain, the instance processes the inbound email as a "guest user" but does not create a guest user in the instance.

    -   Type: string
    -   Default value: \*
    -   Location: **System Properties** &gt; **Email**
-   **glide.workflow.model.cache.max**

    Maximum number of models held in the workflow cache. You must restart the instance after changing this property to apply the change.

    -   Type: integer
    -   Default value: 300
    -   Location: **Workflow** &gt; **Properties**
-   **glide.wsdl.definition.use\_unique\_namespace**

    Enables \(**true**\) or disables \(**false**\) use of a unique WSDL namespace value when publishing a ServiceNow table through web services. If **true**, the WSDL target namespace is www.service-now.com/&lt;table name&gt;.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.wsdl.maximum\_hierarchy**

    Maximum number of hierarchical levels returned in a WSDL when hierarchical SOAP web service is enabled. This property has a maximum value of 3.

    -   Type: integer
    -   Default value: 3
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.wsdl.show\_nillable**

    Enables \(**true**\) or disables \(**false**\) allowing a WSDL element to be valid if it has no element content despite a \{content type\} which would otherwise require content.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.ws.use\_row\_lock**

    If **true**, avoid using the current web service lock that applies before running the transform. Use the row lock that applies after the OnStart method.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.xmlhttp.excessive**

    Sets the number of items visible in the Available half of a many-to-many or one-to-many collection box.

    -   Type: integer
    -   Default value: 100
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **glide.xmlprocessor.use\_unload\_format**

    Enables \(true\) or disables \(false\) unloading the XML using the display\_value format. To unload using this format, add the parameter **useUnloadFormat=true** to the request URL.

    -   Type: true \| false
    -   Default value: false
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **google.maps.auto\_close**

    If **true**, automatically closes the current info window before opening a new one. Clear the check box to enable multiple pop-up windows to remain open at once.

    -   Type: true \| false
    -   Default value: true
    -   Location: **System Properties** &gt; **Google Maps**
-   **google.maps.client**

    Client ID for Google Maps API for Business. This client ID authorizes production use of Google Maps API for Business. By default, this ID is provided by ServiceNow. ServiceNow may require you to purchase a separate Client ID based on your usage.

    -   Type: string
    -   Default value: gme-servicenow
    -   Location: **System Properties** &gt; **Google Maps**
-   **google.maps.key**

    Map key from Google, tied to the URL of the server. This key is the private key authorizing development use of Google Maps.

    -   Type: string
    -   Default value: empty
    -   Location: **System Properties** &gt; **Google Maps**
-   **google.maps.latitude**

    Starting latitude of the map. This value determines the starting latitude displayed in Google Maps.

    -   Type: string
    -   Default value: 36.008522
    -   Location: **System Properties** &gt; **Google Maps**
-   **google.maps.longitude**

    Starting longitude of the map. This value determines the starting longitude displayed in Google Maps.

    -   Type: string
    -   Default value: -95.221764
    -   Location: **System Properties** &gt; **Google Maps**
-   **google.maps.max\_items**

    Maximum number of items to display on the map. This setting determines how many icons can be displayed on a map.

    -   Type: integer
    -   Default value: 500
    -   Location: **System Properties** &gt; **Google Maps**
-   **google.maps.table**

    Table used by the map. This setting names the table containing the name, longitude, and latitude fields.

    -   Type: string
    -   Default value: cmn\_location
    -   Location: **System Properties** &gt; **Google Maps**
-   **google.maps.zoom**

    Starting zoom level of the map \(1 is the lowest\).

    -   Type: integer
    -   Default value: 4
    -   Location: **System Properties** &gt; **Google Maps**
-   **help.base.default**

    \(Context-Sensitive Help plugin\) Sets the base URL for help contexts in which ServiceNow wiki is **false** and an absolute URL is not specified.

    -   Type: string
    -   Default value: http://servicenow.com/docs/?context=
    -   Location: System Property \[sys\_properties\] table
-   **help.base.servicenow**

    \(Context-Sensitive Help plugin\) Sets the base URL for help contexts in which ServiceNow wiki is **true**

    -   Type: string
    -   Default value: http://servicenow.com/docs/?context=
    -   Location: System Property \[sys\_properties\] table
-   **mid.server.rba\_debug\_powershell**

    Enables probe-level debugging for PowerShell probes. With this property enabled, PowerShell probes write detailed activity information to the MID Server log.

    -   Type: true \| false
    -   Default value: false
    -   Location: **Orchestration** &gt; **MID Server Properties**
-   **mid.version.override**

    Sets an override condition for the current version for all MID Servers in your environment. For more information on version control, see [MID Server version control properties](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    -   Type: string
    -   Default value: none \(If this property is left empty, the MID Servers get their version information from the mid.buildstamp property.\)
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **par\_vis\_config.data\_source.can\_select\_indicator**

    Specifies roles \(comma-separated\) which can select indicators as data sources from the Data Visualization configuration panel. If empty, all users can select the indicator sources that they have access to.

    -   Type: string
    -   Default value: empty
    -   Location: System Property \[sys\_properties\] table
-   **par\_vis\_config.live\_refresh\_rate\_min\_value**

    Specifies the minimum interval in seconds for the **Live refresh rate** setting in the Data Visualization configuration. If set, a user can still set an empty or 0 value.

    -   Type: integer
    -   Default value: 30 \(seconds\)
    -   Location: System Property \[sys\_properties\] table
-   **par\_viz.table\_data.max\_data\_points**

    Maximum number of data points for data visualization charts based on table sources.

    -   Type: integer
    -   Default value: 10000
    -   Location: System Property \[sys\_properties\] table
-   **par\_viz.table\_data.max\_groups**

    Maximum number of groups to be displayed for data visualization charts based on table sources.

    -   Type: integer
    -   Default value: 50
    -   Location: System Property \[sys\_properties\] table
-   **password\_reset.activity\_monitor.incident\_threshold**

    Specifies the maximum number of lockouts before an alert is issued.

    -   Type: integer
    -   Default value: 10 \(lockouts\)
    -   Location: System Property \[sys\_properties\] table
-   **password\_reset.activity\_monitor.incident\_window**

    Specifies the amount of time that is used for recording and counting the number of user lockouts.

    -   Type: integer
    -   Default value: 60 \(minutes\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.captcha.ignore**

    Enables and disables CAPTCHA functionality.

    The password reset application uses Google re-CAPTCHA as the default CAPTCHA service. To use the base system CAPTCHA, change the **password\_reset.captcha.google.enabled** system property to **false**.

    -   Type: true \| false
    -   Default value: false
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.qa.num\_enroll**

    Specifies the number of questions a user must select and answer to be enrolled in the password reset program.

    **Note:** This security question property can be overridden by adding a value for the **num\_enroll** parameter in a security question verification.

    -   Type: integer
    -   Default value: 5 \(questions\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.qa.num\_reset**

    Specifies the number of questions a user must answer to verify their identity during the password reset process.

    **Note:** This security question property can be overridden by adding a value for the **num\_reset** parameter in a security question verification.

    -   Type: integer
    -   Default value: 3 \(questions\)
    -   Possible values: integers that are less than the number specified for the **num\_enroll** property.
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.request.max\_attempt**

    Specifies the number of password reset attempts a user has before they are locked out for a period determined by the value in **max\_attempt\_window**.

    -   Type: integer
    -   Default value: 3 \(attempts\)
    -   Location: **Password Reset** &gt; ****Properties
-   **password\_reset.request.max\_attempt\_window**

    Specifies how long a user is locked out or prevented from changing their password after trying the maximum number of times.

    -   Type: integer
    -   Default value: 1440 \(minutes\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.request.retry\_window**

    Specifies the length of time before the count for password reset attempts refreshes.

    -   Type: integer
    -   Default value: 1440 \(minutes\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.request.success\_window**

    Specifies how long a user is locked out after they have successfully reset their password.

    -   Type: integer
    -   Default value: 10 \(minutes\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.sms.default\_complexity**

    Specifies the number of characters in the SMS code that are required for a user to reset their password.

    **Note:** This SMS code property can be overridden by adding a value for the complexity parameter in an SMS code verification.

    -   Type: integer
    -   Default value: 4 \(digits\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.sms.expiry**

    Specifies the amount of time, in minutes, until the SMS code sent to the user expires.

    **Note:** This SMS code property can be overridden by adding a value for the expiry parameter in an SMS code verification.

    -   Type: integer
    -   Default value: 5 \(minutes\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.sms.max\_per\_day**

    Specifies the maximum number of SMS codes that are sent to a user within one 24-hour period. When a user clicks the **Send Verification Code** button, the 24-hour period begins.

    **Note:** This SMS code property can be overridden by adding a value for the **max\_per\_day** parameter in an SMS code verification.

    -   Type: integer
    -   Default value: 10 \(per day\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.sms.pause\_window**

    Specifies the amount of time to pass before another SMS code can be sent to a user.

    **Note:** This SMS code property can be overridden by adding a value for the **pause\_window** parameter in an SMS code verification.

    -   Type: integer
    -   Default value: 2 \(minutes\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.wf.refresh\_rate**

    Specifies how often to check the status of the workflow. Represented in the password reset process progress bar.

    -   Type: integer
    -   Default value: 90000 \(milliseconds\)
    -   Location: **Password Reset** &gt; **Properties**
-   **password\_reset.wf.timeout**

    Specifies the maximum wait time, in milliseconds, for the workflow to execute. The workflow is triggered during the password reset request when the user clicks **Submit**.

    -   Type: integer
    -   Default value: 500 \(milliseconds\)
    -   Location: **Password Reset** &gt; **Properties**
-   **promin.show\_records.limit**

    Specifies the maximum number of records that can be returned for an arc or node for the **Show Records** link to display. If more records are returned than the set limit, the link does not display.

    -   Type: integer
    -   Default value: 100,000 \(records\)
    -   Location: [Add the property](r_AvailableSystemProperties.md#) to the System Property \[sys\_properties\] table.
-   **remember\_me.max\_duration\_in\_days**

    Sets a maximum cap for the **remember\_me\_cookie.duration\_in\_days** cookie to expire before forcing a user to reauthenticate into the instance.

    -   Type: integer
    -   Default value: 30 \(days\)

        **Note:** Maximum value 365 days.

    -   Location: System Property \[sys\_properties\] table
-   **remember\_me\_cookie.duration\_in\_days**

    Sets the default expiration for the "remember me" cookie. When a user logs in with "remember me" enabled, each login within the expiration limit resets the expiration period.

    -   Type: integer
    -   Default value: 15 \(days\)

        **Note:** Maximum value 30 days.

    -   Location: System Property \[sys\_properties\] table
-   **sa\_analytics.aggregation.include\_service**

    Includes all CIs for alert aggregation. If **false**, includes only CIs not related to a business service.

    -   Type: true \| false
    -   Default value: true
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sa\_analytics.aggregation\_enabled**

    Enables alert aggregation. Enables aggregation of correlated alerts for services and alert groups.

    -   Type: true \| false
    -   Default value: true
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sa\_analytics.alert.severity\_threshold**

    Alert severity threshold, above which alerts are included in analysis. Only alerts with severity that is above the threshold are included in alert aggregations and root cause CI analysis.

    -   Type: choice list
    -   Default value: Info
    -   Other possible values:
        -   Warning
        -   Minor
        -   Major
        -   Critical
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sa\_analytics.rca\_enabled**

    Enables \(**true**\) or disables \(**false**\) root cause analysis for business services. Enables RCA for alerts associated with business services, to identify root-cause CIs.

    -   Type: true \| false
    -   Default value: false
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sa\_analytics.rca.input\_purge\_days**

    Purge staging tables \(in days\). Number of days that RCA input is kept before it is purged.

    -   Type: integer
    -   Default value: 90
    -   Range of possible values: 30-180
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sa\_analytics.rca.learner\_group\_interval\_secs**

    Time interval \(in seconds\) criteria for grouping alerts. Interval that alerts must be created in, to be included in a group.

    -   Type: integer
    -   Default value: 300
    -   Range of possible values: 60-900
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sa\_analytics.rca.learner\_query\_interval\_secs**

    Length of time period \(in seconds\) from which to include alerts for analysis. Period of past time from which to include alerts in alert aggregation analysis.

    -   Type: integer
    -   Default value: 86400
    -   Range of possible values: 43200-86400
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sa\_analytics.rca.output\_purge\_days**

    Number of days that RCA output is kept before it is purged.

    -   Type: integer
    -   Default value: 3
    -   Range of possible values: 3-5
    -   Location: System Property \[sys\_properties\] table
-   **sa\_analytics.rca.query\_probability\_threshold**

    Confidence score % threshold, above which RCA correlated alert groups appear in the Event Management dashboard and alerts console. Confidence score that must be met by RCA correlated alert groups before the groups are displayed on the Event Management dashboard and alerts console.

    -   Type: integer
    -   Default value: 0
    -   Range of possible values: 0-100
    -   Location: **Alert Aggregation and RCA** &gt; **Properties**
-   **sam.install\_deletion\_deadline**

    Defines the number of days after which a software install is deleted if not discovered with the configuration item. Use a value that is greater than the number of days between consecutive Discovery runs.

    -   Type: integer
    -   Default value: 7
    -   Location: System Property \[sys\_properties\] table
-   **security.list.internal.domains**

    Other domains \(excluding the ones in the comma-separated list in this property\) are classified as external email domains. The counts of incoming emails from these external domains display in the External Incoming Emails metric in the Instance Security Center.

    -   Type: choice string
    -   Default value: None
    -   Other possible values: Comma-separated list of all internal email domains in the organization.
    -   Location: System Property \[sys\_properties\] table
-   **sn\_acc\_vis\_content.set\_assigned\_to**

    Determines if Assigned To attribute is overridden by ACC-V or not.

    -   Type: Boolean
    -   Default value: false
-   **sn\_acc\_vis\_content.assigned\_to\_user\_order**

    Defines the source of Assigned To user and its priority for ACC-V. The order of the username sources defined is used to define the priority based on which the Assigned To user is set for a computer CI. For example, computer\_system\_username, logged\_in\_users. These two different sources decide which user name derived from which source takes preference in deciding the attribute Assigned To for a computer CI.

    computer\_system\_username: The source is derived from the native command for Windows machine wmic computersystem get user username.

    Logged\_in\_users: Source is OsQuery which gets logged in users from the OsQuery table.

    -   Type: choice string
    -   Default value: computer\_system\_username, logged\_in\_users
-   **sn\_acc\_vis\_content.persist\_os\_user\_type**

    Persists the type of users that you are interested in for ACC-V.

    -   Type: Comma separated parameter
    -   Default value: local,system
-   **sn\_acc\_vis.column\_name\_for\_user\_mapping**

    The name of the column in the Agent Client Collector Discovery result containing user identity information, such as a username or an email address. This property maps a discovered device to a user record \(sys\_user\), which is then used to set the **Assigned to** field in the Computer CI \(cmdb\_ci\_computer\) table. If the field is empty, the discovered device is mapped based only on the username and not the domain.

    -   Type: String
    -   Default value: &lt;empty&gt;
-   **sn\_agent.disco\_minimum\_threshold\_for\_rediscovery\_minutes**

    The minimum number of minutes since the last Enhanced Discovery on a given IP before a rediscovery can be triggered. This helps to prevent too frequent Enhanced Discovery in cases where a network intermittently has a break or a laptop is rebooted repeatedly.

    -   Type: Integer
    -   Default value: 60
-   **sn\_agent.disco\_disable\_ci\_clobber\_of\_agentless\_disco**

    If true, checks whether CI already exists discovered with matching criteria \(discovery\_source=ServiceNow\) and instead of re-discovering, links the agent record to existing CI.

    -   Type: Boolean
    -   Default value: true
-   **sn\_agent.disco\_ci\_clobber\_of\_agentless\_disco\_threshold\_days**

    The maximum number of days since an existing CI has been discovered using Agent-less Discovery where the existing CI links instead of re-discovering it using the Agent.  This takes effect when disco\_disable\_ci\_clobber\_of\_agentless\_disco is true and it has been an extended period of time \(over 14 days, by default\) since a non-ACC discovery\_source \(like ServiceNow\) has discovered the CI. Once this threshold is exceeded, Enhanced Discovery is allowed to execute and clobber an existing CI regardless of whether a CI has been previously discovered by a non-ACC discovery\_source. This enables the most recent discovered data to be present in the CMDB.

    -   Type: Integer
    -   Default value: 14
-   **sn\_agent.host\_data\_collection.disable\_when\_container**

    If true, when host data collection occurs and it is found that the Agent Client Collector is running in a container, the incoming data will not be processed and the host data collection status will be set to disabled.

    -   Type: Boolean
    -   Default value: true
-   **sn\_acc\_vis\_content.persist\_sam\_usage\_metrics**

    Enable to leverage the SAM Basic metering functionality. If this flag is set to True, after fetching details about all the software installed, including the last accessed time via osquery, the information goes into the Software Usage \[samp\_sw\_usage\] table. The SAM plugin also needs to be enabled to persist the information.

    -   Type: Boolean
    -   Default value: true
-   **sn\_app\_insights.minutes\_between\_triggers**

    How many minutes to wait before sending out a notification for an identical metric trigger.

    -   Type: Integer
    -   Default value: 30
-   **sn\_app\_insights.p1\_predict\_factor.semaphores**

    The normalizing factor for data for the semaphores metric in the p1 prediction model.

    -   Type: Integer
    -   Default value: 21
-   **sn\_app\_insights.p1\_predict\_factor.sys\_load**

    The normalizing factor for data for the sys\_load metric in the p1 prediction model.

    -   Type: Integer
    -   Default value: 923
-   **sn\_app\_insights.p1\_predict\_max\_cooldown**

    The number of consecutive "no p1 predicted” minutes required to exit the p1 alert state.

    -   Type: String
    -   Default value: 5
-   **sn\_app\_insights.p1\_predict\_threshold**

    The minimum confidence required for the p1 predict model to predict a p1 alert state.

    -   Type: Integer
    -   Default value: 90
-   **sn\_bm\_client.dashboard\_display\_unit**

    Time unit to use for KPI values on the Benchmarks dashboard. Options are **Hours** or **Days**.

    -   Type: choice list
    -   Default value: Days
    -   Location: System Property \[sys\_properties\] table
-   **sn\_chg\_soc.change\_soc\_initial\_limit**

    Defines the number of change\_request records to display on load of the Change Schedule.

    -   Type: Integer
    -   Default value: 40
    -   Location: System Property \[sys\_properties\] table
-   **sn\_chg\_soc.change\_soc\_scroll\_load\_limit**

    Defines the number of change\_request records to display as the Change Schedule is scrolled.

    -   Type: Integer
    -   Default value: 20
    -   Location: System Property \[sys\_properties\] table
-   **sn\_chg\_soc.change\_soc\_total\_limit**

    Defines the total number of change\_request records that can be displayed on a Change Schedule.

    -   Type: Integer
    -   Default value: 1000
    -   Location: System Property \[sys\_properties\] table
-   **sn\_chg\_soc.landing\_page.pinned\_notification**

    Shows a message for pin or unpin a change schedule.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **sn\_chg\_soc.schedule\_window\_days**

    Specifies the number of days to be factored before and after the respective start/end of a change\_request record when displaying blackout and maintenance window spans on the Change Schedule page.

    -   Type: Integer
    -   Default value: 30
    -   Location: System Property \[sys\_properties\] table
-   **sn\_devstudio.servicenow\_studio\_banner.enable**

    Shows the banner for navigating to ServiceNow Studio from App Engine Studio or legacy Studio. Change this property to false to hide the banner.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Properties \[sys\_properties\] table
-   **sn\_disco\_cd.scheduled\_job\_time\_out\_in\_mins**

    This property sets the value for the maximum run time of the scheduled job for Cloud Resources in minutes.

    -   Type: integer
    -   Default value: 120
-   **sn\_disco\_certmgmt.cert\_task\_default\_approval\_group**

    This property is used to set default Approval Group name for Certificate Inventory and Management for manual approval processes for requesting new, renewing, or revoking certificates for automated workflows only. You can add more than one approval group, separated by commas. The task chooses the current domain group first and then the global domain group. If no group is found, the task will fail.

    -   Type: string
    -   Default value: none
-   **sn\_disco\_certmgmt.default\_cert\_order\_validity\_period**

    This property is used to set the validity period of the certificate order being placed in Certificate Inventory and Management.

    -   Type: integer
    -   Default value: 1000 days
-   **sn\_disco\_certmgmt.default\_cert\_task\_priority**

    This property is used to configure New and Renew task priorities in Certificate Inventory and Management. Accepts values 1, 2, 3, 4, 5. If any invalid value \(&lt;1 \|\| &gt;5 \|\| other strings\) is provided, the value reverts to P3.

    -   Type: integer
    -   Default value: 3 \(if property doesn't exist\)
-   **sn\_disco\_certmgmt.default\_revoke\_cert\_task\_priority**

    This property is used to configure Revoke task priorities in Certificate Inventory and Management. Accepts values 1, 2, 3, 4, 5. If any invalid value \(&lt;1 \|\| &gt;5 \|\| other strings\) is provided, the value reverts to P1.

    -   Type: integer
    -   Default value: 1 \(if property doesn't exist\)
-   **sn\_global\_searchui.hide\_results\_count**

    Hides \(**true**\) or displays \(**false**\) the number of matching records for search groups and tables on the [Global search](../../search-administration/concept/global-search-polaris-ui.md#) page.

    To modify this property, select **Enhanced Global Search UI** from the [application picker](../../../build/applications/task/t_SelectAnAppFromTheAppPicker.md) before opening the System Properties table.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **sn\_nowassist\_va.com.glide.cs.gen\_ai.enable\_mid\_topic\_ai\_search\_conversational\_catalogs**

    In Mid Topic Discovery AI Search results, change the value to true to show catalog results. By default, these Mid Topic AI Search results only show knowledge base results.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **sn\_nowassist\_va.nass\_animated\_avatar\_enabled**

    An animated sparkle ![Animated AI sparkle icon.](../../../common/image/icon-ai-sparkle.png) icon appears while the LLM response streams to the end user. The animated sparkle ![Animated AI sparkle icon.](../../../common/image/icon-ai-sparkle.png) icon changes to the static branded Virtual Agent icon after the response has fully loaded. If this system property is set to `false`, the animated ellipsis ![Ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg) icon appears after the loading messages.

    -   Type: true \| false
    -   Default value: true
    -   Location: System Property \[sys\_properties\] table
-   **sn\_nowassist\_va.synthesized\_autostart\_items**

    When synthesized response only returns a singular action, configure whether to automatically launch the action. By default, only Virtual Agent topics automatically launch. You can configure this for whenever synthesized response returns a single conversational catalog item, a single Virtual Agent topic along with Knowledge Base information, or a single conversational catalog item along with Knowledge Base information.

    -   Type: string
    -   Default value: topic
    -   Location: System Property \[sys\_properties\] table
-   **sn\_vad\_genai.com.glide.small\_talk.closure.prompt\_enabled**

    Includes a confirmation message to end the conversation whenever closure small talk is recognized.

    -   Type: true \| false
    -   Default value: false
    -   Location: System Property \[sys\_properties\] table
-   **subscription.custom\_table.enforce\_entitlement**

    You can enable guardrails around custom tables when using certain applications, such as Mobile Studio, in a production or non-production environment.

    When set to **true**, the property limits the list of custom tables available in applications such as Mobile Studio to those you are entitled to use, based on the active subscriptions present on your instance. If you want to remove these guardrails, setting the property to **false** enables you to access to all custom tables, regardless of your active subscription entitlements.

    -   Type: Boolean
    -   Default value:
    -   Location: System Property \[sys\_properties\] table
    **Note:** Setting this property to **false** enables you to use applications with custom tables that may not be entitled. See the service description for your active subscriptions to determine which custom tables \(if any\) you are entitled to use with selected applications.

-   **sys\_par\_insights\_enabled**

    Enables the Proactive Analytics feature.

    -   Type: true/false \(Boolean\)
    -   Default value: true
    -   Location: To change the value, create this property in the System Properties table.
    -   More information: [Add a system property](r_AvailableSystemProperties.md#)
-   **tablet.footer.text**

    Text that appears on the footer of the tablet UI.

    -   Type: string
    -   Default value: Copyright ServiceNow 2012
    -   Location: **System Properties** &gt; **Tablet UI Properties**
-   **tablet.header.text**

    Text that appears on the right-hand side of the tablet UI header.

    -   Type: string
    -   Default value: ServiceNow
    -   Location: **System Properties** &gt; **Tablet UI Properties**

**Parent Topic:**[Basic system configuration](../../core-configuration/concept/p_CoreConfigurationOverview.md)

## Add a system property

Add or create a property to control system behavior.

Add a system property 

### Before you begin

Role required: admin

For more information on creating system properties for your own applications, take the training on the [ServiceNow® Developer Site](https://developer.servicenow.com/dev.do#!/learn/courses/tokyo/app_store_learnv2_automatingapps_tokyo_automating_application_logic/app_store_learnv2_automatingapps_tokyo_application_properties/app_store_learnv2_automatingapps_tokyo_what_are_application_properties).

### About this task

Some properties in the system aren’t visible in an instance by default and must be added to the System Property \[sys\_properties\] table. If a feature requires the addition of the property, you can add a system property.

**Important:** System properties store configuration information that rarely or never changes. Each time you change or add a system property, the system flushes the cache to keep all nodes in the cluster in sync. This cache flush has a very high performance cost for one to 10 minutes, which can potentially cause an outage if done excessively. To prevent such outages, don’t use a system property to store configuration information that changes more than once or twice a month. Instead, use a custom table to store regularly changing configuration information.

### Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Verify that the property doesn’t exist by searching for the property name.

3.  Select **New**.

4.  Complete the System Property form using the database name of the property.

    Make sure to specify the correct data **Type** and add the new value that you want the property to use.

    Properties that you add already contain default values. You add properties to change this value.

<table id="table_tqn_cfv_s1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the property you’re creating.

</td></tr><tr><td>

Description

</td><td>

Type a brief, descriptive phrase describing the function of the property.

</td></tr><tr><td>

Choices

</td><td>

Comma-separated values for a choice list. If you need a different choice list label and value, use an equal sign \(=\) to separate the label from the value. For example, `Blue=0000FF`, `Red=FF0000`, `Green=00FF00` displays **Blue**, **Red**, and **Green** in the list, and saves the corresponding hex value in the property value field.

</td></tr><tr><td>

Type

</td><td>

Select the appropriate data type from the list \(for example, **integer**, **string**, or **true\|false\)**.

</td></tr><tr><td>

Value

</td><td>

Set the desired value for the property. All property values are stored as strings. When retrieving properties via the gs.getProperty\(\) method, treat the results as strings. For example, a true\|false property returns 'true' or 'false' \(strings\), not the Boolean equivalent.

</td></tr><tr><td>

Ignore cache

</td><td>

The system stores system property values in server-side caches to avoid querying the database for configuration settings. When you change a system property value, the system always flushes the cache for the sys\_properties table. Use this field to determine whether to flush this property's value from all other server-side caches.

 The default cleared check box means that the system will flush all server-side caches and retrieve the current property value from the database. Leave the check box cleared when you want to ensure all caches have the current property value.

 Select the check box to ignore flushing some server-side caches, thus flushing only the cache for the sys\_properties table and preserving the prior property value in all other caches. This option avoids the performance cost of flushing all caches and retrieving new property values.

 Typically, you should only select the check box and enable ignoring the cache when you have a system property that changes more frequently than once a month, and the property value is only stored in the sys\_properties table.

</td></tr><tr><td>

Private

</td><td>

Set this property to true to exclude this property from being imported via update sets. Keeping system properties private prevents settings in one instance from overwriting values in another instance. For example, you may not want a system property in a development instance to use the same value as a production instance.

</td></tr><tr><td>

Read roles

</td><td>

Define the roles that have read access to this property.

</td></tr><tr><td>

Write roles

</td><td>

Defines the roles that have write access to this property.

</td></tr></tbody>
</table>5.  Select **Submit**.

    Depending on the property name, an administrator might be able to change its value only through a new module. It may also appear in one of the Properties pages in System Properties.

    **Note:** If the **Ignore cache** check box is selected, the system flushes the server cache when the parameter is changed.


## Create a system properties module

You can add a module in the application navigator to access the list of system properties. This module makes it easy to add properties to the System Properties table.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Menus**.

2.  Search for the application you want to add the properties table to, for example **System Properties**.

    Select an application that is restricted to the admin role so that non-admin users cannot access it.

3.  From the Modules related list, click **New**.

4.  Complete the form fields.

    |Field|Description|
    |-----|-----------|
    |Title|Module name. For example, **All Properties**.|
    |Application Menu|Specifies the name of the application menu the module appears under. This field should automatically be populated with the name of the application you accessed the Modules related list from.|
    |Link type|Specifies the type of link this modules opens. For a list of system properties, select **List of Records**.|
    |Table|Specifies the table used by the module. Select **System Properties \[sys\_properties\]**.|

5.  Click **Submit**.

6.  Verify that the module was created. For example, navigate to **System Properties** &gt; **All Properties**.


### What to do next

If you want to include additional parameters for the list of system properties module, see [Create a module](https://www.servicenow.com/docs/access?context=test-steps-app-navigator-category&version=yokohama&pubname=yokohama-application-development&section=t_CreateAModule&ft:locale=en-US).

