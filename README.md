# Project Name: BAK2SQLite

## Description

BAK2SQLite is an open-source project aiming to decrypt and convert SQL Server backup files (.bak) into a SQLite database. This tool provides a streamlined solution for transforming cumbersome SQL Server backups into a more accessible and compatible format, enabling further analysis and processing without reliance on closed Microsoft technologies.

## Background

The .bak backup file is the standard backup format of SQL Server, widely prevalent on on-premises Windows machines. Unfortunately, this format is not directly usable in Azure and lacks compatibility with regular data science tools. This project aims to overcome these limitations by offering an alternative approach to handling SQL Server backups.

## Tsql examples (SQL Server)
```
BACKUP DATABASE YourDatabaseName TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

```
RESTORE DATABASE YourRestoredDatabaseName FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```



## Research

#### https://github.com/KyleBruene/mtf
mtf - a Microsoft Tape Format reader (and future writer?)

## References
- https://docs.fileformat.com/database/mdf/
