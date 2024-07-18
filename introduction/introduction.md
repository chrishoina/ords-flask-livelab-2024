# Integrating ORDS APIs into your applications

## Introduction

This workshop illustrates how Oracle REST Data Services (ORDS) can complement an already-existing web application. The sample application found in this workshop uses ORDS, the Flask framework, Jinja2 templating, and *light* JavaScript.

This lab will guide you through obtaining from Oracle Object storage a sample Python application. You will also set up the application's project directories.

Estimated Time: 10 minutes

### About Product/Technology

Oracle REST Data Services is a *free* Java application responsible for:

1. Intercepting HTTP/HTTPS web requests, *then*
2. As a proxy/universal `ORDS_PUBLIC_USER` database user satisfying these requests, where finally
3. Responding to the requesting end user, client, or application with the results of that HTTP/HTTPS request

HTTP requests can be one of following methods: `GET`, `POST`, `BATCH LOAD`, `PUT`, `DELETE`. *Although*, ORDS makes REST-enabling SQL, PL/SQL stored procedures and functions, Views, Tables, and other database objects intuitive and simple. As you become more familiar with ORDS, you will engineer novel solutions to your ELT and ETL needs.

### Objectives

In this lab, you will become acquainted with:

* Oracle REST Data Services
* Methods and operations available in ORDS

### Prerequisites

* An OCI Always Free, Free Tier or paid tenancy
* A provisioned Oracle Autonomous Database
* Access to Database Actions as the Admin user

This lab assumes you have:

* An Oracle account
* All previous labs successfully completed

## Learn More

* [ORDS home](https://www.oracle.com/database/technologies/appdev/rest.html)
* [ORDS forum](https://forums.oracle.com/ords/apexds/domain/dev-community/category/oracle_rest_data_services)

## Acknowledgements

* **Author** - Chris Hoina, Senior Product Manager, Database Tools
* **Contributors** -  Jeff Smith, Distinguished Product Manager, Database Tools
* **Last Updated By/Date** - Chris Hoina, Senior Product Manager, Database Tools
