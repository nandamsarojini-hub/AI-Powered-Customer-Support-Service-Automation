# Deploy Prompt Builder Using Lightning App Builder

## Overview
This document outlines the steps to deploy the configured AI Prompt Template onto the Lightning Record Page. By upgrading the page layout to Dynamic Forms, the AI Prompt Template is embedded directly into the `Ai Summary` field on the `User Case` object. This allows support agents to auto-generate case inspection summaries with a single click.

---

## Step 1: Open User Case Record
1. Click the **App Launcher** (the 9-dot grid icon in the top left).
2. Search for and select **User Cases**.
3. Open any existing User Case record from the list view.

## Step 2: Edit Lightning Page
1. Click the **Gear Icon** in the top right corner of the screen.
2. Select **Edit Page** to open the Salesforce Lightning App Builder.

## Step 3: Upgrade to Dynamic Detail Page
1. Click anywhere on the **Record Detail** component in the center canvas to select it.
2. In the right-hand properties panel, locate the message about Dynamic Forms and click the **Upgrade Now** button.
3. Click **Next** on the configuration prompt.
4. Select the **User Case Layout** as the source layout.
5. Click **Finish**.

## Step 4: Assign the Prompt Template to the Field
1. On the central canvas, locate and click on the **Ai Summary** field to highlight it.
2. In the right-side properties panel, scroll down to the **Einstein Generative AI** section.
3. Search for and select the Prompt Template created in the previous phase: `MetaDataInspection`.

## Step 5: Save & Activate the Page
1. Click **Save** in the top right corner of the App Builder.
2. Click **Activate** to make the changes live.
3. In the activation menu, select **Assign as Org Default**.
4. Choose **Desktop and Phone** to ensure the AI summary generation feature is accessible across all devices.
5. Click **Next**.
6. Click **Save**.
7. Click **Back** (the top-left arrow) to return to the live record page and verify the AI generation button is active.
