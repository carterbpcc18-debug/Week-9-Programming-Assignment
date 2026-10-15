Sunnydale Solutions Journal
Phase 1: Form Foundation and Intercept

What did I accomplish?
I created an HTML feedback form with fields for the reviewer's name, star rating, and comments. I also added a JavaScript submit event listener that uses event.preventDefault() to stop the browser's default form submission. The entered values are logged to the browser console so I can verify that JavaScript can access the form data.

Why is preventDefault() necessary?
If I forget to call event.preventDefault(), the browser will perform its default form submission behavior, which can refresh the page or navigate to another location. Since this assignment processes feedback entirely in the browser without a backend server, preventing the default behavior allows JavaScript to handle the submission and display feedback directly on the page.

Testing and challenges
I tested the form by entering a name, selecting a rating, and writing comments. The browser console displayed the entered values, and the page did not refresh after submission. This confirmed that the submit event listener was working as expected.



Phase 2: Form Validation and Error Messaging

What validation approach did I take?
I used an array called errors to collect validation messages. I checked whether the name was empty after trimming whitespace, whether the rating was exactly 5, and whether the comments contained the word "wonderful" without considering capitalization.

Did I display errors all at once or one at a time?
I chose to display all applicable errors at once in the error container. This helps users understand everything they need to correct without repeatedly submitting the form. One disadvantage is that multiple messages can make the form look busy, but for this assignment, showing all errors together is more helpful than revealing them one at a time.

Testing and challenges
I tested an empty form and verified that all three validation messages appeared. I also tested a 4-star rating and comments that did not contain "wonderful" to check that the appropriate errors appeared. The validation logic was designed to accept the word regardless of capitalization, such as "Wonderful" or "WONDERFUL".



Phase 3: Successful Submission and Local Storage State

What did I accomplish?
I added a success message that appears when all validation rules pass. The reviewer's name is saved in localStorage under the key "reviewerName". After a successful submission, the form is cleared and hidden. When the page is loaded again, the saved name is retrieved, displayed in a welcome-back message, and placed back into the name field.

Why use localStorage instead of cookies?
localStorage is convenient for client-side state because it provides a simple way to store and retrieve data using JavaScript. The data remains available across page reloads and browser sessions without having to include it in every HTTP request.
Cookies may be preferable when information needs to be sent automatically to a server, such as for session management. Cookies also support settings related to expiration and security. For this assignment, localStorage is a suitable choice because the application only needs to remember the reviewer's name in the browser.

Testing and challenges
I tested the successful submission flow using a valid name, a 5-star rating, and comments containing "wonderful". The expected behavior is that the success receipt appears, the form is hidden, and the reviewer's name is stored in localStorage. After refreshing the page, the saved name should appear in the welcome-back message and be pre-filled in the form.