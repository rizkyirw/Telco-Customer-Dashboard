# Telco-Customer-Dashboard
Deep dive analytics and recommendation from telco customer churn over data

## Dataset
The data source is from :
https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113.

## Data Dictionary
### Demographics
- CustomerID: A unique ID that identifies each customer.
- Count: A value used in reporting/dashboarding to sum up the number of customers in a filtered set.
- Gender: The customer’s gender: Male, Female
- Age: The customer’s current age, in years, at the time the fiscal quarter ended.
- Senior Citizen: Indicates if the customer is 65 or older: Yes, No
- Married: Indicates if the customer is married: Yes, No
- Dependents: Indicates if the customer lives with any dependents: Yes, No. Dependents could be children, parents, grandparents, etc.
- Number of Dependents: Indicates the number of dependents that live with the customer.

### Location
- CustomerID: A unique ID that identifies each customer.
- Count: A value used in reporting/dashboarding to sum up the number of customers in a filtered set.
- Country: The country of the customer’s primary residence.
- State: The state of the customer’s primary residence.
- City: The city of the customer’s primary residence.
- Zip Code: The zip code of the customer’s primary residence.

### Population
- ID: A unique ID that identifies each row.
- Zip Code: The zip code of the customer’s primary residence.
- Population: A current population estimate for the entire Zip Code area.

### Services
- CustomerID: A unique ID that identifies each customer.
- Tenure in Months: Indicates the total amount of months that the customer has been with the company by the end of the quarter specified above.
- Phone Service: Indicates if the customer subscribes to home phone service with the company: Yes, No
- Payment Method: Indicates how the customer pays their bill: Bank Withdrawal, Credit Card, Mailed Check
- Monthly Charge: Indicates the customer’s current total monthly charge for all their services from the company.
- Total Charges: Indicates the customer’s total charges, calculated to the end of the quarter specified above.
- Streaming Movies: Indicates if the customer uses their Internet service to stream movies from a third party provider: Yes, No. The company does not charge an - additional fee for this service.
- Online Security: Indicates if the customer subscribes to an additional online security service provided by the company: Yes, No
- Online Backup: Indicates if the customer subscribes to an additional online backup service provided by the company: Yes, No

### Online Security: Indicates if the customer subscribes to an additional online security service provided by the company: Yes, No

- Online Backup: Indicates if the customer subscribes to an additional online backup service provided by the company: Yes, No
- Churn Label: Yes = the customer left the company this quarter. No = the customer remained with the company. Directly related to Churn Value.

## Dashboard Details
From the dataset, total customer in the company is 7043, with 5174 Stay using company services, and 1869 customer is leaving from company services.
![Telco Dashboard](https://github.com/rizkyirw/Telco-Customer-Dashboard/assets/108413685/e421773a-b519-4f3a-9080-1fac0d674e03)

## Insight
Based on the Exploratory Data Analysis, we breakdown the data and here the insight :
![image](https://github.com/rizkyirw/Telco-Customer-Dashboard/assets/108413685/a3f484a9-25ba-4a52-ba44-94650ec4c69d)
### Churn Rate by Demography
From the graph it is known that:
Gender *does not* determine whether consumers churn or not.
The consumer's marital status (Partner) determines the consumer's churn or stay using the company's services, with unmarried consumers tending to choose churn.
The majority of consumers who live with their families choose to stay using the company's services, while there are some consumers who live alone who choose to churn. Common users of this company's services are people of productive age under 65 years of age and are more likely to churn than those over 65 years of age.

Assumption :
Most users of this service still do not have a partner, and are also likely renting a house when using the company's services. It could be that they will move places and at any time can disconnect the company's services compared to permanent users who already have partners and live with their families who will tend to continue using the company's services.


![image](https://github.com/rizkyirw/Telco-Customer-Dashboard/assets/108413685/e2510835-f54b-4196-abe5-3cead5950f86)
### Churn Rate by Service
From the graph it is known that:
Fiber Optic service products are the services most chosen by consumers, but also have a high churn rate compared to other services.
To find out the churn rate of additional services in the form of Tech Support and Online Security, from this data it can be seen that consumers who do not choose additional services in the form of Tech Support and Online Security tend to churn quite significantly.

Assumption :
Fiber optic has a faster speed than DSL, besides that the use of fiber optic in communication devices has become popular recently, for example wifi provider services that use fiber optic as a channel. This makes consumers more interested in trying to use Fiber optic compared to DSL (a beginner), but this also results in many consumers churning from Fiber optic services due to the differences in how Fiber Optic and DSL work.


![image](https://github.com/rizkyirw/Telco-Customer-Dashboard/assets/108413685/e3ed2223-4afc-4fd4-b036-1e762b0a3ad7)
### Churn Rate by Contract
Based on the graph above, it can be seen that:
Most consumers who choose annual contracts tend to continue using the company's services compared to consumers who choose monthly contract services, many of whom tend to leave the company's services this quarter.

Assumption :
The company has something that can make old consumers continue to subscribe, but it is not able to retain new consumers who are still trying to use the company's products month to month or on a monthly basis. Month to month contracts have different network quality compared to annual contracts, so consumers are not satisfied with the service and decide to churn.

## Recommendation
### PRODUCT INNOVATION
Update the product provided with consideration to retaining new consumers.
### IMPROVE SERVICE QUALITY
Improve service quality especially Fiber Optic which is able to attract many consumers but is unable to retain them.
### PRODUCT REDESIGN
Companies can redesign the product so that there is no inequality in service consumers who add additional services or do not add services to Tech support and OnlineSecurity.
### PROMOTION FOR CUSTOMER CONTRACT MONTH TO MONTH
Carry out discount promotions for consumers who extend (stay) contracts for using products offered by the company.
