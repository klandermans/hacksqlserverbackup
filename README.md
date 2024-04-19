# Unraveling sql server bak / mdf / ldf

## Description

This is an open-source project aiming to decrypt and convert SQL Server backup files (.bak) into a SQLite database. This tool provides a streamlined solution for transforming cumbersome SQL Server backups into a more accessible and compatible format, enabling further analysis and processing without reliance on closed Microsoft technologies.

## Background

The .bak backup file is the standard backup format of SQL Server, widely prevalent on on-premises Windows machines. Unfortunately, this format is not directly usable in Azure and lacks compatibility with regular data science tools. This project aims to overcome these limitations by offering an alternative approach to handling SQL Server backups.

## .bak file

A BAK file, identified by its .bak extension, typically serves as a backup file utilized by various software tools to preserve data backups. Specifically within the realm of databases, a BAK file is integral to Microsoft SQL Server's backup mechanism, housing comprehensive database contents. This format ensures that all database data and associated files are securely stored, enabling retrieval in scenarios where the database may face corruption or other issues. For added safety, these backup files can be replicated and indexed on alternative servers.

Numerous applications are capable of generating BAK files, including SQL Server Management Studio, Transact-SQL, and Windows PowerShell.

The internal structure of a BAK file is not universally documented; however, it is widely speculated to adhere to the Microsoft Tape Format (MTF). Although detailed specifications of MTF are accessible, they presuppose a foundational understanding of storage management operations, tape drives, and file systems, thereby providing insights into the BAK file's composition and operation.

## .mdf file 
The MDF (Master Data File) file is the primary data file for a SQL Server database. It contains the actual data and schema objects, including tables, indexes, stored procedures, and so on. When you create a new database in SQL Server, it typically creates an MDF file to store its data.

## .LDF file 
The LDF (Log Data File) file is the transaction log file for a SQL Server database. It records all transactions and modifications made to the database, allowing for rollback or recovery in case of system failure or data corruption. The log file ensures the ACID (Atomicity, Consistency, Isolation, Durability) properties of database transactions.


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
