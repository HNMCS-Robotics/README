# Organizations

With GitHub Organization, a company (or a team like HNMCS Robotics or Dr. K's ICS4U) owns the GitHub account and repositories. However, contributors, such as employees and freelancers ( and students), can access the organization’s repositories using their personal accounts.

You can use organizations to collaborate with an unlimited number of people across many projects at once, while managing access to your data and customizing settings. Creating an organization helps you centralize your organization’s code. All repositories live under the organization, and billing goes through a central organization account.

You can create teams which allows you easily manage permission controls of all the members. Teams give people access to the organization’s code, making it easy to add or remove people to many repositories at once.

### Helpful Links for instructions/guides

[The Ultimate Manual for Managing Teams and Organizations in GitHub](https://nira.com/managing-teams-and-organizations-in-github/)

[Creating a new organization from scratch - GitHub Docs](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch)

[Adding People to your Organization - GitHub Docs](https://docs.github.com/en/enterprise-server@3.6/organizations/managing-membership-in-your-organization/adding-people-to-your-organization)

[Remove a member from your Organization - GitHub Docs](https://docs.github.com/en/enterprise-server@3.6/organizations/managing-membership-in-your-organization/removing-a-member-from-your-organization)

### Managing User Access to Repositories

You can give organization members, outside collaborators, and teams of people different levels of access to repositories owned by an organization by assigning them to roles.

**From the least access to the most access**

* **Read:** Recommended for non-code contributors who want to view or discuss your project

* **Triage:** Recommended for contributors who need to proactively manage issues and pull requests without write access

* **Write:** Recommended for contributors who actively push to your project

* **Maintain:** Recommended for project managers who need to manage the repository without access to sensitive or destructive actions

* **Admin:** Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repository

More details on the access of each role can found [here](https://docs.github.com/en/enterprise-server@3.6/organizations/managing-user-access-to-your-organizations-repositories/repository-roles-for-an-organization).

#### Base Permissions

You can set base permissions that apply to all members of an organization when accessing any of the organization's repositories. Base permissions do not apply to outside collaborators. 

If someone with admin access to an organization's repository grants a member a higher level of access for the repository, the higher level of access overrides the base permission.

Here is the step-by-step guide to set base permissions for an Organization: [Setting base permissions for an Organization - GitHub Docs](https://docs.github.com/en/enterprise-server@3.6/organizations/managing-user-access-to-your-organizations-repositories/setting-base-permissions-for-an-organization)

</br>

### Roles in an Organization

Reference: [Creating a new organization from scratch - GitHub Docs](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch)

* Organization owners – 

These users have complete administrative control of their organization. Ideally, you want to limit access to this role. For example, you can have two organization owners just in case one is absent when you need to change the billing information or change a member’s permissions.

* Organization members – 

These users can create repositories and project boards, among other permissions. You can also adjust the default permissions for organization members. For instance, you can give the member role read-only or write access. It will apply to everyone in the team with this role. 

* Organization moderators – 

These users have additional powers compared to the members. For example, moderators can set interaction limits and block and unblock non-member contributors.

* Outside collaborators – 

This role is typically granted to external collaborators such as freelancers, consultants, and temporary employees. This role helps you separate users who aren’t full members of your organization for security purposes.

* Billing manager - 

Can manage the billing settings (payment information)

</br>

### Branch Protection

Step-by-step guide to create a Branch protection rule: [Managing a branch protection rule - GitHub Docs](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule)

You can protect important branches by setting branch protection rules, which define whether collaborators can delete or force push to the branch and set requirements for any pushes to the branch, such as passing status checks or a linear commit history.

You can enforce certain workflows or requirements before a collaborator can push changes to a branch in your repository, including merging a pull request into the branch, by creating a branch protection rule. You can apply rules on a specific branch, all the branches, or any branch with a keyword. 

*For example*: We can protect the **main** branch by restricting so that only Admins can merge to **main**. Members can only commit and push to other branches. Pull requests are required and it must be reviewed by code owner before being merged to a protected branch.

By default:

* Branch protection rules disables "force pushes" to the branch and prevents the branch from being deleted. *This can be enabled in the settings while creating the branch protection rule

* Restrictions of branch protection rules **will not** apply to members with admin access to the repository. 

* Protected branch cannot be deleted. When you enable deletion of a protected branch, anyone with at least write permissions to the repository can delete the branch.

Here are some examples for rules that can be applied to branches: 

* [Require status checks before merging](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches#require-status-checks-before-merging) : to ensure that the branch must be of a certain status  before collaborators can make changes to a protected branch. The default status check is **Strict**, it make sures that "the branch must be up to date with the base branch before merging".

