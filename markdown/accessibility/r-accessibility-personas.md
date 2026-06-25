---
title: Accessibility by persona
description: Specific accessibility features and user preferences can help users with varying access needs. Learn more about accessibility personas and the ServiceNow products and features that can support them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/accessibility/r-accessibility-personas.html
release: nofamily
topic_type: reference
last_updated: "2026-03-18"
reading_time_minutes: 4
keywords: [accessibility, visual disability, cognitive disability, physical disability, accessibility persona, speech disability]
breadcrumb: [Product accessibility]
---

# Accessibility by persona

Specific accessibility features and user preferences can help users with varying access needs. Learn more about accessibility personas and the ServiceNow products and features that can support them.

## What are accessibility personas

Creating inclusive digital experiences begins with understanding the diverse needs of users with disabilities. Accessibility personas are fictional yet research-informed profiles that represent users with varying abilities, such as visual, auditory, speech, cognitive or physical impairments. The following sections outline five main personas and ServiceNow's accessibility features that support them.

## Permanent, temporary, and situational disabilities

Disabilities can be permanent, temporary, or situational. Understanding this spectrum helps teams design more inclusive experiences that benefit all users, not just those with permanent disabilities.

**Permanent disabilities** are long-term conditions that affect how a person interacts with technology. Examples include blindness, deafness, paralysis, or cognitive conditions like dyslexia or ADHD.

**Temporary disabilities** are short-term impairments that limit abilities for a period of time. Examples include a broken arm preventing mouse use, an ear infection causing temporary hearing loss, or eye surgery requiring limited screen time.

**Situational disabilities** occur when environmental or contextual factors create barriers. Examples include bright sunlight making a screen difficult to read, a noisy environment preventing audio comprehension, or holding a baby while trying to navigate a website with one hand.

This framework demonstrates that accessibility features benefit everyone. For instance, captions help not only deaf users \(permanent\) but also users in loud environments \(situational\) or those with ear infections \(temporary\). Similarly, keyboard navigation supports users with mobility impairments \(permanent\), users with a broken wrist \(temporary\), and users holding coffee while working \(situational\).

When ServiceNow designs for permanent disabilities, the platform creates better experiences for all users across all contexts.

## Visual

This persona includes individuals who are blind, have low vision, or experience color blindness. They may rely on screen readers, braille displays, magnification tools, or high-contrast settings. Accessible content for this group includes well-structured headings, descriptive alt text for images, keyboard navigability, and color choices that don’t rely solely on hue to convey meaning.

The ServiceNow AI Platform has several features and settings to support low-vision users.

For the Next Experience UI, these include:

-   Screen-reader compatibility
-   Light and Dark Mode
-   Reflow compatibility to enable magnification up to 200%\*
-   Accessibility Preferences on the Next Experience
    -   Replace colors with patterns in charts and graphs
    -   Reduce the motion of animations
-   Theme builder allows developers to adjust colors and contrast of components to suit branding and accessibility

For Core UI, the following accessibility features are available:

-   Enable a high contrast theme
-   Color and style accessibility
-   Screen reader accessibility

For the Mobile platform, these accessibility features support low vision users:

-   Change mobile analytics views for accessibility
-   Defining font size settings for mobile devices
-   Configure chart views from color segments to black and white patterns

## Auditory

This persona includes individuals who are deaf or hard of hearing. They may use hearing aids, cochlear implants, or rely on visual communication methods such as sign language or captions. Accessibility features include transcripts for audio content, real-time captioning, visual alerts for sound-based notifications, and ensuring that important information is not conveyed through audio alone.

The ServiceNow AI platform emphasizes accessibility for deaf and hard of hearing individuals by providing captions and audio transcripts on many videos. For information on multilingual support, see [ServiceNow AI Platform translation and localization](https://www.servicenow.com/docs/r/platform-administration/system-localization/translation-and-localization.html).

## Speech

People with speech disabilities may have difficulty producing spoken language due to conditions such as stuttering, mutism, or neurological impairments. They often use augmentative and alternative communication \(AAC\) tools like speech-generating devices or text-based interfaces. Accessible systems should support non-verbal input methods and avoid requiring voice commands as the sole interaction mode.

The ServiceNow AI Platform supports users with speech disabilities by providing text input and other non-verbal input methods. For information on multilingual support, see [ServiceNow AI Platform translation and localization](https://www.servicenow.com/docs/r/platform-administration/system-localization/translation-and-localization.html).

## Cognitive/Neurodiverse

Individuals with cognitive disabilities may experience challenges with memory, attention, problem-solving, or language processing. This includes people with ADHD, dyslexia, autism, or intellectual disabilities. Accessible content should use plain language, consistent layouts, clear instructions, and options to reduce distractions. Providing multiple ways to understand and interact with content is key.

The ServiceNow Platform offers accessibility features and settings to support individuals with cognitive disabilities. These include:

-   Text adjust Neurodiversity browser extension
-   Next Experience accessibility user preferences:
    -   Show date and time formats on forms
    -   Show all buttons without the need to hover
    -   Reduce the motion of animations
-   Managing user sessions in Core UI:
    -   Modify session timeout
    -   Configure how much time users have to extend a session

## Physical

This persona represents individuals with limited physical movement, which may affect their ability to use a mouse, keyboard, or touchscreen. They may use assistive technologies such as switch devices, eye-tracking systems, or voice control. Accessibility considerations include ensuring full keyboard support, avoiding time-sensitive interactions, and designing interfaces that minimize the need for precise gestures.

To support users with mobility impairments, the Next Experience offers:

-   Keyboard navigation support
-   An accessibility setting to activate over 40 keyboard shortcuts
-   Keyboard focus on truncated text
-   Voice input through the Now Assist panel

Core UI also includes accessibility features such as:

-   Keyboard navigation and accessibility
-   The use of skip links
-   The option to modify session time out
-   The ability to configure how much time users have to extend a session

## Accessibility Persona Cards on Horizon

To explore more information about accessibility personas, visit the Horizon site to download [Accessibility Persona Cards](https://horizon.servicenow.com/guidelines/accessibility/accessibility-persona-cards).

This resource is a set of 12 cards that presents specific functional limitations that users with disabilities experience. These cards help developers and designers envision and better understand specific challenges users might experience, so that they can plan accordingly.

**Parent Topic:**[Product accessibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/nofamily/markdown/accessibility/product_accessibility.md)

