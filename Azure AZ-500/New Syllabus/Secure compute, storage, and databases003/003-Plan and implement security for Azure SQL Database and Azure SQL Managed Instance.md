# Microsoft Purview's governance solutions:
- To manage your on-premises, multicloud, and software-as-a-service (SaaS) data.
- Using the Microsoft Purview Data Catalog, Data Map, Data Sharing, Data Estate Insights, and Policies

## Data classification in the Microsoft Purview governance portal:
- a `way of categorizing data assets by assigning unique logical tags or classes to the data assets.`
- Classification is based on the business context of the data.
- For example, you might classify assets by Passport Number, Driver's License Number, Credit Card Number, SWIFT Code, Person’s Name, and so on.
- `Classification is the process of organizing data into logical categories that make the data easy to retrieve, sort, and identify for future use.`
- Types of classification:  System (200+) & Custom Type

## Auditing for Azure SQL Database and Azure Synapse Analytics: 
- 

1. Data Map:
-  A `cloud native PaaS service that captures metadata about enterprise data present in analytics and operation systems on-premises and cloud.`
-  Automatically kept up to date with built-in automated scanning and classification system.
2. `Data Catalog`	`Finds trusted data sources` by browsing and searching your data assets. The data catalog aligns your assets with friendly business terms and data classification to identify data sources.
3. `Data Estate Insights`	Gives you an overview of your data estate to help you discover `what kinds of data you have and where it is.`
4. `Data Sharing`	Allows you to `securely share data internally or cross organizations` with business partners and customers.
5. `Data Policy`	A `set of central, cloud-based experiences` that help you provision access to data securely and at scale.

## Transparent data encryption (TDE):
- `encrypts SQL Server, Azure SQL Database, and Azure Synapse Analytics data files.`
- This encryption is known as encrypting data at rest.

## Notes:
- `Applies to:  SQL Server  Azure SQL Database  Azure SQL Managed Instance  Azure Synapse Analytics  Analytics Platform System (PDW)`
- TDE isn't available for system databases. It can't be used to encrypt master, model, or msdb.
- If you make the certificates password protected after TDE uses them, the database becomes inaccessible after a restart.

## Dynamic data masking:
- `Applies to:  SQL Server 2016 (13.x) and later  Azure SQL Database  Azure SQL Managed Instance  Azure Synapse Analytics`
- Dynamic data masking (DDM) limits sensitive data exposure by masking it to nonprivileged users.
- The purpose of dynamic data masking is to limit exposure of sensitive data, preventing users who shouldn't have access to the data from viewing it.
- Users with CONTROL SERVER or CONTROL at the database level could view masked data in its original form.
- This includes admin users or roles such as sysadmin, serveradmin, db_owner etc.****







