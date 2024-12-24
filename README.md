# mssql
## Source - https://github.com/MicrosoftLearning/dp-300-database-administrator
## https://github.com/microsoft/sql-server-samples/releases/tag/adventureworks/

# Which port it uses.
## https://www.youtube.com/watch?v=wI4HWGlI6gM
## DDL
## DML
## DQL
<img width="450" alt="image" src="https://github.com/user-attachments/assets/eebd2bb6-ea1a-4777-a9b1-0d576f3a6ede" />


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
