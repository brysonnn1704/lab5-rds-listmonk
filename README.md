# Lab 5 Assignment 1 – Listmonk with AWS RDS PostgreSQL

## 1. Project Overview

This project deploys the Listmonk application from Lab 4 on an AWS EC2 instance and connects it to an Amazon RDS PostgreSQL database.

The application demonstrates all CRUD operations:

- Create
- Read
- Update
- Delete

## 2. AWS Architecture

User
↓
EC2 – Listmonk Application
↓
PostgreSQL : 5432
↓
Amazon RDS PostgreSQL

## 3. EC2 Configuration

Application: Listmonk

EC2 Instance:
listmonk-lab4

Application URL:
http://3.108.234.182

## 4. RDS Configuration

Database Engine: PostgreSQL

RDS Instance:
listmonk-postgres-rds

Database:
listmonk

Port:
5432

The Listmonk application connects to the PostgreSQL database hosted on Amazon RDS.

## 5. Database Connection

The Listmonk configuration was modified to use the RDS PostgreSQL endpoint instead of the local PostgreSQL database.

The database connection uses:

- RDS endpoint
- PostgreSQL port 5432
- Database name: listmonk
- Database user: listmonk
- SSL mode: require

Passwords and other sensitive credentials are not included in this repository.

## 6. Security Configuration

The RDS security group allows PostgreSQL traffic on port 5432 only from the EC2 security group.

RDS Security Group:
listmonk-rds-sg

EC2 Security Group:
listmonk-lab4-sg

No public 0.0.0.0/0 rule is used for PostgreSQL database access.

## 7. CRUD Demonstration

### Create

A new Listmonk list named `Lab5 CRUD Test` was created through the running EC2 application.

### Read

The created list was displayed in the Listmonk Lists page.

### Update

The list was updated from:

`Lab5 CRUD Test`

to:

`Lab5 CRUD Test Updated`

### Delete

The updated list was deleted successfully through the Listmonk application.

## 8. Evidence

The project evidence includes:

1. RDS PostgreSQL deployment
2. RDS security group configuration
3. EC2 Listmonk application
4. Create and Read operation
5. Update operation
6. Delete operation

## 9. Conclusion

The Lab 4 Listmonk application was successfully connected to an Amazon RDS PostgreSQL database.

The application successfully demonstrates Create, Read, Update and Delete operations using the deployed database.
