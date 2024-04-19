# Project Name: BAK2SQLite

## Description

BAK2SQLite is an open-source project aiming to decrypt and convert SQL Server backup files (.bak) into a SQLite database. This tool provides a streamlined solution for transforming cumbersome SQL Server backups into a more accessible and compatible format, enabling further analysis and processing without reliance on closed Microsoft technologies.

## Background

The .bak backup file is the standard backup format of SQL Server, widely prevalent on on-premises Windows machines. Unfortunately, this format is not directly usable in Azure and lacks compatibility with regular data science tools. This project aims to overcome these limitations by offering an alternative approach to handling SQL Server backups.

## Features

- **Extraction of SQL Server Backups**: BAK2SQLite utilizes advanced algorithms to decrypt .bak backup files and extract their contents.
  
- **Conversion to SQLite**: The extracted data is then converted into a SQLite database format, making it accessible to a wide range of tools and platforms.

- **Easy Integration**: The project provides clear documentation and simple command-line interfaces for seamless integration into existing data science and ETL workflows.

## Research

### https://github.com/KyleBruene/mtf
mtf - a Microsoft Tape Format reader (and future writer?)

