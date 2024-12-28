# mssql
## Source - https://github.com/MicrosoftLearning/dp-300-database-administrator
## https://github.com/microsoft/sql-server-samples/releases/tag/adventureworks/
![image](https://github.com/user-attachments/assets/3890ccfc-33db-4006-851e-9a5605729ce7)

# Which port it uses.
## https://www.youtube.com/watch?v=wI4HWGlI6gM
## DDL
## DML
## DQL
## Profiler
<img width="450" alt="image" src="https://github.com/user-attachments/assets/eebd2bb6-ea1a-4777-a9b1-0d576f3a6ede" />
![image](https://github.com/user-attachments/assets/9d22f06f-1ee7-4f52-bbb6-72dda5c07d77)


```
-- In Master database
CREATE LOGIN [NewUser] WITH PASSWORD = 'StrongPassword123!'
GO

-- In target Database
CREATE USER [NewUser] FOR LOGIN [NewUser]
GO

EXEC sp_addrolemember 'db_owner', 'NewUser'
GO

-- Ti give server wide credentials
ALTER SERVER ROLE serveradmin ADD MEMBER [NewUser]
GO



```
