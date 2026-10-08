---
title: Customer Success Management release notes
description: The ServiceNow Customer Success Management application helps you to streamline your onboarding process, define and track objectives and outcomes, identify and mitigate risks, and increase renewal rates. See the following sections for release notes by version.The October 2026 release includes structured meeting agenda and follow-up tracking, support for linking a single engagement to multiple onboarding cases, and improved AI-generated touchpoint meeting assistance.The September 2026 release adds AI-generated engagement updates, success play recommendations, and automated meeting preparation for touchpoint meetings to Customer Success Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/account-lifecycle-rn.html
release: brazil
topic_type: topic
last_updated: "2026-10-04"
reading_time_minutes: 2
breadcrumb: [Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Customer Success Management release notes

The ServiceNow® Customer Success Management application helps you to streamline your onboarding process, define and track objectives and outcomes, identify and mitigate risks, and increase renewal rates. See the following sections for release notes by version.

## About Customer Success Management

-   Capture meeting agenda items and follow-up next steps as structured records instead of freeform text.
-   Associate a single engagement with multiple onboarding cases.

See [Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Customer Success Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/technology-industry-rn-landing.md)

## Version 2.0

The October 2026 release includes structured meeting agenda and follow-up tracking, support for linking a single engagement to multiple onboarding cases, and improved AI-generated touchpoint meeting assistance.

### What's new

-   **[Meeting agenda items and next steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-scheduler-plus.md)**

    Capture structured meeting agendas and follow-ups instead of relying on a single freeform text field. Record each agenda topic as a Meeting Agenda Item with a state \(Planned, Discussed, or Deferred\), allotted time, presenter, and decision. Capture unresolved follow-ups from a meeting as Meeting Next Steps, and later triage each one by converting it to an action item or dropping it.

-   **[Engagement onboarding links](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-engage-onb-links.md)**

    Associate a single engagement with multiple onboarding cases directly in the platform, without manual workarounds. A new many-to-many relationship connects engagements to onboarding cases. The **Applicable Onboarding Cases** related list appears on the Engagement record, and the **Applicable Engagements** related list appears on the Onboarding Case record.


### What's changed

-   **[Meeting page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-page.md)**

    The prep brief now uses real meeting data for its AI-generated summary, fixing issues that caused fabricated citations and inaccurate sentiment claims.


### Plugin information

-   **New plugins**

    Meeting Scheduler Plus \(app-meeting-sch-plus\): Deploys structured meeting agenda item and next step tracking alongside the existing meeting management app.


## Version 1.0

The September 2026 release adds AI-generated engagement updates, success play recommendations, and automated meeting preparation for touchpoint meetings to Customer Success Management.

### What's new

-   **[Touchpoint meetings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-page.md)**

    Automate the generation, updating, and enrichment of conversation briefs by integrating meeting transcripts, emails, and notes. Identify key discussion topics, risks, issues, and action items.

-   **[AI recommended success plays](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-360-view-reco-actions.md)**

    Guide customer success managers by recommending AI-generated success plays for users in neutral or positive states. Examples include sustained adoption, high CSAT or NPS scores, or value realization milestones.

-   **[AI powered executive briefings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-gen.md)**
    -   Monitor individual engagement health from the Engagement Record Page with a daily AI-generated summary. The summary synthesizes risk, declining metrics, opportunities, team activity changes, and upcoming changes into a prioritized, digestible brief.
    -   Review recent account activity from the Account 360 Overview tab with a daily AI-generated account briefing.
    -   Track prioritized activities across accounts from the Executive Portfolio dashboard with an AI-generated portfolio briefing.
-   **[Technology Account 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/proactive-service-exp-workflows/technology-account-360.md)**

    Use the Technology Account 360 to get a unified view of customer or partner account details combining account health, financial, product usage, and open tasks.


### Plugin information

-   **New plugins**

    Technology Account Management Experiences \(sn\_tech\_exp\): View account 360 and executive portfolio page of the customer or partner account.

    AI Agents for Meetings\(sn\_meeting\_ai\_ag\): Automates meeting preparation by reading relevant records, proposing agendas, and coordinating logistics for review and confirmation.


