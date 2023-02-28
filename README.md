# Compare Writing Styles of IaC among the 5 Tools

This is a repository comparing the writing styles of Infrastructure as Code (IaC) tools. IaC refers to the practice of managing and deploying infrastructure through code, and can help development teams be more efficient. The document lists five different IaC tools: Azure CLI, Ansible Playbook, Terraform, ARM Template, and Bicep. Each tool is described in detail, including the name of the code file, whether it can work, and relevant references. If you are comparing the use of these tools, this repository can provide useful information.

| Tools | Filename | Can work? | Note |
| --- | --- | --- | --- |
| Azure CLI | azcli-create-private-aro.azcli | Yes | [Ref][4] |
| Ansible Playbook | create-private-aro.yml | Yes | [Ref][3] |
| Terraform | terraform-create-private-aro.tf | No | [Ref][5] |
| ARM Template | arm-template-create-private-aro.json | Yes | [Ref][2] |
| Bicep | bicep-create-private-aro.json | Yes | [Ref][1] |

## Suggested Comparison Order

1. Azure CLI v.s. Ansible Playbook: Understand the readability and differences brought by Ansible Playbook
2. Azure CLI v.s. Terraform: Understand the difference between imperative and declarative
3. Ansible Playbook v.s Terraform: Understand that Terraform has better dependency management for the Azure platform
4. ARM Template v.s Terraform: Understand the styles of two declarative languages
5. ARM Template v.s. Bicep: Understand the styles of two declarative languages provided by the official sources

## Environment Requirements

- Req 1: From nothing to running
- Req 2: Deploy Azure Red Hat OpenShift
- Req 3: Should be private cluster instead of public cluster


[1]: https://learn.microsoft.com/en-us/azure/openshift/quickstart-openshift-arm-bicep-template?pivots=aro-bicep#deploy-the-azuredeployjson-template
[2]: https://learn.microsoft.com/en-us/azure/openshift/quickstart-openshift-arm-bicep-template?pivots=aro-arm#deploy-the-azuredeployjson-template
[3]: https://docs.ansible.com/ansible/latest/collections/azure/azcollection/index.html
[4]: https://learn.microsoft.com/en-us/cli/azure/aro?view=azure-cli-latest
[5]: https://github.com/hashicorp/terraform-provider-azurerm/blob/f96e0d47579e6315e45f8e7914d7c0a15679673a/internal/services/redhatopenshift/redhat_openshift_cluster_resource_test.go#L155-L433