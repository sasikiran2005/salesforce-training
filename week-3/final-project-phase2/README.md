# Final Project – Phase 2

## Project Title

Customer Churn Prediction and Business Management System

---

# 1. Final Architecture

### Architecture Overview

The system follows a multi-layer architecture:

### Presentation Layer

* Lightning Web Components (LWC)
* Salesforce Lightning App
* Dashboards and Reports

### Business Logic Layer

* Apex Classes
* Apex Triggers
* Validation Rules
* Record-Triggered Flows

### Data Layer

* Customer Object
* Subscription Object
* Support Ticket Object
* Churn Prediction Object
* User Object

### Integration Layer

* External APIs (Future Enhancement)
* Email Notifications
* Scheduled Jobs

### Architecture Flow

User → LWC Interface → Salesforce Objects → Apex/Flows → Reports & Dashboards

---

# 2. Workflow Explanation

### Customer Management Workflow

1. Customer record is created.
2. Validation rules ensure data quality.
3. Customer subscription details are captured.
4. Churn prediction process evaluates risk score.
5. High-risk customers are flagged automatically.
6. Notifications are sent to managers.
7. Support team initiates retention activities.
8. Reports are updated in real time.

### Ticket Management Workflow

1. Customer raises a support request.
2. Ticket is assigned automatically.
3. Support representative updates status.
4. Resolution is recorded.
5. Customer receives notification.
6. Closed tickets are included in reporting metrics.

---

# 3. Approval Workflows

### Customer Retention Approval

#### Stage 1

* Support Agent submits retention offer.

#### Stage 2

* Manager reviews the proposal.

#### Stage 3

* Approval or rejection decision.

#### Outcome

* Approved offers are sent to customers.
* Rejected offers return for revision.

### Discount Approval Workflow

1. Discount request submitted.
2. Manager approval required.
3. Finance review for high-value discounts.
4. Final approval updates customer account.

---

# 4. Reporting and Dashboard Ideas

### Executive Dashboard

* Total Customers
* Active Customers
* Churn Rate
* Monthly Revenue
* Customer Retention Rate

### Customer Analytics Dashboard

* High-Risk Customers
* Churn Predictions
* Customer Segmentation
* Subscription Trends

### Support Dashboard

* Open Tickets
* Closed Tickets
* Average Resolution Time
* Customer Satisfaction Metrics

### Sales Dashboard

* New Customer Acquisition
* Revenue Growth
* Renewal Success Rate
* Upsell Opportunities

---

# 5. Failure Handling Ideas

### Data Validation Failures

* Prevent incomplete records from saving.
* Display clear error messages.

### Workflow Failures

* Send automated error notifications.
* Log failure details for administrators.

### Integration Failures

* Retry failed API requests.
* Maintain error logs.
* Alert support teams.

### Approval Process Failures

* Escalate pending approvals.
* Send reminder notifications.

### System Failures

* Backup critical records.
* Enable recovery procedures.
* Maintain audit logs.

---

# 6. Scalability Discussion

### Horizontal Scalability

* Support additional business units.
* Add new customer segments.

### Vertical Scalability

* Increase data storage capacity.
* Optimize Apex code performance.

### Future Enhancements

* AI-powered churn prediction.
* Real-time analytics.
* Mobile application support.
* Third-party CRM integrations.
* Advanced customer behavior tracking.

### Performance Optimization

* Use indexed fields.
* Implement efficient SOQL queries.
* Minimize governor limit consumption.
* Use asynchronous processing where applicable.

---

# 7. Reflection

This project provided practical experience in designing and implementing a Salesforce-based business solution. The system demonstrates how customer information, support operations, and churn prediction processes can be integrated into a single platform.

Throughout the project, key Salesforce concepts such as custom objects, relationships, validation rules, flows, Apex automation, approval processes, and reporting were applied. The project also highlighted the importance of data quality, workflow automation, user experience, and scalability.

Future improvements could include machine learning-based churn prediction, external system integrations, advanced analytics, and mobile accessibility. Overall, the project strengthened skills in Salesforce development, business process automation, and solution architecture.