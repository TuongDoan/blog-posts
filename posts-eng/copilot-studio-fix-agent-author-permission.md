---
type: Post
title: "Guide - Granting Users Access to Create and Manage Copilot Studio Agents"
description: >-
    Encountering permission issues in Copilot Studio? This guide walks you through the steps to ensure you and your team have the access needed to create and manage agents
date: '2025-09-01'
tag: Copilot Studio, AI, Agent, Governance, Power Platform
---
<img width="631" height="235" alt="Screenshot 2025-09-01 at 10 23 38 AM" src="https://github.com/user-attachments/assets/d20602c0-f8a8-4390-80e7-f258e238e7fe" />

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
<img width="800" height="524" alt="Screenshot 2025-09-02 at 12 47 16 AM" src="https://github.com/user-attachments/assets/2b941a2b-bcc8-44a9-8d86-b3233d47b5c4" />


3.  A side panel will pop up. Pick a security group. Anyone in that group will now be able to create and manage agents.
<img width="506" height="681" alt="Screenshot 2025-09-01 at 11 46 09 PM" src="https://github.com/user-attachments/assets/5b0d7799-9fe3-4a4e-ac8d-3822bb51f9a2" />


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
<img width="800" height="631" alt="Screenshot 2025-09-01 at 11 50 11 PM" src="https://github.com/user-attachments/assets/d108302e-777a-4e2e-be70-5dc01e2f2d37" />


    * Here's a closer look at the tenant license details:*
<img width="1094" height="418" alt="Screenshot 2025-09-02 at 12 52 41 AM" src="https://github.com/user-attachments/assets/68a94a3f-4a01-4fe5-b886-efca825e6c5a" />


5.  After that, find the **Microsoft Copilot Studio User License** under **"Add-ons"** section as showed in the picture above. "Buy" as many of these licenses as you need. It's free ($0)

6.  Finally, go to **Users** > **Active users**, pick the people you want to give access to, and assign them the **Microsoft Copilot Studio User License**.

---

> If your company works with a Cloud Solution Provider (CSP), you'll need to talk to your CSP partner to get the right Azure subscription or message packs set up.
