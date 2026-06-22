---
title: Combined Password Reset release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Password Reset from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-passwordreset-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Password Reset release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Password Reset from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Password Reset release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Password Reset to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Password Reset.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Experience improved expiration settings of Soft PIN](https://www.servicenow.com/docs/access?context=password-reset-global-properties&family=washingtondc&ft:locale=en-US)**

Give your users the experience of secured Soft PIN enrollment. While enrolling for the Soft PIN verification, they can view the number of days in which the Soft PIN expires. While resetting the Soft PIN, users view the rules that their Soft PIN must comply with. Also, users get email and ServiceNow® Virtual Agent notifications when their passwords are about to expire.

As a Password Reset administrator, you can configure the Soft PIN expiration settings such as setting the number of days when the passwords expire, the frequency of sending password expiration reminder emails, and history policies on Soft PIN.

These settings are enabled by default even if you've upgraded Password Reset from the previous version.

-   **View the security score for your Password Reset processes**

View the security score for your Password Reset processes. Based on the score, you get notifications for potential configuration improvements to the processes.

While creating the Password Reset process, view security scores for the process. If you see any deviations between the maximum attainable and current scores, you get an email with an actionable list of recommendations to improve the configuration. You get informative messages indicating whether the process configuration is ideal.

Evaluate configurations for identification and verification steps. If your configurations are less secure, get process-wise actionable suggestions on how to improve the strength.

**Note:** Starting Washington DC, the Self-Service or the Service Desk Password Reset Experience is restricted for security\_admin users. Only a user with the `security_admin` role can set the password of another `security_admin` user using the sys\_user record to further enhance the security.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Deny ACLs for Password Reset Access](https://www.servicenow.com/docs/access?context=r_InstalledWithPasswordReset&family=yokohama&ft:locale=en-US)**

Enhance the security of Password Reset related tables by restricting access to non-authenticated users through Deny ACLs.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Granular admin roles in Password Reset](https://www.servicenow.com/docs/access?context=r_InstalledWithPasswordReset&family=australia&ft:locale=en-US)**

Configure the Password Reset application features using the granular Password Reset admin role \(password\_reset\_admin\).


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Password Reset features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Enhancing Password Reset Security URL](https://www.servicenow.com/docs/access?context=password-reset-global-properties&family=xanadu&ft:locale=en-US)**

Control the expiration duration of a password reset URL by setting the `glide.pwd_reset.onetime.token.validity` property. By default, the URL is valid for one hour.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Password Reset features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Password Reset workflows are deprecated and have been replaced by flows in the base system for most users. zBoot users must still use the Password Reset flows.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Password Reset features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The 3DES encryption and decryption have been deprecated in the Password Reset flows and workflows.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Password Reset.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Password Reset is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

Password Reset is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Password Reset is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Password Reset is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Password Reset is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Password Reset we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Password Reset we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Password Reset, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Password Reset we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Password Reset we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Let your users experience the improved security of Soft PIN conforming to its expiration. As a Password Reset administrator, configure the Soft PIN expiration settings for an assured and secured Soft PIN enrollment.
-   View the security score for your Password Reset processes. Based on the score, you get notifications for potential configuration improvements to the processes.
-   Use the **password\_reset.request.max\_email** property to set the maximum number of times a user can receive the "Reset Password" link through email, in a span of 24 hours.

 See [Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

Control the duration of the validity of the Password Reset URL provided in a notification email.

 See [Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enhanced security for all client-callable script includes by switching off the sandbox mode.
-   Enhanced security access for Password Reset tables.

 See [Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.

 See [Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Use the Password Reset granular admin role to configure Password Reset features.

 See [Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

