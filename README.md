# create-iam-groups

Create/Update IAM groups for a project

## Requirements

Ansible >= 2.4
Boto3 installed

## Role Variables

* `iam_groups`: List of groups to be created/updated, it can contain any number
  of groups, I'm going to show an `GroupName` to give an example
  * `GroupName`: Substitute with the name of the group
    * `managed_policy`: List of arns of allowed policies, for example
      `arn:aws:iam::aws:policy/AdministratorAccess`
    * `users`: List of users associated to the group

I've set up some basic groups: `Admins`, `Developers` and `Billing` in
`defaults/main.yml`.

## Dependencies

None

## Example playbook

```yaml
- hosts: all
  roles:
    - create-iam-groups
```

## License

GPLv2

## Author Information
jamatute (jamatute@paradigmadigital.com)
