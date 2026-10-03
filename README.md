# Hospital Management Database

A relational database for a hospital network, with a Java Swing app for browsing it. Team project for CS 157A (Database Management Systems) at San Jose State University, summer 2022.

## What's in it
- **Schema** ([`App/SQL/createFile.sql`](App/SQL/createFile.sql)): 35 tables covering patients, insurance, appointments, rooms and admissions, procedures, departments, hospitals, employees (doctors, nurses, accountants, pharmacists), prescriptions, medicine and pharmacies. Many-to-many relationships use junction tables with composite primary keys and foreign keys with `ON DELETE` rules.
- **Sample data** ([`App/SQL/InsertFile2.SQL`](App/SQL/InsertFile2.SQL)): about 1,000 lines of insert statements with sample rows.
- **Desktop app prototype** (`App/src`): a Swing window with a table picker and a sortable results view, plus a JDBC class that connects to Oracle and runs SQL statements. The results view still shows placeholder rows, so the two halves aren't connected yet.

## Tech stack
SQL, Oracle Database XE, Java, JDBC, Swing

## Running it
1. Start Oracle Database XE locally on port 1521.
2. Run `createFile.sql`, then `InsertFile2.SQL`.
3. To try the prototype UI, open the `App` folder in IntelliJ IDEA and run `frontend.Application`. The JDBC class needs the Oracle driver (`ojdbc`) on the classpath.

The database login in `MedicalConnection.java` is the default for a local XE install.
