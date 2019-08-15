# Contributing to RattleIn

* [Code of Conduct](#code-of-conduct)
* [Issues](#issues)
* [Pull Requests](#pull-requests)
* [How Your Change Gets Merged](#merge)

## [Code of Conduct](./doc/guides/contributing/coc.md)

This project has a
[Code of Conduct](https://github.com/nodejs/admin/blob/master/CODE_OF_CONDUCT.md)
to which all contributors must adhere.

See [details on our policy on Code of Conduct](./doc/guides/contributing/coc.md).


## Issues

### How to Contribute in Issues
For any issue, there are fundamentally three ways an individual can
contribute:

1. By opening the issue for discussion: For instance, if you believe that you
   have uncovered a bug in this project, creating a new issue in the 
   issue tracker is the way to report it.
   
2. By helping to triage the issue: This can be done either by providing
   supporting details (a test case that demonstrates a bug), or providing
   suggestions on how to address the issue by Jira
   
3. By helping to resolve the issue: Typically this is done either in the form
   of demonstrating that the issue reported is not a problem after all, or more
   often, by opening a Pull Request that changes some bit of something in
     in a concrete and reviewable manner.

## Pull Requests

### How to Submit A Change
1. Fork this repo
You should create a fork of this project in your account and work from there. You can create a fork by clicking the fork button in GitHub.

2. One feature, one branch
Work for each new feature/issue should occur in its own branch. To create a new branch from the command line:

    ```git checkout -b my-new-feature```
    ** where my-new-feature describes the ticket that you're working on

3. Check code style
Before opening a pull request, your new code should conform to the style guide. Projects scaffolded using HomeAway's generators will include eslint and the HomeAway style guide. Code style can be checked by running:

    ```npm run test:style```

4. Add tests for any bug fixes or new functionality
Our goal for framework code is to keep coverage above 95%. Tests can be run by executing:

    ```npm test```
    
Mocha will execute your tests, and notify you of any errors in your code or in style. Istanbul will prepare a coverage report, which can be found at docs/reports/coverage/html/index.html.

5. Add documentation for new or updated functionality
This project uses JSDoc-formatted inline documentation to generate reference materials. If your changes would alter the behavior of existing functions, please update the inline docs. Similarly, please document any new functionality. Before opening a PR, check to see if your inline documentation is rendered correctly by running:

    ```npm run documentation```

6. Add to CHANGELOG.md
Any notable changes that are made should be recorded in the changelog as a bullet point under the latest version. For more details on what a changelog is and how to maintain one, check out Keep a Changelog.

7. Squash commits
Your PR should only have a single, descriptive commit. This helps to keep the project commit history from becoming cluttered. The preferred way to do this is is to run

    ```git rebase -i <commit-hash>```
where is the hash of the commit immediately preceding yours.

8. Submit PR and describe the change
Push your changes to your branch and open a pull request against the parent repo on GitHub. The project owner will review your pull request and respond with feedback.

## How Your Change Gets Merged
Upon PR submission, your code will be reviewed by maintainers.

They will confirm at least the following:

Tests run successfully. (unit, coverage, integration, style)
Contribution policy has been followed.
Two (human) reviewers will need to sign off on your project before it can be merged.
