---
title: Password Reset Windows Application release notes
description: Version history for the Password Reset Windows Application in ancillary software on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-ancillary-software-prwa.html
release: store
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - Ancillary software release notes, ServiceNow Store release notes]
---

# Password Reset Windows Application release notes

Version history for the Password Reset Windows Application in ancillary software on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.1.0 - February 2024**
    -   Minor fixes
    -   Supported: The Password Reset Windows Application supports newline characters in the Password rule hint text. The other formatting is not supported. For example, bold, underline, or hyperlink.
    -   Not supported:
        -   Custom verifications are not supported. For some verification types, you can use only one verification.
        -   The password strength indicator is not supported.
        -   Custom UI macros configured on the Process &gt; Advanced page are not supported. For example, Entry, success, or failure macros. The system displays only the default success and failure messages.
    -   Other information:
        -   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface.
        -   The application only works with the entitlement of the com.glideapp.password\_reset.addon.orchestration plugin.
-   **Version 5.0.1 - June 2023**
    -   Minor fixes.
    -   Changed:
        -   The Password Reset Windows Application supports newline characters in the Password rule hint text. The other formatting is not supported. For example, bold, underline, or hyperlink.
        -   Custom verifications are not supported. For some verification types, you can use only one verification.
        -   The password strength indicator is not supported.
        -   Custom UI macros configured on the **Process &gt; Advanced** page are not supported. For example, Entry, success, or failure macros. The system displays only the default success and failure messages.
        -   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface. The application only works with the entitlement of the com.glideapp.password\_reset.addon.orchestration plugin.
-   **Version 5.0.0 - November 2022**
    -   New:
        -   Updated user experience
        -   The Windows app UI matches the Next Experience UI theme
    -   Supported:
        -   The Password Reset Windows Application supports newline characters in the Password rule hint text. Other formatting is not supported; for example: bold, underline, or hyperlink.
    -   Not supported:
        -   Custom verifications are not supported. For some verification types, you can use only one verification.
        -   The password strength indicator is not supported.
        -   Custom UI macros configured on the Process &gt; Advanced page are not supported. For example: Entry, success, or failure macros. The system displays only the default success and failure messages.
    -   Other information:
        -   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface.
        -   The application only works with the entitlement of the com.glideapp.password\_reset.addon.orchestration plugin.
-   **Version 4.5.0 - August 2022**

    New:

    -   PAC \(Proxy Auto-Configuration\) file support in the application.
    -   Multi-Identification support during Identify step of the password reset.
    -   Extended the application certificate expiration.
    Supported:

    The Password Reset Windows Application supports newline characters in the Password rule hint text. The other formatting is not supported, for example, bold, underline, or hyperlink.

    Not supported:

    -   Custom verifications are not supported. For some verification types, you can use only one verification.
    -   The password strength indicator is not supported.
    -   Custom UI macros configured on the Process Advanced page are not supported, for example, entry, success, or failure macros. The system displays only the default success and failure messages.
    Other information:

    -   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface.
    -   The application only works with the entitlement of the com.glideapp.password\_reset.addon.orchestration plugin.
-   **Version 4.4.0 - May 2021**
    -   Fixed: Addressed the security issues in the application.
    -   Supported:
        -   The Password Reset Windows Application supports newline characters in the Password rule hint text. Other formatting is not supported \(bold, underline, hyperlink, and so on\). See the topic titled "Configure the connection to a credential store for the Password Reset processes" in https://docs.servicenow.com.
    -   Not supported:
        -   Custom verifications: For some verification types, you can use only one verification. Custom verifications are not supported. See the topic titled "Password Reset verifications" at https://docs.servicenow.com.
        -   Password strength indicator: See the topic titled "Configure your Password Reset process" in https://docs.servicenow.com.
        -   Custom UI macros configured on the Process &gt; Advanced page are not supported \(for example, entry, success, or failure macros\). The system displays only the default success and failure messages. Other information The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface. See the section titled "Settings on the Details tab of the Password Reset Processes form" in https://docs.servicenow.com. The application will only work with the entitlement of plugin ‘com.glideapp.password\_reset.addon.orchestration.
    -   Other information: The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface. See the section titled "Settings on the Details tab of the Password Reset Processes form" in https://docs.servicenow.com. The application will only work with the entitlement of plugin ‘com.glideapp.password\_reset.addon.orchestration.
