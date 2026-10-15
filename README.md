# aws-iam-access-management
A hands-on AWS IAM project demonstrating users, groups, policies, and access control testing.
<br>
## Project Overview
This project demonstrates AWS Identity and Access Management (IAM) through a practical lab. It covers IAM users, groups, policies, least-privilege principles, and permission testing.

<br>

## Problem Statement

Without proper access management, cloud environments are exposed to security risks such as excessive permissions, unauthorized access, and accidental changes to critical resources. Managing permissions user by user is also difficult to scale, easy to get wrong, and hard to audit.

<br>

## Proposed Solution

This project uses AWS IAM to create users and groups and assigns permissions through policies that follow the principle of least privilege. Access controls are then tested with allowed and denied actions to confirm that each user can only perform the tasks their role requires.

<br>
<br>

## Architecture Design

The project uses the following structure:

```
AWS Account
|
|-- IAM Group: Developers
|   |
|   |-- IAM User: dev-user
|   |
|   |-- Policy: ReadOnlyAccess
|
|-- IAM Group: Admins
    |
    |-- IAM User: admin-user
    |
    |-- Administrative permissions
```
<br>
<br>

## Resources Used

- IAM user: Dev_user
- IAM group: Admin_user
- AWS managed policy: ReadOnlyAccess

<br>
<br>


## Security Best Practices

- Follow the principle of least privilege.
- Enable MFA for privileged access.
- Avoid unnecessary access keys.
- Review permissions regularly.
- Never commit passwords, secret keys, or sensitive account information.

<br>
<br>


## References

- [AWS IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [IAM Policies and Permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html)
- [AWS IAM Security Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
