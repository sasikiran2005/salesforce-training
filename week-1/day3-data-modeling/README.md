## Day3 - Data Modelling

# Difference Between:  App  Object  Record  Field 

**App**
- App is a collection of objects , fields and tabs and other functionalities that supports a Business process of an Organisation. App is a collection of needed tabs .

**Object**
- Objects are the Database tables used to store a particular type of information. Objects contain records and fields. 
Objects are categorised into two types: 
1 Standard Object
2 Custom Object

**Record**
- Records are the rows in the tables. Records are specific instances of object ,used to store detailed data such as contact information ,opportunities and account details.
 
**Field**
- Fields are the columns of the tables . fields refer to a piece of information stored in a record such as name , account number etc. 
            Fields are categorised into two types:
            1. Standard field
            2. Custom field

# Standard vs Custom Objects 

1. **Standard Object**
- These are the Objects provided by salesforce by default.
- Limited customisation is possible
- Objects like Account, opportunity , contact are standard objects.
- These objects are available in every salesforce org by default 
2. **Custom Objects**
- Objects created by the user based on requirements of business 
- These are not provided by default in salesforce
- Created by admin or  developer 
- These objects are fully customizable and must be created manually 

# Formula Fields 
- The powerful tool that gives you control of how your data is displayed.
- They automatically calculate values in real-time based on other fields, expressions, or related records .
- They enable dynamic data representation  and are updated instantly when any source field changes 
# Validation Rules 
- Validation rules used to verify data entered by users in records meet the standards and requirements that admin specify before saving them.
- It can contain a formula or expression that evaluates the data in one or more fields and returns the value as True or False
- Validation rules will also display the error message in user screen, when user made a mistake while entering data.

# College Data Model 

- **objects**
1. Department 
2. program 
3. course 
4. section 
5. student 
6. faculty 
- **Relationships** 
1. Department has many programs
2. program has many courses
3. course has many sections
4. one  Section has many Students 
5. one faculty can teach many sections 
                
