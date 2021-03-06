=============
Organizations
=============

Create Organization
===================
When you create a new :term:`organization` from scratch, it doesn't have any repositories associated with it.

Go to **Profile -> Settings -> Organizations -> New organization**

Repository permission levels
----------------------------
You can customize access to each repository in your organization with granular permission levels, giving people access to the features and tasks they need.

People with admin permissions can manage individual and team access to an organization-owned repository.

Permission levels
+++++++++++++++++
You can give organization members, outside collaborators, and teams of people different levels of access to repositories owned by an organization. 
Each permission level progressively increases access to a repository's content and settings. 
Choose the level that best fits each person or team's role in your project without giving people more access to the project than they need.

From least access to most access, the permission levels for an organization repository are:

* Read: Recommended for non-code contributors who want to view or discuss your project
* Triage: Recommended for contributors who need to proactively manage issues and pull requests without write access
* Write: Recommended for contributors who actively push to your project
* Maintain: Recommended for project managers who need to manage the repository without access to sensitive or destructive actions
* Admin: Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repository

Setting base permissions
++++++++++++++++++++++++
You can set base permissions for the repositories that an organization owns.

Organization owners can set base permissions for an organization.

You can set base permissions that apply to all members of an organization when accessing any of the organization's repositories. Base permissions do not apply to outside collaborators.

By default, members of an organization will have Read permissions to the organization's repositories.

If someone with admin permissions to an organization's repository grants a member a higher level of permission for the repository, the higher level of permission overrides the base permission.

Go to **Profile -> Organizations (on bottom left) -> Settings -> Member privileges**

Accessing the audit log
-----------------------
The audit log lists actions performed within the last 90 days. Only owners can access an organization's audit log.

Go to **Profile -> Organizations (on bottom left) -> Settings -> Audit log**


About teams
===========
:term:`Teams` are groups of organization members that reflect your company or group's structure with cascading access permissions and mentions.

Organization owners and team maintainers can give teams admin, read, or write access to organization repositories. 
Organization members can send a notification to an entire team by mentioning the team's name. 
Organization members can also send a notification to an entire team by requesting a review from that team. 
Organization members can request reviews from specific teams with read access to the repository where the pull request is opened. 
Teams can be designated as owners of certain types or areas of code in a :term:`CODEOWNERS` file.

Team visibility
---------------
Teams can be visible or secret:

* Visible teams can be viewed and @mentioned by every organization member.
* Secret teams are only visible to the people on the team and people with owner permissions. They're great for hiding teams with sensitive names or members, such as those used for working with external partners or clients. Secret teams cannot be nested under parent teams or have child teams.

Nested teams
------------
You can reflect your group or company's hierarchy within your GitHub organization with multiple levels of nested teams. 
A parent team can have multiple child teams, while each child team only has one parent team. You cannot nest secret teams.

Child teams inherit the parent's access permissions, simplifying permissions management for large groups. 
Members of child teams also receive notifications when the parent team is @mentioned, simplifying communication with multiple groups of people.

For example, if your team structure is **Employees > Engineering > Application Engineering > Identity**, granting Engineering write access to a repository means Application Engineering and Identity also get that access. 
If you @mention the Identity Team or any team at the bottom of the organization hierarchy, they're the only ones who will receive a notification.

Create/Delete a team
--------------------

To create
+++++++++
Go to **Profile -> Organizations (on bottom left) -> Teams -> New Team**

To delete
+++++++++
Go to **Profile -> Organizations (on bottom left) -> Teams -> Select Team -> Delete (from dropdown)**


Add/Remove members to a team
----------------------------

To Add
++++++
Go to **Profile -> Organizations (on bottom left) -> Teams -> Select Team -> Members -> Add a member**

To Remove
+++++++++
Go to **Profile -> Organizations (on bottom left) -> Teams -> Select Team -> Members -> Select member -> Remove from team (from dropdown)**
