---
author: josaw1
description: This topic explains how to configure user access for payment service provider (PSP) roles in Microsoft Dynamics 365 Fraud Protection.
ms.author: josaw
ms.date: 01/27/2022
ms.topic: conceptual
search.app: 
  - Capaedac-fraudprotection
search.audienceType:
  - admin
title: User roles and access (PSPs)

---

# User roles and access (PSPs)

[!include [preview banner](includes/preview-banner.md)]

Payment service providers (PSPs) can grant users of Microsoft Dynamics 365 Fraud Protection various levels of access, based on logical or functional roles.

## Assign PSP roles

Users are managed through your assigned Azure Active Directory (Azure AD) tenant.

Roles can be assigned to either of the following types of users:

- Users inside the organization's Azure tenant
- Users outside the organization's Azure tenant, who will be invited to join the tenant as guest users

> [!IMPORTANT]
> Users inside the organization's Azure tenant who are member users can view a list of all other users in the tenant. By contrast, users outside the tenant who join as guest users can view only users who are in the same Fraud Protection environment that they have access to. Assign member or guest roles to user according to your business privacy requirements.

For more information about how to directly add users to your Azure AD tenant as members or non-guest users, see [Create a user account in Azure Active Directory](/azure/active-directory/manage-apps/add-application-portal-assign-users#create-a-user-account).

### Assign PSP roles to users in Fraud Protection

To assign PSP roles to users in Fraud Protection, follow these steps.

1. Open the Fraud Protection portal page.
1. In the left navigation pane, select **Settings**, and then select **User access**.
1. Select **Assign role(s)**.
1. Enter the name or email address of the person or group that you want to assign a Fraud Protection PSP role to.

    > [!NOTE]
    > In the Azure tenant, suggestions for users will appear while you type. Select a suggestion if it matches the user that you want to assign a user role to. Otherwise, a message informs you that an invitation email will be sent to the person or group that you entered, so that the person or group can join the Fraud Protection environment.

1. In the **Roles** field, select one or more defined roles that you want to assign to the user.
1. Select **Assign role(s)**.

> [!NOTE]
> Users outside the Azure tenant will join the tenant as guest users and will appear in the **User access** grid after they accept the invitation that is emailed to them and complete the sign-in/sign-up process.

### Edit assigned roles

To edit the role that is assigned to a user in Fraud Protection, select the user in the member list, and then select **Edit**.

In this part of the page, roles can be added to or deleted from a user. If you edit your own account (for example, if you delete your own administrative role), your edits might interfere with your ability to use some features of Fraud Protection. If you must restore permissions, you can reset them in the [Azure portal](https://portal.azure.com/#home).

To learn more about the available PSP roles, see the [PSP user roles and access](psp-user-roles.md#psp-user-roles-and-access) section of this topic.

### Revoke user access to the environment

To revoke a user's access to the current environment, select the user in the member list, and then select **Revoke access**.

> [!IMPORTANT]
> When you revoke access for a user, the user is removed from the current environment. However, they might still have access to other environments in the hierarchy. To fully remove a user's access to Fraud Protection, [delete the user from your Azure AD tenant](/azure/active-directory/fundamentals/add-users-azure-active-directory#delete-a-user). In this way, you completely remove the user's access to your tenant and its associated applications or services.

## PSP user roles and access

Fraud Protection offers a defined set of user roles, each of which has access to specific features and functions. You can select the features and functions when you assign a user to the system.

<table>
<thead>
<tr>
<th>Section</th>
<th>Sub-page (tab)</th>
<th>PSP Admin</th>
<th>Fraud Manager</th>
<th>Fraud Supervisor</th>
<th>Fraud Analyst</th>
<th>Manual Review Agent</th>
<th>Technical Developer</th>
<th>Customer Service Support</th>
<th>Reporting</th>
</tr>
</thead>
<tbody>
<td rowspan="2">Purchase</td>
<td>Summary</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td>Transaction Search</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read only/View only</td>
<td>Read/Write</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Rules</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read only/View only</td>
<td>Read only/View only</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Velocities</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read only/View only</td>
<td>Read only/View only</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td rowspan="2">Lists</td>
<td>Custom</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read only/View only</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td>Support</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read only/View only</td>
<td>*Write only</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">External calls</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Manual review</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Graph explorer</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Event tracing</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
<td>Read/Write</td>
</tr>
<tr>
<td colspan="2">Data upload</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td rowspan="2">API Management</td>
<td>API requests</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td>Errors</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td rowspan="3">Integration</td>
<td>Dashboard</td>
<td>Read only/View only</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>Read only/View only</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td>AAD Apps*</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td>Device Fingerprinting</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Subscription</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">User access</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Subject requests</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
<tr>
<td colspan="2">Transaction Acceptance Booster</td>
<td>Read/Write</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
<td>No access</td>
</tr>
</tbody>
</table>

\* To create an Azure AD application, the user who is assigned the **PSP Admin** or **Technical Developer** role must also be assigned the **Application Administrator**, **Cloud Application Administrator**, or **Global Administrator** role in your Azure tenant.

The following roles are available for PSP users:

- **PSP Admin** – This role is a high-level administrative account that has full access to all PSP-related features. A user in this role can manage Fraud Protection for a PSP and its merchant customers.
- **Fraud Manager** – This role is an internal role in a PSP. A user in this role is intended to manage Fraud Protection for the PSP's merchant customers.
- **Fraud Supervisor** – This role provides the highest level of authority in a PSP's merchant customer. A user in this role can access merchant-facing functions that the PSP delegates to them.
- **Fraud Analyst** – This role is intended for a PSP's merchant customer who will run analysis and reports. A user in this role has read-only access to the merchant customer's data.
- **Manual Review Agent** – A user in this role is responsible for reviewing individual transactions and approving or declining them. Although manual review agents don't have direct access to the **Support Lists** page, they can modify the status of an entry in the support list through the **Transaction Search** page.
- **Technical Developer** – A user in this role is responsible for managing the technical configurations and integrations of a Fraud Protection instance for a PSP.
- **Customer Service Support** – A user in this role can view the transaction details and is provided with information that is required to handle customer queries.
- **Reporting** – This role provides access to event tracing only, to enable Fraud Protection events and data to be consumed into the PSP's internal reporting infrastructure. 

### Member access

Members can access Fraud Protection by visiting [https://dfp.microsoft.com/](https://dfp.microsoft.com/) and using a Microsoft account to sign in.

### Guest user access

Guest users can access Fraud Protection after they accept an email invitation and sign up (or sign in).

To accept an invitation to Fraud Protection, follow these steps.

1. Check your email inbox for an email that has the subject line "\<Name\> invited you to access applications within their organization."
1. Select **Accept invitation**.
1. If an existing Microsoft account or related account uses your email address, you're prompted to use that account to sign in. Otherwise, follow the setup process to sign up for a new account. After you're fully signed in, you should have access to Fraud Protection.
1. Return to the invitation email, and write down or bookmark the exact link that appears after the text "If you accept this invitation, you will be sent to...." This link will be in the format `https://dfp.microsoft.com/.../...`. Each time that you access Fraud Protection, you must use this exact link.

## Additional resources

[Configure user access](configure-user-access.md)

[Create a user account in Azure Active Directory](/azure/active-directory/manage-apps/add-application-portal-assign-users#create-a-user-account)

[Assign a user account to an enterprise application](/azure/active-directory/manage-apps/add-application-portal-assign-users#assign-a-user-account-to-an-enterprise-application)


[!INCLUDE[footer-include](includes/footer-banner.md)]
