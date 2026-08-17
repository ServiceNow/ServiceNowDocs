---
title: Employee Slate release notes
description: Employee Slate is a new AI-first employee experience that boosts employee productivity, powered by Moveworks or Now Assist.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Employee Slate, AI-native portal, Moveworks, Now Assist, conversation-first]
---

# Employee Slate release notes

Employee Slate is a new AI-first employee experience that boosts employee productivity, powered by Moveworks or Now Assist.

## Employee Slate highlights for the Zurich release

-   Deploy a conversation-first employee experience with intelligent search and personalized interactions.
-   Access all your work-related information from a personalized homepage from widgets such as To-dos, Employee Communications, Popular Content, Quick Links, Profile, Notifications, and Calendar.
-   Navigate between conversations and content without losing context through an interactive split view that displays content alongside conversations.
-   Create a personalized workspace by managing widgets on your personal canvas along with some default widgets.
-   Track all activities from an inbox that consolidates tasks, requests, approvals, and to-dos from multiple departments and external applications.
-   Surface important communications through a banner-style widget featuring targeted announcements with image, headline, and short description capabilities.
-   Manage and create content from content library with conversational content generation.
-   Navigate organizational hierarchies with an integrated search experience for detailed employee information access.

For more information, see  documentation.

**Important:** Employee Slate is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Conversation-first experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-conversation-first.md)**

    Replaces traditional browse navigation with an AI-powered search bar and personalized canvas, supporting service delivery across departments.

-   **[Employee Slate home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/emp-slate-home-page.md)**

    Provides a homepage centered on an AI-powered search bar with five configurable widgets: To-dos, Employee Communications, Trending Content, Quick Links, and Holiday Calendar.

-   **Interactive split view [Employee Slate home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/emp-slate-home-page.md)**

    Displays content alongside the conversation for seamless interaction with forms, articles, and tasks.

-   **[Personalized canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-personalized-canvas.md)**

    Employees can drag, drop, resize, and remove widgets; administrators can lock widgets to keep critical information visible.

-   **[Tasks and requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/emp-slate-inbox.md)**

    Consolidates tasks, requests, approvals, and to-dos from multiple departments and external applications, with AI summaries from Now Assist.

-   **[Employee org chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/emp-slate-orgchart.md)**

    Displays organizational hierarchies with employee details and supports contextual AI questions through Now Assist.

-   **[Employee communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-employee-comms.md)**

    Displays targeted banner announcements on the homepage, linked to knowledge articles or other resources.

-   **Visual content authoring [Employee Slate home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/emp-slate-home-page.md)**

    Provides a content library accessible from the profile icon where authors can create, filter, and publish announcements, with Now Assist generating content from a prompt.

-   **[Employee Slate notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/emp-slate-notifications.md)**

    Delivers 14 pre-configured notification types for approvals, tasks, and requests, with support for bulk actions and grouping.

-   **[Configure branding and theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-config-admin-console.md)**

    Applies a logo, primary color, and accent color consistently across the portal, Moveworks, and Now Assist experiences, with a live preview panel.

-   **[AI-powered widget builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-ai-widget-builder.md)**

    Builds custom widgets through a prompt-driven interface using a model context protocol \(MCP\) with built-in design components and accessibility support.

-   **[Analytics and reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-analytics-reporting.md)**

    Tracks session details, page visits, and widget interactions in a dedicated Employee Slate destination within User Experience Analytics. Measures announcement impressions, clicks, and top-performing content through the communications analytics dashboard in User Experience Analytics.

-   **[Conversation-first catalog and knowledge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-conversational-catalog.md)**

    Integrates search results directly into chat responses, with a side panel for filtering and exploration across all configured connectors. Chat pre-fills catalog form fields from conversation context and opens forms in split view for review and completion.

-   **[Moveworks enterprise search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/employee-slate-moveworks.md)**

    Searches documents across enterprise systems including SharePoint, OneDrive, Google Drive, Slack, and Outlook through the Moveworks assistant.

-   **[Calendar and schedule management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/eslate-calendar-schedule.md)**

    Provides time-aware information through calendar management with My Calendar widget in Canvas displaying the meetings from your schedule. And the Upcoming Holiday widget displays the next relevant holiday on the home page.


## Activation information

Employee Slate requires Zurich Patch 9 or later and an AI assistant \(Moveworks or Now Assist\). Access the Employee Slate setup experience through the profile icon to configure branding, data sources for search, and experience settings.

-   Set up data sources and search configurations
-   Configure assistant-specific settings in Moveworks or Now Assist setup
-   Content author or content manager role required for authoring experience access

For more information, see .

## Accessibility information

Employee Slate includes built-in accessibility compliance through the AI-native widget builder. Custom widgets automatically meet accessibility standards when created through the prompt-driven interface with design components that include accessibility features by default.

## Related ServiceNow applications and features

-   ****

    Previous generation employee portal that remains supported for customers requiring advanced experiences like journeys, intranet, and indoor mapping not yet available in Employee Slate.

-   ****

    Enhanced employee portal with AI capabilities that continues as an option for customers needing features not yet migrated to Employee Slate, with coexistence options available for organizations requiring both portals.

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow AI assistant providing contextual, bi-directional chat capabilities, agentic catalog experiences, and platform-native notifications when embedded in Employee Slate. Requires migration to off-Glide AI orchestrator for optimal performance.

-   ****

    AI assistant platform providing enterprise search across multiple systems, specialized assistance apps like World Knowledge, cross-platform notifications, and over 100 language support when embedded in Employee Slate.

-   **[Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/user-exp-analytics-landing.md)**

    Analytics platform that includes dedicated Employee Slate destination for tracking sessions, events, page visits, and communications effectiveness with custom funnel building capabilities and integrated communications analytics dashboard.


**Parent Topic:**[Unified Employee Experience release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/uex-rn-landing.md)

