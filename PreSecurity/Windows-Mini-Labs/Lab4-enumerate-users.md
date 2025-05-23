# Lab 4 – Enumerate Users and Privilege Escalation

## Objective

Demonstrate how privilege escalation can occur using basic Command Prompt tools. Enumerate existing users and administrator group members, then simulate privilege escalation by adding and removing a test user from the Administrators group. Capture before/after states.

- Run the following commands in Command Prompt:
  - `net user`
  - `net localgroup administrators`
- Add a test user to the Administrators group
- Remove the user afterward
- Document and screenshot before and after states

## Steps Taken

1. Enumerated local users  
- Ran `net user` to display all local users on the system.
- This command lists both system and manually created accounts.
- Example output included: ``Administrator``, ``Admin``, ``Test_User``.
2. Checked Administrators group members
- Used `net localgroup administrators` to see which users currently have admin rights.
- The list included default ``Administrator`` account and `Admin` account created by me, before the escalation.
3. Added `Test_User` to Administrators group
- Ran the command:
`net localgroup administrators testuser /add`
- Verified that `Test_User` now appeared in the admin group.
4. Removed `Test_User` from Administrator group.
- Used the command:
`net localgroup administrators testuser /delete`
- Confirmed removal by re-running `net localgroup administrators`.


## Evidence

Before Privilege Escalation:

`net user` command output showing all accounts:

<img src="../images/net_user.png" width="800" />

`net localgroup administrators` without `Test_User`:

<img src="../images/net_localgroup_admins_no.png" width="800" />

After Adding to Admins:

`net localgroup administrators` showing `Test_User` after add

<img src="../images/net_localgroup_add.png" width="800" />

After Removing:

`net localgroup administrators` after removing the test user:

<img src="../images/net_localgroup_delete.png" width="800" />


# Findings

- Users can easily be added or removed from privileged groups via command line.
- If a user gains local access and is not monitored, they may escalate privileges this way.
- This type of privilege escalation is basic but effective, especially if system auditing is not enabled.
- Any user group change should be logged and monitored.

# Relevance for SOC Analyst

- Group membership changes should be logged and reviewed regularly.
- In Event Viewer, group changes appear under Security log, Event ID 4728 (user added to group) and 4729 (user removed).
- Privilege escalation is a common technique in post-exploitation phases.
- Monitoring these changes can help detect insider threats or compromised accounts.