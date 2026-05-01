---
title: Reference
description: Reference information for user roles and best practices when implementing onboarding modals.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Onboarding modals, Adoption services, Configure user experiences]
---

# Reference

Reference information for user roles and best practices when implementing onboarding modals.

## User Roles

Onboarding modals require specific role assignments for configuration and usage:

|Role|Capabilities|
|----|------------|
|admin|Full access to create, edit, and delete guidance records, guidance steps, and help content. Can configure client scripts and launch mechanisms. Access to all Adoption Services modules.|
|help\_content\_admin|Edit existing guidance content without full administrative privileges. Useful for content management teams maintaining onboarding materials.|
|User \(any role\)|View and interact with onboarding modals assigned to their role. Navigate through steps, answer questions, and dismiss or complete modals.|

## Best Practices

Follow these guidelines to create effective onboarding experiences:

**Content Design**

-   **Keep steps focused:** Each step should cover one concept. Limit modals to 5-7 steps maximum to avoid overwhelming users.
-   **Use clear language:** Avoid jargon and technical terms without explanation. Write for your least experienced user persona.
-   **Provide visual context:** Include screenshots or annotated images showing exactly where to find features. Users learn better with visual references.
-   **Make exit clear:** Always provide a **Later** or **Skip** option. Never trap users in mandatory onboarding that blocks critical work.

**Technical Implementation**

-   **Test across themes:** Verify modal appearance in dark, light, and coral themes. Images and text should remain readable in all contexts.
-   **Validate sys\_id references:** When using programmatic triggers, ensure guidance sys\_id is correct. Invalid references fail silently without user-facing errors.
-   **Set appropriate roles:** Match modal role requirements to actual user populations. Over-restrictive roles mean users never see guidance; over-permissive roles show irrelevant content.
-   **Use descriptive names:** Name guidance records and steps clearly for maintainability. Future administrators should understand purpose without reading all content.

**Maintenance and Updates**

-   **Review quarterly:** Product updates and UI changes can make onboarding content outdated. Schedule regular reviews to maintain accuracy.
-   **Gather user feedback:** Add feedback mechanisms or monitor help desk tickets mentioning onboarding. Users will tell you what's confusing.
-   **Version content:** Use the **Order** field and **Status** field to manage content versions. Keep draft versions for testing before publishing changes.
-   **Document customizations:** Maintain external documentation of custom client scripts and launch mechanisms. Update sets may not capture all dependencies.

**Parent Topic:**[Onboarding modals](../concept/next-experience-onboarding.md)

