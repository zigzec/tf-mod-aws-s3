## Usage

To run this example you need to execute:

```bash

terraform plan
terraform apply
--------------------
atlantis plan
atlantis apply
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.1.2 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 4.0.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | >= 4.0.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="ec2"></a> [ec2](#ec2) | ../ | v0.0.0 |


## Resources

| Name | Type | Require |
|------|------|--------|
| [aws\_s3\_bucket]() | resource | * |
| [aws\_s3\_bucket_acl]() | resource | * |
| [aws\_s3\_bucket\_versioning]() | resource | * |
| [aws\_s3\_bucket\_server\_side\_encryption\_configuration]() | resource | * |
| [aws\_s3\_bucket\_ownership\_controls]() | resource | * |
| [aws\_s3\_bucket\_policy]() | resource | * |
| [aws\_s3\_bucket\_public\_access\_block]() | resource | * |
| [aws\_s3\_bucket\_cors\_configuration]() | resource | * |
| [aws\_iam\_policy]() | resource | * |

## Inputs

| Name | Input | Type |
|------|------|------|
| [prefix]() | The service name | string |
| [env]() | Environment like prod, stg, dev, alpha ... | string |
| [purpose]() | The team tag used to managed resources | string |
| [team]() | The team tag used to managed resources | string |
| [bucket\_name]() | The bucket name | string |
| [bucket\_acl]() | The canned ACL to apply to the bucket | string |
| [versioning]() | Map containing versioning configuration | map(string) |
| [sse\_config]() | Map containing server-side encryption configuration | any |
| [ownership\_config]() | Map containing bucket ownership configuration | any |
| [bucket\_policy]() | Bucket policy | string |
| [enable\_public\_access\_block]() | whether or not to enable public access block | bool |
| [create\_full\_access\_policy]() | whether or not to create iam policy of s3 full access | bool |
| [create\_readonly\_access\_policy]() | whether or not to create iam policy of s3 readonly access | bool |
| [required\_bucket\_acl]() | wheter or not to set acl | bool |


## Outputs

| Name | Description |
|------|-------------|
| [bucket\_name]() | Bucket Name |
| [bucket\_arn]() | Bucket Arn |
| [full\_access\_policy\_arn]() | Full Access policy arn |
| [readonly\_access\_policy\_arn]() | Readonly Access policy arn |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
