automongobackup
===============

Overview
--------
```automongobackup``` can be used to take automated backups (via cron) of a MongoDB server or replica set.

Options Documentation
---------------------

| Option            | Required? | Explanation                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| ```DBNAME```      | Optional  | **Comment out if unused.** Specify to only backup a specific database and no others. Unnecessary if authentication is off.                                 |
| ```DBUSERNAME```  | Optional  | **Comment out if unused.**  Username for user that has at least SELECT permissions on ALL databases. Unnecessary if authentication is off.            |
| ```DBPASSWORD```  | Optional  | **Comment out if unused.** Password for user that has at least SELECT permissions on ALL databases. Comment out if unused. Unnecessary if authentication is off.             
| ```DBHOST```      | Required  | Server or replica set to backup. Set this to 127.0.0.1 for localhost. For a replica set, use replSet connection syntax ```replSetName\host1,host2,host3``` |
| ```DBPORT```      | Required  | Port number to connect to on ```DBHOST```(s). Default: ```21017```                                                                                         |
| ```BACKUPDIR```   | Required  | This is where the backup will be stored.                                                                                                                   |
| ```MAILCONTENT``` | Required  | Valid options are ```log```, ```files```, ```stdout```, or ```quiet```. More info below.                                                                   |
| ```MAXATTSIZE```  | Required  | Set the maximum allowed email attachment size in kilobytes (```4000``` = approximately 5MB email).                                                                    |
| ```MAILADDR```    | Optional  | **Comment out if unused.** Supports a single email address or multiple email addresses in a space separated list.                                                                     |

You will need a destination directory for the backup with enough space to store
the backup.

License
-------
Please see licensing information in [LICENSE](LICENSE)
