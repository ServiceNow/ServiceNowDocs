---
title: AWS APIs used for Amazon
description: Explore the AWS APIs used in AI Service Graph Connector for Amazon.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/aws-apis-used-in-ai-service-graph-connector-for-amazon.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-06-02"
reading_time_minutes: 1
breadcrumb: [AWS, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower, Enable AI experiences]
---

# AWS APIs used for Amazon

Explore the AWS APIs used in AI Service Graph Connector for Amazon.

This section lists all AWS APIs used in AI Service Graph Connector for Amazon.

Amazon bedrock agents:

|Action Name|AWS API|
|-----------|-------|
|sgawsbedrock\_agent|GetAgent|
|sgawsbedrock\_get\_agent|GetAgent|
|sgawsbedrock\_list\_agent|ListAgents|
|sgawsbedrock\_list\_agent\_aliases|ListAgentAliases|
|sgawsbedrock\_list\_versions|ListAgentVersions|
|sgawsbedrock\_get\_agent\_action\_group|GetAgentActionGroup|
|sgawsbedrock\_list\_agent\_action\_groups|ListAgentActionGroups|
|sgawsbedrock\_list\_agent\_collaborators\_stream|ListAgentCollaborators|
|sgawsbedrock\_test\_connection|\(ListAgents\)|

Amazon Bedrock Foundation \(bedrock\)

|Action Name|AWS API|
|-----------|-------|
|sgawsbedrock\_get\_inference\_profile|GetInferenceProfile|
|sgawsbedrock\_get\_foundation\_model|GetFoundationModel|

Amazon Bedrock AgentCore Control \(bedrock-agentcore-control\)

|Action Name|AWS API|
|-----------|-------|
|`look_up_gateways_stream`|ListGateways|
|`look_up_gateway_by_id`|GetGateway|
|`look_up_gateway_targets_stream`|ListGatewayTargets|
|`look_up_gateway_target_by_id`|GetGatewayTarget|
|`look_up_agent_runtimes_stream`|ListAgentRuntimes|
|`look_up_agent_runtime_by_id`|GetAgentRuntime|
|`look_up_code_interpreters_stream`|ListCodeInterpreters|
|`look_up_code_interpreter_by_id`|GetCodeInterpreter|
|`look_up_browsers_stream`|ListBrowsers|
|`look_up_browser_by_id`|GetBrowser|
|`sgaws_agentcore_test_connection`|\(ListGateways\)|

Amazon CloudWatch Logs \(logs\):

|Action Name|AWS API|
|-----------|-------|
|`look_up_cloudwatch_startquery`|StartQuery|
|`sgawscloudwatch_startquery`|StartQuery|
|`sgawscloudwatch_getqueryresults`|GetQueryResults|
|`look_up_cloudwatch_getquery`|GetQueryResults|
|`sgawscloudwatch_test_connection`|StartQuery|
|`sgaws_agentcore_cloudwatch_test_connection`|StartQuery|

Amazon SageMaker \(SageMaker\)

|Action Name|AWS API|
|-----------|-------|
|`aws_sagemaker_model_discovery`|ListModels|
|`aws_sagemaker_model_card_discovery`|ListModelCards|
|`aws_sagemaker_describe_model_card`|DescribeModelCard|
|`aws_sagemaker_test_connection`|ListModels|

