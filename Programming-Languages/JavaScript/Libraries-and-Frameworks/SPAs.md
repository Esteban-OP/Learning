# Single pages applications (SPAs)

SPAs load only one HTML page and dynamically update the content as the user interacts with the app, without relouding the entire page.

## How they work?

They use JavaScript to manage the application's state and render content. Instead of requesiting new HTML pages from server, SPAs use JS to manipulate the DOM and fecth data asynchronously using libreries and frameworks like React, Vue or Angular.

## Common issues

- Screen readers may struggle with dynamically update content.
- An SPA that renders new vieews without updating the URL leaves the back and forward buttons doing nothing, and gives the user no addres to bookmark.
- Search engines like Google (SEO) can have difficulty indecing dynamically loaded content because they may not execute JS properly or may miss content that isn't include in the initial HTML page.