---
title: Upgrade Accounts Payable Operations from version 2.0
description: Upgrade Accounts Payable Operations with Document Intelligence from lower to higher versions.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Upgrade Accounts Payable Operations, Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Upgrade Accounts Payable Operations from version 2.0

Upgrade Accounts Payable Operations with Document Intelligence from lower to higher versions.

## Before you begin

-   Upgrade Accounts Payable Operations version 2.0 and above to Accounts Payable Operations 4.0 by installing Document Intelligence version 4.0.
-   As part of APO 2.0 or APO 3.0, in Use cases `sys_di_task_definition` table, verify OOB Use case – “DO NOT USE- Invoice Processing v2”.

Role required: Admin

## Procedure

1.  Verify if the OOB pre-trained model Use case is available in the `sys_di_task_definition` table.

    Verify if the OOB pre-trained model is used for copying and creating Use cases. The upgrade applies only if the users use OOB Use case – “DO NOT USE- Invoice Processing v2” to create a new use case.

2.  Verify the newly added pre-trained model Use case “DO NOT USE - Invoice Processing v3” exists.

3.  Execute the following script from the background script in `sn_ap_ic` Accounts Payable Operations integration with Document Intelligence scope.

4.  To execute the below script, perform the following steps.

5.  ```javascript
functionalignParentUseCaseSysIds(oldReadOnlyUseCaseSysId,newReadOnlyUseCaseSysId){varoldCopyUseCaseGr=newGlideRecord("sys_di_task_definition");oldCopyUseCaseGr.addQuery("parent_task_definition","CONTAINS","base_trained_model");if(oldReadOnlyUseCaseSysId){oldCopyUseCaseGr.addQuery("parent_task_definition","CONTAINS",oldReadOnlyUseCaseSysId).addOrCondition("parent_task_definition","CONTAINS","di_source");}else{oldCopyUseCaseGr.addQuery("parent_task_definition","CONTAINS","di_source");}oldCopyUseCaseGr.query();while(oldCopyUseCaseGr.next()){replaceCopyUseCaseSysId(oldCopyUseCaseGr,oldReadOnlyUseCaseSysId,newReadOnlyUseCaseSysId);}}functionreplaceCopyUseCaseSysId(copyUseCaseGr,oldReadOnlyUseCaseSysId,newReadOnlyUseCaseSysId){varoldParentUseCase=copyUseCaseGr.getValue("parent_task_definition");varoldParentUseCaseObj={};varnewParentUseCaseObj={};if(!oldParentUseCase||!oldParentUseCase.includes("base_trained_model")){return;}oldParentUseCaseObj=JSON.parse(oldParentUseCase);newParentUseCaseObj=oldParentUseCaseObj;if(oldParentUseCaseObj["sys_di_parent"]&&oldReadOnlyUseCaseSysId&&oldParentUseCaseObj["sys_di_parent"]===oldReadOnlyUseCaseSysId){newParentUseCaseObj["sys_di_parent"]=newReadOnlyUseCaseSysId;newParentUseCaseObj["base_trained_model"]=getNewReadOnlyUseCaseTrainingSolutionName(newReadOnlyUseCaseSysId);}elseif(oldParentUseCaseObj["di_parent"]&&!oldParentUseCaseObj["sys_di_parent"]){newParentUseCaseObj["sys_di_parent"]=newReadOnlyUseCaseSysId;newParentUseCaseObj["base_trained_model"]=getNewReadOnlyUseCaseTrainingSolutionName(newReadOnlyUseCaseSysId);}else{newParentUseCaseObj["base_trained_model"]=getNewReadOnlyUseCaseTrainingSolutionName(newReadOnlyUseCaseSysId);}varnewParentUseCase=JSON.stringify(newParentUseCaseObj);copyUseCaseGr.setValue("parent_task_definition",newParentUseCase);copyUseCaseGr.update();}functiongetNewReadOnlyUseCaseTrainingSolutionName(newReadOnlyUseCaseSysId){vargr=newGlideRecord("sys_di_task_def_solution_def");gr.addQuery("task_definition",newReadOnlyUseCaseSysId);gr.addQuery("solution_type","be5131acb70a2110cbc68b91ee11a981");gr.query();if(gr.next()){returngr.getDisplayValue("ml_capability_definition_base.solution_name").toString();}else{return"";}}alignParentUseCaseSysIds("54214afa87c32110822cb887cebb35ff","d679b5744736f110d10671dc416d4390");
```

6.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

7.  Set the **In scope** as `sn_ap_ic`.

8.  Copy and paste the script in the **Scripts** area.

9.  Click **Run Script**.

    -   Use cases configured for Invoice processing flow in Accounts Payable Operations integration with Document Intelligence scope `[sn_ap_ic]` only will get upgraded.
    -   Use cases will be upgraded if there is at least one trained task that are manually trained by the user from Document Intelligence Workspace.
    Use cases are upgraded with latest model.


