# Contributing to the Netuitive Agent Ansible Playbook
Contributions are welcome and can be represented in many different ways as noted below. Help is greatly appreciated and credit will always be given.

## Labels
| Name          | Description   |  
| ------------- |---------------|
| bug           | Reserved for describing anything from degraded performance to errors. |
| feature       | Reserved for ideas and functionality that is *not* currently available in the project.      |
| question      | Reserved for questions about the functionality (or lack thereof) of the project.      |
| help wanted   | Reserved for users both inside and outside of Netuitive wanting a feature built or wanting help building a feature.     |
| improvement   | Reserved for ideas and enhancements to existing functionality in the project.     |
| documentation | Reserved for improvements or additions to the project's documentation. We can always use more documentation!    |
| wontfix     | Typically invoked by Netuitive users when something is deemed unfixable under current circumstances or not worth fixing.    |
| on-hold       | Typically invoked by Netuitive users when we're waiting on additional functionality first or the issue isn't worth fixing currently.    |
| duplicate     | Reserved for issues that duplicate existing or previously resolved issues.      |

## Workflow

1. If you're looking to help, find a `bug`, `feature`, `help wanted`, `improvement`, or `documentation` issue and claim it to let us know you're working on it. If you're using the project and encounter a bug or think the project could be improved but you're not sure how to implement the improvement, create an issue and label it appropriately; your workflow will end here unless you pick up the issue later. If you don't see something that matches up with what you want to work on or have worked on, skip to the next step.

1. Fork the repo and clone it locally.

1. Setup your upstream (just in case).  
`$ git remote add upstream https://github.com/main-repo/name.git`

1. Create a new branch from the *Develop* branch. Please name your branch based on the type of issue it's referencing, e.g., `bug/description`, `feature/description`, or `improvement/description`.  
`$ git checkout -b feature/magic-numbers develop`

1. Maintain your fork as necessary by staying in sync with the your upstream.
    ```
    git checkout feature/my-new-feature
    git fetch -a
    git pull --rebase upstream develop
    git push --force-with-lease origin feature/my-new-feature
    ```

1. Make your changes and keep pushing commits to the initial branch using `--amend`/`--rebase` as necessary. Don't mix
unrelated issues in a single branch.   
**Note:** Reference issues by the `closes #XXX` or `fixes #XXX` notation in the commit
message. Please use a descriptive, useful commit message that could be used to understand why a
particular change was made.

1. Clean up the branch (rebase with develop to synchronize, squash, edit commits, test, etc.) to
prepare for it to be merged.

1. Open a pull request comparing your fork to the main repo. If you aren't sure your PR will solve the issue
or may be controversial, we're okay with you opening an issue separately and linking to it in
your PR. That way, if the PR is not accepted, the issue will remain and be tracked.   
**Note:** Travis will run automatically once you've submitted your PR. Our Travis tests also use Rubocop for testing your Ruby syntax. If the Travis build fails, you should be able to access the link to the build to see what failed and then make commits accordingly.

1. After reviewing your commits for documentation, passed continuous integration (CI) tests,
version bumps, changelogs, and good, descriptive commit messages, a project maintainer can merge your request.

1. Create/update the changelog if necessary.
