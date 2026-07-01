# Activity 3: Creating Recording Triggering Flow

## 1. Overview
The Case Auto Assignment & SLA Flow isolates critical escalations at the exact second a support ticket enters the platform. If a customer logs an issue marked with an urgent priority profile, standard queue pathways are bypassed to meet critical service metrics.

## 2. Configuration Parameters
* **Flow Label:** Case Auto Assignment & SLA Flow
* **Object:** User Case
* **Trigger the Flow When:** A record is created
* **Optimization:** Actions and Related Records

## 3. Detailed Logic Steps
1. **SLA Evaluation Gate (Is High Priority):**
   * Element Type: Decision
   * **Outcome 1: High Priority Criteria Met**
     * Condition: `{!$Record.Priority__c}` Equals `High`
     * Route: Proceeds directly to priority routing updates.
   * **Default Outcome:** If priority condition isn't met, the transaction proceeds along the baseline path (End).
2. **Ownership Escalation (Update Records 1):**
   * Filter Criteria: Set to update the triggering `User Case` record.
   * **Field Level Value Adjustments:**
     * Field: `OwnerId`
     * Value: Specify targeted administrative escalation queue or manager user record ID (e.g., `3D00Gfj0000007Qgyr`).
3. **Activation:** Save the automated asset, execute validation trials using the debugger canvas, and click **Activate**.