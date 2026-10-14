# aws-iam-access-management
A hands-on AWS IAM project demonstrating users, groups, policies, and access control testing.

## Project Overview
This project demonstrates AWS Identity and Access Management (IAM) through a practical lab. It covers IAM users, groups, policies, least-privilege principles, and permission testing.


## Objectives

- Understand AWS IAM users and groups.
- Assign permissions using IAM policies.
- Implement role-based access organization through groups.
- Test allowed and denied actions.
- Document implementation and results.


## Architecture

AWS Account  
→ IAM Users  
→ IAM Groups  
→ IAM Policies  
→ Permission Testing


### Resources Created

| RESOURCE                  | NAME                             | PURPOSE                                |
|---------------------------|----------------------------------|----------------------------------------|
| IAM user                  | Dev_user                         | Developer identity                     |
| IAM group                 | Admin_user                       | Group-based permission management      |
| AWS managed policy        | Readonlyaccess                   | Demonstration of read-only permissions |

  


## Implementation Steps

1. Signed in to the AWS Management Console.
2. Opened the IAM service.
3. Created the Developers group.
4. Attached the ReadOnlyAccess policy.
5. Created dev-user and added the user to Developers.
6. Tested permitted and denied actions.
7. Recorded the results and captured sanitized screenshots.


## Testing and Results

| Test                      | Expected Result                  | Actual Result              |
|---------------------------|----------------------------------|----------------------------|
| User sign-in              | Successful                       | Successful                 |
| View permitted resources  | Allowed where authorized         | Successfully viewed resources |
| Attempt resource creation | Denied where not authorized      | Access denied              |
| Verify group membership   | dev-user belongs to Developers   | Verified                   |


## Security Best Practices

- Follow the principle of least privilege.
- Enable MFA for privileged access.
- Avoid unnecessary access keys.
- Review permissions regularly.
- Never commit passwords, secret keys, or sensitive account information.


## Screenshots

See the `screenshots/` directory for sanitized evidence of the configuration and permission tests.


## Lessons Learned

- How IAM users, groups, and policies work together.
- How AWS evaluates permissions.
- How to verify access controls.
- How to document a cloud security lab.


## References

- [AWS IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [IAM Policies and Permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html)
- [AWS IAM Security Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
