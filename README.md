# terraform-scaleway-database

## Usage

```hcl
module "database" {
  databases = {
    main = {
      node_type      = "DB-DEV-S"
      engine         = "PostgreSQL-11"
      is_ha_cluster  = true
      disable_backup = false
    }
  }
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.13 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_scaleway"></a> [scaleway](#provider\_scaleway) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [scaleway_rdb_database.this](https://registry.terraform.io/providers/scaleway/scaleway/latest/docs/resources/rdb_database) | resource |
| [scaleway_rdb_instance.this](https://registry.terraform.io/providers/scaleway/scaleway/latest/docs/resources/rdb_instance) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_databases"></a> [databases](#input\_databases) | The scaleway Database configurations | `map(any)` | n/a | yes |
| <a name="input_region"></a> [region](#input\_region) | Region to be used with the scaleway provider | `string` | `"fr-par"` | no |
| <a name="input_zone"></a> [zone](#input\_zone) | Zone to be used with the scaleway provider | `string` | `"fr-par-1"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_this"></a> [this](#output\_this) | A map of the scaleway\_rdb\_database and scaleway\_rdb\_instance resources grouped by databases definitions |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
