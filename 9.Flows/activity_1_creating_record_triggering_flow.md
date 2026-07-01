# Activity 1: Creating Record Triggering Flow

## 1. Overview
This business automation process routes incoming cases automatically to specialized support queues based on the case classification. This reduces manual case handling and speeds up resolution triage.

## 2. Configuration Parameters
* **Object:** User Case (`User_Case__c`)
* **Trigger the Flow When:** A record is created or updated
* **Condition Requirements:** None (All records pass to evaluation)
* **Optimization:** Actions and Related Records

## 3. Detailed Logic Steps
1. **Case Initialization (Case S1):** 
   * Element Type: Assignment
   * Variable: `{!$Record.CaseStatus}`
   * Operator: Equals
   * Value: `Open`
2. **Conditional Routing Node (Check Case Type):**
   * Element Type: Decision
   * **Outcome 1: Damage Case**
     * Condition: `{!$Record.Case_Type__c}` Equals `Damage`
     * Route: Diverts path to Damage dynamic queue assignment.
   * **Outcome 2: Warranty Case**
     * Condition: `{!$Record.Case_Type__c}` Equals `Warranty`
     * Route: Diverts path to Warranty dynamic queue assignment.
3. **Database Execution (Update Records):**
   * Dynamically applies the evaluated owner queue record ID onto the triggering case file.
4. **Activation:** Save, test via debug run, and click **Activate**.
