---
type: Post
title: "Guide - Granting Users Access to Create and Manage Copilot Studio Agents"
description: >-
    Encountering permission issues in Copilot Studio? This guide walks you through the steps to ensure you and your team have the access needed to create and manage agents
date: '2025-09-01'
tag: Copilot Studio, AI, Agent, Governance, Power Platform
---

![Error message showing insufficient permissions to create a copilot](./images/copilot-studio-permission-error.png)

Ever get that error message when publishing an agent, or you don't even have the right to create one? It means you don't have the right permissions. Let's walk through how to fix it!

## Why Can't I Create/Manage an Agent?

In Copilot Studio, how you get permission to build an agent depends on your tenant's billing setup. There are two main setups:

1.  **Pay-As-You-Go (via Azure)**: This setup uses a role called **Copilot Studio authors** in the Power Platform admin center.
2.  **Capacity-based (Message Packs)**: This setup involves buying licenses from the Microsoft 365 admin center.

Figure out which one your org uses, and then follow the steps below.

>Please make sure that you have the right privileges to perform the actions below; otherwise, ask your IT team


---

### Option 1: For Pay-As-You-Go (Azure) Setups

If your environment is on a Pay-As-You-Go plan tied to an Azure subscription, getting access is pretty straightforward. You just need to be added to the **Copilot Studio authors** role.

1.  Head over to the **Power Platform admin center** and open the [Tenant settings](https://admin.powerplatform.microsoft.com/manage/tenantsettings) page.

2.  Find and click on **Copilot Studio authors** in the list.

    ![Screenshot of Tenant settings with Copilot Studio authors highlighted](./images/ppac-tenant-settings.png)

3.  A side panel will pop up. Pick a security group. Anyone in that group will now be able to create and manage agents.

    ![Screenshot of the Copilot Studio authors side panel for assigning a security group](./images/ppac-assign-security-group.png)

Once that's saved, you and your team should be good to go!

---

### Option 2: For License Pack Setups

If your organization uses message packs, you'll need to obtain two different licenses:

1.  **A tenant-level Copilot Studio License (Message Pack)**: This is the main license for the whole tenant.
2.  **A user-level Copilot Studio License**: This is a free ($0) add-on that needs to be assigned to every person who will be building agents.

Here’s how to get them set up:

1.  Go to the **Purchase services** area in the [Microsoft 365 admin center](https://admin.cloud.microsoft/?#/catalog) <= click here

2.  Search for "Copilot Studio" to see the licenses.

3.  Grab the main **Microsoft Copilot Studio** tenant license.

    ![Screenshot of the Microsoft Copilot Studio tenant license in the M365 admin center](./images/m365-tenant-license.png)

    *Here's a closer look at the tenant license details:*
    ![Screenshot showing details of the tenant license](./images/m365-tenant-license-details.png)

4.  After that, find the **Microsoft Copilot Studio User License**. "Buy" as many of these licenses as you need. It's free ($0), but you still need to assign it.

5.  Finally, go to **Users** > **Active users**, pick the people you want to give access to, and assign them the **Microsoft Copilot Studio User License**.

---

> If your company works with a Cloud Solution Provider (CSP), you'll need to talk to your CSP partner to get the right Azure subscription or license packs set up.