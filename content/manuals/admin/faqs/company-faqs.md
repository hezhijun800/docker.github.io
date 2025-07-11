---
title: FAQs on companies
linkTitle: Company
weight: 30
description: Company FAQs
keywords: Docker, Docker Hub, SSO FAQs, single sign-on, company, administration, company management
tags: [FAQ]
aliases:
- /docker-hub/company-faqs/
- /faq/admin/company-faqs/
---

### Are existing subscriptions affected when you create a company and add organizations to it?

You can manage subscriptions and related billing details at the organization level.

### Some of my organizations don’t have a Docker Business subscription. Can I still use a parent company?

Yes, but you can only add organizations with a Docker Business subscription to a company.

### What happens if one of my organizations downgrades from Docker Business, but I still need access as a company owner?

To access and manage child organizations, the organization must have a Docker Business subscription. If the organization isn’t included in this subscription, the owner of the organization must manage the organization outside of the company.

### Does my organization need to prepare for downtime during the migration process?

No, you can continue with business as usual.

### How many company owners can I add?

You can add a maximum of 10 company owners to a single company account.

### Do company owners occupy a subscription seat?

Company owners do not occupy a seat unless one of the following is true:

- They are added as a member of an organization under your company
- SSO is enabled

Although company owners have the same access as organization owners across all
organizations in the company, it's not necessary to add them to any
organization. Doing so will cause them to occupy a seat.

When you first create a company, your account is both a company owner and an
organization owner. In that case, your account will occupy a seat as long as
you remain an organization owner.

To avoid occupying a seat, [assign another user as the organization owner](/manuals/admin/organization/members.md#update-a-member-role) and remove yourself from the organization.
You'll retain full administrative access as a company owner without using a
subscription seat.

### What permissions does the company owner have in the associated/nested organizations?

Company owners can navigate to the **Organizations** page to view all their nested organizations in a single location. They can also view or edit organization members and change single sign-on (SSO) and System for Cross-domain Identity Management (SCIM) settings. Changes to company settings impact all users in each organization under the company. For more information, see [Roles and permissions](../../security/for-admins/roles-and-permissions.md).

### What features are supported at the company level?

You can manage domain verification, SSO, and SCIM at the company level. The following features aren't supported at the company level, but you can manage them at the organization level:

- Image Access Management
- Registry Access Management
- User management
- Billing

To view and manage users across all the organizations under your company, you can [manage users at the company level](../../admin/company/users.md) when you use the [Admin Console](https://app.docker.com/admin).

Domain audit isn't supported for companies or organizations within a company.

### What's required to create a company name?

A company name must be unique to that of its child organization. If a child organization requires the same name as a company, you should modify it slightly. For example, **Docker Inc** (parent company), **Docker** (child organization).

### How does a company owner add an organization to the company?

You can add organizations to a company in the Admin Console. For more information, see [Add organizations to a company](../../admin/company/organizations.md#add-organizations-to-a-company.md).

### How does a company owner manage SSO/SCIM settings for a company?

See your [SCIM](scim.md) and [SSO](../../security/for-admins/single-sign-on/configure/_index.md) settings.

### How does a company owner enable group mapping in an IdP?

See [SCIM](scim.md) and [group mapping](../../security/for-admins/provisioning/group-mapping.md) for more information.

### What's the definition of a company versus an organization?

A company is a collection of organizations that are managed together. An organization is a collection of repositories and teams that are managed together.
