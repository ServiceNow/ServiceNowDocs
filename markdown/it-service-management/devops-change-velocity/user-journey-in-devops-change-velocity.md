---
title: User journey for DevOps Change Velocity
description: Review the adoption journey of the DevOps Change Velocity application to enable a phased \(crawl, walk, run, fly\) approach toward complete automation of change approvals.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, DevOps Change Velocity, IT Service Management]
---

# User journey for DevOps Change Velocity

Review the adoption journey of the DevOps Change Velocity application to enable a phased \(crawl, walk, run, fly\) approach toward complete automation of change approvals.

![DevOps user adoption journey phases.](../image/devops-adoption-journey.png)

While automating change request creation from the Continuous Integration \(CI\) and Continuous Deployment \(CD\) pipelines and automatically approving them will be your end goals with DevOps Change Velocity, you can approach your implementation in this phased manner. Each phase here provides incremental value over the previous phase and enables you to get started with minimum changes to your existing processes:

1.  Connect Tools and Applications: Get started by integrating your key DevOps tools and choosing the key objects from these tools to track. This can be done without needing to modify your pipelines or any of the development assets. And then create DevOps Apps for the teams that you want to onboard first. Completing this phase is necessary to bring data from your tools over to the ServiceNow AI Platform.

    For more information on integrating tools, see [Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md).

2.  Change traceability: After you have established integration with your key DevOps tools, relevant data from these tools will start coming into ServiceNow. Then you can continue to use your existing process to create changes but save time by having all relevant information added to the change request with just a few clicks. This information includes stories, code commits, test results, quality scans, and others. For more information on modeling a change request flow, see [Customizing DevOps flows](using-dev-ops-model-change-flow.md).

    After these two phases are completed, you can progress toward the next two phases, which help you achieve automation of your change process, accelerate deployments, and increase velocity. You can start your implementation with these two phases as they don’t need any changes to your existing processes or pipelines.

3.  Change registration: This phase builds value further by automating the change request creation from the CI/CD pipelines. With this phase you’ll need to modify the team's CI/CD pipeline to enable automatic creation of change requests. This automation saves the time of your developers as they don't have to manually fill the change requests, which reduces the risk of human error. For more information, see [Configuring DevOps change request details within the pipeline](dev-ops-config-change-details.md).
4.  Change automation: This is the final phase in value realization where data from the tools will come into ServiceNow in real time, change requests will be automatically created and they’ll be automatically approved or rejected based on data driven policies. This phase requires creating policy guidelines and enabling automated change approvals decisions based on input data to reduce risk and increase the rate of change success. For more information, see [Accelerating your DevOps change process](dev-ops-change-acceleration.md).

All through these four phases, the Insights dashboards help you analyze operational and business reports and to determine the overall efficiency  and growth of your  development processes.

**Parent Topic:**[Exploring DevOps Change Velocity](dev-ops-landing-page.md)

