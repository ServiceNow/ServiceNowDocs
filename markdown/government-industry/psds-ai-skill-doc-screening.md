---
title: Document Screening Al Skill for Public Sector Digital Services
description: Document Screening Al Skill is an Al-powered capability powered by NowAssist for Document Intelligence and available through Now Assist for PSDS.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Generative AI skills, Explore, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Document Screening Al Skill for Public Sector Digital Services

Document Screening Al Skill is an Al-powered capability powered by NowAssist for Document Intelligence and available through Now Assist for PSDS.

It automatically analyzes documents uploaded by applicants, identifies the type or category of each document \(for example, driver's license, passport, budget, or narrative\), and validates whether the uploaded document matches what was requested in an application checklist. If there is a mismatch, the agent flags it and helps government employees generate Al-assisted messages requesting corrected documentation.

This AI skill uses Al to screen documents and ensure they match what the applicant was required to submit. Instead of waiting for a human to discover an issue later in the process, the system identifies problems immediately and helps resolve them faster.

1.  When an applicant uploads a document, NowAssist automatically analyzes the content of that file. It determines what type of document it is—for example, a driver's license, a passport, a budget document, or a narrative attachment. These document types are configurable, so agencies can define what categories matter to their specific programs.
2.  Once the document type is detected, NowAssist compares it against the expected document type for that step in the application.
3.  If everything matches, the document is marked as valid.
4.  If it doesn't-say a driver's license was required but a different file was uploaded — NowAssist flags the document, explains why, and recommends a corrective action. The results are surfaced directly in the user interface, next to each uploaded document. Agents can immediately see which files are valid for the selected document type, which ones aren't, and why. They can also confirm or dispute the Al's classification if needed. And when a document is flagged, agents can use Al assistance to quickly draft a message back to the applicant requesting the correct documentation. One important clarification: this agent does not validate the accuracy of the information inside the document. It does not verify identity or check data correctness. Its role is focused and intentional-it screens documents and ensures the right document types are submitted. In short, the Document Screening Skill takes one of the most time-consuming steps in public sector case work and makes it faster, smarter, and more accurate- improving outcomes for agencies, agents, and constituents alike.


The Document Screening Skill uses Al-driven document intelligence. Key capabilities include:

-   Document Category Detection: The Al analyzes document content to determine its type \(e.g., ID, passport, budget, narrative\).
-   Validation Against Expected Category: It compares the detected category with what the applicant was required to submit.
-   Error Notification &amp; Recommendations: If the document does not match expectations, the Al agent flags it, explains why, and recommends corrective action.
-   Ul Integration: Validation results are displayed directly next to each uploaded document, allowing human agents to confirm or dispute the classification.
-   Al-Assisted Message Composition: Agents can quickly generate messages requesting corrected documents, which are reprocessed automatically upon re-upload.

For more information on Document Intelligence, see [Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/document-intelligence-landing.md).

The Document Screening Skill delivers measurable value across agencies: Reduced manual effort by eliminating repetitive document checks, Faster application processing and reduced case backlogs, Improved accuracy and consistency in document validation, Lower operational risk from missed or incorrect documentation, Higher agent productivity, allowing staff to focus on complex case work.

The primary users are government employees and case workers, including:

-   Social benefits administrators
-   Grants management officers
-   Public sector intake and eligibility review teams
-   Information request processing staff

There are 6 stages of Document Verifications

-   Unverified : When the document is uploaded or manually undo by Human Agent
-   Verified : Manually Verifed by Human Agent
-   Flagged : Manually Flagged by Human Agent
-   Pre-Verified - Verified by AI
-   Pre-Flagged : Flagged by AI
-   Screening failed by AI : System unable to process documents

For more information on how to activate and customize \(what\) of the Document screening skill, see [Activate the Document screening Al skill in Now Assist for PSDS](psds-ai-skills-doc-screening-activate.md).

