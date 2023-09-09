# SQLite Commands

## Basic Bash

### Open Connection

```bash
sqlite3
```

### Close Connection

```bash
ctrl + D
```

## List Databases

```bash
.databases
```

## List Tables

```bash
.tables
```

## Create Table

```bash
# CREATE TABLE <db-name>.<new-table-name>(
#   <colum-1-name> <column-1-type> PRIMARY KEY NOT NULL,
#   <colum-2-name> <column-2-type> NOT NULL,
#   <colum-3-name> <column-3-type> NOT NULL
# );
```

## Create Table (ex:)

```bash
CREATE TABLE main.movies(
  ID INT PRIMARY KEY NOT NULL,
  TITLE TEXT NOT NULL,
  YEAR INT NOT NULL
);
```

## Insert Record to Table

```bash
INSERT INTO movies VALUES(1, 'Saving Private Ryan', 1998);
```

## List all records from table

```bash
# SELECT * FROM <table-name>;
SELECT * FROM movies;
```

## Order Data by Key

```bash
#SELECT * FROM <table-name> ORDER BY <column>;
SELECT * FROM movies ORDER BY YEAR;
```

Default will be ascending order (lowest value first) but you
can configure this to work in the reverse (descending) with
options: `ASC | DESC`, ex:

```bash
# Highest number first
SELECT * FROM movies ORDER BY YEAR DESC;
```
