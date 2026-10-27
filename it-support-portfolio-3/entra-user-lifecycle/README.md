# Entra user lifecycle — Lab, completed Oct 26, 2026

- Microsoft Entra ID Free tenant
- Lab only, no production users, no paid services, all data practice
- Tenant IDs, domains, and passwords omitted on purpose

## Practice company
- Northline HVAC, 12 practice users, 3 Security groups, Assigned membership
- Office: billing and schedules, no payroll
- Technicians: job sheets only
- Dispatch: assign jobs and schedules, no payroll
- Access by group, not person by person — change the group, change the access

## Joiner
- Created a practice user account, Maya Chen, with a company login and a temporary password, account enabled
- Assigned the user to the Office group
- Verified: Office members listed the user, total users went from 1 to 2

## Mover
- Moved the same user from Office to Dispatch
- Same login kept, group membership changed
- Verified: Office no longer listed the user, Dispatch did
- Result: billing access lost, dispatch access gained, no account recreation

## Password reset
- Reset the password to a new temporary password, change required on next sign-in
- Old password stopped working, new password set by the user on next login
- MFA re-register procedure documented: force fresh MFA setup if a user loses their phone, applicable only if MFA was enrolled

## Leaver
- Blocked sign-in on the same day — account enabled off
- Removed the user from Dispatch
- Verified: user showed as blocked/disabled, Dispatch no longer listed the user
- Account left blocked, not deleted, to preserve the record for audit

## Not included
- No Microsoft 365 licences, no mailbox administration
- No Conditional Access, no Lifecycle Workflows — not in Entra ID Free
- No paid Azure services, no pay-as-you-go upgrade
- Full practice company list: practice-company-note.md
