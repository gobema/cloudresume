# Owner

The `owner` branch introduces a small update to the `users` database table, but this update provides a major change in
user experience. It allows me to create two types of users: reviewers and owners. Now I can control who can create
posts, similar to a personal blog post, so as an owner, I can limit posts to sections of my résumé for review.

The objectives I want to achieve with this change:

* access to the signup page to create an owner during an initial deployment
* access to the signup page by an owner to create reviewers
* access to only the login page if not logged in
* no access to the signup and create page by a reviewer

To implement this change, I needed to make several updates to the code base.

In the Users model, I added the `Owner` boolean and updated and created methods for the new feature. From here, I'm able
to rely on the pattern of the authentication feature, so I backtracked down a path that is the core of web application
design: middleware, routes, handlers, and helper functions to implement my new feature. The design of the Snippetbox
code base facilitates these changes. Finally, I updated existing tests and mock data.

As with the `reviews` branch, the `owner` branch builds and runs. If you want to host your own cloud résumé based on
this repository, the `owner` branch includes all the basic features that I wanted to add without any personal changes,
which I will be adding to the branch `cloudresume`.
