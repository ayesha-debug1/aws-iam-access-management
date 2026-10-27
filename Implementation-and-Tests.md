
# AWS IAM Project Implementation Steps


## Step 1: Access the AWS IAM Console

1. Sign in to the AWS Management Console.
2. Search for IAM in the AWS service search bar.
3. Open the IAM dashboard.
4. Verify that you are working in the correct AWS account.
   
<br>

## Step 2: Create the 'Developers' & 'admin' Group

1. Open User groups in IAM.
2. Select Create group.
3. Enter `Developers` as the group name.
4. Select the AWS managed policy `EC2ReadOnlyAccess`.
5. Create the group.
6. Verify that the policy is attached.
7. Repeat the same for admin group with policy "administratoraccess"

<br>

## Step 3: Create the Developer & admin User

1. Open Users in IAM.
2. Select Create user.
3. Enter `dev-user` as the username.
4. Add the user to the `Developers` group.
5. Complete user creation.
6. Verify the user's group membership.
7. Repeat the same for admin user and add under "admin" group

<br>

## Step 4: Test Permissions

Performed the following tests and recorded the actual results.

### Developer (dev-user)

| Test |  Result |
|------|---------------|
| Developer sign-in | [View screenshot](Screenshots/dev-signin.png) |
| View permitted AWS resources | [View screenshot](Screenshots/Read-only-access.png) |
| Attempt a resource-creation action | [View screenshot](Screenshots/Access-denied.png) |
| Verify group membership | [View screenshot](Screenshots/verify-group-and-perm.png) |
| Verify attached policy | [View screenshot](Screenshots/verify-group-and-perm.png) |

### Admin (admin-user)

| Test |  Result |
|------|---------------|
| Admin sign-in |  [View screenshot](Screenshots/Admin-signin.png) |
| Attempt a resource-creation action |  [View screenshot](Screenshots/Resource-creation-successfull.png) |
| Verify group membership | [View screenshot](Screenshots/verify-group-and-permission.png) |
| Verify attached policy | [View screenshot](Screenshots/verify-group-and-permission.png) |

<br>

##  Conclusion

This lab demonstrated how AWS Identity and Access Management (IAM) users, groups, and policies work together to control access to cloud resources. By assigning permissions through groups and applying the principle of least privilege, each user was given only the access needed for their role. Testing the access controls confirmed that permitted actions succeeded while restricted actions were denied, showing how AWS evaluates permissions in practice. Overall, the lab reinforced that careful permission design, regular reviews, and good security habits such as enabling MFA and keeping credentials out of repositories are essential for keeping an AWS environment secure

<br>
