---
title: Application state indicators in Application Manager
description: Application detail page headers display indicators with additional information about the state of that application. Indicators tell you about any specific requirements, limitations, or blockers related to installing the application.
locale: en-US
release: australia
product: Application Manager
classification: application-manager
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Reference, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Application state indicators in Application Manager

Application detail page headers display indicators with additional information about the state of that application. Indicators tell you about any specific requirements, limitations, or blockers related to installing the application.

<table id="table_inv_hvp_zgc"><thead><tr><th>

Indicator

</th><th>

Meaning

</th><th>

Action needed

</th></tr></thead><tbody><tr><td>

None

</td><td>

No application state indicators apply to this application.

</td><td>

No action needed. If all dependencies can be installed or updated, the application is available for installation.

 For more information about application dependencies, see [Application Manager application details](../concept/app-details-app-mgr.md#).

</td></tr><tr><td>

"Unavailable for Instance"

</td><td>

The app can't be installed on the type of instance you're currently in.

</td><td>

Install the app from a different kind of instance. For example, trials can only be installed in non-production instances.

 For more information about installation, see [Installing applications, plugins, and products](../concept/installing-apps-app-manager.md).

</td></tr><tr><td>

"Incompatible"

</td><td>

The application version isn't compatible with either the family or patch version of your instance.

</td><td>

Select a compatible application version from the version selector in the application details. If no compatible version is available, consider upgrading your ServiceNow AI Platform instance. For more information about upgrading your instance, see [Prepare your upgrade](https://www.servicenow.com/docs/access?context=rn-prepare-landing-page&version=australia&pubname=australia-release-notes&ft:locale=en-US).

</td></tr><tr><td>

"Demo Available"

</td><td>

The application can be installed on non-production instances for demonstration purposes.

</td><td>

Install the application in a non-production instance to demonstrate functionality. For more information about installing applications, see [Installing applications, plugins, and products](../concept/installing-apps-app-manager.md).

</td></tr><tr><td>

"App Terms Not Accepted"

</td><td>

This application has custom terms and conditions that haven't been accepted yet.

</td><td>

Accept the application's custom terms and conditions on the ServiceNow Store to enable installation. For more information, see [Get a free application](../../../build/applications/task/get-free-app.md).

</td></tr><tr><td>

"Store Terms Not Accepted"

</td><td>

The standard terms and conditions for the ServiceNow Store must be accepted.

</td><td>

Go to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) and accept the standard terms and conditions. For more information, see [Terms and conditions in the ServiceNow Store](../../servicenow-store/concept/sn-store-tncs.md).

</td></tr><tr><td>

"License Required for Subprod"

</td><td>

The application requires a license to install in non-production instances. You don't currently have the necessary license.

</td><td>

Purchase the necessary license. For more information, see [Buy a ServiceNow application](../../servicenow-store/task/buy-servicenow-app.md).

</td></tr><tr><td>

"License Expiring"

</td><td>

Your license for this application is expiring soon.

</td><td>

Contact your account executive or the application's provider and renew your license to continue using the application. For more information about contacting an application provider, see [Contact a seller](../../servicenow-store/task/contact-seller.md).

</td></tr><tr><td>

"Not Licensed"

</td><td>

You don't have a valid license for this application yet, or your license has expired.

</td><td>

Purchase the necessary license. For more information about purchasing applications, see [Buy a ServiceNow application](../../servicenow-store/task/buy-servicenow-app.md) or [Buy a partner application](../../servicenow-store/task/buy-partner-app.md).

</td></tr><tr><td>

"Approval Required"

</td><td>

This application requires approval from the provider before it can be procured or installed.

</td><td>

Go to the ServiceNow Store and request the application. Paid applications and applications that are available at no additional cost can require approval.

 For more information about procuring applications from the ServiceNow Store, see [Getting apps and trials from the ServiceNow Store](../../servicenow-store/concept/getting-apps-trials.md).

</td></tr><tr><td>

"Approval Requested"

</td><td>

A request to purchase or install this application has been submitted.

</td><td>

Monitor the email address associated with your ServiceNow Store account for updates. Approval is granted at the application provider's discretion.

</td></tr><tr><td>

"Purchase in Progress"

</td><td>

Your purchase of this application is being processed.

</td><td>

Monitor the email address associated with your ServiceNow Store account for updates. For more information about purchasing applications, see [Buy a ServiceNow application](../../servicenow-store/task/buy-servicenow-app.md) or [Buy a partner application](../../servicenow-store/task/buy-partner-app.md).

</td></tr><tr><td>

"Purchase Rejected"

</td><td>

The request to purchase the application wasn’t approved by the provider.

</td><td>

Purchase approval is granted at the discretion of the application provider. If you have questions, you can contact the provider. For more information, see [Contact a seller](../../servicenow-store/task/contact-seller.md).

</td></tr><tr><td>

"Deactivation Requested"

</td><td>

The application provider has requested that you deactivate the application.

</td><td>

Uninstall or deactivate the application on your instance. For more information, see [Uninstalling applications](../concept/uninstalling-apps-app-manager.md).

 If you have questions, you can contact the application provider. For more information, see [Contact a seller](../../servicenow-store/task/contact-seller.md).

</td></tr><tr><td>

"Trial Available"

</td><td>

A trial of this application is available to request from the ServiceNow Store.

</td><td>

Request a trial of the application from the ServiceNow Store. For more information, see [Start an application trial from the ServiceNow Store](../../servicenow-store/task/start-trial.md).

</td></tr><tr><td>

"Trial Approval Required"

</td><td>

Installing a trial of this application requires approval from the provider.

</td><td>

Request a 30-day trial of the application from the ServiceNow Store. For more information, see [Start an application trial from the ServiceNow Store](../../servicenow-store/task/start-trial.md).

</td></tr><tr><td>

"Trial Approval Requested"

</td><td>

Your trial request for this application has been submitted to the application provider.

</td><td>

Monitor the email address associated with your ServiceNow Store account for updates. Trial approvals are granted at the application provider's discretion. For more information, see [Start an application trial from the ServiceNow Store](../../servicenow-store/task/start-trial.md).

</td></tr><tr><td>

"Trial Active"

</td><td>

A 30-day trial of this application has been activated.

</td><td>

Install the application in a non-production instance for testing and evaluation. For more information, see [Install an application or plugin](../../../build/applications/task/installing-applications-in-application-manager.md).

 If you want to install the application in a production instance or continue using it after the trial period, purchase the application from the ServiceNow Store. For more information about purchasing applications, see [Buy a ServiceNow application](../../servicenow-store/task/buy-servicenow-app.md) or [Buy a partner application](../../servicenow-store/task/buy-partner-app.md).

</td></tr><tr><td>

"Trial Rejected"

</td><td>

Your trial request for this application has been rejected.

</td><td>

Trial approval is granted at the discretion of the application provider. If you have questions, you can contact the provider. For more information, see [Contact a seller](../../servicenow-store/task/contact-seller.md).

</td></tr><tr><td>

"Trial Expired"

</td><td>

The application trial period has expired.

</td><td>

If you don't want to continue using the application after the trial period, uninstall or deactivate the application. For more information, see [Uninstalling applications](../concept/uninstalling-apps-app-manager.md).

 If you want to continue using the application in a production instance, purchase the license from the ServiceNow Store. For more information about purchasing applications, see [Buy a ServiceNow application](../../servicenow-store/task/buy-servicenow-app.md) or [Buy a partner application](../../servicenow-store/task/buy-partner-app.md).

</td></tr><tr><td>

"Trial Deactivation Requested"

</td><td>

The provider of this application has requested that you deactivate the trial.

</td><td>

Uninstall or deactivate the application on your instance. For more information, see [Uninstalling applications](../concept/uninstalling-apps-app-manager.md).

 If you have questions, you can contact the application provider. For more information, see [Contact a seller](../../servicenow-store/task/contact-seller.md).

</td></tr><tr><td>

"Service Provider Blocked"

</td><td>

Your service provider hasn't made this application available on the current instance.

</td><td>

If you want to install the application on the current instance, contact your service provider and request access.

</td></tr><tr><td>

"Beta App"

</td><td>

This application is part of the ServiceNow Store beta program. The provider has made it available to you for evaluation and feedback.

</td><td>

Refer to the information that was provided in the Beta Publish Program agreement.

</td></tr><tr><td>

"Innovation Lab"

</td><td>

This application is an innovation lab offering. Innovation lab applications are early-stage, experimental projects being developed to introduce new functionality to the ServiceNow AI Platform. Due to the experimental nature of innovation lab offerings, these applications are unsupported and have no warranty.

</td><td>

This state indicator is for informational purposes and requires no action. Refer to other application state indicators for installation availability, if present.

 If no other application state indicators and all dependencies can be installed or updated, the application is available for installation. For more information, see [Application Manager application details](../concept/app-details-app-mgr.md#).

</td></tr></tbody>
</table>**Parent Topic:**[Application Manager reference](app-mgr-reference.md)

