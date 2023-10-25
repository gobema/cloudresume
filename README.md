# Packaging

The `base` branch can run the Snippetbox web application locally, but this involves manually setting up a local database
and configuring the `-dsn` flag to connect to it.

With the `build` branch, I implemented a container build and push GitHubs Actions workflow so that I can deploy the web
application to different environments.

I also added database migrations to create the necessary database tables when a container is run, and I created
the `config` struct to hold database secrets and environment variables, which I will implement as part of the
infrastructure deployment.

The build `branch` is my first addition to the Snippetbox code base.
