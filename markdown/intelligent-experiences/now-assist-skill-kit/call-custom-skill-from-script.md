---
title: Call a custom skill from a script
description: You can use a script to call a custom skill.
locale: en-US
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Call a custom skill from a script

You can use a script to call a custom skill.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Actions**.

2.  Create a UI action.

    For more information on creating UI actions, see [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

3.  Add your script.

    The following script is an example. You can replace the variables with your data.

    ```
    var inputsPayload = {};
    
    // create the payload to deliver input data to the skill
    
    inputsPayload[‘input name’] = {
    
      tableName: 'table name',
    
      sysId: 'sys_id',
    
      queryString: ''
    
    };
    
    
    //create the request by combining the capability sys ID and the skill config sys ID
    
    var request = {
    
        executionRequests: [{
    
            payload: inputsPayload,
    
            capabilityId: ‘capability sys id’,
    
            meta: {
    
                skillConfigId: ‘skill config sys id’
    
            }
    
        }],
    
        mode: 'sync'
    
    };
    
    
    //run the custom skill and get the output in a string format
    try {
    var output = sn_one_extend.OneExtendUtil.execute(request)['capabilities'][request.executionRequests[0].capabilityId]['response'];
    var LLMOutput = JSON.parse(output).model_output;
    } catch(e) {
     gs.error(e);
     gs.addErrorMessage('Something went wrong while executing the skill.');
    }
    action.setRedirectURL(current);
    ```


**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill](create-new-skill.md)

[Create a prompt](create-prompt-template.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Evaluate a prompt](evaluate-prompt.md)

[Finalize and publish a skill](publish-skill.md)

[Activate a skill](activate-skill.md)

