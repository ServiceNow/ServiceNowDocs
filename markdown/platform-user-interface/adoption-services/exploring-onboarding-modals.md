---
title: Exploring new experiences
description: Onboarding modals introduce you to new ServiceNow experiences through wizard-like interfaces in Next Experience. Learn about capabilities, benefits, and implementation approaches for effective user onboarding.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
keywords: [Explore experiences with onboarding modals, Overview, Trigger modals]
breadcrumb: [Onboarding modals, Adoption services, Configure user experiences]
---

# Exploring new experiences

Onboarding modals introduce you to new ServiceNow® experiences through wizard-like interfaces in Next Experience. Learn about capabilities, benefits, and implementation approaches for effective user onboarding.

## Overview to Onboarding modals

Onboarding modals are part of ServiceNow® Adoption Services suite, designed to introduce users to new experiences and applications through interactive, guided workflows. These modals appear as overlay windows that walk users through features, providing contextual help at critical moments.

Onboarding modals support multiple content types including text descriptions, images, video links \(YouTube and Vimeo\), and interactive questions. The modal interface adapts to your instance's theme \(dark, light, or coral\), ensuring visual consistency across the user experience.

Modals can be triggered automatically on first login, when accessing specific applications, or programmatically through custom business logic, giving you complete control over when and how users receive guidance.

## Benefits

Onboarding modals provide benefits across different user populations:

|Benefit|Feature|Users|
|-------|-------|-----|
|Reduce onboarding time|Step-by-step guided modals|All users|
|Consistent user experience|Theme-aware interfaces|All users|
|Flexible deployment|Programmatic triggers|Administrators|
|Customizable content|Multiple content types|Administrators|

## Get Started

Begin using onboarding modals by following this implementation sequence:

1.  **Review default modals:** Navigate to **All** &gt; **Adoption Services** &gt; **All Guidance** to examine the pre-configured onboarding modal included with Next Experience. Test the user experience to understand baseline functionality.
2.  **Plan your content:** Map out the user journey for your application or feature. Identify key concepts users need to learn, optimal sequence for information delivery, and decision points requiring user input.
3.  **Create guidance structure:** Navigate to **All** &gt; **Adoption Services** &gt; **Create Guidance**. Configure the guidance form with appropriate name, type \(Modal\), roles, and application scope.
4.  **Build guidance steps:** Add individual steps using the Help Guidance Steps related list. Choose layouts \(Text, Video, Image and Text, Image and Question, or Question\) and define the presentation order.
5.  **Configure launch mechanism:** Implement the programmatic trigger using UIB client scripts and event dispatching, or leverage automatic triggers based on application access patterns.

## User Journey

The typical user journey with onboarding modals follows this pattern:

**Initial trigger:** User logs in for the first time, accesses a new application, or triggers a custom business rule. The system evaluates whether to display an onboarding modal based on user profile, role assignments, and previous interaction history.

**Modal presentation:** The onboarding modal appears as an overlay, presenting the first guidance step. Users see the title, content \(text, image, or video\), and navigation controls \(Next, Previous, or custom action buttons\).

**Progressive disclosure:** Users navigate through subsequent steps at their own pace.

**Interactive elements:** Question-based steps collect user input through radio buttons \(single answer\) or checkboxes \(multiple answers\). Responses can inform subsequent content or be recorded for analytics purposes.

**Completion:** Upon reaching the final step, users receive a completion confirmation and return to the application. The system records the interaction, preventing duplicate displays unless the modal is explicitly reset.

**Parent Topic:**[Onboarding modals](next-experience-onboarding.md)

