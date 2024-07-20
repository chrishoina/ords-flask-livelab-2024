# ORDS URI Route Patterns

## Introduction

This lab will introduce to Route Patterns and how you can include them in your ORDS Resource Handlers.

Estimated Time: 20 minutes

### Objectives

In this lab, you will:

* Explore ORDS Route Patterns
* Test a sample ORDS Route Pattern
* Review the `/movie-single/:id` ORDS endpoint

### Prerequisites (Optional)

This lab assumes you have:

* An Oracle account
* All previous labs successfully completed

  > **Note:** If you have a **Free Trial** account, when your Free Trial expires your account will be converted to an **Always Free** account. You will not be able to conduct Free Tier workshops unless the Always Free environment is available. **[Click here for the Free Tier FAQ page.](https://www.oracle.com/cloud/free/faq.html)**

## Task 1: Navigate to the `/movie-single/:id` endpoint

1. From the Database Actions LaunchPad, navigate to the Development category, then the REST section.

    ![REST workshop section.](images/workshop-presentation-one.png " ")

2. Next, click the `Modules` tile, followed by the `moviestream` Resource Module.

    ![Selecting modules.](images/workshop-presentation-two.png " ")

    ![Selecting the moviestream resource module.](images/workshop-presentation-three.png " ")

3. Next, select the `movie-single/:id` Resource Template followed by the `movie-single/:id` Resource Handler.

    ![Selecting the movie-single/:id resource template.](images/workshop-presentation-four.png " ")

    ![Selecting the movie-single/:id resource handler.](images/workshop-presentation-five.png " ")

## Task 2: Explore the `/movie-single/:id` Resource Handler code

1. Observe the following SQL in the **Source** section.

    ```sql
    SELECT * FROM movie wHERE movie_id = :id
    ```

2. You can test this endpoint by clicking the `Start` icon. A dialog will appear, choose any number between `0` and `3800`.

    ![Entering in a bind variable for the resource template.](images/workshop-presentation-six.png " ")

   Notice the query results, you will notice the `MOVIE_ID` column matches the same number you selected in the Bind variable dialog.

   You may also take this `/movie-single/:id` endpoint, and place it in a new browser tab. Replace `:id` with a different number. You'll see the results from this query, but returned in a `JSON` format.

    ![Viewing the JSON payload in a browser format.](images/workshop-presentation-seven.png " ")

3. If it isn't obvious, you should recognize some of the data included in this `JSON` document. But instead of being displayed like this, you've previously seen it displayed in a modal. Like this:

    ![Image alt text](images/workshop-presentation-eight.png " ")

## Task 3: Putting it all together

1. You've now seen how this ORDS endpoint works. You've also seen the output in several different presentations. Next we'll explore how easy it is to drop-in this ORDS endpoint into our application's code.

2. After making their selecting their movie preferences, a user is redirected to a movie results table. From here, the user can click any of the `More` buttons to see a movie's additional details. This is accomplished with a simple Event Listener, and the JavaScript `Fetch()` API.

    ![Image alt text](images/workshop-presentation-nine.png " ")

   When a user clicks the `More` button, the associated `movie_id` value is used in the Route Pattern of this ORDS endpoint.

     ![Image alt text](images/workshop-presentation-ten.png " ")

3. Before, you manually simulated this by inputting a value into the Resource Handler's Bind variable dialog box. Instead here, the JavaScript and `Fetch()` API provide the ORDS endpoint with the necessary `movie_id` value, resulting in the modal you previously observed.

     ![Image alt text](images/workshop-presentation-eleven.png " ")

4. You may have noticed two other buttons, in addition to the `More` button. In the next lab you'll explore pagination, or paging results, with ORDS APIs.

    ![Image alt text](images/workshop-presentation-twelve.png " ")

## Learn More

* [Using route patterns in ORDS](https://docs.oracle.com/en/database/oracle/oracle-rest-data-services/24.2/orddg/developing-REST-applications.html#GUID-50E24524-32BB-470D-8015-6C25C9B47A44)
* [ORDS route patterns first introduction](https://blog.cdivilly.com/2015/03/10/route-patterns)
* [ORDS route patterns background](https://download.oracle.com/otn/java/ords/javadocs/3.0/plugin-api/route-patterns.html?AuthParam=1720464470_9c1ded06a5aabeae295cddc90ff3dfd7)

## Acknowledgements

* **Author** - Chris Hoina, Senior Product Manager, Database Tools
* **Contributors** - Jeff Smith, Distinguished Product Manager, Database Tools
* **Last Updated By/Date** - Chris Hoina, Database Tools, July 2024