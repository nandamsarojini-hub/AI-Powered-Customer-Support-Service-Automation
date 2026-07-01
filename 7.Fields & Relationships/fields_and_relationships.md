# Fields & Relationships Configuration

This document maps the custom fields, data types, and lookup relationships configured for the application's database schema.

### Table 1: Customer Object Fields
Maintains core client details.

| Field Label | Data Type | Description |
| :--- | :--- | :--- |
| Customer Name | Text | Full name of the client. |
| Email | Email | Contact email address. |
| Phone | Phone | Contact phone number. |
| Customer Type | Picklist | Values: Individual, Business. |

### Table 2: Merchandise Object Fields
Tracks product inventory and specifications.

| Field Label | Data Type | Description |
| :--- | :--- | :--- |
| Product Name | Text | Name of the product. |
| Product Code | Text | Unique SKU identifier. |
| Category | Picklist | Product classification. |
| Warranty (Months)| Number | Duration of warranty coverage. |
| Active | Checkbox | Indicates if the product is currently sold. |

### Table 3: Orders Object Fields
Links customers to purchased merchandise.

| Field Label | Data Type | Description |
| :--- | :--- | :--- |
| Order Number | Auto Number | System-generated ID. |
| Order Date | Date | Date of transaction. |
| Status | Picklist | Values: New, Shipped, Delivered. |
| Customer | Lookup | Relationship to the Customer object. |
| Product | Lookup | Relationship to the Merchandise object. |

### Table 4: User Case Object Fields
The core ticketing object that interfaces with Prompt Builder.

| Field Label | Data Type | Description |
| :--- | :--- | :--- |
| Product | Lookup | Relationship to Merchandise object. |
| Order | Lookup | Relationship to Orders object. |
| Priority | Picklist | Values: Low, Medium, High. |
| Issue Category | Picklist | Values: Delivery, Damage, Warranty. |
| AI Summary | Long Text Area | 32,000 character limit; target field for Prompt Builder output. |
