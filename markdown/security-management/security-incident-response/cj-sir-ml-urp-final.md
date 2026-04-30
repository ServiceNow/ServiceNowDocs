---
title: Final verdict generation for User Reported Phishing
description: Security Incident Response teams can now drive the finalized verdict for a user reported phishing record based on results from predictive intelligence and threat enrichment integrations.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage Predictive Intelligence for User Reported Phishing, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Final verdict generation for User Reported Phishing

Security Incident Response teams can now drive the finalized verdict for a user reported phishing record based on results from predictive intelligence and threat enrichment integrations.

This final verdict generation is enabled through a decision table construct and leveraged within a flow.

**Prerequisites**

Ensure that all the plugins listed in [Required components and plugins](cj-sir-ml-urp-comp.md) have been installed.

Navigate to **Predictive Intelligence for Phishing** &gt; **Final Verdict** &gt; **Final Verdict for Phishing Security Incident**.

The **Decision Inputs** tab shows the different conditions that were evaluated to arrive at the final verdict.

![User Reported Phishing: ML Config: Decision Inputs](../image/cj-sir-ml-urp-final0.png)

The following conditions are available with the base system:

-   Predicted as suspicious: When predictive intelligence has classified the user reported phishing email as **suspicious**.
-   At least one observable is malicious: When an observable involved in the security incident \(For example, URL, Domain, IP, Hash\) has been classified as **malicious** by threat intelligence sources.
-   Observable enrichment are suspect: When enrichment on observables \(For example, recency of phishing domain registration, country of phishing domain registration\) are deemed to be suspect.
-   Sender domain is spoofed: When the phisher’s email domain is suspected of spoofing a trusted domain.
-   Sender name is spoofed: When the phisher’s email address is suspect of spoofing an trusted employee of an organization.

The **Decisions** tab shows the final verdict options that can be arrived at for a given security incident.

![User Reported Phishing: ML Config: Decisions](../image/cj-sir-ml-urp-final1.png)

The following decisions are available with the base system:

-   Confirmed Phish: When the conditions have led to the final verdict as being a confirmed phishing email.
-   Likely Phish: When the conditions have led to the final verdict as a potential phishing attempt.
-   Likely Benign: When the conditions have led to the final verdict as a benign submission.

You can see the conditions that were evaluated for each of the final verdict options. Click on the Label link to see the conditions.

![User Reported Phishing: ML Config: Decision](../image/cj-sir-ml-urp-final2.png)

You can customize the decision table provided with the base system or create your own decision table. This decision table can be leveraged in security incident response playbooks. The **Generate Final Verdict for Phishing Security Incidents** subflow is available with the base system. This subflow automatically generates the final verdict for a phishing security incident and applies a security tag based on that decision. You can include this subflow as part of the **Automated Phishing** playbook.

The inputs for this subflow are:

-   incident\_id: The sys ID of the phishing security incident.
-   c\_level\_names: Comma separated list of names \(For example, names of executives in the organization\) likely being spoofed in the phishing attack.
-   trusted\_domains: Comma separated list of trusted email domains.
-   enrichment\_keywords: Comma separated list of keywords that indicate the maliciousness of the observable from enrichment results.
-   sender\_email \(optional\): The email address of the sender of the phishing email.

The output of this flow can be **Confirmed Phish**, **Likely Phish**, or **Likely Benign**.

![User Reported Phishing: ML Config: Phishing subflow](../image/cj-sir-pi-phishing-subflow.png)

