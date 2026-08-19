# Lab 5 Assignment 1 – Listmonk with AWS RDS PostgreSQL

## 1. Project Overview

This project deploys the Listmonk application on an AWS EC2 instance and connects it to an Amazon RDS PostgreSQL database.

The application demonstrates CRUD operations:

- Create
- Read
- Update
- Delete

## 2. AWS Architecture

User
↓
AWS EC2 – Listmonk
↓
PostgreSQL : 5432
↓
Amazon RDS PostgreSQL

## 3. EC2 Configuration

Application: Listmonk

EC2 Instance: `listmonk-lab4`

Application URL:

http://65.2.75.226

Application Port: `9000`

## 4. RDS Configuration

Database Engine: PostgreSQL

RDS Instance: `listmonk-postgres-rds`

Database: `listmonk`

Port: `5432`

The Listmonk application connects to the PostgreSQL database hosted on Amazon RDS.

## 5. Database Connection

The Listmonk configuration was modified to use the Amazon RDS PostgreSQL endpoint instead of a local database.

Connection configuration:

- RDS endpoint
- PostgreSQL port: 5432
- Database: `listmonk`
- User: `listmonk`
- SSL mode: `require`

Database passwords and other sensitive credentials are not included in this repository.

## 6. Security Configuration

The EC2 security group allows HTTP traffic for the Listmonk application.

The RDS security group allows PostgreSQL traffic on port `5432` from the EC2 security group.

Database access is therefore restricted and is not exposed through a public PostgreSQL rule.

## 7. CRUD Demonstration

### Create

A new Listmonk list was created through the running application.

### Read

The created list was displayed on the Listmonk Lists page.

### Update

The created list was modified through the Listmonk application.

### Delete

The updated list was deleted successfully.

## 8. Evidence

Screenshots are available in the `screenshots/` directory.

Evidence includes:

1. EC2 instance running
2. RDS PostgreSQL deployed
3. RDS security group configuration
4. Listmonk application running
5. Create operation
6. Read operation
7. Update operation
8. Delete operation

## 9. Configuration Files

Example configuration:

`config/config.example.toml`

Deployment information:

`config/deployment.md`

Actual database credentials are intentionally excluded.

## 10. Conclusion

The Listmonk application was successfully deployed on AWS EC2 and connected to an Amazon RDS PostgreSQL database.

The application demonstrates Create, Read, Update and Delete operations using the deployed database.
