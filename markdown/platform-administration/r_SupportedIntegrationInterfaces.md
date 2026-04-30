---
title: Supported integration interfaces
description: ServiceNow provides a number of interfaces to be able to directly integrate with the platform. These interfaces are considered part of the platform and are provided at no additional charge.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Supported integration interfaces

ServiceNow provides a number of interfaces to be able to directly integrate with the platform. These interfaces are considered part of the platform and are provided at no additional charge.

|Interface|
|---------|
|[Email](../../../administer/notification/concept/c_InboundEmailActions.md)|
|[JDBC](../../inbound-other-web-services/task/t_JDBCProbe.md)|
|[JSONv2 Web Service](https://www.servicenow.com/docs/access?context=c_JSONv2WebService&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|
|[LDAP integration](https://www.servicenow.com/docs/access?context=c_LDAPIntegration&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)|
|[SOAP web service](https://www.servicenow.com/docs/access?context=c_SOAPWebService&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|
|[REST API](https://www.servicenow.com/docs/access?context=c_RESTAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|
|[SAML](https://www.servicenow.com/docs/access?context=c_SAML2.0WebBrowserSSOProfile&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)|
|[Digest token authentication](https://www.servicenow.com/docs/access?context=c_DigestTokenAuthentication&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)|
|[ODBC driver](https://www.servicenow.com/docs/access?context=c_ODBCDriver&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|
|[Data Export](../../../administer/exporting-data/concept/c_ExportData.md)|
|[CTI](../../incident/reference/r_ComputerTelephonyIntegration.md)|
|[Syslog probe](r_SyslogProbe.md)|

-   **[Computer Telephony Integration](../../incident/reference/r_ComputerTelephonyIntegration.md)**  
Computer Telephony Integration \(CTI\) is accomplished by the CTI client on the user machine sending a URL to the instance.
-   **[Integrating ServiceNow with your Intranet](../../inbound-other-web-services/concept/c_IntegratServiceNowIntranet.md)**  
You can add a ServiceNow login link to your intranet.
-   **[JDBCProbe](../../inbound-other-web-services/task/t_JDBCProbe.md)**  
A JDBC probe runs on the MID Server to query an external database via \[JDBC\] and returns results to ServiceNow.
-   **[Build a search provider for your instance](../../inbound-other-web-services/task/t_BuildSearchProviderForInstance.md)**  
ServiceNow Search Providers allow you search and our Forums from the IE and Firefox search bar.
-   **[Syslog probe](r_SyslogProbe.md)**  
The ServiceNow Syslog probe uses the MID Server to deliver log messages from a ServiceNow instance to another machine, such as a dedicated log server, using the syslog protocol over an IP network.

**Parent Topic:**[Integration options](../../concept/c_IntegrationOptions.md)

