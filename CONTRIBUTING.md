# Contributing to CleanAPI

Hello, and welcome! Whether you are looking for help, trying to report a bug,
thinking about getting involved in the project or about to submit a patch, this
document is for you! Its intent is to be both an entry point for newcomers to
the community (with various technical backgrounds), and a guide/reference for
contributors and maintainers.

Consult the Table of Contents below, and jump to the desired section.

## Table of Contents

- [Where to seek for help?](#where-to-seek-for-help)
  - [Enterprise Edition](#enterprise-edition)
  - [Community Edition](#community-edition)
- [Where to report bugs?](#where-to-report-bugs)
- [Where to submit feature requests?](#where-to-submit-feature-requests)
- [Contributing](#contributing)
  - [Improving the documentation](#improving-the-documentation)
  - [Proposing a new plugin](#proposing-a-new-plugin)
  - [Submitting a patch](#submitting-a-patch)
    - [Git branches](#git-branches)
    - [Commit atomicity](#commit-atomicity)
    - [Commit message format](#commit-message-format)
    - [Static linting](#static-linting)
    - [Writing tests](#writing-tests)
    - [Writing performant code](#writing-performant-code)
  - [Contributor T-shirt](#contributor-t-shirt)
- [Code style](#code-style)

## Where to seek for help?

### Enterprise Edition

If you are a CleanAPI Enterprise customer, contact the Enterprise Support channels
by opening an Enterprise support ticket on
[https://support.cleanapi.io](https://support.cleanapi.io/).

If you are interested in becoming a CleanAPI Enterprise customer, please visit
https://cleanapi.io/cleanapi-enterprise-edition/ or contact us at
[sales@cleanapi.io](mailto:sales@cleanapi.io).

[Back to TOC](#table-of-contents)

### Community Edition

There are several channels where you can get answers from the community
or the maintainers of this project:

- Our public forum, [CleanAPI Nation](https://discuss.cleanapi.io), is great for
  asking questions, giving advice, and staying up-to-date with the latest
  announcements. CleanAPI Nation is frequented by CleanAPI maintainers.

**Please avoid opening GitHub issues for general questions or help**, as those
should be reserved for actual bug reports. The CleanAPI community is welcoming and
more than willing to assist you on those channels!

[Back to TOC](#table-of-contents)

## Where to report bugs?

Feel free to [submit an issue](https://github.com/fkacar/cleanapi/issues/new/choose) on
the GitHub repository, we would be grateful to hear about it! Please make sure
to respect the GitHub issue template, and include:

1. A summary of the issue
2. A list of steps to reproduce the issue
3. The version of CleanAPI you encountered the issue with
4. Your CleanAPI configuration, or the parts that are relevant to your issue

If you wish, you are more than welcome to propose a patch to fix the issue!
See the [Submit a patch](#submitting-a-patch) section for more information
on how to best do so.

[Back to TOC](#table-of-contents)

## Where to submit feature requests?

You can [submit an issue](https://github.com/fkacar/cleanapi/issues/new/choose) for feature
requests. Please add as much detail as you can when doing so.

You are also welcome to propose patches adding new features. See the section
on [Submitting a patch](#submitting-a-patch) for details.

[Back to TOC](#table-of-contents)

## Contributing

We welcome contributions of all kinds, you do not need to code to be helpful!
All of the following tasks are noble and worthy contributions that you can
make without coding:

- Reporting a bug (see the [report bugs](#where-to-report-bugs) section)
- Helping other members of the community on the support channels
- Fixing a typo in the code
- Fixing a typo in the documentation at https://docs.cleanapi.io (see
  the [documentation contribution](#improving-the-documentation) section)
- Providing your feedback on the proposed features and designs
- Reviewing Pull Requests

If you wish to contribute code (features or bug fixes), see the [Submitting a
patch](#submitting-a-patch) section.

[Back to TOC](#table-of-contents)

### Improving the documentation

The documentation hosted at https://docs.cleanapi.io is open source and built
with [Jekyll](https://jekyllrb.com/). You are welcome to propose changes to it
(correct typos, add examples or clarifications...) and contribute to the
[CleanAPI Hub](https://docs.cleanapi.io/hub/)!

The repository is also hosted on GitHub at:
https://github.com/fkacar/docs.cleanapi.io/

[Back to TOC](#table-of-contents)

### Proposing a new API Integration

If you wish to write a new API integration script for your own needs, you should start by
reading the [API Integration Development
Guide](https://docs.cleanapi.io/latest/api-integration-development).

If you already wrote a plugin, and are thinking about making it available to
the community, we strongly encourage you to create a pull request.

To give visibility to your integration script, we advise that you:

1. [Add your
   script](https://github.com/fkacar/docs.cleanapi.io/blob/master/CONTRIBUTING.md#contributing-to-cleanapi-documentation-and-the-cleanapi-hub)
   to the [CleanAPI Hub](https://docs.cleanapi.io/hub/)
2. Create pull request
3. Create a post in the [Announcements category of CleanAPI
   Nation](https://discuss.cleanapi.io/c/announcements)

[Back to TOC](#table-of-contents)

### Submitting a patch

Feel free to contribute fixes or minor features, we love to receive Pull
Requests! If you are planning to develop a larger feature, come talk to us
first!

When contributing, please follow the guidelines provided in this document. They
will cover topics such as the different Git branches we use, the commit message
format to use or the appropriate code style.

Once you have read them, and you are ready to submit your Pull Request, be sure
to verify a few things:

- Your work was based on the appropriate branch (`master` vs. `next`), and you
  are opening your Pull Request against the appropriate one
- Your commit history is clean: changes are atomic and the git message format
  was respected
- Rebase your work on top of the base branch (seek help online on how to use
  `git rebase`; this is important to ensure your commit history is clean and
   linear)
- The static linting is succeeding: run `yarn lint`, or `npm run link .` (see the
  development documentation for additional details)
- The tests are passing: run `yarn test`, `npm run test`, or whichever is
  appropriate for your change
- Do not update CHANGELOG.md yourself. Your change will be included there in
  due time if it is accepted, no worries!

If the above guidelines are respected, your Pull Request has all its chances
to be considered and will be reviewed by a maintainer.

If you are asked to update your patch by a reviewer, please do so! Remember:
**you are responsible for pushing your patch forward**. If you contributed it,
you are probably the one in need of it. You must be prepared to apply changes
to it if necessary.

If your Pull Request was accepted and fixes a bug, adds functionality, or
makes it significantly easier to use or understand CleanAPI, congratulations!
You are now an official contributor to CleanAPI. Get in touch with us to receive
your very own [Contributor T-shirt](#contributor-t-shirt)!

Your change will be included in the subsequent release Changelog, and we will
not forget to include your name if you are an external contributor. :wink:

[Back to TOC](#table-of-contents)

#### Git branches

We work on two branches: `master`, where non-breaking changes land, and `next`,
where important features or breaking changes land in-between major releases.

When contributing to CleanAPI, this distinction is important. Please ensure that
you are basing your work on top of the appropriate branch, it might save you
some time down the road!

If you have write access to the GitHub repository, please follow the following
naming scheme when pushing your branch(es):

- `feat/foo-bar` for new features
- `fix/foo-bar` for bug fixes
- `tests/foo-bar` when the change concerns only the test suite
- `refactor/foo-bar` when refactoring code without any behavior change
- `style/foo-bar` when addressing some style issue
- `docs/foo-bar` for updates to the README.md, this file, or similar documents

[Back to TOC](#table-of-contents)

#### Commit atomicity

When submitting patches, it is important that you organize your commits in
logical units of work. You are free to propose a patch with one or many
commits, as long as their atomicity is respected. This means that no unrelated
changes should be included in a commit.

For example: you are writing a patch to fix a bug, but in your endeavour, you
spot another bug. **Do not fix both bugs in the same commit!** Finish your
work on the initial bug, propose your patch, and come back to the second bug
later on. This is also valid for unrelated style fixes, refactors, etc...

You should use your best judgment when facing such decisions. A good approach
for this is to put yourself in the shoes of the person who will review your
patch: will they understand your changes and reasoning just by reading your
commit history? Will they find unrelated changes in a particular commit? They
shouldn't!

Writing meaningful commit messages that follow our commit message format will
also help you respect this mantra (see the below section).

[Back to TOC](#table-of-contents)

#### Commit message format

To maintain a healthy Git history, we ask of you that you write your commit
messages as follows:

- The tense of your message must be **present**
- Your message must be prefixed by a type, and a scope
- The header of your message should not be longer than 50 characters
- A blank line should be included between the header and the body
- The body of your message should not contain lines longer than 72 characters

Here is a template of what your commit message should look like:

```
<type>(<scope>) <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

##### Type

The type of your commit indicates what type of change this commit is about. The
accepted types are:

- **feat**: A new feature
- **fix**: A bug fix
- **hotfix**: An urgent bug fix during a release process
- **tests**: A change that is purely related to the test suite only (fixing
  a test, adding a test, improving its reliability, etc...)
- **docs**: Changes to the README.md, this file, or other such documents
- **style**: Changes that do not affect the meaning of the code (white-space
  trimming, formatting, etc...)
- **perf**: A code change that significantly improves performance
- **refactor**: A code change that neither fixes a bug nor adds a feature, and
  is too big to be considered just `perf`
- **chore**: Maintenance changes related to code cleaning that isn't
  considered part of a refactor, build process updates, dependency bumps, or
  auxiliary tools and libraries updates (LuaRocks, Travis-ci, etc...).

##### Scope

The scope is the part of the codebase that is affected by your change. Choosing
it is at your discretion, but here are some of the most frequent ones:

- **proxy**: A change that affects the proxying of requests
- **router**: A change that affects the router, which matches a request to the
  desired configured API
- **admin**: A change to the Admin API
- **balancer**: Changes related to the internal Load Balancer
- **core**: Changes affecting a large part of the core, and touching many parts
  such as `proxy`, `balancer`, `dns`
- **dns**: Changes related to internal DNS resolution
- **dao**: A change related to the DAO, the interface to the datastores
- **cli**: Changes to the CLI
- **cache**: Changes to the configuration entities caching (datastore entities)
- **deps**: When updating dependencies (to be used with the `chore` prefix)
- **conf**: Configuration-related changes (new values, improvements...)
- **`<plugin-name>`**: This could be `basic-auth`, or `ldap` for example
- `*`: When the change affects too many parts of the codebase at once (this
  should be rare and avoided)

##### Subject

Your subject should contain a succinct description of the change. It should be
written so that:

- It uses the present, imperative tense: "fix typo", and not "fixed" or "fixes"
- It is **not** capitalized: "fix typo", and not "Fix typo"
- It does **not** include a period. :smile:

##### Body

The body of your commit message should contain a detailed description of your
changes. Ideally, if the change is significant, you should explain its
motivation, the chosen implementation, and justify it.

As previously mentioned, lines in the commit messages should not exceed 72
characters.

##### Footer

The footer is the ideal place to link to related material about the change:
related GitHub issues, Pull Requests, fixed bug reports, etc...

##### Examples

Here are a few examples of good commit messages to take inspiration from:

```
fix(admin) send HTTP 405 on unsupported method

The appropriate status code when the request method is not supported
on an endpoint it 405. We previously used to send HTTP 404, which
is not appropriate. This updates the Admin API helpers to properly
return 405 on such user errors.

* return 405 when the method is not supported in the Admin API helpers
* add a new test case in the Admin API test suite

Fix #678
```

Or:

```
tests(proxy) add a new test case for URI encoding

When proxying upstream, the URI sent by CleanAPI should be the one
received from the client, even if it was percent-encoded.

This adds a new test case which was missing, to ensure it is
the case.
```

[Back to TOC](#table-of-contents)

#### Static linting

As mentioned in the guidelines to submit a patch, the linter must succeed. We
use [Eslint](https://github.com/eslint/eslint) to statically lint our Node
code. You can lint the code like so:

```
$ yarn lint
```

Or:

```
$ npm run lint .
```

[Back to TOC](#table-of-contents)

#### Writing tests



[Back to TOC](#table-of-contents)

#### Writing performant code


[Back to TOC](#table-of-contents)

### Contributor T-shirt

If your Pull Request to [fkacar/cleanapi](https://github.com/fkacar/cleanapi) was
accepted, and it fixes a bug, adds functionality, or makes it significantly
easier to use or understand CleanAPI, congratulations! You are eligible to
receive the very special Contributor T-shirt! Go ahead and fill out the
[Contributors Submissions form](https://cleanapi.io/contributors-submissions-form).

Proudly wear your T-shirt and show it to us by tagging
[@thecleanapiinc](https://twitter.com/thecleanapiinc) on Twitter!


[Back to TOC](#table-of-contents)

## Code style


[Back to TOC](#table-of-contents)

### Table of Contents - Code style

- [Modules](#modules)
- [Variables](#variables)
- [Tables](#tables)
- [Strings](#strings)
- [Functions](#functions)
- [Conditional expressions](#conditional-expressions)

### Modules


[Back to code style TOC](#table-of-contents---code-style)

### Variables


[Back to code style TOC](#table-of-contents---code-style)

### Tables


[Back to code style TOC](#table-of-contents---code-style)

### Strings


[Back to code style TOC](#table-of-contents---code-style)

### Functions


[Back to code style TOC](#table-of-contents---code-style)

### Conditional expressions


[Back to code style TOC](#table-of-contents---code-style)
