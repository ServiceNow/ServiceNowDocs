---
title: Ansible permissions
description: Ansible Config Provider, Ansible Catalog and operations permissions.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CSC references, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Ansible permissions

Ansible Config Provider, Ansible Catalog and operations permissions.

<table id="table_okp_yzg_hzb"><thead><tr><th>

Permission type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ansible Config Provider Discovery on Day 0

</td><td>

1.  Configure Ansible credentials reference link: [https://docs.ansible.com/ansible-tower/latest/html/userguide/credentials.html](https://docs.ansible.com/ansible-tower/latest/html/userguide/credentials.html)
2.  Creating Ansible tower users: [https://docs.ansible.com/ansible-tower/3.2.5/html/userguide/users.html](https://docs.ansible.com/ansible-tower/3.2.5/html/userguide/users.html)
3.  Roles/permissions can be granted to Ansible tower users per project/ inventory/ job template/credentials as required. For more details: [https://docs.ansible.com/ansible-tower/latest/html/userguide/users.html\#users-permissions](https://docs.ansible.com/ansible-tower/latest/html/userguide/users.html#users-permissions)
4.  CAPI uses basic authentication token based mechanism which uses the Ansible tower user's credentials. OAuth tokens based on basic authentication credentials are generated.
5.  Projects that contain the GitHub credentials of the playbook \(this is where .yml files exist\) is configured manually on Ansible. For more information: [https://docs.ansible.com/ansible-tower/latest/html/userguide/credentials.html\#source-control](https://docs.ansible.com/ansible-tower/latest/html/userguide/credentials.html#source-control)
6.  Uses Ansible credentials for Discovery of Inventory, projects, cfg installable– job templates \(fetching playbooks and its extra variables\) using CAPI.

</td></tr><tr><td>

Ansible Catalog provision/ de-provision on Day 1

</td><td>

Uses Ansible tower user credentials and service account credentials of Amazon Web Services/ Azure given in the Ansible job template.

</td></tr><tr><td>

Ansible tag:GetResources for discovery

</td><td>

Uses

```
 tag:GetResources
```

permission to discover AWS resources provisioned through Ansible pipeline.

</td></tr><tr><td>

Ansible Day 2 operations

</td><td>

Uses Ansible tower user credentials, service account credentials of Amazon Web Services/ Azure and private ssh key pair or windows user name/password, to connect to the particular cloud resource provisioned.

</td></tr></tbody>
</table>**Parent Topic:**[CSC references](csc-reference.md)

