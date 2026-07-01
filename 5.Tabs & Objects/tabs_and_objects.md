# Custom Objects and Tabs Configuration

## 1. Creating Custom Objects
Custom objects form the backbone of the application's database, storing all relevant support and operational data.

### Configuration Steps (Example: Customer Object)
1. Navigate to **Setup** > **Object Manager**.
2. Click **Create** > **Custom Object**.
3. Provide the required details:
   * **Label:** Customer
   * **Plural Label:** Customers
   * **Object Name:** Customer
   * **Record Name:** Customer Name
   * **Data Type:** Text
4. Enable Optional Features: **Allow Reports**, **Allow Activities**, **Track Field History**.
5. Enable **Allow Search** under Search Status.
6. Click **Save**.

*This process was repeated for the following objects: `Merchandise`, `User Case`, `Order`, and `Knowledge`.*

## 2. Creating Custom Tabs
Tabs expose the custom objects to the Lightning Experience UI.

### Configuration Steps
1. Navigate to **Setup** > search for **Tabs** in the Quick Find box.
2. Under **Custom Object Tabs**, click **New**.
3. Select the newly created object (e.g., **Customer**) from the dropdown.
4. Choose an appropriate **Tab Style** (icon/color).
5. Click **Next**, assign visibility to **All Profiles**, and click **Save**.

*This process was repeated for all custom objects to ensure they are accessible in the App Launcher.*
