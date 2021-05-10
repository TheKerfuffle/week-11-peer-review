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
  - [ x ] Able to add feedback
    - [ x ] Data collected on individual pages & components
    - [ x ] Click on next takes you to the next page in sequence
    - [ x ] Data saves in DB after *all* the parts are completed (not piecemeal)
    - [ x ] Thank you page takes you back to the first view
    - [ 0* ] Old Data is cleared on form completion
      * Old data is not cleared from the store on submit. Still works, as the comment form will submit an empty string if no new comment is added

- Client code:
  - [ x ]  Individual components for each form part
  - [ x ]  Redux setup complete
    - [ x ] Store linked to react with `<Provider>`
    - [ x ] Store setup with reducer(s) and logger middleware 
  - [ x ] Reducers & Actions Working
    - [ x ] Actions are in SCREAMING_SNAKE_CASE and semantically named
    - [ x ] Actions have a `type` key, and `payload` if sending data
    - [ 0*] Reducers are returning a new state, or the old state (not mutating)
      * There is one type of command for each reducer. It does not effect functionality at all and the code works as intended, but we do not clear out the states ever, just set it to a new state
    - [ 0 ] Reducers are using spread correctly (to keep old data, while adding new)
      *Not at all needed for this project, the way you have it set up.
  - [ x ] Review Component shows at all times with current redux state
  - [ x ] React-Redux Working
    - [ x ] Dispatching actions onClick
    - [ x ] Grabbing data from the redux store with `useSelector`
  - [ x ] Axios POST request to add feedback


- Server code:   
  - [ x ] Router made for GET, POST
    * Stretch goals for get route not done


## General Items
Feedback should be provided for these items, but they do not impact scoring.

- Git 
  - [ x ] Multiple git commits showing incremental progress
  - [ x ] Commits are descriptive of the changes made or feature added 
  - [ x ] Has .gitignore with node_modules
  - [ x ] Readme file updated (assuming this is previously discussed)
- Code Style 
  - [ x ] Appropriate amount of code comments
  - [ x ] Code is consistently formatted
- Client
  - [ x ] Appropriate use of HTML tags
  - [ x ] Basic CSS styling with margins/padding
    * No new styling, but the project looks good, so def not needed


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
Hey ___,

General Feedback.

---
| Functional Requirements | Complete? | yes
| --- | :---: |
| Multi page form with client side routing and navigation (next button) | yes |
| Data stored in Redux when navigating from page to page | yes |
| User is notified when trying to leave a blank score | yes |
| Review Component displays scores and comments from current redux state | yes |
| Submit button sends data to the server via Axios | yes |
| Confirmaion Page displays after data is POSTed to the server | yes |
| Button on Confirmation Page clears Redux and starts a new survey | yes |
| Views are broken down into components | yes |

---
### Notes:

Notes on the above Functional Requirements.

---
| General Items | Complete? |
| --- | :---: |
| More than 15 git commits | yes |
| Commits are descriptive of the changes made or feature added | yes |
| Readme file updated | yes |
| Appropriate amount of code comments | yes |
| Code is consistently formatted | yes |
| Server code organized with router & module files | no | 
 *Really not necessary for this project though...

---
### Notes:

Notes on General Items

```
I think this is a really tight and clean project! Your code works as intended! The only thing is that you don't clear out the reducers at any point. You shouldn't need to for how your code works though. Otherwise I think everything looks really good for base mode!