-   **Version 4.3.1 - April 2021**
    -   Fixed:
        -   Fixed the Localization issues in Password Reset Windows App.
        -   Fixed the UI issues in Password Reset Windows App.
-   **Version 4.3.0 - December 2020**
    -   Fixed: Issues with Password Reset Windows App with proxy configuration.
-   **Version 4.2.0 - June 2020**
    -   Fixed: Fixed issues with 'Reset Password' and 'Unlock Account' actions in the password reset windows application.
    -   The application will only work with the entitlement of plugin com.glideapp.password\_reset.addon.orchestration.
-   **Version 4.1.0 - June 2019**
    -   Supported:
        -   The Password Reset Windows Application supports newline characters in the Password rule hint text. Other formatting is not supported \(bold, underline, hyperlink, and so on\). See the topic Configure the connection to a credential store for the Password Reset processes.
    -   Not supported:
        -   Custom verifications: For some verification types, you can use only one verification. Custom verifications are not supported. See the topic Password Reset verifications.
        -   Password strength indicator: See the topic Configure your Password Reset process.
        -   Custom UI macros configured on the **Process** &gt; **Advanced** page are not supported \(for example, entry, success, or failure macros\). The system displays only the default success and failure messages.
    -   Other information:
        -   The Password Reset Windows Application uses the base-system CAPTCHA service even if the Password Reset application is configured to use Google reCAPTCHA with the web interface. See the section Settings on the Details tab of the Password Reset Processes form.
-   **Version 4.0 - March 2019**
    -   Changed: This release contains compatibility changes. Previously, Password Reset Windows Application has been supporting 2 distinct versions \(i.e. Password Reset Windows Application 3.5 for Kingston and later as well as Password Reset Windows Application 2.12 for Jakarta and earlier\). Starting with the Password Reset Windows Application 4.0 release, there will be a single version that supports Kingston, London and Madrid.
-   **Version 3.5 - January 2019**
    -   Compatibility: Password Reset Windows Application 3.5 is compatible with Kingston and later releases.
    -   Fixed:
        -   Keyboard focus does not move to the **X** \(close\) button.
        -   Each question answer ends with 'Password edit required' on the Verify page.
        -   Incorrect tab order on the **Reset Password** step.
        -   After selecting **Reset password**, an unexplained long wait occurs without comment by JAWS.
        -   Screen reader issues when an error occurs on the identity, success, and reset pages.
-   **Version 3.4 - October 2018**
    -   Compatibility: Password Reset Windows Application 3.4 is compatible with Kingston and later releases.
    -   Fixed:
        -   Focus does not move to the first error element once **OK** on the Error dialog is pressed.
        -   The email address label and Reset page's **New Password** field are not read by JAWS.
        -   Text overlaps in the Password Reset Windows Application window.
        -   Other performance issues and security fixes.
-   **Version 3.3 - June 2018**
    -   Compatibility: Password Reset Windows Application 3.3 is compatible with the Kingston and later release.
    -   Fixed: Security fixes and performance improvements.
-   **Version 3.2 - May 2018**
    -   Compatibility: Password Reset Windows Application 3.2 is compatible with the Kingston and later release.
    -   Fixed: Security fixes and performance improvements.
-   **Version 3.1 - December 2017**
    -   Compatibility: Password Reset Windows Application 3.1 is compatible with the Kingston and later release.
    -   Fixed: Security fixes and performance improvements.
-   **Version 3.0 - November 2017**
    -   New: Enhancements and updates in the Kingston release.
