---
title: Supported features and metadata in custom templates
description: Custom templates in App Engine Studio \(AES\) support most features and metadata, including, but not limited to tables, forms, roles, ACLs, record producers, simple workspaces, flows, and actions.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Reference, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Supported features and metadata in custom templates

Custom templates in App Engine Studio \(AES\) support most features and metadata, including, but not limited to tables, forms, roles, ACLs, record producers, simple workspaces, flows, and actions.

Custom templates can be created in two ways, either from scratch or using an existing scoped application as a starting point.

When you create a custom template, the pre-scan checks to make sure that everything in the application is supported. There are three possible outcomes.

-   All items are supported: The custom template is created. All the objects are available in the custom template and in apps created from the custom template.
-   Some items aren't supported: You can continue to create the template but a few items are not available in the custom template. There’s no impact on the custom template or the apps created from the template.
-   Some items are denied: You encounter an error message and cannot continue further until the errors are fixed. The author must change the app, if it was created from an existing app or the template, if it was created from scratch.

**Note:** Creating an AES template using an application that contains a workspace is not supported.

For more information on the template creation process, see [Build a custom template](../concept/build-custom-template.md).

## Supported metadata

|Label|Name|
|-----|----|
|Access Control|sys\_security\_acl|
|Access Roles|sys\_security\_acl\_role|
|Action Assignment|sys\_declarative\_action\_assignment|
|Action Category|sys\_hub\_category|
|Action Definition|sys\_declarative\_action\_definition|
|Action Exclusion|sys\_workspace\_declarative\_action\_exclusion|
|Action Inputs|sys\_hub\_action\_input|
|Action Instance|sys\_hub\_action\_instance|
|Action item|sys\_sg\_write\_back\_action\_item|
|Action Model Field|sys\_declarative\_action\_model\_field|
|Action Outputs|sys\_hub\_action\_output|
|Action parameters mapping|sys\_sg\_action\_param\_map|
|Action Payload Definition|sys\_declarative\_action\_payload\_definition|
|Action Payload Field|sys\_declarative\_action\_payload\_field|
|Action Payload Mapping|sys\_declarative\_action\_payload\_mapping|
|Action Type|sys\_hub\_action\_type\_definition|
|Activity Definition|sys\_pd\_activity\_definition|
|Activity Stream Screen|sys\_sg\_activity\_stream\_screen|
|Analytics preview|sys\_sg\_chart|
|Analytics section|sys\_sg\_chart\_section|
|Application Menu|sys\_app\_application|
|Application Menu|sys\_ui\_application|
|Application Search Sources|m2m\_search\_context\_config\_search\_source|
|Audience|sys\_ux\_applicability|
|Basic Auth Configuration|sys\_auth\_profile\_basic|
|Builder Template|sys\_uib\_template|
|Business Rule|sys\_script|
|Card|sys\_sg\_view\_config|
|Card element|sys\_sg\_view\_config\_element|
|Card element attribute|sys\_sg\_view\_config\_element\_attribute|
|Card template|sys\_sg\_view\_template|
|Card template element|sys\_sg\_view\_template\_slot|
|Card template element attribute|sys\_sg\_view\_template\_slot\_attribute|
|Catalog Client Scripts|catalog\_script\_client|
|Catalog Item|sc\_cat\_item|
|Catalog Item Available for|sc\_cat\_item\_user\_criteria\_mtom|
|Catalog Item Category|sc\_cat\_item\_category|
|Catalog Item Not Available for|sc\_cat\_item\_user\_criteria\_no\_mtom|
|Catalog Items Catalog|sc\_cat\_item\_catalog|
|Catalog UI Policy|catalog\_ui\_policy|
|Catalog UI Policy Action|catalog\_ui\_policy\_action|
|Catalog Variable Set|io\_set\_item|
|Category Property|sys\_properties\_category\_m2m|
|Chart Colors|sys\_report\_chart\_color|
|Chart screen|sys\_sg\_chart\_screen|
|Choice|sys\_choice|
|Choice Set|sys\_choice\_set|
|Client Script|sys\_script\_client|
|Color Definition|sys\_report\_color|
|Complex Object|sys\_complex\_object|
|Composite Data Broker|sys\_ux\_data\_broker\_composite|
|Contained Role|sys\_user\_role\_contains|
|Cross scope privilege|sys\_scope\_privilege|
|Data Broker Scriptlet|sys\_ux\_data\_broker\_scriptlet|
|Data Broker Server Script|sys\_ux\_data\_broker\_transform|
|Data Item|sys\_sg\_data\_item|
|Data Parameter|sys\_sg\_item\_parameter|
|Data Policy|sys\_data\_policy2|
|Data Policy Rule|sys\_data\_policy\_rule|
|Decision|sys\_decision\_question|
|Decision Condition|sn\_decision\_table\_decision\_condition|
|Decision Input|sys\_decision\_input|
|Decision Table|sys\_decision|
|Decision Table Multiple Result|sys\_decision\_multi\_result|
|Details screen|sys\_sg\_details\_screen|
|Dictionary Entry|sys\_dictionary|
|Dictionary Entry Override|sys\_dictionary\_override|
|Dynamic Filter Options|sys\_filter\_option\_dynamic|
|Email Address Filter|sys\_email\_address\_filter|
|Email Address Filter Domain|sys\_email\_address\_filt\_domain|
|Email Client Configuration|sys\_email\_client\_configuration|
|Email Client From Address|sys\_email\_client\_from\_address|
|Email Client Template|sys\_email\_client\_template|
|Email Filter|sys\_email\_filter|
|Email Layout|sys\_email\_layout|
|Email Reply Separator|sys\_email\_reply\_separator|
|Email Script|sys\_script\_email|
|Email Template|sysevent\_email\_template|
|Embedded Help Role Priority|sys\_embedded\_help\_role|
|Empty State|sys\_sg\_empty\_state|
|EVAM Data Filter|sys\_ux\_composite\_data\_filter|
|EVAM Data Source Filter|sys\_ux\_composite\_datasource\_filter|
|EVAM Datasource|sys\_ux\_composite\_datasource|
|EVAM Datasource M2M|sys\_ux\_composite\_data\_m2m\_datasource|
|EVAM Definition|sys\_ux\_composite\_data|
|EVAM View Config|sys\_ux\_composite\_data\_template\_predicate|
|EVAM View Config Action Assignment M2M|sys\_ux\_predicate\_m2m\_action\_assignment|
|EVAM View Config Bundle|sys\_ux\_composite\_data\_template\_predicate\_bundle|
|EVAM View Config Bundle M2M|sys\_ux\_composite\_data\_m2m\_predicate\_bundle|
|Event Registration|sysevent\_register|
|Export Definition|sys\_export\_definition|
|Export Set|sys\_export\_set|
|Export Target|sys\_export\_target|
|Extended Flow Logic Inputs|sys\_hub\_flow\_logic\_ext\_input|
|Extended Step Input Variable|sys\_hub\_step\_ext\_input|
|Extended Step Output Variable|sys\_hub\_step\_ext\_output|
|Extension Instance|sys\_extension\_instance|
|Extension Point|sys\_extension\_point|
|Facet|sys\_search\_facet|
|Field Label|sys\_documentation|
|Field Map|sys\_impex\_entry|
|Filter|sys\_filter|
|Filter Action|sys\_email\_filter\_action|
|Flow|sys\_hub\_flow|
|Flow catalog variable|sys\_flow\_cat\_variable|
|Flow Inputs|sys\_hub\_flow\_input|
|Flow Logic Instance|sys\_hub\_flow\_logic|
|Flow Snapshot|sys\_hub\_flow\_snapshot|
|Flow Stages|sys\_hub\_flow\_stage|
|Flow Variables|sys\_hub\_flow\_variable|
|Form|sys\_ui\_form|
|Form Header|sys\_aw\_form\_header|
|Form Section|sys\_ui\_section|
|Function|sys\_sg\_button|
|Function instance|sys\_sg\_button\_instance|
|GraphQL Data Broker|sys\_ux\_data\_broker\_graphql|
|Highlighted Value|sys\_highlighted\_value|
|Highlighted Value Condition|sys\_highlighted\_value\_condition|
|HTTP Headers|sys\_rest\_message\_headers|
|HTTP Headers|sys\_rest\_message\_fn\_headers|
|HTTP Method|sys\_rest\_message\_fn|
|HTTP Query Parameters|sys\_rest\_message\_fn\_param\_defs|
|Icon|sys\_sg\_icon|
|Icon section destination launcher|sys\_sg\_navigation\_section\_destination\_applet\_launcher|
|Images|db\_image|
|Import Export Map|sys\_impex\_map|
|Inbound Email Actions|sysevent\_in\_email\_action|
|Indexes|sys\_index|
|Launcher header title|sys\_sg\_applet\_launcher\_header|
|Launcher screen|sys\_sg\_applet\_launcher|
|Launcher section mapping|sys\_sg\_applet\_launcher\_m2m\_section|
|Launcher tab|sys\_sg\_applet\_launcher\_tab|
|Layout Applicability|sys\_ux\_applicability\_m2m\_layout|
|Legacy card|sys\_sg\_item\_view|
|Legacy icon section|sys\_sg\_icon\_section|
|List|sys\_ui\_list|
|List Applicability|sys\_ux\_applicability\_m2m\_list|
|List Control|sys\_ui\_list\_control|
|List item config|sys\_sg\_master\_item|
|List screen|sys\_sg\_list\_screen|
|List stream|sys\_sg\_item\_stream|
|M2m Action Assig Ux Action Config|sys\_ux\_m2m\_action\_assignment\_action\_config|
|M2m Workspace Header Ux Header Config|sys\_ux\_m2m\_workspace\_header\_ux\_header\_config|
|Many to Many Definition|sys\_m2m|
|Message|sys\_ui\_message|
|Mobile UI Rule|sys\_sg\_ui\_rule|
|Mobile UI Rule Action|sys\_sg\_ui\_rule\_action|
|Module|sys\_ui\_module|
|Module|sys\_app\_module|
|Navigation Tab Map|sys\_sg\_navigation\_tab\_map|
|New Record Menu Item|sys\_aw\_new\_menu\_item|
|Notification|sys\_notification|
|Notification|sysevent\_email\_action|
|Notification Category|sys\_notification\_category|
|Notification Common Content|sys\_notification\_common\_content|
|Notification Route|notification\_route|
|Notification Workspace Content|sys\_notification\_workspace\_content|
|Number|sys\_number|
|Playbook Activity Override|sys\_playbook\_activity\_renderer|
|Playbook Activity UIs|sys\_playbook\_experience\_activity\_ui|
|Playbook Experience Action Assignment Map|sys\_playbook\_experience\_action\_assignment\_map|
|Playbook Experience Record Generator|sys\_playbook\_experience\_record\_generator|
|Playbook Experiences|sys\_playbook\_experience|
|Process Definition|sys\_pd\_process\_definition|
|Process Definition Swim Lane Images|sys\_pd\_swim\_lane\_image|
|Process Flow Trigger Plan|sys\_flow\_trigger\_plan|
|Public Pages|sys\_public|
|Push Notification|sys\_sg\_push\_notification|
|Push Notification Installation|sys\_push\_notif\_app\_install|
|Push Notification Message|sys\_push\_notif\_msg|
|Push Notification Message Content|sys\_push\_notif\_msg\_content|
|Question Choice|question\_choice|
|Quick actions menu|sys\_sg\_alp\_quick\_action\_map|
|Recipient Qualifier|sys\_recipient\_qualifier|
|Record Producer|sc\_cat\_item\_producer|
|Record screen|sys\_sg\_form\_screen|
|Record screen segment|sys\_sg\_form\_segment|
|Record section|sys\_sg\_item\_section|
|Redirection destination fields|sys\_sg\_redirect\_dest\_field|
|Related List|sys\_ui\_related\_list|
|Relationship|sys\_relationship|
|Relationship Data Item|sys\_sg\_relationship\_data\_item|
|Report|sys\_report|
|Report Users and Groups|sys\_report\_users\_groups|
|REST Data Broker|sys\_ux\_data\_broker\_rest|
|REST Message|sys\_rest\_message|
|Result|sys\_decision\_multi\_result\_element|
|Role|sys\_user\_role|
|Route Configuration|sys\_ux\_dynamic\_route\_config|
|Route Mapping|sys\_ux\_dynamic\_route\_mapping|
|Scheduled Script Execution|sysauto\_script|
|Screen Applicability|sys\_ux\_applicability\_m2m\_screen|
|Screen fields|sys\_sg\_screen\_field|
|Screen parameters mapping|sys\_sg\_screen\_param\_map|
|Screen segment|sys\_sg\_item\_stream\_segment|
|Screen tab|sys\_sg\_applet\_tab|
|Screen UI Policy|sys\_sg\_ui\_policy|
|Script Action|sysevent\_script\_action|
|Script Include|sys\_script\_include|
|Scripted REST API|sys\_ws\_definition|
|Scripted REST Query Parameter|sys\_ws\_query\_parameter|
|Scripted REST Query Parameter Association|sys\_ws\_query\_parameter\_map|
|Scripted REST Resource|sys\_ws\_operation|
|Search Application Configuration|sys\_search\_context\_config|
|Search config|sys\_sg\_global\_search|
|Search M2M item config|sys\_sg\_global\_search\_m2m\_master\_item|
|Search Source|sys\_search\_source|
|Secondary Values|sys\_aw\_form\_header\_secondary\_values|
|Service Fulfillment Approval Step|sc\_service\_fulfillment\_approval\_step|
|Service Fulfillment Stage|sc\_service\_fulfillment\_stage|
|Service Fulfillment Step|sc\_service\_fulfillment\_step|
|Service Fulfillment Task Step|sc\_service\_fulfillment\_task\_step|
|Service Offering SLA|service\_offering\_sla|
|SLA Definition|contract\_sla|
|SLA Timer Configuration|sla\_timer\_config|
|SLA timer configuration mapping|sla\_timer\_config\_mapping|
|Step Instance|sys\_hub\_step\_instance|
|Stream M2M item config|sys\_sg\_item\_stream\_m2m\_master\_item|
|Stream M2M segment|sys\_sg\_item\_stream\_m2m\_segment|
|Style|sys\_ui\_style|
|Subflow Instance|sys\_hub\_sub\_flow\_instance|
|Subflow Instance Inputs|sys\_hub\_sub\_flow\_instance\_inputs|
|Suggestion Reader and Suggestion Reader Group Relations|m2m\_sys\_suggestion\_reader\_sys\_suggestion\_reader\_group|
|Suggestion Reader Group|sys\_suggestion\_reader\_group|
|Sys Ux M2m Action Layout Item|sys\_ux\_m2m\_action\_layout\_item|
|Sys Ux M2m Highlighted Value Config|sys\_ux\_m2m\_highlighted\_value\_config|
|Sys Ux M2m Workspace View Rule Ux View Rule Config|sys\_ux\_m2m\_workspace\_view\_rule\_ux\_view\_rule\_config|
|System Property|sys\_properties|
|System Property Category|sys\_properties\_category|
|Table|sys\_db\_object|
|Task Relationship Type|task\_rel\_type|
|Task Relationships Allowed|task\_rel\_allowed|
|Template|sys\_template|
|Transform Script|sys\_transform\_script|
|Trigger Definition|sys\_pd\_trigger\_definition|
|Trigger Execution|sys\_flow\_trigger\_auto\_script|
|Trigger Instance|sys\_hub\_trigger\_instance|
|UI Action|sys\_ui\_action|
|UI Action Layout|sys\_aw\_form\_uiaction\_layout|
|UI Action Role|sys\_ui\_action\_role|
|UI Formatter|sys\_ui\_formatter|
|UI Page|sys\_ui\_page|
|UI parameter|sys\_sg\_ui\_parameter|
|UI Policy|sys\_ui\_policy|
|UI Policy Action|sys\_ui\_policy\_action|
|UI Policy Rule|sys\_sg\_ui\_policy\_rule|
|UI Script|sys\_ui\_script|
|UI View|sys\_ui\_view|
|UIB Screen Test Values|sys\_uib\_screen\_test\_values|
|UX Actions Configuration|sys\_ux\_action\_config|
|UX Add-on Event Mapping|sys\_ux\_addon\_event\_mapping|
|UX App Configuration|sys\_ux\_app\_config|
|UX App Route|sys\_ux\_app\_route|
|UX App Theme|m2m\_app\_config\_theme|
|UX Application|sys\_ux\_page\_registry|
|UX Application Category M2M|sys\_ux\_registry\_m2m\_category|
|UX Asset|sys\_ux\_lib\_asset|
|UX Client Script|sys\_ux\_client\_script|
|UX Client Script Include|sys\_ux\_client\_script\_include|
|UX Custom Content Extension|sys\_ux\_custom\_content\_root\_elem|
|UX Dashboard Route Permission|sys\_ux\_route\_permission|
|UX Event|sys\_ux\_event|
|UX Form Actions|sys\_ux\_form\_action|
|UX Form Actions Layout|sys\_ux\_form\_action\_layout|
|UX Form Actions Layout Group|sys\_ux\_form\_action\_layout\_group|
|UX Form Actions Layout Item|sys\_ux\_form\_action\_layout\_item|
|UX Header Configuration|sys\_ux\_header\_config|
|UX Highlighted Value Configuration|sys\_ux\_highlighted\_value\_config|
|UX List|sys\_ux\_list|
|UX List Category|sys\_ux\_list\_category|
|UX List Menu Configuration|sys\_ux\_list\_menu\_config|
|UX Macroponent Definition|sys\_ux\_macroponent|
|UX Page Element Permissions|sys\_ux\_page\_element\_m2m\_role|
|UX Page Property|sys\_ux\_page\_property|
|UX Ribbon Configuration|sys\_ux\_ribbon\_config|
|UX Screen|sys\_ux\_screen|
|UX Screen Collection|sys\_ux\_screen\_type|
|UX Screen Condition|sys\_ux\_screen\_condition|
|UX Theme|sys\_ux\_theme|
|UX Theme Asset|sys\_ux\_theme\_asset|
|UX Theme Assets|sys\_ux\_theme\_m2m\_asset|
|UX View Rules Configuration|sys\_ux\_view\_rules\_configuration|
|Variable|item\_option\_new|
|Variable Set|item\_option\_new\_set|
|Variable Substitutions|sys\_rest\_message\_fn\_parameters|
|View Rule|sysrule\_view\_workspace|
|View Rule|sysrule\_view|
|View Template|sys\_ux\_composite\_data\_template|
|Workspace|sys\_aw\_master\_config|
|Workspace Global Search Configuration|sys\_aw\_global\_search\_config|
|Workspace List|sys\_aw\_list|
|Workspace List Category|sys\_aw\_list\_category|
|Workspace Module|sys\_aw\_module|

