---
layout: post
title:  "Building my jQuery front end app"
date:   2016-06-28 16:29:23 -0400
---


Even though the assignment suggested that I continue working on building out the app I built for the Rails assessment, I decided that I wanted to build something entirely different. Given I'm likely to be looking for developer jobs in the not-too-distant future, I thought it would be interesting to build out something related to looking for a new job.

This app is pretty simple and there's definitely additional functionality that could be built out; the purpose of this project was purely to show my understanding of JavaScript and jQuery.

There are only two models in this application: jobs and companies. Companies have a name, while jobs have a title, city, state, description, salary, and belong to a company. Originally I had users and industries that I was planning to use to help provide additional functionality, but I found that I was able to demonstrate my understanding of jQuery and meet the requirements of the project without those additional models.

When you go to the homepage, you're greeted by an image of people working furiously at a table, the logo in the center of the page, and the navbar. The navbar has two buttons: one that directs you to the jobs index page, and another that directs you to the company index page. All of the data visualized in this application is rendered using jQuery and an AMS JSON serialization (fulfilling requirement #1).

The company index page is pretty simple; it's just a list of the companies that have posted jobs on the site. If you click on one of the hyperlinks for one of the companies, it takes you to that company's show page. There you can find all of the jobs associated with that company (fulfilling requirement #3). If you go to the jobs show page, you see a table with all of the data associated with jobs currently listed. The salary value in the table is formatted using a Javascript Model Object method, fulfilling requirement #5.  On that page, you're also able to create a new job using the form at the bottom of the table and have it rendered in the table without refreshing the page, fulfilling requirement #2.  If you click on the hyperlink associated with the job's title you come to that job's show page. There is listed all of the data associated with that job and an edit form for that role. If you fill out the form and click "Update Job", it updates the data on the page without refreshing, thereby fulfilling requirement #2.

I thought this was a really worthwhile assignment. I didn't get as much out of the JS/jQuery sectionsas I'd hoped (the assessments didn't require much critical thinking beyond copying what was coded), but this project required more critical thinking and forced me to apply what I'd learned in the section. The thing I actually found most insightful was learning how the CSS and JS manifests work. I think those lessons were a little vague, so it was good to have the practice of witing my own asset code and having it included in my application the right way.
