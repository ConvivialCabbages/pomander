# Pomander
> */pōˈmandər,ˈpōˌmandər/* (noun) -
> a ball or perforated container of sweet-smelling substances such as herbs and spices, placed in a closet, drawer, or codebase to perfume the air or (formerly) carried as a supposed protection against infection.

## System Requirements 
You need a working copy of [yarn](https://yarnpkg.com/en/), the fast, reliable, and secure dependency manager.

Using yarn, install ESLint:

```
yarn add eslint --dev
```

## Installation
Within a git repository, run the following command:
```sh
curl -s https://raw.githubusercontent.com/mementologists/pomander/master/bin/install | bash
```

## Usage
Pomander uses a pre-commit hook to run staged JavaScript files through ESLint before each commit.
This version uses the locally-installed version of eslint to enable use of npm-installed style guide/eslint configurations like eslint-config-airbnb.

Within your package.json, add the following script:
```
"pomander": "curl -s https://raw.githubusercontent.com/mementologists/pomander/master/bin/install | bash"
```

Then run the command: 
```
yarn run pomander
```

You can also add the command as a postinstall script:
"postinstall": "curl -s https://raw.githubusercontent.com/mementologists/pomander/master/bin/install | bash"

[ESLint](http://eslint.org/) is a popular linter that checks your code for syntax and style errors. By default, ESLint only checks for syntax errors. (http://eslint.org/docs/user-guide/getting-started) 

To skip Pomander, commit with the `--no-verify` option.
