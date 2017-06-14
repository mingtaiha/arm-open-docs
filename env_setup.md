Upgraded to use Python 3.6.1

Set up virtualenv with:
`virtualenv -p python3.6 <venv_name>`

Instsalled required packages from `requirements.txt`
'pip install --upgrade -r requirements.txt'

This file is also used by Heroku deployment system to install the correct packages


Needed to add `RUN bash setup-env.sh` to Dockerfile in order pass enviornment variables
to Docker container


Needed to apply for API keys for Stripe and Google Analytics (GA)
