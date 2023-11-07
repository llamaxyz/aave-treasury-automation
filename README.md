# aave-treasury-automation

AAVE v3 Treasury Claim Automation

## Setup

### Remote

The apps in this repository are hosted on [Modal](https://modal.com/) which is an end-to-end stack for cloud compute.

Install the modal client locally

```
pip install modal
```

Setup an API token for your organization through the Modal dashboard and follow the relevant commands to link it to your local client. Your token and key should be automatically set locally in the `/Users/<user>/.modal.toml` file once you follow the instructions.

Switch your Modal environment locally to use your organization's profile.

```
modal profile activate <org>
```

Check if the right Modal environment has been set.

```
modal profile current
```

Go through the [documentation](https://modal.com/docs/guide) in order to understand how Python programs work in Modal.

### Local

Install pipenv for local python virtual environment and package management.

```
brew install pipenv
```

Setup pipenv environment at root of this repository for all required packages to be installed

```
pipenv install
```

## Testing

Modal makes it easy to test your application locally while running the actual compute on their cloud compute environment

```
pipenv shell
```

```
modal run aave-treasury-automation/main.py
```

## Deployment

Modal makes it very easy to deploy, build and test in their cloud compute environment

```
pipenv shell
```

```
modal deploy aave-treasury-automation/main.py
```
