---
layout: post
title:  Retrieving Data in SQL I
tags:
- Tags
- Blog
- Post
- Database
- SQL
- MySQL
- Data Types
- Retrieving Data
---

In this series we will looking at concepts which are related to retrieving data in SQL. This is the first post of the series. We will discuss about various data types, NULL values, how to get the details of DB objects using DESC[RIBE] and INFO[RMATION][+] commands and also touch base on error messages, DUAL table, Quote Operator, Arithmetic operators, DISTINCT & Unique Keywords and concatenation operators, not necessarily in that order in this series.

### **Data Types**

Columns, variables & expressions stores different types of data, the attribute that specifies the type of data in the columns, variables or expressions is generally called as data types. the major data types are,

1. **VARCHAR2(size)** - Variable length character data, size determines the maximum size or length of character that can be stored in the variable or column. in case of VARCHAR2 data type, if the size of the character set or sting is smaller, then lower amount of memory will be consumed.
2. **CHAR(size)** - Fixed length character data, size determines the  size or length of character that can be stored in the variable or column. If the size of the character set or sting is smaller, then the remaining amount of memory will still be consumed.
3. **NUMBER(p,s)** - Variable length Numeric data. **p** is the precision (number of digits in a number. It ranges from 1 to 38) and **s** is the scale (number of digits to the right of the decimal point in a number. It ranges from -84 to 127). 
4. **DATE** - Stores Date Time in in internal numeric format. Default/Standard DATE data type. Stores Date time values such as century, year, month, day, hours, minutes & seconds. The default date format is *DD-MON-RR*
5. **TIMESTAMP** - Similar to **DATE** but stores fractional seconds as well. Stores values such as century, year, month, day, hours, minutes, seconds & fractional seconds.
6. **TIMESTAMP with TIMEZONE** - Similar to **TIMESTAMP** but stores timezone of the Database Operating system time as well. Stores values such as century, year, month, day, hours, minutes, seconds, fractional seconds & DB OS Timezone.
7. **TIMESTAMP with Local TIMEZONE** - Similar to **TIMESTAMP with TIMEZONE** but stores timezone of the user session instead of database OS timezone. Stores values such as century, year, month, day, hours, minutes, seconds, fractional seconds & user session Timezone.
8. **LONG** - Variable length character data type with high capacity (upto 2GB). This is not recommended to be used as this is a legacy data type maintained mainly for backward compatibility.
9. **RAW & LONG RAW** - mainly used to store RAW binary Data. Similar to LONG, this is also a legacy data type and maintained for backward compatibility. Not recommended.
10. **CLOB** - Recommended data type used mainly for storing large character values. Maximum size is (4 gigabytes - 1) * (database block size). CLOB is short for Character Large Objects.
11. **BLOB** - Recommended data type used mainly for storing large unstructured data like images, videos, music etc. Maximum size is 4GB. BLOB is short for Binary Large Objects.
12. **BFILE** - Recommended data type used mainly for storing the locator information to a binary file stored outside the database. Maximum size is 4GB.
10. **ROWID** - data type of the pseudocolumn ROWID which stores the hexadecimal number used to uniquely identify a row in the database. ROWIDs have multiple uses, They are the fastest way to identify a row in a transaction, uniquely identifies a row in a table and show you how rows in tables are stored. ROWIDs can change in certain circumstances, During EXPORT/IMPORT cycle, table rebuild and when the row is deleted and recreated. ROWIDs does not change on select or update. ROWIDs can be used to identifying rows in transactions but not recommended to be stored in tables as a key value.

We will continue the series of blog posts related to retrieving data in the future posts.

Regards,<br>
Sandeep