-   **Version 2.12 - January 2019**
    -   Compatibility: Password Reset Windows Application 2.12 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   Keyboard focus does not move to the **X** \(close\) button.
        -   On the Verify page, each question answer ends with 'Password edit required'.
        -   Incorrect tab order on the **Reset Password** step.
        -   After selecting **Reset password**, an unexplained long wait occurs without comment by JAWS.
        -   Screen reader issues when an error occurs on the identity, success, and reset pages.
-   **Version 2.11 - October 2018**
    -   Compatibility: Password Reset Windows Application 2.11 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   Focus does not move to the first error element once **OK** on the Error dialog is pressed.
        -   The email address label and Reset page's **New Password** field are not read by JAWS.
        -   Text overlaps in the Password Reset Windows Application window.
        -   Other performance issues and security fixes.
-   **Version 2.10 - June 2018**
    -   Compatibility: Password Reset Windows Application 2.10 is compatible with Jakarta and earlier releases.
    -   Fixed: Security fixes and performance improvements.
-   **Version 2.9 - May 2018**
    -   Compatibility: Password Reset Windows Application 2.9 is compatible with Jakarta and earlier releases.
    -   Fixed: Security fixes and performance improvements.
-   **Version 2.8 - December 2017**
    -   Compatibility: Password Reset Windows Application 2.8 is compatible with Jakarta and earlier releases.
    -   Fixed: Security fixes and performance improvements.
-   **Version 2.7 - November 2017**
    -   Compatibility: Password Reset Windows Application 2.7 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   When the process is using AD credential store, Password Reset Windows Application crashes after verification.
        -   In Windows 7, users cannot see the heading for the tabs for the steps they are not on.
-   **Version 2.6 - September 2017**
    -   Compatibility: Password Reset Windows Application 2.7 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   The application displays a reset error page instead of showing a non-fatal error message.
        -   The application labels are missing when Traditional Chinese language packs are involved.
        -   When using the application and SMS verification, users cannot change the password.
        -   The application UI close button is missing.
-   **Version 2.5 - July 2017**
    -   Compatibility: Password Reset Windows Application 2.7 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   Labels are missing when Traditional Chinese language packs are involved.
        -   The application does not progress when pressing enter-key.
        -   Several cosmetic issues occur in the application.
        -   The language setting is not correct for target computers.
-   **Version 2.4 - June 2017**
    -   Compatibility: Password Reset Windows Application 2.7 is compatible with Jakarta and earlier releases.
    -   Updated: Add legal disclosures to Password Reset top-level directory.
-   **Version 2.3 - March 2017**
    -   Compatibility: Password Reset Windows Application 2.7 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   Inconsistent and vague errors when internet is disconnected or if the URL is invalid.
        -   Multiple duplicate users/credentials under the 'More choices' list.
        -   Some French translations in the Password Reset Windows Application are failing.
-   **Version 2.2 - February 2017**
    -   Compatibility: Password Reset Windows Application 2.7 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   When no one is logged into a device, Password Reset shows the 'Other User' tile.
        -   Password Reset hides other credential providers, and 'Forgot password' is shown as a separate login tile.
-   **Version 2.1 - December 2016**
    -   Compatibility: Password Reset Windows Application 2.7 is compatible with Jakarta and earlier releases.
    -   Fixed:
        -   Password Reset Windows Application is crashing when the user does not provide user ID/password in proxy server address.
        -   The 'Unable to establish connection to server' message displays when some users try to unlock an account in the reset page.
        -   The app crashes when the glide.security.use\_csrf\_token sys property is missing or set to false on the instance.
        -   The desktop application does not correctly parse special characters in the password rule hint.
        -   Quickly clicking the 'Forgot password?' link results in an error showing that Password Reset application is already running.
        -   Timeouts during password reset or password unlock result in an unhandled exception.
        -   Multiple tiles are appearing after installing PasswordResetWinAppInstall.
        -   Security fixes and other performance improvements.

**Parent Topic:**[ServiceNow Store - Ancillary software release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-ancillary-software.md)

