---
title: Console Audit Logging
summary: Learn about the log auditing feature for the TiDB Cloud Console.
---

# Console Audit Logging

Console audit log is a capability provided by TiDB Cloud. It is used to track various behaviors and operations of users on the console. For example: log in to the TiDB Cloud console, create a cluster, etc.

## Prerequisites

- You are the owner of your organization in TiDB Cloud. Otherwise, you cannot see the audit-related options in the TiDB Cloud console. For more information, see [Manage role access](/tidb-cloud/manage-user-access.md#manage-role-access).
- You can only enable and disable the console audit log for your organization. You can only track the actions of users in your organization.
- After the audit log is enabled, all event types will be recorded, and you cannot specify auditing filter rules.

## Enable console audit log

You can enable the console audit log function.

1. Click <MDSvgIcon name="icon-top-organization" /> **Organization** in the upper-right corner of the TiDB Cloud console.
2. Click **Console Audit Log**. The Console Audit Log management page is displayed by default.
3. Click **Enable console audit log**. Or click **Setting** in the upper-right corner and enable Console audit log in the pop-up window

## Disable console audit log

You can disable the console audit log function.

1. Click <MDSvgIcon name="icon-top-organization" /> **Organization** in the upper-right corner of the TiDB Cloud console.
2. Click **Console Audit Log**. The Console Audit Log management page is displayed by default.
3. Click **Setting** in the upper-right corner and disable Console audit log in the pop-up window

## View console audit logs

You can only view the console audit log information of your organization. 

1. Click <MDSvgIcon name="icon-top-organization" /> **Organization** in the upper-right corner of the TiDB Cloud console.
2. Click **Console Audit Log**. The Console Audit Log management page is displayed by default. You can view the latest console audit log information of your organization.
3. Click **Type** tab. You can filter the console audit log information you need to view according to the event type.
4. Click **Result** tab. You can filter the console audit log information you need to view according to the event result.
5. Click **All time** tab. You can filter the console audit log information you need to view according to the time period when the event occurred.
6. Click **Advanced filter**  tab. You can filter the console audit log information you need to view according to other fields.

## Export console audit logs

You can export the console audit log information of your organization. 

1. Click <MDSvgIcon name="icon-top-organization" /> **Organization** in the upper-right corner of the TiDB Cloud console.
2. Click **Console Audit Log**. The Console Audit Log management page is displayed by default.
3. If you need to export a specific part of console audit logs, you can filter through various conditions. Otherwise, skip this step.
4. Click **Export** tab. You can choose to download the selected console audit log information in JSON or CSV format.

## Console audit log storage policy

The storage time is 90 days, after which the console audit logs will be automatically cleaned up.

> **Note:**
>
> Console audit log temporarily does not support users to set the storage location of logs.

## Console audit event type description

Various user activities on the TiDB Cloud console are recorded in the console audit log. The console audit log covers the following event types:

| Console audit event type | Description |
|---|---|
| CreateOrganization | Create an organization |
| LoginOrganization | User logs into organization |
| SwitchOrganization | User switches out from current organization |
| LogoutOrganization | User logs out from organization |
| InviteUserToOrganization | Invite a user to join the organization |
| DeleteInvitationToOrganization | Delete a user's invitation to join the organization |
| ResendInvitationToOrganization | Resend the invitation to join the organization for a user |
| ConfirmJoinOrganization | The invited user confirms joining the organization |
| DeleteUserFromOrganization | Delete a joined user from the organization |
| UpdateUserRoleInOrganization | Update a user's role in the organization |
| CreateAPIKey | Create an API Key |
| EditAPIKey | Edit an API Key |
| DeleteAPIKey | Delete an API Key |
| UpdateTimezone | Update your organization's time zone |
| ShowBill | Show organization bill  |
| DownloadBill | Download organization bill |
| ShowCredits | Show organization credits |
| AddPaymentCard | Add a payment card |
| UpdatePaymentCard | Update a payment card |
| DeletePaymentCard | Delete a payment card |
| SetDefaultPaymentCard | Set default payment card |
| EditBillingProfile | Edit billing profile information |
| ContractAction | Organizing contract-related activities |
| EnableConsoleAuditLog | Enable console audit log |
| ShowConsoleAuditLog | Show console audit log |
| InviteUserToProject | Invite a user to join the project |
| DeleteInvitationToProject | Delete a user's invitation to join the project |
| ResendInvitationToProject | Resend the invitation to join the project for a user |
| ConfirmJoinProject | The invited user confirms joining the project |
| DeleteUserFromProject | Delete a joined user from the project |
| CreateProject | Create a project |
| CreateProjectCIDR | Create a new project CIDR |
| CreateAWSVPCPeering | Create an AWS VPC Peering |
| DeleteAWSVPCPeering | Delete an AWS VPC Peering |
| CreateGCPVPCPeering | Create a GCP VPC Peering |
| DeleteGCPVPCPeering | Delete a GCP VPC Peering |
| CreateAWSPrivateEndPoint | Create AWS private endpoint |
| EditAWSPrivateEndPoint | Edit AWS private endpoint |
| DeleteAWSPrivateEndPoint | Delete AWS private endpoint |
| SubscribeAlerts | Subscribe alerts |
| UnsubscribeAlerts | Unsubscribe alerts |
| CreateDatadogIntegration | Create datadog integration |
| DeleteDatadogIntegration | Delete datadog integration |
| CreateVercelIntegration | Create vercel integration |
| DeleteVercelIntegration | Delete vercel integration |
| CreatePrometheusIntegration | Create prometheus integration |
| DeletePrometheusIntegration | Delete prometheus integration |
| CreateCluster | Create a cluster |
| DeleteCluster | Delete a cluster |
| PauseCluster | Pause a cluster |
| ResumeCluster | Resume a cluster |
| ScaleCluster | Scale a cluster |
| DownloadTiDBClusterCA | Download TiDB cluster CA certificate |
| OpenWebSQLConsole | Connect to TiDB Cluster through Web SQL |
| SetRootPassword | Set the root password of TiDB cluster |
| UpdateIPAccessList | Update the IP access list of TiDB cluster |
| DeleteAccessList | Delete the IP access list of TiDB cluster |
| SetAutoBackup | Set the automatic backup mechanism of TiDB cluster |
| DoManualBackup | Do manual backup of TiDB cluster |
| DeleteBackupTask | Delete backup task |
| DeleteBackup | delete backup file |
| RestoreFromBackup | Restore to TiDB cluster based on the backup file |
| RestoreFromTrash | Restore to TiDB cluster based on the backup files in the trash |
| ImportDataFromAWS | Import data from AWS |
| ImportDataFromGCP | Import data from GCP |
| CreateMigrationJob | Create migration job |
| SuspendMigrationJob | Suspend migration job |
| ResumeMigrationJob | Resume migration job |
| DeleteMigrationJob | Delete migration job |
| ShowDiagnose | Show diagnose information |
| DBAuditLogAction | Set the activity of database audit log |
| AddDBAuditFilter | Add database audit log filter |
| DeleteDBAuditFilter | Delete database audit log filter |
| EditProject | Edit a project's information |
| DeleteProject | Delete a project |
| BindSupportPlan | Bind support plan |
| CancelSupportPlan | Cancel support plan |
| UpdateOrganizationName | Update organization name |
| CreatePrivateEndpointService | Create private endpoint service |
| DeletePrivateEndpointService | Delete private endpoint service |

## Console audit log field description

For the console audit log, each event record needs to be clear and complete to ensure that the information is sufficient to track user activities. TiDB Cloud provides the following fields:

| Field name | Data type | Description |
|---|---|---|
| type | string | Event type |
| ends_at | timestamp | Event time |
| operator_type | enum | Operator type: user, api_key |
| operator_id | uint64 | Operator ID |
| operator_name | string | Operator name |
| operator_ip | string | Operator's IP address |
| operator_login_method | enum | Operator's login method: google, github, email, api_key |
| org_id | uint64 | Organization ID to which the event belongs |
| org_name | string | Organization name to which the event belongs |
| project_id | uint64 | Project ID to which the event belongs |
| project_name | string | Project name to which the event belongs |
| cluster_id | uint64 | Cluster ID to which the event belongs |
| cluster_name | string | Cluster name to which the event belongs |
| trace_id | string | Trace ID of the request initiated by the operator |
| result | enum | Event result: success, failure |
| details | json | Detailed description of the event |
