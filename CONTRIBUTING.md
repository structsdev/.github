# Contributing

We'd love to accept your patches and contributions to this project through the
process of creating a [pull request][] (**PR**). This document details the
process of submitting a PR so that it can be reviewed and merged into the
codebase. It also contains some guidelines for writing good commits, reporting
issues, and guidelines for project maintainers.

---

## Reporting issues

Bugs, feature requests, and development-related questions should be directed to
the specific project's issue tracker or discussion board.

### Bugs

If reporting a bug, please submit an issue and provide as much context as
possible such as your operating system, architecture, library release version,
Go version (if applicable), and anything else that might be relevant to the bug.

Fill out as much information as possible in the form provided by the issue
template.

#### SECURITY BUGS

We take security bugs ***VERY*** seriously!

Please promptly report security related bugs to <security@devnw.com>. Please
follow [responsible disclosure guidelines][] when publicizing any security related
information, ensuring that maintainers are aware of the issue and are able to
address it promptly.

Please include:

1. Information about the vulnerability
1. Associated CVEs (if any)
1. Affected release(s)
1. Affected package(s)

### Feature Requests

For feature requests, please explain what you're trying to do, and
how the requested feature would help you do that.

Security related bugs can either be reported in the issue tracker, or if they
are more sensitive, emailed to <security@devnw.com>.

[responsible disclosure guidelines]: https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html

---

## Submitting a Pull Request

  1. It's generally best to start by opening a new issue describing the bug or
     feature you're intending to fix. Even if you think it's relatively minor,
     it's helpful to know what people are working on. Mention in the initial
     issue that you are planning to work on that bug or feature so that it can
     be assigned to you.

  1. Follow the normal process of [forking][] the project, and setup a new
     branch to work in. It's important that each group of changes be done in
     separate branches in order to ensure that a pull request only includes the
     commits related to that bug or feature.

  1. Our projects will all generally contain a `.pre-commit-config.yaml` file
     that configures a set of pre-commit actions that the maintainers run on their
     system prior to committing. We recommend installing the [pre-commit][] hook
     framework and running it on your system *prior* to submitting a PR.
     See the [pre-commit usage documentation][] for more information.

  1. Our Go based projects include a config for the [golangci-lint][] tool that
     helps you run your code through a series of checks. As noted in the
     [golangci-lint quickstart][], it's easy to install and run. The
     configuration is documented in the `.golangci.yml` file in the root of the
     project.

  1. Any significant changes should almost always be accompanied by tests. The
     project already has good test coverage, so look at some of the existing
     tests if you're unsure how to go about it.
     **NOTE:** For go environments [gocov][] and [gocov-html][]
     are invaluable tools for seeing which parts of your code aren't being
     exercised by your tests.

  1. Do your best to have [well-formed commit messages][] for each change.
     This provides consistency throughout the project, and ensures that commit
     messages are able to be formatted properly by various git tools.

  1. Finally, push the commits to your fork and submit a [pull request][].
     **NOTE:** It is recommended that you [squash][] your commits into a single
       commit before submitting a pull request.

     * When submitting a pull request, please include a [link to the issue][]
       that you're submitting a pull request for. This will help us to track the
       progress of the issue.

[forking]: https://help.github.com/articles/fork-a-repo
[golangci-lint]: https://golangci-lint.run/
[golangci-lint quickstart]: https://golangci-lint.run/usage/quick-start/
[pre-commit]: https://pre-commit.com/
[pre-commit usage documentation]: https://pre-commit.com/#usage
[gocov]: https://github.com/axw/gocov
[gocov-html]: https://github.com/matm/gocov-html
[well-formed commit messages]: http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
[squash]: http://git-scm.com/book/en/Git-Tools-Rewriting-History#Squashing-Commits
[pull request]: https://help.github.com/articles/creating-a-pull-request
[link to the issue]: https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue
---

## Code Organization

---

## Maintainer's Guide

(These notes are mostly only for people merging in pull requests.)

It is the responsibility of the maintainer to ensure that the code is passing
all checks and tests. The maintainer should also ensure that the code is
consistent with the project's [code style][] and [documentation][]. The
maintainer should also ensure that the code is well-documented and tested
before merging in a pull request.

[git-aliases]: https://github.com/willnorris/dotfiles/blob/d640d010c23b1116bdb3d4dc12088ed26120d87d/git/.gitconfig#L13-L15
[rebase-comment]: https://github.com/google/go-github/pull/277#issuecomment-183035491
[modified-comment]: https://github.com/google/go-github/pull/280#issuecomment-184859046
