# Test Plan


## Scope
 The scope of this Test plan is to give a short overview of what will be done during Testing lifecycle of Klausapp Dashboard. 

## Test Strategy

End-to-end testing framework is used as Testing Strategy and has three parts:

1. **Build User Functions:**
    1. Login
    2.  Check statistics on Dashboard:
        - Filter the view of Dashboard:
            - Time period
            - User
            - Feedback
            - Include/exclude self-review
            - Company
            - Time period
        - Views of 'cards':
            - Graph: 
                - Multiple-select
                - Different graph for different section
            - Matrix:
                - Sorting: increase/decrease

        - Internal quality score:
            - Year: Months/ quarters
            - Quarter: Weeks/Months
            - Last 30 days / last month: Days/Weeks
            - Last 7 days / last week: Days
    3. Check calculations of the Statistics on Dashboard in different sections:
        - Ratings by Category
        - Quality Scores
        - Scores by Category
        - Scores By tickets
    4. Possibility to change statistics:
        - Add comments
        - Add ratings
    5. Export file with statistics in each section:
        - Export All
        - Ratings by Category
        - Quality Scores
        - Scores by Category
        - Scores By tickets
    6. Scores by Ticket:
        - Change amount of viewable tickets
        - Possibility to go to ticket from Dashboard
    7. Logout


2. **Build Conditions**
    
    Login Page:
    - Successfully login
    
    Dashboard:
    - Overview
    - Choose suitable filter for Dashboard
    - Check the statistics and scores
    - Review tickets
    - Export 'card' data as excel file
    
    Logout
   

3. **Build Test Scenario:**


    As example below will be given one Test Scenario that covers the most functionality of Dashboard. But it can be splitted into multiple test cases.


    1.	Log in into the system
    2.	Check Dashboard Overview
    3.	Change Time period filter for last month
    4.	Change Reviewer to QA Test Account
    5.	Change feedback type by Received Feedback
    6.	Check quality scores
    7.	Check Ratings by category 
    8.	Check calculations of Total in Ratings by Category
    9.	Sort Scores by category by Ratings
    10.	Check calculations of Total in Scores by Category
    11.	Check Scores by ticket
    12.	Check Calculations of Total in Scores by Ticket
    13.	Change feedback type to Given feedback
    14.	Include Self-reviews
    15.	Check calculations of Quality Scores, Ratings by category, Scores by category
    16.	Export all cards
    17.	Export from Quality scores card
    18. Export from Scores by Category card
    19. Export from Ratings by Category
    18.	Logout

## Resources/Roles and Responsibilities

At the moment available resource is one QA specialist that will implement Automation Tests.

## Tools
1.  Cypress io: 
    -   Advantages:
        - comfortable to use, as members of the team can help with javascript
        - quite fast to develop and make test cases
        - Chrome famile and Firefox support
        - API testing is supported
        - cli support

    - Disadvantages:
        - supports only Chrome family and Firefox, means safari and ithers may not be tested with ithers
        - caanot be tested cases with external login(Google)

2. Selenium + any lang(Java is prefferable), in case of critical testing external login or not supported browsers by cypress

3. Postman for API testing, supports command line interface, that is needed CI

4. Any tool, that supports CI

## Schedule
- Test plan: 6 hours (once)
- Documentation review 30 min/day
- Manual Test Cases are documentation quality depended: 30 min/each 
- Automation Testing environment setting up: 8 hours
- Automation Tests: 30 min/each 
- Review: 30 min/day

## Environment
 Environment that is going to be used for testing KlausApp Dashboard is: 

 https://app.klausapp-staging.com/dashboard
## Deliverables
    
Deliverables are Test Scripts and comments to them created during Test Automation proccess. As Test Script is used Test Scenario

## Risks
- **Pesticide Paradox**
    
    Repeating the same test cases again and again will not find new bugs. So it is necessary to review the test cases and add or update test cases to find new bugs.

- **Too many UI tests can break testing**

    CSS and XPath locations in the UI change often. If you target attributes like these in automated tests, it can lead to false positives and continued maintenance when the changes weaken or break the tests.

- **Nonqualified Test Team**


    An automated software testing tool requires new skills for software testing engineers & test analysts, therefore additional training is required.
- **Inadequacy of the Test Tool**
    
    The automation tool must be in accordance to the company’s business needs with the test process introduced. The choice of the most adequate tool depends on characteristics of applications, test stages to be automated, as well as on the test policy adopted by the organization.

- **Attempt to automate every type of test**

    Exhaustive testing is not possible, as it takes a lot of effort, what is impractical


## Test Data
Test data was pre-created with no possibility to change it. It gives restrictions on doing Automation Tests. One of them is possibility to get in Pesticide paradox using fixed data.

**It is more reasonable to give access to create test data, as it gives overview on what happens and more reliable output/results**


## Reports/Results
Reports/ Results are usually provided by Test Tools(Cypress.io, Postman). In case of developing own Automation Test Tool it can be created and modified according to team needs.

Report must be readable for any team member and in it must be:

1. Test Scenario name
2. Steps
3. Pass/Fail
4. Time o run
5. Total of Passed/Failed Tests
6. Screenshot in case of Failed Tests



