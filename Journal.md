Sunnydale Solutions Journal
Phase 1: Form Foundation and Intercept

What did I accomplish?
I created an HTML feedback form with fields for the reviewer's name, star rating, and comments. I also added a JavaScript submit event listener that uses event.preventDefault() to stop the browser's default form submission. The entered values are logged to the browser console so I can verify that JavaScript can access the form data.

Why is preventDefault() necessary?
If I forget to call event.preventDefault(), the browser will perform its default form submission behavior, which can refresh the page or navigate to another location. Since this assignment processes feedback entirely in the browser without a backend server, preventing the default behavior allows JavaScript to handle the submission and display feedback directly on the page.

Testing and challenges
I tested the form by entering a name, selecting a rating, and writing comments. The browser console displayed the entered values, and the page did not refresh after submission. This confirmed that the submit event listener was working as expected.