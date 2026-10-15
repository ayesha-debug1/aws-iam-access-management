
# AWS IAM Project Implementation Steps


## 1. Step 1: Access the AWS IAM Console

1. Sign in to the AWS Management Console.
2. Search for IAM in the AWS service search bar.
3. Open the IAM dashboard.
4. Verify that you are working in the correct AWS account.
   
<br>

## 2. Step 2: Create the 'Developers' & 'admin' Group

1. Open User groups in IAM.
2. Select Create group.
3. Enter `Developers` as the group name.
4. Select the AWS managed policy `EC2ReadOnlyAccess`.
5. Create the group.
6. Verify that the policy is attached.
7. Repeat the same for admin group with policy "administratoraccess"

<br>

## 3. Step 3: Create the Developer & admin User

1. Open Users in IAM.
2. Select Create user.
3. Enter `dev-user` as the username.
4. Add the user to the `Developers` group.
5. Complete user creation.
6. Verify the user's group membership.
7. Repeat the same for admin user and add under "admin" group

<br>

## 4. Step 5: Test Permissions

Performed the following tests and recorded the actual results.

### Developer (dev-user)

| Test | Expected Result | Actual Result |
|------|-----------------|---------------|
| Developer sign-in | Successful | Successful - [View screenshot](Screenshots/dev-signin.png) |
| View permitted AWS resources | Allowed where authorized | Successfully viewed resources - [View screenshot](Screenshots/Read-only-access.png) |
| Attempt a resource-creation action | Denied where no permission allows it | Access denied - [View screenshot](Screenshots/Access-denied.png) |
| Verify group membership | Correct membership | dev-user belongs to Developers group - [View screenshot](Screenshots/verify-group-and-perm.png) |
| Verify attached policy | Is attached successfully | Is attached successfully - [View screenshot](Screenshots/verify-group-and-perm.png) |

### Admin (admin-user)

| Test | Expected Result | Actual Result |
|------|-----------------|---------------|
| Admin sign-in | Successful | Successful - [View screenshot](Screenshots/Admin-signin.png) |
| Attempt a resource-creation action | Creation successful due to full access | Successful - [View screenshot](Screenshots/Resource-creation-successfull.png) |
| Verify group membership | Correct membership | admin-user belongs to Admins group - [View screenshot](Screenshots/verify-group-and-permission.png) |
| Verify attached policy | Is attached successfully | Is attached successfully - [View screenshot](Screenshots/verify-group-and-permission.png) |


<br>

## 5. Conclusion

This lab demonstrated how AWS Identity and Access Management (IAM) users, groups, and policies work together to control access to cloud resources. By assigning permissions through groups and applying the principle of least privilege, each user was given only the access needed for their role. Testing the access controls confirmed that permitted actions succeeded while restricted actions were denied, showing how AWS evaluates permissions in practice. Overall, the lab reinforced that careful permission design, regular reviews, and good security habits such as enabling MFA and keeping credentials out of repositories are essential for keeping an AWS environment secure

<br>

## 6. References

- [AWS IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [AWS IAM Security Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
