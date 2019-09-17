Assignment 3 - Persistence: Two-tier Web Application with Flat File Database, Express server, and CSS template
===
## Ramen Ordering Website
Carla Duarte

http://a3-ciduarte.glitch.me

Login Credentials:
Username: carla
Password: 1234

My project was inspired by a restaurant in Cambridge, MA called Yume Wo Katare.
The only thing on the menu is a bowl of ramen, and you get to choose how many pieces
of pork you'd like. Before starting the meal, customers are encouraged to share their
dream with the chef.

My website features an order form and a table to view all of the orders fetched from
the server. Within the table, you can edit or delete entries from the database.

### Challenges
The challenges I faced were primarily around documentation, specifically with the Material
framework and Passport middleware. Implementation of some of the Passport functions was unclear,
and Material had inconsistent component instantiation methods. Specifically with Material, I chose
to use the precompiled all-in-one CSS and JS bundles from unpkg. There wasn't a lot of clarity
around how to configure certain features using this approach.

### CSS Framework
- **Material.io**: I had recently attended a conference where I got to learn about the
design process that Google used while creating the Material.io design strategy, so I 
was inspired to learn and implement it for this assignment. I made custom CSS changes
to account for font and theme colors, as well as features that Material did not provide
such as a hero image, center alignment within divs, etc.
- **Note**: Aside from the responsive layout that Material offers, I preferred my design
in Assignment 2 using my custom CSS over the design I achieved in this assignment.

### Middleware
- **body-parser**: Parses HTTP request body into JSON.
- **compression**: Compresses HTTP responses.
- **serve-static**: Serves static files.
- **passport**: Authenticates users.
- **express-session**: Establishes a session using a cookie upon user login.
- **helmet**: Secure apps by setting various HTTP headers.

### Authentication/Database
I chose to use passport-local and lowdb because they were the easiest to implement.

### Technical Achievements
- **Logout**: I implemented passport's logout capability so that multiple users can log in/out
without having to restart the server.
- **User Sign Up**: Rather than adding a new user based on the input of a new user & password
combo, I created a feature that allows users to select to create an account.

### Design/Evaluation Achievements
- **Responsive layout**: A goal I set in the last project was to focus on creating a responsive layout
that was optimized for both mobile and desktop. Through the use of Material.io, I was able to control
how all the components on the page scaled up or down.
- **Error handling**: I separated my login functionality into a separate HTML file, so when you
access the ordering platform, it's done through the url "orderPlatform.html". Because you can bypass
the login by typing in "orderPlatform.html" in the browser, I added error handling that asks the user
to login if they attempt to view the order history tab or if they try to place an order.