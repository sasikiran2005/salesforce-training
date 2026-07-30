# Salesforce     – Day 3 Assignment

## 1. Which requirements did you solve using Flow?

The following requirements were implemented using Record-Triggered Flows:

- Automatically populate the Application Date when a new Application record is created.
- Send a confirmation email when a new Application is submitted.
- Automatically create an Offer Letter record when the Application Status changes to **Selected**.

---

## 2. Which requirements required Validation Rules?

The following requirements were implemented using Validation Rules:

- Application Date cannot be after the Job Closing Date.
- Mandatory fields such as Student, Job, and Application Date cannot be left blank.

---

## 3. Which requirements still needed Apex?

The following requirement required Apex:

- Prevent duplicate applications when the same student applies for the same job more than once.

Apex Trigger is required because Validation Rules cannot query other records in the database to check for duplicates.

---

## 4. Why did you choose those solutions?

- **Flow** was used for automation tasks such as updating fields, sending emails, and creating related records because it is a declarative (low-code) solution that is easy to build and maintain.
- **Validation Rules** were used to enforce data quality and prevent invalid data from being saved.
- **Apex Trigger** was chosen for duplicate application checking because it requires querying existing records and implementing custom business logic, which cannot be achieved using Validation Rules alone.

---

## Objects Used

- Student__c
- Job__c
- Application__c
- Offer_Letter__c

---

## Features Implemented

- Record-Triggered Flow for Application Date
- Record-Triggered Flow for Offer Letter Creation
- Send Email Action
- Validation Rules
- Custom Objects and Relationships
