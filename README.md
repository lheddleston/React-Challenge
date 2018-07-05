# React-Challenge


## Engineering Challenge Part 1

Build a web server that has 2 endpoints. These endpoints will interact with other
pages on the web to get html information from them. All responses from your application
should be in application/json format!
### Endpoint #1:
The first endpoint should return all tags that match the user-passed tag value on
the page passed in the endpoint value.
Request signature:
- http://your-web-address.com/parse?endpoint=www.cobalt.io&tag=h1
In the above example request your server should output a list of the h1 tags from
the ‘endpoint’ url in a json format.
Example output:
{
h1 : [
{
innerText: ‘Pen Testing as a Service for Modern SaaS Businesses’,
innerHtml: ‘<span class="text-nowrap">Pen Testing as a Service</span> <span
class="text-nowrap">for Modern SaaS Businesses</span>’ },
{
innerText:’Crowdsourced Pen Testing for Modern SaaS Businesses ‘,
innerHTML:’<span class="text-nowrap">Crowdsourced Pen</span> <span
class="text-nowrap">Testing for Modern</span> <span class="text-nowrap">SaaS Businesses</span>’
}
... ]
}
### Endpoint #2:
The second endpoint should check to see if a given page contains a certain html
tag that has certain text inside of it.
- http://your-web-address.com/contains?endpoint=www.cobalt.io&tag=h1&text=Pen%252
0Testing%2520as%2520a%2520Service
Example Output:
{
exists: true
}
This would return true as ​www.cobalt.io​ contains an H1 tag with the text
“Pen Testing as a Service”. If this wasn’t the case it would return exists: false.

## Engineering Challenge Part 2

Please build a front end preferably using React.js & Redux that interacts with
the endpoints in Part 1.
Your front end should load a page with two text input fields and a submit button.
The input fields: one for “Endpoint” and one for “Tag”.
When the submit button is clicked, the app should make a call to the backend endpoint #1.
It should include the values from the text inputs.
The app should take the response and store it in Redux.
You can then chose to display the response from endpoint #1 on screen however you’d like!
