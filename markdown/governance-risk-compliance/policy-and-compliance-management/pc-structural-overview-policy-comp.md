---
title: Structural overview of Policy and Compliance Management
description: The structural overview of Policy and Compliance Management enables you to understand how the different modules that make up the Policy and Compliance Management application of ServiceNow integrate and interact with one another.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Structural overview of Policy and Compliance Management

The structural overview of Policy and Compliance Management enables you to understand how the different modules that make up the Policy and Compliance Management application of ServiceNow integrate and interact with one another.

![Infographic for structural process flow of the modules in Policy and Compliance. For text description refer to the steps in the process flow.](../image/p-c-process-flow-comp-updte-ovrv.png "Structural overview of the modules in Policy and Compliance")

-   **Authority document**

    Policy and Compliance Management application begins by identifying authority documents. These documents are external regulations that include laws, regulations, and standards that your organization need to be compliant with, which depend on the type of business that your organization does and its location. Regulatory requirements are usually published by regulatory agencies that provide requirements outlined by law or a certain industry. These requirements might come from federal or state regulations such as Health Insurance Portability and Accountability Act \(HIPAA\), international regulations such as General Data Protection Regulation \(GDPR\), or industry regulations such as Payment Card Industry \(PCI\). Each of these documents such as HIPAA, GDPR, and PCI is an authority document.

    For example, Payment Card Industry Data Security Standards \(PCI DSS\) is an information security standard and an authority document that is meant to reduce payment card fraud. It provides a set of security standards for all organizations that accept credit card payments. Financial service providers must comply with PCI standards to prevent fraud and protect cardholder data and ensure that their business services are safe and legal.

-   **Citation**

    A citation is a passage or an expression from an authority document \(for example, Unified Compliance Framework \(UCF\)\) that your business must specifically comply with. It is an individual requirement within an authority document. For example, encrypting transmission of cardholder data across public networks is one of the requirements of PCI DSS to prevent theft of consumer's personal financial information through payment card transactions.

    Citations can be created manually or imported via UCF.

-   **Entity type**

    Entity type is a grouping of the entities that match a set of filter conditions. You can automatically generate entities based on a conditioned query to any table within your instance. For example, consider a customer holding an account in a bank as an entity type. The customer has attributes such as a Name, Customer ID, Account type, Income source, and others, which are stored in a customer information table, which can be queried based on any of the attributes.

-   **Entity**

    An entity can be people, departments, applications, objects, servers, external network equipments, different locations, data servers, data warehouse – essentially anything you are going to do a control test against and is of policy and compliance in nature. For example, a person holding an account in a bank with a name and related financial information.

    Entities are automatically generated when an entity type is created.

-   **Policy**

    After authority documents are identified, companies develop policies that specify how the business unit would comply with the authority documents. At a high level, policy statements define what the business should or should not do. For example, an organization can set a policy for data protection that defines the requirements for protecting sensitive customer information. Policies are internal documents of an organization and can be like a firewall policy, networking policy, acceptable use policy, information security, networks security, environmental protection, and others. They are an aggregation of different controls and control objectives that deal with a particular aspect of the business.

-   **Policy acknowledgement**

    The policy acknowledgement module allows policy owners or compliance teams to send out policies for review and acknowledgement by employees to meet compliance requirements.

-   **Policy exception**

    This allows you to have an exception on a policy. For some reason, if you cannot comply with a policy or a control, then you can log an exception.

    The Policy Exception module documents any situation where the organization is not able to follow the documented control. Policy exception has its own life cycle and approvals.

-   **Control objective**

    Control objectives are specific goals that the controls are meant to achieve. For example, to ensure data protection policy, the company can build and maintain a secure network. For an acceptable use policy, there can be a control objective to have a proxy to keep control over the websites that the users are visiting. For a network policy, there can be a control objective to have strong passwords.

    It is through the control objectives that authority documents and policies can be tied together to ease the burden of compliance – one control objective can enforce multiple internal and external requirements. Citations can also be associated to one or more control objectives. It is also at the control objective level the controls and policies are tied to one another. Alternatively, you can look at a Control Objective and see the mappings back to Authority Documents and Policies that show why you do the actions indicated in the objectives.

    The control objectives module is the main hub of the Policy and Compliance Management application. While authority documents state regulatory objectives, and policies document what the organization should or shouldn’t do, the control objectives define exactly how to adhere to those policies and authority documents.

-   **Control**

    A control is a specific implementation of a control objective. For example, for a data protection policy, the company may ensure data is backed up regularly, or set up automated backup system.

    Controls are automatically generated when you associate a policy with an entity type or an entity type with a control objective where a control is created for each entity listed in the entity type for the control objective. However, controls can also be manually created. Controls are tested to see if they are successful in achieving the intended control objective.

-   **Control test**

    A control is put to test to ensure that it is effective in achieving the control objective. For example, a penetration test ensures proper implementation of data encryption.

-   **Indicator**

    An indicator allows you to do a test on the controls, and tests can be scheduled daily, weekly, monthly, or quarterly. An indicator task is created and sent to the user to check whether the control is compliant, and the indicator can be marked as Pass or Fail. If the task fails, then the control is not compliant, and an issue is created. If the indicator passes the test, then the control is compliant until the next scheduled test.

    Indicator templates allow the creation of multiple indicators for similar controls. The Indicator template defines the parameters of the Indicators and is mapped to the Risk Statement or the Control objective according to the Type of Indicator it monitors.

    A task is created each time when the indicator is executed to collect the indicator result. An indicator task is created according to a schedule to ensure monitoring according to a pre-set frequency on the indicator form.

-   **Attestation**

    An attestation assesses the control to continuously monitor its compliance. Unlike an indicator, attestation is mostly ad hoc and may not be scheduled.

-   **Issue**

    If a gap is identified while testing a control, then that gap is termed as an issue. Issues can include operational observations from audits, regulatory compliance violations, security breaches, or other negative results. Or, when a control test fails and is non-compliant, an issue is created. Issues can be shared amongst the Policy and Compliance Management, Risk Management, and Audit Management GRC applications. You can measure the effectiveness of your company's risk management program by how quickly and thoroughly it identifies and reacts to risk and compliance issues.

-   **Remediation task**

    After an issue is confirmed, the organization identifies necessary steps to remediate the issue. To mitigate a risk you can create a remediation task to track the remediation work. If a triage was performed, the triage issue is converted into an actual issue or risk event. You can also track the issue as a recommendation or close it as a non-issue.


