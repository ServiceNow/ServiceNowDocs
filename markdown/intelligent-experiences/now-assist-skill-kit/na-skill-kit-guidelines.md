---
title: General guidelines for Now Assist Skill Kit
description: General guidelines are available to use Now Assist Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skill-kit/na-skill-kit-guidelines.html
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# General guidelines for Now Assist Skill Kit

General guidelines are available to use Now Assist Skill Kit.

## Now Assist Skill Kit guidelines overview

Think about the process of building a custom skill as having the following phases:

1.  [Scoping the skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/scoping-the-skill.md)
2.  [Collecting data and creating a dataset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/creating-a-dataset.md)
3.  [Developing the prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/developing-the-prompt.md)
4.  [Conducting a performance evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/evaluating-the-prompt.md)
5.  [Deploying and monitoring the skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/deploying-and-monitoring.md)

\[Omitted image "MMASSET0020509-general-guidelines-now-assist-skill-kit-landing.png"\] Alt text: Stages of building a custom skill.

You should adopt a data-driven mindset while you build a skill. A data-driven mindset means emphasizing evidence-based decisions and minimizing speculation about how a large language model \(LLM\) can interpret the specific wording of a prompt.

Now Assist Skill Kit needs intermediate skills in prompt engineering. If you're not a developer, you should equip yourself with the relevant knowledge before working with this tool.

There’s information and helpful tooltips in many places throughout the product. Use this information to understand how to use the tool more effectively.

To ensure that there’s a proper segregation of duties, a developer or generative AI practitioner creates the skill and then publishes it. After the skill is published, a Now Assist Admin will activate the skill, so that it shows up at the configured touch points and is available to use.

