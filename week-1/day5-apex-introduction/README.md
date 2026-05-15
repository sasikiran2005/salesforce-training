Day 5 — Apex Introduction

1. What is Apex?
-----------------
Apex is the programming language used in Salesforce. It lets developers write code that runs on Salesforce servers. You can use Apex to add custom logic, check data, and do tasks that normal setup tools cannot do.

2. Difference
-------------
- Flow vs Apex: Flow is a tool you can use without code. It works well for simple business processes. Apex is code and is needed when the logic is more complex.
- Configuration vs Coding: Configuration means using standard Salesforce setup, like fields and rules. Coding means writing Apex code, which is more powerful but needs a developer.

3. Real Examples Where Apex Is Needed
------------------------------------
1. When many records need to be updated at once and Flow would be too slow or hit limits.
2. When the system must call an external website or service.
3. When business logic is too complex for standard Salesforce rules.

4. Integrated System Design — College Management System
-----------------------------------------------------
Overview: Design a College Management System using both declarative and programmatic approaches.

- CRM: Use Salesforce objects to model Students, Courses, Enrollments, Instructors, and Departments.
- Objects: Create `Student__c`, `Course__c`, `Enrollment__c`, `Instructor__c`, `Department__c` with relevant fields.
- Relationships: Use lookup/master-detail for `Enrollment__c` -> `Student__c` and `Course__c`; use lookup for instructor association.
- Validation: Implement field-level validation rules and required checks for basic data integrity (e.g., course capacity, valid enrollment dates).
- Flow: Build Flows for declarative automations such as enrollment confirmation emails, schedule reminders, and simple capacity checks.
- Apex: Use Apex for bulk enrollment processing, external integrations (payment gateways, LMS), and complex business rules (e.g., waitlist processing, seat allocation across multiple sections).

5. Pseudocode Examples
----------------------
Example A — Bulk Enrollment Processor (Apex class pseudocode):

```
class EnrollmentProcessor {
  method processEnrollments(list<Enrollment__c> enrollments) {
    group enrollments by Course__c into courseMap
    for each course in courseMap {
      validate seat availability
      create or update Enrollment records in bulk
      handle waitlist if needed
    }
  }
}
```



Example b — Branch Seat Vacancy Check (pseudocode):

```
public class SeatCheck {

    public static void checkSeats(Id courseId) {

        // Get course details from database
        Course__c course = [
            SELECT Name, Total_Seats__c FROM Course__c WHERE Id = :courseId LIMIT 1 ];

        // Count enrolled students
        Integer enrolledStudents = [ SELECT COUNT() FROM Student__c WHERE Course__c = :courseId ];

        // Calculate available seats
        Integer availableSeats = course.Total_Seats__c - enrolledStudents;

        // Check seats
        if(availableSeats > 0) {
             System.debug('Seats Available');
            System.debug('Available Seats: ' + availableSeats);
             } else {

            System.debug('No Seats Available');

        }
    }
}
```



