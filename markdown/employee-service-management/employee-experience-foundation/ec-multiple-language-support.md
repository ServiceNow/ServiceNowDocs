---
title: Configuring translation for Content Publishing after upgrade
description: Content Publishing supports multi-lingual content creation by enabling content managers to easily change the interface language and request content translation through the Localization Framework.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Reference, Employee Center, Employee Service Management]
---

# Configuring translation for Content Publishing after upgrade

Content Publishing supports multi-lingual content creation by enabling content managers to easily change the interface language and request content translation through the Localization Framework.

For more information on multiple language support in the Content Library, see [Switch language for Content Publishing](ec-switch-language.md).

For information on translating custom widgets, see [Translate a client script message](https://www.servicenow.com/docs/access?context=t_TranslateAClientScriptMessage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

-   Translation is available through Content Publishing versions 21.0.15 and later.
-   When upgrading your version of Content Publishing, you will not automatically receive translations support for all fields. The following tables are not updated to use translated text instead of the original type field:

    -   Portal Content \(sn\_cd\_content\_portal\)
    -   Block Content \(sn\_cd\_block\)
    -   To-Do Content \(sn\_cd\_content\_todo\)
    -   News Content \(sn\_cd\_content\_article\)
    -   Notification Content \(contains emails \) \(sn\_cd\_content\_notification\)
    Admins can manually enable the changes to the tables to use translations. Go into the table definitions \(sys\_db\_object\) for each table and change the field types to Translated Text or Translated HTML.

    **Warning:** Before you change the field types for a table, ensure you perform a back up your data into another column or by exporting the data first. This is a safe guard against losing any data.


The tables and fields that require changing are:

|Table|Field|Original type|New type|
|-----|-----|-------------|--------|
|Portal Content \(sn\_cd\_content\_portal\)|button\_text|String|Translated Text|
|Portal Content \(sn\_cd\_content\_portal\)|link\_text|String|Translated Text|
|Portal Content \(sn\_cd\_content\_portal\)|rich\_text|HTML Script|Translated HTML|
|Rich Content HTML \(sn\_cd\_content\_portal\)|headline|HTML|Translated HTML|
|Rich Content HTML \(sn\_cd\_content\_portal\)|heading\_text|String|Translated Text|
|Block Content \(sn\_cd\_block\)|rich\_text|HTML|Translated HTML|
|Block Content \(sn\_cd\_block\)|rich\_text\_user\_specific|HTML Script|Translated HTML|
|To-do Content \(sn\_cd\_content\_todo\)|button\_text|String|Translated Text|
|News Content \(sn\_cd\_content\_article\)|headline|String|Translated Text|
|News Content \(sn\_cd\_content\_article\)|rich\_content\_html|HTML|Translated HTML|
|News Content \(sn\_cd\_content\_article\)|title|String|Translated Text|
|Notification Content \(sn\_cd\_content\_notification\)|rich\_text\_plain\_html|HTML|Translated HTML|
|Notification Content \(sn\_cd\_content\_notification\)|subject|String|Translated Text|
|Notification Content \(sn\_cd\_content\_notification\)|description|String|Translated Text|

-   **[Integration with Localization Framework](ec-int-localization-framework.md)**  
Language translation fulfillers can provide translations faster and more efficiently by integrating with Localization Framework.
-   **[Switch language for Content Publishing](ec-switch-language.md)**  
When creating content from the Content Library, you have the option to select a different language to view in your session similar to changing your language at login.

**Parent Topic:**[Employee Center reference](../reference/emp-center-reference.md)

**Related topics**  


[Activity Configuration form](../reference/ec-activity-configuration-form.md)

[Activity Configuration Detail form](../reference/activity-configuration-detail-form.md)

[Approvals experience reference](../reference/approval-hub-ootb.md)

[Block content form](../reference/block-content-form.md)

[Browser Extension for Employee Center forms](ecbe-forms.md)

[Campaign overview and Campaign analytics dashboards](ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](../reference/components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](../reference/installed-content-engagement.md)

[Components installed with Content Experiences](../reference/installed-with-content-auto.md)

[Components installed with Content Publishing](../reference/installed-with-content-delivery-1.md)

[Components installed with Content Governance](../reference/ec-installed-content-governance.md)

[Components installed with Content Analytics](../reference/ecpro-installed-content-analytics-1.md)

[Connected Content form](../reference/connected-content-form.md)

[Content Analytics dashboards](content-analytics-dashboards.md)

[Content engagement dashboard](ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](content-library-overview-dashboard.md)

[Default Employee Profile Header Configuration record](../reference/default-profile-header.md)

[Employee Center widgets](employee-center-widgets-list.md)

[Employee Profile form](../reference/employee-profile-fieldconfig.md)

[Employee Profile Header Configuration form](../reference/profile-header-config-form.md)

[Employee Profile portal configuration form](../reference/profile-portal-config-form.md)

[Employee Profile upgrade scenarios](../reference/emp-profile-upgrade.md)

[Enhanced Requests Experience forms](../reference/req-concept-ec.md)

[External Link form](../reference/external-link-form.md)

[Featured Content form](../reference/featured-content-form.md)

[Feedback Analytics dashboard](ex-fdback-board.md)

[Feedback configuration form](../reference/ex-feedback-new-record.md)

[Feedback definition form](../reference/fdbck-dfnition-record.md)

[Footer form](../reference/ec-footer-form.md)

[Footer Menus form](../reference/ec-footer-menus.md)

[Guided Self-Service reference](../reference/gss-guided-self-service-reference-info.md)

[Link content form](../reference/link-content-form.md)

[Menu Item form](../reference/menu-item-form.md)

[Notification content form](../reference/notification-content-form.md)

[Employee Profile Overview section form](../reference/profile-overview-section-form.md)

[Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md)

[Properties installed with Content Governance](../reference/properties-installed-content-governance.md)

[Properties installed with Content Publishing](../reference/properties-with-content-delivery.md)

[Quick Link form](../reference/ec-quick-link-form.md)

[Standard banner and icon sizes](../reference/ec-portal-images-size.md)

[Tab widget mapping form](../reference/tab-widget-mapping-form.md)

[Taxonomy form](../reference/taxonomy-form.md)

[To-do content form](../reference/to-do-content-form.md)

[Topic form](../reference/topic-form.md)

[User Criteria form](../reference/ec-user-criteria-form.md)

[User Criteria output](../reference/user-criteria-output.md)

