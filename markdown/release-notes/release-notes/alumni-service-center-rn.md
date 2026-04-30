---
title: Alumni Center release notes
description: The ServiceNow Alumni Center application provides a way to stay connected with former employees and non-employees like volunteers and contractors. Alumni Center was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Alumni Center release notes

The ServiceNow® Alumni Center application provides a way to stay connected with former employees and non-employees like volunteers and contractors. Alumni Center was enhanced and updated in the Zurich release.

## Alumni Center highlights for the Zurich release

-   The application name Alumni Service Center is now called Alumni Center.
-   As an alumni, you can see the revamped Alumni Center with Employee Center Pro experiences such as My Active Items, Proactive Prompts, and Content Widgets.
-   As an alumni, you can use improved alumni services available out-of-the-box.
-   As an alumni, you can securely access your documents directly from your profile.
-   As an alumni, use the **Register as alumni** option to create an account with the Alumni Center and login to the Alumni Center website.
-   As an alumni registering in the Alumni Center portal, you can enter details like first name, last name, personal email address and employee number which can be used to verify and match the ex-employee records.
-   As an alumni, you can maintain and update your personal details directly within your profile.
-   As an alumni, you can enter your legacy employment details and latest employment details to maintain your employment history.
-   As an alumni, your can enable or disable notifications for recommended job opportunities, and news/event updates in your profile.
-   As an alumni admin, you can configure the customer specific termination conditions using the HR profile fields to trigger alumni creation process automatically on employee termination.
-   As an alumni admin, you can configure the Alum Self-registration form based on the organization needs.
-   As an alumni admin, you can highlight and showcase the recommended job opportunities.​​​

See  for more information.

**Important:** Alumni Center is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **Alumni Center revamp**

    The revamped alumni home page is a central hub where former employees can update their details, manage preferences, and access personalized job recommendations. It also provides quick access to alumni services, news, resources, and tasks to stay connected and engaged.

    Alumni can maintain their employment history with legacy &amp; latest employment details.

    Alumni can view the existing job opportunities​ and also get personal job recommendation based on your job preferences.

-   **Alumni Self-registration**

    A former employee can sign up on the Alumni Center and provide details to register as an alumni.

    The personal email provided by the employee is validated to verify the employee status ensuring accurate identification and preventing impersonation or duplication.

-   **Configure automatic alumni user creation**

    Alumni user creation is streamlined with a configurable process that allows organizations to generate alumni accounts automatically during an employee offboarding. ​Configurable termination conditions can be used to create the alumni and admins can restrict automatic creation with approvals if needed.

-   **Personal Details Verification**

    Employees in the offboarding stage can review and confirm their personal details such as email, phone number, and shipping address to facilitate effective communication post offboarding and ease alumni onboarding. The offboarding task is available in the Employee Center to-dos and offboarding journeys.


## Removed in this release

The following system properties are removed and the existing configured values are copied to the alumni common configuration UI.

-   Email property - sn\_asc.self\_registration.personal.email.domains
-   Deleted properties - sn\_asc.import.default.state, sn\_asc.import.user\_name.max.tries, sn\_asc.import.alumni.suffix

## Activation information

Install Alumni Center by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   ****

    Explicit roles from Employee Center Pro and Human Resources Scoped App: Core \(com.sn\_hr\_core\).


-   **[Self-register to ServiceNow instance](https://www.servicenow.com/docs/access?context=external-user-self-registration&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Soft dependency on External User Self-Registration plugin \(com.snc.external\_user\_self\_registration\).


**Parent Topic:**[HR Service Delivery release notes](hr-service-delivery-landing.md)