## Skipped features and metadata

The template creation process only skips items that should not impact the template or apps created from the template.

|Label|Name|
|-----|----|
|Activity Designer|wf\_element\_activity|
|Activity Variables|wf\_activity\_variable|
|Content Link|content\_link|
|Content Themes|content\_theme|
|Content Type|content\_type|
|Database View|sys\_db\_view|
|Detail Pages|content\_type\_detail|
|Detailed Content|content\_block\_detail|
|Disallows "create from scratch" templates to be re-templatized if there are running executions| |
|Dynamic Content|content\_block\_programmatic|
|Flash Movie|content\_block\_flash|
|Flow Template Mapping|sys\_app\_flow\_template\_mapping|
|IFrames|content\_block\_iframe|
|Input Detail|sys\_app\_template\_input\_detail|
|Lists of Content|content\_block\_lists|
|Login Rule|content\_page\_rule|
|Menu Items|menu\_item|
|Menu Sections|menu\_section|
|Meta Tags|content\_page\_meta|
|Navigation Menu|content\_block\_menu|
|Pages|content\_page|
|Payload|sys\_app\_scan\_payload|
|Payload Loader Rule|sys\_app\_payload\_loader\_rule|
|Payload Rule|sys\_app\_payload\_unloader\_rule|
|Processor|sys\_processor|
|Site|content\_site|
|Spoke Configuration|sys\_app\_template\_spoke\_configuration|
|Stage Default|wf\_stage\_default|
|Static Content|content\_block\_static|
|Style Sheet|content\_theme\_css|
|Subtemplate|sys\_app\_subtemplate|
|Template|sys\_app\_template|
|Template Dependency|sys\_app\_template\_dependency|
|Template Dependency Definition|sys\_app\_template\_dependency\_definition|
|Template Details|sys\_app\_template\_detail|
|Template Function Type|sys\_app\_template\_function\_type|
|Template Input Variable|sys\_app\_template\_input\_var|
|Template Manifest|sys\_app\_template\_manifest|
|Template Output Variable|sys\_app\_template\_output\_var|
|Template Page|sys\_app\_template\_page|
|Template Page Configuration|sys\_app\_template\_page\_configuration|
|Template Wizard|sys\_app\_template\_wizard|
|Variable|sys\_app\_scan\_variable|
|Variable Type|sys\_app\_scan\_variable\_type|
|View Field|sys\_db\_view\_table\_field|
|View Table|sys\_db\_view\_table|
|Workflow|wf\_workflow|
|Workflow Activity Definition|wf\_activity\_definition|
|Workflow Instance|wf\_workflow\_instance|
|Workflow SC Variable|wf\_variable|
|Workflow Schedule|wf\_workflow\_schedule|
|Workflow UI Policy|wf\_ui\_policy|

**Parent Topic:**[App Engine Studio reference](aes-reference.md)

