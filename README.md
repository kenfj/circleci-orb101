# circleci-orb101
Use the Hello-Build Orb from https://circleci.com/docs/2.0/hello-world/

Simple Orb example of circleci/slack@0.1.10

## How to send slack messages using circleci/slack orb

* Slack side
  - https://api.slack.com/apps -> click `Create New App`
  - set some target slack Channel in the app
  - copy the `Webhook URL`
* CircleCI side
  - Add Project (for example this repo circleci-orb101)  
    https://circleci.com/add-projects/gh/kenfj
  - Project Settings  
    https://circleci.com/gh/kenfj/circleci-orb101/edit
  - add Environment Variables `SLACK_WEBHOOK` as the `Webhook URL`  
    https://circleci.com/gh/kenfj/circleci-orb101/edit#env-vars
* commit in GitHub then this project circleci-orb101
* it will send slack message to the channel as in the slack app settings
* details: https://circleci.com/orbs/registry/orb/circleci/slack


## Tips to create .circleci/config.yml quickly

* Config validation

```bash
brew install circleci       # if not installed
circleci config validate    # validate .circleci/config.yml
```

* YAML validation

```bash
cat .circleci/config.yml | ruby -r yaml -e 'YAML.load STDIN'
```
