# Create Prompt Template (Agentforce & Prompt Builder)

## Overview
This document outlines the steps to enable Salesforce Einstein (Agentforce) and configure a Prompt Template. This setup allows the system to use Generative AI to automatically read record data and generate professional inspection summaries.

---

## Step 1: Enable Einstein (Agentforce)
Before creating prompt templates, generative AI features must be enabled in the org.
1. Click the **Gear Icon** → Select **Setup**.
2. In the Quick Find box, search for **Einstein Setup**.
3. Click on **Einstein Setup**.
4. Toggle **Turn on Einstein** to the active (On) position.
5. *Refresh the page after enabling Einstein.*

---

## Prerequisite: Create AI Summary Field
Before selecting the target field in Prompt Builder, you must create a dedicated Long Text Area field to store the AI-generated output.
1. Click the **Gear Icon** → **Setup**.
2. In Quick Find, search for **Object Manager**.
3. Select the target object: **User Case**. *(Note: Ensure you are on the User Case object as defined in your architecture)*.
4. Click **Fields & Relationships** → **New**.
5. Select **Long Text Area** → Click **Next**.
6. **Field Label:** `Ai Summary`
7. **API Name:** Auto-populates as `Ai_Summary__c`
8. **Set Length:** `32000` and **Visible Lines:** `5-10`.
9. Click **Next** → **Save**.

---

## Step 2: Open Prompt Builder
1. In the Quick Find box, search for **Prompt Builder**.
2. Click **Prompt Builder**.
3. Click the **New Prompt Template** button in the top right corner.

---

## Step 3: Select Prompt Type
1. **Prompt Template Type:** Choose **Field Generation** from the dropdown menu. This allows the AI to generate content specifically for the field we created.

---

## Step 4: Enter Details
Fill in the configuration details for the new template:
* **Label Name:** `MetaDataInspection`
* **API Name:** Auto-populates.
* **Object:** User Case
* **Field:** Ai Summary
* Click **Next**.

---

## Step 5: Insert Resources & Prompt Text
In the Prompt Workspace, you must define the instructions and data inputs for the AI.

1. Click **Insert Resource** and select the `User Case` object.
2. Choose the following fields to provide context to the AI:
   * `{!$Input:User_Case__c.Name}`
   * `{!$Input:User_Case__c.CreatedDate}`
   * `{!$Input:User_Case__c.Status__c}`
3. **Paste this Prompt under the Fields:** 
   > "Generate a clear and professional inspection summary using the provided inspection details. Explain the inspection status, inspection date, and key observations. Ensure the summary is easy to understand and suitable for business users."

---

## Step 6: Save and Activate
1. Click **Save** in the Prompt Builder interface.
2. Click **Activate** to make the Prompt Template available for use within the Lightning Record Pages.
3. Your Prompt Template is now ready to auto-generate summaries!
