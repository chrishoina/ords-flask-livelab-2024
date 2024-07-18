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

In this lab, you will:

* Retrieve from Oracle Object Storage the sample application project folder
* Extract the project folder
* Set up the project
* Install all required Python dependencies

### Prerequisites

* An OCI Always Free, Free Tier or paid tenancy
* A provisioned Oracle Autonomous Database
* Access to Database Actions as the Admin user

This lab assumes you have:

* An Oracle account
* All previous labs successfully completed

## Task 1: Obtain the project folder from Oracle Object storage

1. Download the project folder from object storage.

    <!-- Need to include link to project folder -->

    <!-- *IMPORTANT: do not include zip files, CSV, PDF, PSD, JAR, WAR, EAR, bin or exe files - you must have those objects stored somewhere else. We highly recommend using Oracle Cloud Object Store and creating a PAR URL instead. See [Using Pre-Authenticated Requests](https://docs.cloud.oracle.com/en-us/iaas/Content/Object/Tasks/usingpreauthenticatedrequests.htm)* -->

2. Extract the project ZIP file.

    ![download-and-extract-flask-project-from-object-storage](images/download-and-extract-flask-project-from-object-storage.jpeg " ")

3. Import the project into your code editor.

   > Note: This lab uses Microsoft Visual Studio Code. Available [here](https://code.visualstudio.com/).

4. Example with bold **text**.

  If you add another paragraph, add 3 spaces before the line.

## Task 2: TBD

1. TBD

  Use tables sparingly:

  | Column 1 | Column 2 | Column 3 |
  | --- | --- | --- |
  | 1 | Some text or a link | More text  |
  | 2 |Some text or a link | More text |
  | 3 | Some text or a link | More text |

2. You can also include bulleted lists - make sure to indent 4 spaces:

    - List item 1
    - List item 2

3. Code examples

    ```
    Adding code examples
  	Indentation is important for the code example to appear inside the step
    Multiple lines of code
  	<copy>Enclose the text you want to copy in <copy></copy>.</copy>
    ```

4. Code examples that include variables

	```
  <copy>ssh -i <ssh-key-file></copy>
  ```

## Learn More

*(optional - include links to docs, white papers, blogs, etc)*

* [URL text 1](http://docs.oracle.com)
* [URL text 2](http://docs.oracle.com)

## Acknowledgements
* **Author** - <Name, Title, Group>
* **Contributors** -  <Name, Group> -- optional
* **Last Updated By/Date** - <Name, Group, Month Year>
