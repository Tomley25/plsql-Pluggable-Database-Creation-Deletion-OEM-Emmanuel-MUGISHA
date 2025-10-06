# Assignment 2: Pluggable Database Creation, Deletion & OEM

---

### Name: Emmanuel MUGISHA
### ID: 27811
### Group C

---

### Itroduction
> <b>This project focuses on setting up and managing Oracle Pluggable Databases (PDBs) using Oracle Enterprise Manager. It includes the steps taken to create, configure, Delete and monitor PDBs while maintaining proper documentation through Git. So the main goal is to gain hands-on experience in database administration and version control.</b>



**Step 1: Creating a New Pluggable Database PDB**
``` sql
create pluggable database Mu_pdb_27811
  2  admin user Mugisha_plsqlauca_27811 identified by "blessed"
  3  file_name_convert = (
  4  'C:\app\DELL\product\21c\oradata\XE\pdbseed',
  5  'C:\app\DELL\product\21c\oradata\XE\Mu_pdb_27811'
  6  );
```
<img src= "https://github.com/Tomley25/plsql-Pluggable-Database-Creation-Deletion-OEM-Emmanuel-MUGISHA/blob/main/PDB/CREATE%20PDB.png" width=600>
<img scr= "https://github.com/Tomley25/plsql-Pluggable-Database-Creation-Deletion-OEM-Emmanuel-MUGISHA/blob/main/PDB/SHOW%20PDBS%201.png" width=400>

**Step 2: Creating and Deleting a PDB**
> *Creating*
```sql
create pluggable database Mu_to_delete_pdb_27811
  2  admin user Mugisha_plsqlauca_27811 identified by "blessed"
  3  file_name_convert = (
  4  'C:\app\DELL\product\21c\oradata\XE\pdbseed',
  5  'C:\app\DELL\product\21c\oradata\XE\Mu_to_delete_pdb_27811'
  6  );
```
<img src= "https://github.com/Tomley25/plsql-Pluggable-Database-Creation-Deletion-OEM-Emmanuel-MUGISHA/blob/main/PDB/CREATE%20TO_DELETE%20PDB.png" width=600>
<img src= "https://github.com/Tomley25/plsql-Pluggable-Database-Creation-Deletion-OEM-Emmanuel-MUGISHA/blob/main/PDB/ALTER%20PDB%20TO_DELETE%20OPEN.png">

> *Deleting*
```sql
drop pluggable database Mu_to_delete_pdb_27811 including datafiles;
```
<img src= "https://github.com/Tomley25/plsql-Pluggable-Database-Creation-Deletion-OEM-Emmanuel-MUGISHA/blob/main/PDB/DROP%20PDB.png" width=600>

**Step 3: Oracle Enterprise Manager**
<p>Here we link the database to Oracle Enterprise Manager for monitoring and management. In which it allows visual access to database performance, storage, and user sessions through the OEM dashboard.</p>  

<img src="https://github.com/Tomley25/plsql-Pluggable-Database-Creation-Deletion-OEM-Emmanuel-MUGISHA/blob/main/PDB/OEM%20Dashboard.png" weight=400>

---

### What to Note
> Altering a table involves modifying an existing table structure without deleting it. The ALTER TABLE command is used to add new columns, change data types, rename columns, or drop existing ones. It allows updates to the database design as requirements change, without losing existing data.

> Other relating Tables are the following:

<p float='left'>
<img src= "https://github.com/Tomley25/plsql-Pluggable-Database-Creation-Deletion-OEM-Emmanuel-MUGISHA/blob/main/PDB/ALTER%20PDB%20SAVE%20STATE.png" width=400>
<img src= "PDB/ALTER PDB TO_DELETE CLOSE.png" width=400>
<img src= "PDB/ALTER SESSION SET CONTAINER.png" width=400>
<img src= "PDB/ALTER PDB TO_DELETE CLOSE.png" width=400>
</p>


