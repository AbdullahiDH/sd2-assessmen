Week 2 – HTML Forms (GET and POST)
This week I made two HTML forms — one using GET and one using POST — and tested them with httpbin.org to see the difference between how they send data. I also styled them using Milligram CSS.

What I did
Made form-get.html that sends form data using GET. The data shows up in the URL and in the args section on httpbin.

Made form-post.html that sends form data using POST. The data is sent in the request body and shows in the form section on httpbin.

Added Milligram, Normalize.css, and Google Fonts to make the forms look better.

Used Chrome DevTools to check what was being sent and took screenshots to compare the two methods.

Difference between GET and POST
GET: puts the data in the URL, so it’s visible in the address bar and can be bookmarked or shared.

POST: sends the data in the background, so it’s not shown in the address bar.

On httpbin, GET data is under "args", POST data is under "form".

