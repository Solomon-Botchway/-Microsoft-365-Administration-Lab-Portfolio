## Self-Service Password Reset (SSPR)

Implemented and tested Microsoft Entra Self-Service Password Reset (SSPR) using targeted group-based deployment.

### Configuration

Enabled SSPR for:

```text
FIN-Team-M365
```

rather than all users to allow phased rollout and testing.

### Testing Performed

#### User Outside Scope

Tested using an HR user account.

Result:

```text
Password reset isn't turned on for your account.
```

Validation:

- Confirmed policy scoping worked correctly.
- Verified non-targeted users were unable to use SSPR.

#### User Inside Scope

Tested using a Finance user account.

Result:

```text
You haven't registered for password reset.
```

Validation:

- Confirmed Finance user was correctly targeted.
- Confirmed registration prerequisite enforcement.

#### Support Notification Workflow

Generated password reset assistance requests.

Verified notification delivery to:

- Helpdesk Administrator
- IT-Team-M365 Support Group


### Key Learning Outcomes

- SSPR can be targeted to specific groups.
- SSPR requires authentication method registration.
- Users outside policy receive different experiences than users inside policy.
- Password reset requests can integrate with support workflows.
- Group-based deployment supports phased security rollouts.

## Finance Team Member - Set for SSPR
- <img width="1309" height="628" alt="image" src="https://github.com/user-attachments/assets/80f2dfde-a77c-4f82-ac5f-f93c68836441" />

## HR Team Member - Not Set for SSPR
<img width="927" height="576" alt="image" src="https://github.com/user-attachments/assets/300392a5-d11a-48e9-b41a-7941f369ce1e" />

## Email to HelpDesk and IT Team - for manual reset
<img width="1908" height="757" alt="image" src="https://github.com/user-attachments/assets/f8f1bf08-ebfb-4380-a75f-97ac1962cfba" />
