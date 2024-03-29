# Sops into Azure

![Tfsec](https://github.com/nlamirault/terraform-azurerm-sops/workflows/Tfsec/badge.svg)

## Usage

```hcl
module "sops" {
  source  = "nlamirault/sops/azurerm"
  version = "1.0.0"


}
```

and variables :

```hcl

```

## Documentation

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 1.0.0 |
| azuread | >= 1.4.0 |
| azurerm | >= 2.48.0 |

## Providers

| Name | Version |
|------|---------|
| azuread | >= 1.4.0 |
| azurerm | >= 2.48.0 |

## Modules

No Modules.

## Resources

| Name |
|------|
| [azuread_service_principal](https://registry.terraform.io/providers/hashicorp/azuread/1.4.0/docs/data-sources/service_principal) |
| [azurerm_client_config](https://registry.terraform.io/providers/hashicorp/azurerm/2.48.0/docs/data-sources/client_config) |
| [azurerm_key_vault](https://registry.terraform.io/providers/hashicorp/azurerm/2.48.0/docs/resources/key_vault) |
| [azurerm_key_vault_access_policy](https://registry.terraform.io/providers/hashicorp/azurerm/2.48.0/docs/resources/key_vault_access_policy) |
| [azurerm_key_vault_key](https://registry.terraform.io/providers/hashicorp/azurerm/2.48.0/docs/resources/key_vault_key) |
| [azurerm_resource_group](https://registry.terraform.io/providers/hashicorp/azurerm/2.48.0/docs/resources/resource_group) |
| [azurerm_role_assignment](https://registry.terraform.io/providers/hashicorp/azurerm/2.48.0/docs/resources/role_assignment) |
| [azurerm_user_assigned_identity](https://registry.terraform.io/providers/hashicorp/azurerm/2.48.0/docs/resources/user_assigned_identity) |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| enabled\_for\_disk\_encryption | Specify whether Azure Disk Encryption is permitted to retrieve secrets from the vault and unwrap keys | `bool` | n/a | yes |
| expiration\_date | Expiration UTC datetime (Y-m-d'T'H:M:S'Z') | `string` | n/a | yes |
| purge\_protection\_enabled | Is Purge Protection enabled for this Key Vault | `bool` | n/a | yes |
| resource\_group\_location | The Azure Region where the Resource Group should exist | `string` | n/a | yes |
| resource\_group\_name | Name of the resource group to be imported. | `string` | n/a | yes |
| soft\_delete\_retention\_days | The number of days that items should be retained for once soft-deleted | `number` | `7` | no |
| sp\_name | Name of the main service. | `string` | n/a | yes |
| tags | A mapping of tags to assign to the resource. | `map(string)` | <pre>{<br>  "made-by": "terraform"<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| key\_id | Sops key ID |
| user\_assigned\_identity\_id | ID of the user assigned identity |
| user\_assigned\_identity\_name | Name of the user assigned identity |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
