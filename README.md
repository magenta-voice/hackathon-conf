# hackathon-conf

## Motivation

The intention of this repository is to provide an interface for the [rhapsody hackathon]() participants to configure
their skills for the configurations that are not available/exposed in the [SDP - skill development platform]() yet.

In the future all of the things you can do here should and will be consolidated into the SDP.

For the course of this hackathon we decided only to expose the RegexNLU mechanism to build skills.
In case you want to use a [LUIS model](https://eu.luis.ai/) please contact the organisational team in the [slack](https://remoterhapsod-wxc4115.slack.com). 

## How to use

### I want to build a simple skill without a reprompt model

Fork this repo, and create a pull request (after rebasing your master branch with the master branch of this repository) in your
`TEAM_XY_` folder.

Create the regex NLU for your usecase like so:

```json
[
  {
    "name": "TEAM_XY_<INTENT_NAME>",
    "pattern": "you want to catch everything after this sentence (.*)",
    "entities": ["caught_stuff"]
  }
]
```

Create your domain context metadata using [dcm](https://github.com/4thel00z/dcm/releases/latest):

[![asciicast](https://asciinema.org/a/dMSSqApnb5XKtb3YpP40WTZH5.svg)](https://asciinema.org/a/dMSSqApnb5XKtb3YpP40WTZH5)


### I want to build a simple skill with a reprompt model

Same as above. Just fill out answer-regex.json out.

## License

This project is licensed under the GPL-3 license.
