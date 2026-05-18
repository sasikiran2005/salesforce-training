# Salesforce Summer Program - Day 6

# 1. What is SOQL?

SOQL (Salesforce Object Query Language) is used in Salesforce to retrieve data from objects.

It is similar to SQL, but SOQL is specially designed for Salesforce data.

Example:
```sql
SELECT Name FROM Student__c
```

This query retrieves student names from the Student object.

SOQL helps to:
- Retrieve records
- Filter data
- Access related records
- Display required information

---

# 2. What is an Apex Trigger?

An Apex Trigger is a piece of code that runs automatically when data changes in Salesforce.

Triggers execute before or after events such as:
- Insert
- Update
- Delete

Example:
- After student registration → send welcome email
- After attendance update → send warning message

Triggers automate business processes without manual work.

---

# 3. Difference Between Flow vs Trigger

| Flow | Apex Trigger |
|---|---|
| No-code or low-code automation | Coding-based automation |
| Easy to create | More powerful and flexible |
| Best for simple business logic | Best for complex logic |
| Admin-friendly | Developer-friendly |
| Faster to build | Better control over processing |

---

# 4. Difference Between Before Trigger vs After Trigger

| Before Trigger | After Trigger |
|---|---|
| Runs before record is saved | Runs after record is saved |
| Used for validation and field updates | Used for related actions |
| Faster for modifying fields | Used for emails, tasks, notifications |

Example:
- Before Trigger → Validate fee amount
- After Trigger → Send confirmation email

---

# 5. Trigger Use Cases (5 Examples)

## 1. Student Registration
- Event: After student record is inserted
- Action: Send welcome email automatically

## 2. Course Full Notification
- Event: After course reaches maximum capacity
- Action: Notify faculty members

## 3. Low Attendance Alert
- Event: After attendance record update
- Action: Send warning if attendance is below 75%

## 4. Fee Payment Confirmation
- Event: After fee status changes to “Paid”
- Action: Generate payment receipt automatically

## 5. Faculty Assignment
- Event: After faculty assigned to course
- Action: Update course status to “Faculty Assigned”

---

# 6. Query Examples

- Find students registered this month
  
  ```
- Find faculty members in Computer Science department
 
  ```
- Find students with highest marks

  ```
- Find courses with no assigned faculty
 
  ```
- Find students absent for more than 5 days

  ```

---

# 7. Reflection

## Why do enterprise systems react automatically to data changes?

Enterprise systems manage huge amounts of data daily.

Automatic reactions help to:
- Save time
- Reduce manual work
- Improve accuracy
- Send instant notifications
- Maintain business rules
- Increase efficiency

Example:
When money is transferred in a banking system, the balance updates automatically and an SMS alert is sent immediately.

Without automation, employees would need to manually monitor every action, which is slow and error-prone.
