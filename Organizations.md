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
