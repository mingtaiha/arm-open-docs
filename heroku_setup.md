To setup Heroku:

In `runtime.txt`, needed to change `python-3.5.1` to `python-3.6.1`
because Heroku only Python Buildpacks 2.7.13 and 3.6.1

In order to deploy app on Heroku:

Check this out:
`https://devcenter.heroku.com/articles/getting-started-with-python#introduction`

1) Install basic Heroku CLI (Depends on your OS)
2) Login to Heroku CLI `heroku login`
3) Clone a repository (or make one)
4) Create a git remote (`heroku`) with `heroku create [app_name]`
5) Make a commit, then push to heroku (`git push heroku master`)

Once the repo is pushed to Heroku, the app is deployed,
1) Get an instance of the app running `heroku ps:scale web=1`
2) Run `heroku open` to go to website with CLI, or visit the website
    received from 1)

NOTE: A free-tier app get 550 Dyno Hours (server-hours). To check
usage from Heroku CLI, `heroku ps -a <app_name>`

To check the logs of getting the app running, run `heroku logs --tail`
(Ctrl-C to quit)

This is a way to check for errors

If the app uses environment variables (which server.py does),
Set the env variables (Heroku calls config vars)
`heroku config:set <VAR_NAME>=<VAR_VALUE>`

To add a domain name to host the app, you can do it in...

Dashboard
Add a domain in the Heroku Dashboard, Settings

Heroku CLI

List the domains (Heroku Domain and Custom Domains)
`heroku domains`

Adding a domain
`heroku domains:add <domain_name>`

Removing a domain
`heroku domains:remove <domain_name>`
