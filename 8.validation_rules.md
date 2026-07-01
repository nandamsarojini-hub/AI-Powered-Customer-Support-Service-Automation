# Validation Rules Configuration

Validation rules ensure data integrity by enforcing business logic at the database level. They prevent users from saving records that do not meet specific criteria.

## 1. Damage Case Priority Enforcement
**Purpose:** Ensures that any support ticket categorized as "Damage" is assigned a strict priority level by the agent.

*   **Rule Name:** `Damage_Requires_Priority`
*   **Validation Formula:** 
    ```salesforce
    AND( 
        ISPICKVAL(Case_Type__c, "Damage"), 
        ISBLANK(TEXT(Priority__c)) 
    )
    ```
*   **Error Message:** Priority is mandatory for Damage cases.
*   **Error Location:** Field — Priority

## 2. Warranty and Delivery Case Priority Enforcement
**Purpose:** Ensures that any support ticket categorized as "Warranty" or "Delivery" is assigned a strict priority level before saving.

*   **Rule Name:** `Warranty_Delivery_Requires_Priority`
*   **Validation Formula:** 
    ```salesforce
    AND( 
        OR( 
            ISPICKVAL(Case_Type__c, "Warranty"), 
            ISPICKVAL(Case_Type__c, "Delivery") 
        ), 
        ISBLANK(TEXT(Priority__c)) 
    )
    ```
*   **Error Message:** Priority is mandatory for Warranty and Delivery cases.
*   **Error Location:** Top of Page
