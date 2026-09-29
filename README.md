# SalesforceMarketingCloudProject2026
End-to-end email marketing project in Salesforce Marketing Cloud Exact Target Org: Data, Content, Segmentation, Automation and Journey Builder.
# Northern Trail Outfitters: Salesforce Marketing Cloud Project

An end-to-end email marketing implementation built in Salesforce
Marketing Cloud (Email Studio, Content Builder, Automation Studio,
Journey Builder) as part of the "Essentials for Marketing Cloud
Email Marketers" course.

## What I built
- Subscriber list and sendable/non-sendable data extensions (NTOSubscribers, 15 fields)
- Reusable email templates, dynamic content and an image carousel
- Welcome, Newsletter and Customer Anniversary emails with personalization
- Segmentation using data filters, filtered DEs and SQL query activities
- Automations for file import, data refresh and a Welcome Series
- Journey Builder journeys: Customer Anniversary and Birthday (capstone)

## Tools & skills
Email Studio · Content Builder · Contact Builder · Automation Studio ·
Journey Builder · Data Extensions · SQL · Segmentation · Personalization ·
Email testing and reporting

## Project walkthrough
Modules Covered:
1.Data Setup: Created List and imported contacts, created Sendable as well as Non Sendable Data Extensions.

2.Content Creation inside Email Studio: Created folders, uploaded images in content library, Created emails using Template, Built Reusable content blocks such as Image Carousels, Dynamic Content etc.,incorporated personalization in email content. Created 3 different emails as Customer Anniversary, Welcome, Monthly Newsletter etc.

3.Testing and Analytics: Previewed emails with subscriber data and test the ProperCase function, then sent email with Send Flow to the Test Data Extension. Reviewed tracking (sends, clicks, link view), ran and scheduled the Single Email Performance by Device report, and analyzed a report table of bounces, open rates and click rates.

4.Segmentation: built filtered data extensions (for example Welcome Step 1, Birthday Reminder, myNTO Members, US Hiking and Climbing), then data filters and filter activities for automations; used a Measure (clicks on the "Latest Gear" link in the last 30 days) to segment. wrote SQL Query Activities (for example US myNTO Rewards)

5.Automation and Journey Builder: created a File Transfer and Import File activity and automated importing and refreshing data. Created a Triggered Email Definition (Adventure Welcome) and a Campaign (NTO Welcome Series) that groups the related Data Extensions and emails. Created Send Email activities and the Welcome Series automation (schedule, filter, wait, send). Built the Customer Anniversary data filter, filter activity and automation, created Customer Anniversary Journey in Journey Builder (DE entry source, scheduled by the automation, email, 1-minute wait) and tested it with Run Once.

6.Capstone Project: I designed and built my own journey in Journey Builder. The suggested campaign was the Birthday Campaign. It had a requirement to create at least one email (with dynamic content, a coupon image, an NTO website link and personalization), a test data extension and test data file with pre-existing teammates' emails, and an immediate testing.

## Capstone: Birthday Journey
Short Description: A one-email Birthday Campaign for Northern Trail Outfitters, built in Journey Builder. Each subscriber who enters the journey gets a personalized birthday email with a coupon image, a dynamic offer and a link to Amazon for claiming Birthday Gift. The journey is tested with a small test data extension before any wider rollout.

Goal: Delight subscribers on their birthday and encourage them to redeem the birthday coupon on Amazon Website using data extension, email content, journey Orchestration

Audience: the records in the BirthdayTest data extension that has Birthday dates of me and my colleagues. I also created segment within audience with condition as myNTO Rewards members (myNTOLevel is not empty) and non-members.

Logic:
1. Entry source: the journey pulls contacts from the BirthdayTest data extension, using Run Once with Evaluate all records. In production, a data filter on Birthday (Is the Anniversary of → Today) feeds the journey through an automation
2. Send: each contact receives the NTO Birthday Email. The subject and H1 use %%FirstName%% for personalization.
3. Dynamic content rule:
If myNTOLevel is not empty, show Birthday Offer - myNTO Member (coupon plus a rewards bonus).
Otherwise, show the default Birthday Offer - Standard (coupon only).
4. Call to action: a button links to Amazon website with a tracking alias, so clicks can be measured.
5. Wait: a 1-minute wait after the send, as in the guide's anniversary journey, then the contact exits.
6. Test and verify: activate the journey, check inboxes for you and your teammates, and confirm the name, coupon image, link and correct dynamic block. Then check the journey's contact counts.

## Note
Screenshots are from a training org. All personal data is sample data.
