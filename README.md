# Setting up conventional commits 

This guide will show you how to setup your project to make conventional commits easy to do as well as enforce that commits are entered as conventional commits

## Getting started

[Commitizen](https://github.com/commitizen/cz-cli) is a command line tool that you can install globally that makes conventional commits easy by walking you through the commit with prompts.  I suggest using this in the beginning until you get used to the structure.

If you have npm installed then installation is simple:

```
npm install -g commitizen
```  

One of the more popular adapters for Commitizen is [cz-conventional-changelog](https://github.com/commitizen/cz-conventional-changelog).

This can be installed using npm:

```
npm install cz-conventional-changelog --save-dev
```

After installing in your project you will need to add the following to your package.json file:

```json
"config": {
    "commitizen": {
      "path": "cz-conventional-changelog"
    }
}
```

With these two steps complete you can now run `git cz` after staging files for a commit like so:

```
git add file1 file2 file3
git cz
```

You should then be prompted for all the parts of your commit

```
? Select the type of change that you're committing: (Use arrow keys)
> feat:     A new feature
  fix:      A bug fix
  docs:     Documentation only changes
  style:    Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
  refactor: A code change that neither fixes a bug nor adds a feature
  perf:     A code change that improves performance
  test:     Adding missing tests or correcting existing tests
(Move up and down to reveal more choices)

```
