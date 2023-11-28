# Walking An Application

Manually review a web application for security issues using only your browsers developer tools. Hacking with just your browser, no tools or scripts.




# 1: Walking An Application

In this room you will learn how to manually review a web application for security issues using only the in-built tools in your browser. More often than not, automated security tools and scripts will miss many potential vulnerabilities and useful information.

  

Here is a short breakdown of the in-built browser tools you will use throughout this room:

- **View Source** - Use your browser to view the human-readable source code of a website.
- **Inspector** - Learn how to inspect page elements and make changes to view usually blocked content.
- **Debugger** - Inspect and control the flow of a page's JavaScript
- **Network** - See all the network requests a page makes.

Start the virtual machine on this task, **wait 2 minutes**, and visit the following URL: [https://LAB\_WEB\_URL.p.thmlabs.com](https://lab_web_url.p.thmlabs.com/)[](https://lab_web_url.p.thmlabs.com/) _(this URL will update 2 minutes from when you start the machine)_




# 2: Exploring The Website

As a penetration tester, your role when reviewing a website or web application is to discover features that could potentially be vulnerable and attempt to exploit them to assess whether or not they are. These features are usually parts of the website that require some interactivity with the user.  
  
Finding interactive portions of the website can be as easy as spotting a login form to manually reviewing the website's JavaScript. An excellent place to start is just with your browser exploring the website and noting down the individual pages/areas/features with a summary for each one.

An example site review for the Acme IT Support website would look something like this:

<table class="table table-bordered"><tbody><tr><td style="background-color:#008EFF;color:#FFFFFF"><b>Feature</b><br></td><td style="background-color:#008EFF;color:#FFFFFF"><b>URL</b><br></td><td style="background-color:#008EFF;color:#FFFFFF"><b>Summary</b><br></td></tr><tr><td>Home Page<br></td><td>/<br></td><td>This page contains a summary of what Acme IT Support does with a company photo of their staff.</td></tr><tr><td>Latest News<br></td><td>/news<br></td><td>This page contains a list of recently published news articles by the company, and each news article has a link with an id number, i.e. /news/article?id=1<br></td></tr><tr><td>News Article<br></td><td>/news/article?id=1<br></td><td>Displays the individual news article. Some articles seem to be blocked and reserved for premium customers only.<br></td></tr><tr><td>Contact Page<br></td><td>/contact<br></td><td>This page contains a form for customers to contact the company. It contains name, email and message input fields and a send button.<br></td></tr><tr><td>Customers<br></td><td>/customers<br></td><td>This link redirects to /customers/login.<br></td></tr><tr><td>Customer Login<br></td><td>/customers/login<br></td><td>This page contains a login form with username and password fields.<br></td></tr><tr><td>Customer Signup<br></td><td>/customers/signup<br></td><td>This page contains a user-signup form that consists of a username, email, password and password confirmation input fields.<br></td></tr><tr><td>Customer Reset Password<br></td><td>/customers/reset<br></td><td>Password reset form with an email address input field.</td></tr><tr><td>Customer Dashboard<br></td><td>/customers<br></td><td><p>This page contains a list of the user's tickets submitted to the IT support company and a "Create Ticket" button.<br></p></td></tr><tr><td>Create Ticket<br></td><td>/customers/ticket/new<br></td><td>This page contains a form with a textbox for entering the IT issue and a file upload option to create an IT support ticket.<br></td></tr><tr><td>Customer Account<br></td><td>/customers/account<br></td><td>This page allows the user to edit their username, email and password.<br></td></tr><tr><td>Customer Logout<br></td><td>/customers/logout<br></td><td>This link logs the user out of the customer area.<br></td></tr></tbody></table>

We will start taking a deeper look into some of the pages we have discovered in the next task.




# 3: 