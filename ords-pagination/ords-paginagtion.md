# Pagination with Oracle REST Data Services

## Introduction

In this lab you will explore how to page results when working with ORDS APIs. You'll explore how this sample application takes advantage of ORDS pagination as well.

Estimated Time: 20 minutes

### Objectives

In this lab, you will:

* Discover how pagination works in ORDS
* Learn you can automate pagination
* Learn how you can dynamically page results
* [relative lab url test](?lab=need-help)

### Prerequisites

This lab assumes you have:

* An Oracle account
* All previous labs successfully completed

  > **Note:** If you have a **Free Trial** account, when your Free Trial expires your account will be converted to an **Always Free** account. You will not be able to conduct Free Tier workshops unless the Always Free environment is available. **[Click here for the Free Tier FAQ page.](https://www.oracle.com/cloud/free/faq.html)**

## Task 1: Locate `Previous` and `Next` buttons

<!-- Images -->

1. Scroll to the bottom of any `movieresults.html` page, and locate the `previous` and `next` buttons.

    ![image alt text](images/workshop-presentation-four.png " ")

2. These buttons are enabled or disabled based on the existence of an ORDS property. To review all properties, using the URI you created in Task 3, open a new web browser tab/window and navigate to the ORDS endpoint to review the `JSON` payload.

    ![image alt text](images/workshop-presentation-five.png " ")

3. The typical ORDS payload consists of the following properties:

   * `items`

     ![image alt text](images/workshop-presentation-items-property.png " ")

   * `hasMore`

     ![image alt text](images/workshop-presentation-hasmore.png " ")
  
   * `limit`

     ![image alt text](images/workshop-presentation-limit.png " ")

   * `offset`

     ![image alt text](images/workshop-presentation-offset.png " ")

   * `count`

     ![image alt text](images/workshop-presentation-count.png " ")

   * `links`

     ![image alt text](images/workshop-presentation-links.png " ")

4. The `limit`, `offset`, and `count` properties are interrelated. For instance, if you were to select `25` as the page size, ORDS would only return results in increments of `25`. How does ORDS know to do this? It was set for you automatically, when you created your Resource Module. However, you can modify this (however, auto-REST enable objects are set at `25`).

    ![Image alt text](images/workshop-presentation-pagination-size.png " ")

5. You'll notice on the first page of results the `hasMore: true` condition. This informs the user, client, or application that more data is available. When this condition is true, a `next` link will be made available. You'll notice this `next` link already includes the appropriate `offset`. These details make pagination simple with ORDS APIs.

    ![Image alt text](images/workshop-presentation-first-page-no-previous.png " ")

6. Click the `next` link. The next page of results will be displayed. After reviewing, scroll to the `links` property. Notice anything new or different?

    ![Image alt text](images/workshop-presentation-second-page.png " ")

   You should see the `hasMore: true` condition, but you'll also notice a `previous` link, in addition to the `first` and `next` links. These links make connecting pagination to your UI simpler.

7. If you were to continue clicking the `next` link, eventually you would observe the last page available. It would look like this:

    ![Image alt text](images/workshop-presentation-last-page-no-next.png " ")

   You'd notice the `hasMore: false` property. This signifies to the user, client, or application, that no more results exist. You'd also notice the absence of a `next` link.

8. Next we'll take a look at how this application uses this information.

## Task 2: Reviewing the application

1. Navigate to the `hello.py` file. Locate the `@app.route('/next_page', methods=['GET', 'POST'])` line.

    ![Image alt text](images/workshop-presentation-python-pagination-code.png " ")

2. This code is nearly identical to that found in the `@app.route('/handle_data')`. However, instead of expecting an initial selection (where a user selects a genre and movie runtime), this route expects a `next` URI. There is an identical route for the `previous` links too.

3. After this `next_page` function assembles the necesary information, a new  `movieresult.html` page is rendered and delivered to the UI. All `next` and `previous` links are updated, allowing the user to navigate forward or backward.

    ![Image alt text](images/workshop-presentation-html-next-jinja.png " ")

    ![Image alt text](images/workshop-presentation-previous-jinja.png " ")

4. Should a user reach the end or beginning of a results set, the html has been coded for two conditions.

   If a `previous` link is unavailable, then the `Previous` button is disabled by default.

      ![Image alt text](images/workshop-presentation-previous-button-disabled.png " ")

   And if a `next` link is not detected, then the `Next` button will be disabled.

      ![Image alt text](images/workshop-presentation-next-button-disabled.png " ")

## Learn More

* [URL text 1](http://docs.oracle.com)
* [URL text 2](http://docs.oracle.com)

## Acknowledgements

* **Author** - Chris Hoina, Senior Product Manager, Database Tools
* **Contributors** - Jeff Smith, Distinguished Product Manager, Database Tools
* **Last Updated By/Date** - Chris Hoina, Database Tools, July 2024
