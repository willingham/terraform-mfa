# terraform-mfa
## Script work-around for MFA-required assumption of roles

This is designed to be used when you enforce MFA on all users, including their use of the AWS API.

To enforce mfa, please see the following modules:
- https://github.com/QuiNovas/terraform-modules/tree/master/aws/user
- https://github.com/QuiNovas/terraform-modules/tree/master/aws/user-role
- https://github.com/QuiNovas/terraform-modules/tree/master/aws/assume-role-group

Once you have MFA enforcement setup and cross-account roles established, you use this script in place of the normal `terraform` command.

## Setup
- Update the `terraform-mfa` script with your account ids and profile names.
- Place `terraform-mfa` in your path, and make it executable.

## Running
`AWS_PROFILE=<aws profile> terraform-mfa <apply|plan|destroy|etc>`

