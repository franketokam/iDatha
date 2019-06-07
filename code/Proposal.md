# NAME : iDATHA (data in Xhosa)
===============================================================================

## Project Overview
---------------------------------------------------------------

**What are the major features of your web application?**

```
A data entry application with forms for customer intake, file review and a report dashboard.
```

**What problem is it attempting to solve?**

```
Create a simple interface for organization case manager, and allow manager to view automated program outcomes.
```

**What libraries or frameworks will you use?**

```
I'm planning on using  HTML, Bootstrap, ChartJs for charts and Django as a back end.
(the initial goal was a Desktop app with Electron JS)
```
## Features
---------------------------------------------------------------

###### User stories

```
"As a Case Manager, I want to add customer data to track program efficacy."
``` 

**Walk through the application from the user's perspective.**

```
Staff user will login and be authenticated. (No signup/ password assigned at first)
> Once logged in they can create new customer profile. They can view the profile and add activities, outcomes, customer file submitted.
> Staff can also view data dashboard with program key outcomes 
> Staff cannot edit the data once entered, but Admin can
```

**What will the user see on each page? What can they input and click and see?**

```
| Pages            |  Tabs           | Tasks                                                  |
| ---------------  | -------------   | -----------------------------------------------------  | 
| 1. Log in        | - Login inputs  |                                                        |
| 2. Landing page  | - Home          | Body displays a welcome message.                       |
|                  | - Customer      | - Name, last name or id input fields for search        |
|                  |                 | - An "add" button to add new customers                 |
|                  |                 |   > on click add input fields and save button          |
|                  | - Report        | - Count of customers                                   |
|                  |                 | - chart of employed at intake vs at exit               |
|                  |                 | - chart in disconnected from school at intake vs exit  |
|                  |                 | - chart Quarterly Work Experience count                |
| 3. Result page   |  - Demographic  | form to add no edit                                    |
|                  |  - activity     | sections with add button to add form                   |
|                  |  - file         | sections with add button to add form                   |
|                  |  - outcomes     | sections with add button to add form                   |
|                  |  - exit         | sections with add button to add form                   |
|                  |  - outcomes     | sections with add button to add form                   |
```

**How will their actions correspond to events on the back-end?**

```
1. Log in : sign up authentification
2. get customer record and populate customer tab
3. post request will create a new customer record
4. post request to add data (Demographic, file, activity, outcomes, exit)
5. get request to view data on the page as we add
```

###### Data Model
```
1. 'Profile'
2. 'Activity' 
3. 'Outcome'
4. 'Exit'
5. 'file'
```

###### Schedule
```
Week 1: 
    - [x] Set up repository
    - [ ] Start new Django project
    - [ ] Start apps account and profile
    - [ ] design models 
    - [ ] add urls
    
      
Week 2:
    - [ ] add views 
    - [ ] add templates (login, home with tabs)
    - [ ] add Javascript
    - [ ] link view to templates :tired_face:
       
Break:
    Add with CSS

Week 3:
    Polish, troubleshoot, etc :clap:
```
