# Activity 2: Creating Support Queues

## 1. Overview
Queues allow groups of support team members to manage a shared extraction workload. This configuration establishes distinct queues for specialized handling of technical product errors.

## 2. Damage Support Queue Setup
1. Navigate to **Setup** -> search for **Queues** in Quick Find -> click **New**.
2. **Queue Label:** `Damage Support Queue`
3. **Queue Name:** `Damage_Support_Queue`
4. **Supported Objects:** Select `User Case` (or Case) from Available Objects and move to Selected Objects.
5. **Queue Members:** Under Search dropdown, select `Users`. Locate designated responders (e.g., user `panther`) and shift them to Selected Members.
6. Click **Save**.

## 3. Warranty Support Queue Setup
1. Click **New** on the Queue dashboard.
2. **Queue Label:** `Warranty Support Queue`
3. **Queue Name:** `Warranty_Support_Queue`
4. **Supported Objects:** Select `User Case` (or Case) and move to Selected Objects.
5. **Queue Members:** Select `Users` -> locate designated responders (e.g., user `panther`) -> add to Selected Members.
6. Click **Save**.