# NAME : iDATHA (data in Xhosa)


## Project Overview


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


###### User stories

```
"As a Case Manager, I want to add customer data to track program efficacy."
``` 

**Walk through the application from the user's perspective.**

```
Staff user will login and be authenticated. (No signup/ password assigned at first)
- Once logged in they can create new customer profile. They can view the profile and add 
activities, outcomes, customer file submitted.
- Staff can also view data dashboard with program key outcomes 
- Staff cannot edit the data once entered, but Admin can
```

**What will the user see on each page? What can they input and click and see?**


| Pages            |  Tabs           | Task/action                                                  |
| ---------------  | -------------   | -----------------------------------------------------  | 
| 1. Login page    | Login inputs    |                                                        |
| 2. Home page     | - Home          | Body displays a welcome message.                       |
|                  | - Customer      | - Name, last name or id input fields for search        |
|                  |                 | - An "add" button to add new customers                 |
|                  |                 | - on click adds input fields and save button         |
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
    day 1-2 
    [ ] Loging page (model {user}, forms {sign in}, views {signin, signout, changepassword}, template {base, frontpage})
    day 3-7 
    [ ] Home page: Home tab (company logo and welcome <h1>)
    [ ] Home page: Customer tab (model {profile,activity..}, forms {Searchform, Addform}, views {search, add}, template {customer})
    [ ] Home page: report tab (model {..}, views {}, template {canvas})
    
Week 2:
    [ ] Home page Customer tab .. (model {profile,activity..}, forms {Demographic,activities,files, outcomes,exit}, views)
    [ ] Home page Customer tab demographic tab
    [ ] Home page Customer tab activities tab
    [ ] Home page Customer tab   files tab 


Break:
    Add CSS

Week 3:
    [ ] Home page Customer tab   outcomes tab 
    [ ] Home page Customer tab   exit tab 
    Polish, troubleshoot, etc 
```
