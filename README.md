Git Commit Message StyleGuide
=============================

[![emoji](https://img.shields.io/badge/emoji-%F0%9F%A6%84%20%F0%9F%92%9F-lightgrey.svg)](https://en.wikipedia.org/wiki/Emoji#Unicode_blocks)
[![GitHub contributors](https://img.shields.io/github/contributors/slashsBin/styleguide-git-commit-message.svg)](https://github.com/slashsBin/styleguide-git-commit-message/graphs/contributors)
[![GitHub stars](https://img.shields.io/github/stars/slashsBin/styleguide-git-commit-message.svg)](https://github.com/slashsBin/styleguide-git-commit-message/stargazers)
[![license](https://img.shields.io/github/license/slashsBin/styleguide-git-commit-message.svg)](https://github.com/slashsBin/styleguide-git-commit-message/blob/master/LICENSE)
[![ghit.me](https://ghit.me/badge.svg?repo=slashsBin/styleguide-git-commit-message)](https://ghit.me/repo/slashsBin/styleguide-git-commit-message)


##### TOC
- [About](#about)
- [Commit Message Format](#commit-message-format)
- [Notes](#notes)
- [Suggested Emojis](#suggested-emojis)
- [Tools](#tools)
- [Contributing](#contributing)
- [License](#license)


## About
This is an attempt to standardize the format of commit messages, for the sake of **uniformity** in git log, **best practices** for writing commit messages & **fun**!

Using emojis at the beginning of commit messages, other than being fun, provides a simple way to indicate the intention of that commit, an ease for the eyes when browsing/reviewing git log. It's also a simple measure of the fact that how much that commit is focused on a single purpose, which is a good practice.

If these rules and/or using emojis is an [overkill](/../../issues/21) for your productivity or simply losing its purposes, please tailor them to your needs or don't use them.


## Commit Message Format

All Git Commit Messages **MUST** meet with this Text Format:
```
:emoji1: :emoji2: Subject
(Only One NewLine)
Message Body
(Only One NewLine)
Ref <###>
```

### Rules

1. Capitalize the _Subject_.
2. Do not end the _Subject_ line with a period.
3. Message _Subject_ **SHOULD** Begin with _at-least_ One Emoji(see below for [list of Suggested Emojis](#suggested-emojis)).
4. Message Body **SHOULD** End with _at-least_ One Issue Tracking ID Reference([GitHub Issues](https://github.com/features#issues)/[GitLab Issues](https://docs.gitlab.com/ee/user/project/issues/)/[Phabricator Tasks](http://phacility.com/phabricator/maniphest/)), Ex. `Issue #27`, `Ref T27` or `Ref T27, T56` or `Fixes T8`.  
It's also [recommanded](/../../issues/19) to use _Full URL to Issues_, instead of just Issue ID Number; Doing so will ease browsing issues from terminal.
5. Total Characters of the _Subject Line_ **MUST** be _Less_ than or _Equal_ to **50** Chars Long.
6. Wrap the _Message body_ at **72** characters.
7. Use Valid [MarkDown](https://daringfireball.net/projects/markdown/basics) format in _Message Body_.
8. Use the **Present Tense** ("Add feature" not "Added feature").
9. Use the **Imperative Mood** ("Move cursor to..." not "Moves cursor to...").
10. Use the _Message body_ to explain **what** and **why** vs. how.
11. All WIP(Work In Progress) Commits **MUST** have the WIP Emoji(see below).

## Notes

+ All **WIP** Commits **Should** be Avoided!.
+ Refrencing Issues by using special keywords like `Fixes` or `Resolves` will mark them as closed automatically! For more  information about automatic issue closing using ketwords see: [GitHub](https://help.github.com/articles/closing-issues-via-commit-messages/)/[GitLab](https://docs.gitlab.com/ee/user/project/issues/automatic_issue_closing.html)/[Phabricator](https://secure.phabricator.com/book/phabricator/article/diffusion_autoclose/).
+ There is a **Space** Character between Multiple Emojis!.
+ There is **NO** New-Line After the _Task ID Reference_ Line.
+ Every Raw Emoji Text(`:emoji:`) is Counted as One Char!.
+ See [ToDo Grammar StyleGuide](https://github.com/slashsBin/styleguide-todo-grammar) for more Information on `@XXX` Comment Tags.


## Suggested Emojis

| Emoji | Raw Emoji Code | Description |
|:---:|:---:|---|
| :art: | `:art:` | when improving the **format**/structure of the code |
| :newspaper: | `:newspaper:` | when creating a **new file** |
| :pencil: | `:pencil:` | when **performing minor changes/fixing** the code or language |
| :racehorse: | `:racehorse:` | when improving **performance** |
| :books: | `:books:` | when writing **docs** |
| :bug: | `:bug:` | when reporting a **bug**, with [`@FIXME`](https://github.com/slashsBin/styleguide-todo-grammar#bug-report)Comment Tag |
| :ambulance: | `:ambulance:` | when fixing a **bug** |
| :penguin: | `:penguin:` | when fixing something on **Linux** |
| :apple: | `:apple:` | when fixing something on **Mac OS** |
| :checkered_flag: | `:checkered_flag:` | when fixing something on **Windows** |
| :fire: | `:fire:` | when **removing code** or files, _maybe_ with `@CHANGED` Comment Tag |
| :tractor: | `:tractor:` | when **change file structure**. Usually together with :art: |
| :hammer: | `:hammer:` | when **refactoring** code |
| :umbrella: | `:umbrella:` | when adding **tests** |
| :microscope: | `:microscope:` | when adding **code coverage** |
| :green_heart: | `:green_heart:` | when fixing the **CI** build |
| :lock: | `:lock:` | when dealing with **security** |
| :arrow_up: | `:arrow_up:` | when upgrading **dependencies** |
| :arrow_down: | `:arrow_down:` | when downgrading **dependencies** |
| :fast_forward: | `:fast_forward:` | when **forward-porting features** from an older version/branch |
| :rewind: | `:rewind:` | when **backporting features** from a newer version/branch |
| :shirt: | `:shirt:` | when removing **linter**/strict/deprecation warnings |
| :lipstick: | `:lipstick:` | when improving **UI**/Cosmetic |
| :wheelchair: | `:wheelchair:` | when improving **accessibility** |
| :globe_with_meridians: | `:globe_with_meridians:` | when dealing with **globalization**/internationalization/i18n/g11n |
| :construction: | `:construction:` | **WIP**(Work In Progress) Commits, _maybe_ with `@REVIEW` Comment Tag |
| :gem: | `:gem:` | New **Release** |
| :egg: | `:egg:` | New **Release** with Python egg|
| :ferris_wheel: | `:ferris_wheel:` | New **Release** with Python wheel package |
| :bookmark: | `:bookmark:` | Version **Tags** |
| :tada: | `:tada:` | **Initial** Commit |
| :speaker: | `:speaker:` | when Adding **Logging** |
| :mute: | `:mute:` | when Reducing **Logging** |
| :sparkles: | `:sparkles:` | when introducing **New** Features |
| :zap: | `:zap:` | when introducing **Backward-InCompatible** Features, _maybe_ with `@CHANGED` Comment Tag |
| :bulb: | `:bulb:` | New **Idea**, with `@IDEA` Comment Tag |
| :snowflake: | `:snowflake:` | changing **Configuration**, Usually together with :penguin: or :ribbon: or :rocket: |
| :ribbon: | `:ribbon:` | Customer requested application **Customization**, with `@HACK` Comment Tag |
| :rocket: | `:rocket:` | Anything related to Deployments/**DevOps** |
| :elephant: | `:elephant:` | **PostgreSQL** Database specific (Migrations, Scripts, Extensions, ...)  |
| :dolphin: | `:dolphin:` | **MySQL** Database specific (Migrations, Scripts, Extensions, ...) |
| :leaves: | `:leaves:` | **MongoDB** Database specific (Migrations, Scripts, Extensions, ...) |
| :bank: | `:bank:` | **Generic Database** specific (Migrations, Scripts, Extensions, ...) |
| :whale: | `:whale:` | **Docker** Configuration |
| :handshake: | `:handshake:` | when **Merge files** |


## Tools

- [Commit](https://github.com/jakeasmith/commit)(CLI): This is a nifty CLI tool to aid in standardizing commit messages based on this document, thanks to @jakeasmith.
- [gitMoji](https://github.com/louisgrasset/git-moji)(Chrome Extension): Enhance your commits with emojis!, thanks to @louisgrasset.


## Contributing

[Ask](https://github.com/slashsBin/styleguide-git-commit-message/issues/new) to Be [Creative](https://emoji.codes/)!

To add a new Emoji to the list: [Create an Issue](https://github.com/slashsBin/styleguide-git-commit-message/issues/new) & Send a [PR]().


## License

The Code is licensed under the [MIT License](http://slashsbin.mit-license.org/).
