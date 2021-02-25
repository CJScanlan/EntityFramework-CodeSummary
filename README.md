# Code First EntityFramework Code Summary
Code Summary for internship at Prosper IT Consulting

## Introduction
My internship at Prosper IT Consulting was conducted in a 2 week sprint, collaborating with a group of software developers using DevOps methodology. The overall purpose of the project was to build software for a local theater group to manage its website content without needing any technical knowledge. It includes multiple areas to manage admin functions, subscriber needs, and general public needs. My tasks included fixing a bug in the footer icons, building models for Rental Requests and Rental Surveys, scaffolding these models for CRUD functionality, then linking these models with fully-defined navigation properties. 

### Footer Bugs
My first user story was to fix a bug on the footer icons. The icons were intended to be a full circle, but instead ended up in a oblong shape with two circles slightly overlapping eachother. Additionally, the hover effect only worked on one of the overlapping circles. To solve this, I first had to pinpoint the two elements that were being styled duplicately. This involved commenting out the styling of relevant elements through CSS, and seeing which elements were affected when certain styling was removed. I was able to narrow it down and discover that both the "a" tags and the "i" tags were grouped together in CSS styling, causing a duplicate effect. I removed the "a" tag to eliminate the extra circle around the footer icons, then changed the hover effects to a different color and incorporated a scaled transition. 

![](FooterGif.gif)


### Creating Models for Rental Requests and Rental Surveys
My next user story was to build models for rental requests and rental surveys. I had a schema to follow as far as what to include in each model. After building the models, I scaffolded each one to create a controller with views for CRUD functionality. The result was the ability to view, add, edit, or delete entries via the website for rental requests and rental surveys. 

* [RentalRequest](https://github.com/CJScanlan/EntityFramework-CodeSummary/blob/main/RentalRequestB4Link.png)
* [RentalSurvey](https://github.com/CJScanlan/EntityFramework-CodeSummary/blob/main/RentalSurveyB4Link.png)

### Adding fully-defined navigation properties
The rental requests and rental surveys followed a 1-0-1 relationship. Each rental survey was required to have a rental request linked, but the rental requests did not require a related rental survey. On the rental request model, I added a virtual rental survey property as well as a rental survey ID to establish the foreign key. On the rental survey model, I added a required virtual rental request property, as well as a rental request ID. 

* [RentalRequest](https://github.com/CJScanlan/EntityFramework-CodeSummary/blob/main/RentalRequest.png)
* [RentalSurvey](https://github.com/CJScanlan/EntityFramework-CodeSummary/blob/main/RentalSurvey.png)

## Lessons Learned
This project taught me a wide array of lessons and experience with debugging issues. It required a lot of self teaching, as each user story included tasks that I have not always worked on before. I ran into issues with creating a fully-defined relationship with rental requests and rental surveys, but after reaching out for help I was able to figure out how to correctly set up the foreign key. I enjoyed my time working with a team on building a real-life application for a client. It was a fun project, and I took away many valuable lessons!

