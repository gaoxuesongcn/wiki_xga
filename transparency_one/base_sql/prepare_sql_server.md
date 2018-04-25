```sql
USE TransparencyDW;
 
 CREATE USER booster_user FOR LOGIN booster_user;
 EXEC sp_addrolemember 'db_datareader', 'booster_user';
 EXEC sp_addrolemember 'db_datawriter', 'booster_user';
 EXEC sp_addrolemember 'db_owner', 'booster_user';
```


