# gitcd

Provide a git repository and execute an arbitrary deployment command on changes.

## Dependencies

- git
- bash

## Configuration

Ensure that git is configured so that it has proper access to the repository.

## Usage

````
gitcd -r "/path/to/git/repo" -c "deployment command"
````

### Example Cron

````
*/5 * * * * /usr/bin/gitcd -r "/src/my_application" -c "make deploy" >> /var/log/gitcd.log 2>&1
````

## What About...

I manage the deployments of enterprise applications to scalable infrastructure using multiple CI/CD platforms. I have fleets of build and deployment servers across platforms, cloud providers, and configurations. These are all fully automated and containerized and can be scaled immediately upon demand.

This is not for that. This is for my tiny static HTML website and some other cruft. It goes without saying, this probably shouldn't be relied on for production systems.
