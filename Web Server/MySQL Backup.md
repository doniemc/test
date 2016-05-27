<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [MySQL Backups](#mysql-backups)
	- [MySQL Workbench](#mysql-workbench)
	- [AutoMySQLBackup](#automysqlbackup)
	- [MySQL Dump](#mysql-dump)

<!-- /TOC -->

# MySQL Backups
## MySQL Workbench

In MySQL Workbench go to Data Export

![alt backup](assets/WebServerNotes-49108.png "MySQL")

Select the required Schema / Database from the pane on the left called "Tables to Export" (Not shown on this image)

Select:

```bash
Export to Self-Contained File
```

Change the file name and location if required

Click:

```bash
Start Export
```

## AutoMySQLBackup

AutoMySQLBackup is a command line tool used to generate backups for a MySQL environment.

To install AutoMySQLBackup:

```bash
sudo apt-get install automysqlbackup
```

```bash
sudo automysqlbackup
```

To make changes to the backup schedule edit the following file:

```bash
sudo nano /etc/default/automysqlbackup
```

The default location for backups is "/var/lib/automysqlbackup". Search this directory to see the structure of the backups:

```bash
ls /var/lib/automysqlbackup
```

```bash
daily  monthly weekly
```



## MySQL Dump
