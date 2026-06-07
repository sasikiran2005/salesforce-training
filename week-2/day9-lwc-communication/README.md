# Day 9 - LWC Communication

## Component Communication

Component communication in Lightning Web Components (LWC) allows components to exchange data and interact with each other. The main communication methods are:

### Parent to Child

A parent component passes data to a child component using public properties decorated with `@api`.

### Child to Parent

A child component sends data to its parent using custom events.

### Unrelated Components

Components that are not directly related can communicate using Lightning Message Service (LMS) or a shared data source.

---

## Dashboard Design

The dashboard is designed to provide users with a clear and interactive view of data. Key elements include:

* Header section for navigation
* Summary cards displaying important metrics
* Data tables for detailed information
* Charts and visualizations for trends
* Action buttons for user interaction

The design focuses on simplicity, responsiveness, and user-friendly navigation.

---

## Data Flow Explanation

The data flow in LWC follows a structured pattern:

1. User interacts with the UI.
2. Events are triggered from components.
3. JavaScript controllers process the events.
4. Data is retrieved from Salesforce using Apex methods when required.
5. Updated data is passed between components.
6. The UI refreshes and displays the latest information.

This approach ensures efficient communication and data consistency throughout the application.

---

## Aura vs LWC

| Feature        | Aura Components     | Lightning Web Components (LWC) |
| -------------- | ------------------- | ------------------------------ |
| Performance    | Slower              | Faster                         |
| Standards      | Salesforce-specific | Based on Web Standards         |
| Development    | More Complex        | Simpler                        |
| Reusability    | Good                | Better                         |
| Learning Curve | Higher              | Easier                         |
| Rendering      | Framework-based     | Native Browser Support         |

LWC is generally preferred because it offers better performance, modern development practices, and easier maintenance.

---

## Reflection

Through this activity, I learned how Lightning Web Components communicate with each other using properties, events, and messaging services. I gained a better understanding of dashboard design principles and how data flows between frontend and backend systems. I also explored the differences between Aura Components and LWC, understanding why Salesforce recommends LWC for modern application development. This exercise improved my knowledge of component-based architecture and effective UI development in Salesforce.