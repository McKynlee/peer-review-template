# Weekend Challenge 11 - React-Redux Feedback Form

## Instructions

Reviewing code is an important role developers play. We're going to practice reviewing code from others.

- Get the repo url from your partner
- Get your partner's project running on your computer
- Review the code from your partner and give relevant feedback
- Complete the Markdown section and submit that in the notes section on the assignment app. (Make sure you include who's code you reviewed.)

Practicing compassionate code reviews is important (you can learn more from this video on the topic: https://www.youtube.com/watch?v=Ea8EiIPZvh0 )

## Review Checklist

## Base Required Features 

- Multi-Part Form:  
  - [x] Able to add feedback
    - [x] Data collected on individual pages & components
    - [x] Click on next takes you to the next page in sequence
    - [x] Data saves in DB after *all* the parts are completed (not piecemeal)
    - [x] Thank you page takes you back to the first view
    - [x] Old Data is cleared on form completion

- Client code:
  - [x]  Individual components for each form part
  - [x]  Redux setup complete
    - [x] Store linked to react with `<Provider>`
    - [x] Store setup with reducer(s) and logger middleware 
  - [ ] Reducers & Actions Working
    - [x] Actions are in SCREAMING_SNAKE_CASE and semantically named
    - [x] Actions have a `type` key, and `payload` if sending data
    - [x] Reducers are returning a new state, or the old state (not mutating)
    - [NA] Reducers are using spread correctly (to keep old data, while adding new)
  - [ ] Review Component shows at all times with current redux state
  - [x] React-Redux Working
    - [ ] `connect`ing components correctly & dispatching Actions onClick
    - [ ] `mapStateToProps` when data is needed from Redux for submission
  - [x] Axios POST request to add feedback


- Server code:   
  - [x] Router made for GET, POST


## General Items
Feedback should be provided for these items, but they do not impact scoring.

- Git 
  - [ ] Multiple git commits showing incremental progress
  - [ ] Commits are descriptive of the changes made or feature added 
  - [ ] Has .gitignore with node_modules
  - [ ] Readme file updated (assuming this is previously discussed)
- Code Style 
  - [ ] Appropriate amount of code comments
  - [ ] Code is consistently formatted
- Client
  - [ ] Appropriate use of HTML tags
  - [ ] Basic CSS styling with margins/padding


## Stretch Goals
First must be complete for score of _5 - Exceeds Expectations_

- Previous Steps
  - [ ] allows a user to go to a previous step, either directly or by cycling backward thru the steps
  - [ ] user can upate their score for a step
    - [ ] new score is validated to not be empty
    - [ ] redux is updated with new score
  - [ ] user can continue on to review page and submit as in Base Mode


- Admin View
  - [ ] All entries are visible with correct data from inputs
    - [ ] Most recent is at the top
  - [ ] Can Delete an entry
    - [ ] User is prompted before deleting
  - [ ] Axios GET request to get all feedback for `/admin` view in componentDidMount

  Busywork Goals, consider removing or making more useful

- [ ] Styling with Material UI
- [ ] Ability to flag a feedback item on `/admin` for further review
- [ ] Deployed to Heroku


## Markdown

```
Hey Johnny Goth,

Awesome job on this app!  The layout is crisp and clean- I like your spacing on stuff.
I wrote notes below - I am a verbose person, so the length of notes is about me, not you!  I really like your app - well done on mastering redux/routers!!
---
| Functional Requirements | Complete? |
| --- | :---: |
| Multi page form with client side routing and navigation (next button) | yes |
| Data stored in Redux when navigating from page to page | yes |
| User is notified when trying to leave a blank score | yes |
| Review Component displays scores and comments from current redux state | yes |
| Submit button sends data to the server via Axios | yes |
| Confirmaion Page displays after data is POSTed to the server | yes |
| Button on Confirmation Page clears Redux and starts a new survey | no |
| Views are broken down into components | yes |

---
### Notes:

I love that you used number inputs to ensure the input stays within range, and that an alert shows up if it is left blank!  I noticed that if I leave the comment input empty, the Reducer breaks.  You might change that to either allow empty inputs, or give an alert that they have to say something (I think the instructions said ok to leave blank).
It took me a second to find the Review component since it is named 'Feedback'.  Something to consider to help when we've got a lot of components going on.
Super nice work on all of the routing and collecting the inputs!
Your current setup keeps the most recent inputs displaying on the review page instead of clearing them.  Not a huge deal, but you could also dispatch a CLEAR_INPUTS in the .then of your Feedback component post to reset your reducer and start fresh.
I saw some unused imports (like axios, useState and useEffect on the App.jsx component.  You may have been planning to incorporate those in the next stages of work, but if not you could go ahead and delete them to keep things clean.

---
| General Items | Complete? |
| --- | :---: |
| More than 15 git commits | no- 14 |
| Commits are descriptive of the changes made or feature added | yes |
| Readme file updated | To-Do |
| Appropriate amount of code comments | no |
| Code is consistently formatted | yes |
| Server code organized with router & module files | yes |
---
### Notes:

I really like the code comments you do have- I'd like to see more of them.  If I hadn't also done this project myself, it would take me some time to figure out what each component was doing.  A little explanation about what each component/function is for would be nice from an outside perspective.  Your code is generally very clean, though - bravo!
Eventually having a README that describes your app will be good for showing it off to employers (and how you are able to explain your app and show some screenshots).
Overall, nice work!  Thanks for sharing it with me.
```
