---
title: Cross-account audience sharing
---

<aside><p>This feature is currently in limited beta release. The workflows detailed below are subject to change as additional features are added.</p>
<p>Also note that this feature is intended to facilitate controlled sharing of audience data within a single organization. If you want to share audiences outside of your organization, see <a href="/guides/platform-guide/audiences/#audience-sharing">our main Audience Sharing docs</a></p></aside>

The cross-account audience sharing feature allows you to share audience data between accounts within your organization and offers detailed control over exactly what data is shared. 

You can choose to share audience data broadly within your organization, or to provide access to only as much data as is needed for a campaign.

## Audience sharing permissions

Permissions allow the account which owns an audience to define what data is shared with any receiving accounts.

Permissions can be set per-audience for each account in your organization.

| Permission level | Access details
| --------- | --------
| **Owner** | The account that created and maintains the audience. This account has full access to the audience, can connect it to an output and update the audience definition. Users with admin-level access to this account can also set the permission level allowed to other accounts.
| **Private** | The audience is not visible from the receiving account
| **View only** | The audience is visible from the receiving account but cannot be connected to any audience outputs.
| **Usable** | The audience is visible from the receiving account and can be connected to any audience output, but the audience definition cannot be edited.

### Example

* The mParticle organization has two accounts: mPTravel and mPDine. Cross-account audience sharing is enabled.
* mPTravel sets the following audience-level sharing permissions:
  * The "Potential Parisians" audience is private from mPDine.
  * The "Aspiring Athenians" audiece is view only for mPDine.
  * The "Ibiza Dreamers" audience is "usable" for mPDine.
* A user in the mPDine account will be able to:
  * See the "Aspiring Athenians" and "Ibiza Dreamers" audiences in their **Audiences** view.
  * Connect the "Ibiza Dreamers" audience to an audience output.

## Audience Owner

### Create default audience-level permissions

From your Settings page, navigate to the **Audience Settings** tab. From here you can view and edit current default audience-level sharing settings or add new defaults.

![](/images/audience-sharing-default-permission.png)

Note that any changes to your defaults will _only_ be applied to any new audience created. Changing your defaults won't update existing sharing settings for current audiences.

### See which Audiences are shared

View and edit the sharing settings for each audience from the main **Audiences** view.

![](/images/audience-sharing-list-view.png)

### Update sharing permissions for an audience

Any edits you make to the sharing settings of a specific audience will take precedence over your account defaults.

![medium](/images/audience-sharing-audience-permissions.png)

### Respond to an access request

Users of an account with "view only" access are able to submit a request for additional access. A notification email is sent to the creator of the audience. If you choose to grant the request you can update the audience permissions [as above](#update-sharing-permissions-for-an-audience). You can also seek clarification from the requester by replying to the email.

## Audience Receiver

### See which Audiences are shared

You can access all audiences that are shared with you via the **Shared with me** tab of the **Audiences** page. The **Access** column shows the level of access your account as been granted.

![](/images/audience-sharing-receiver-list.png)

### Request 'usable' access for a 'view only' audience

If you have "view only" access for an audience, you can request a different level of access.

![](/images/audience-sharing-request.png)

To make a request you must provide:

* The sharing level you are requesting.
* The date range of the campaign you are proposing.
* Details of the proposed campaign.
* Activation details, including the proposed campaign platforms.

![](/images/audience-sharing-request-details.png)

The owner of the audience will be automatically notified of your request by email and may request further details by email reply.

## Identity-level permissions

In addition to setting access permission for each audience, you can choose whether or not to make each identity type available to each account when you share audiences. 

For example, you can choose to make Google Advertising ID and Apple IDFA available to a particular account, but email unavailable. These settings are at the account level and apply to all audiences shared from the account.

Only users with Admin access can manage identity-level permissions.

1. Navigate to your **Settings** page.  
  ![medium](/images/audience-sharing-account-settings.png)
2. Naviagte to the **Identity Settings** tab and scroll to the **Identity Sharing** heading. From here you can see how many accounts have been granted permission to receive each identity type, and add new permissions.
  ![](/images/audience-sharing-id-level.png)
3. For each identity type, you can view a list of current permissions and add or update permissions by account.
  ![medium](/images/audience-sharing-id-permission.png)