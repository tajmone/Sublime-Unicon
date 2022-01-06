# Sublime Unicon

![Package Status][Package badge]&nbsp;
[![Unicon Version][Unicon badge]][Get Unicon]&nbsp;
[![ST Version][ST badge]][ST Link]&nbsp;
[![MIT License][License badge]][LICENSE]&nbsp;
[![Build Status][Travis badge]][Travis link]

[Sublime Text 4] syntax support for the [Unicon] programming language.

- https://github.com/tajmone/Sublime-Unicon

By [Tristano Ajmone], January 2022, [MIT License].

-----

**Table of Contents**

<!-- MarkdownTOC autolink="true" bracket="round" autoanchor="false" lowercase="only_ascii" uri_encoding="true" levels="1,2,3" -->

- [About](#about)
    - [Sublime Text 3 Support](#sublime-text-3-support)
    - [Recommended Settings](#recommended-settings)
- [License](#license)
- [Credits](#credits)

<!-- /MarkdownTOC -->

-----

# About

[Sublime Unicon] provides syntax highlighting for [Unicon] source files.
Files with the `.icn` extension are automatically associated with the Unicon syntax.

This package is derived from the [Unicon syntax for Sublime Text 3][ST3 Syntax] found at the [Unicon repository].
It features some improvements to the original syntax definition, along with other package specific features like comments definitions, etc.

My main goal was to create a full-fledged package that end users can install via Package Control and benefit from future package updates thanks to the self-updating functionality.
This alone might prompt other Unicon users to contribute to the package's growth.

Furthermore, I wanted to focus on a package specifically targeting Sublime Text 4, which introduces some new syntax features which are rather cool and powerful, and fixes various bugs from Sublime Text 3 syntax definitions.
Therefore, the Unicon syntax in this package contains [the `version: 2` key][v2key] to enable the new syntax engine of Sublime Text 4, at the cost of breaking backward compatibility.

The long term goals for this package are to improve the syntax semantics and provide further functionality, like completions, build systems, symbols indexing, etc.
Contributions are welcome.

For questions, feedback and suggestions, reach out via [Discussions].
For bug reports and feature requests, [open an Issue] instead.


## Sublime Text 3 Support

This package is designed to take advantage of the new features of [Sublime Text 4].
If you're using [Sublime Text 3], you should download the original [`unicon.sublime-syntax`][ST3 Syntax] from the Unicon repository and copy it inside your Sublime Text 3 `<data_path>/Packages/User/` folder (see [Sublime Text Packages documentation]).

## Recommended Settings

Although the Unicon compiler supports source files that use both tabs and spaces for indentation, and either `CRLF` or `LF` line-endings under Windows, it's strongly recommended to abide to the [recommended code styles conventions]:

- Indentation: 3 spaces.
- Line-endings: Unix-style (`LF`).

Adopting these conventions in your Unicode source files will provide a better collaborative experience in version-controlled cross-platform projects.

To enforce the above settings, create an Unicon syntax-specific settings file in your `Packages/User/` directory:

- `<data_path>/Packages/User/Unicon.sublime-settings`

then copy and paste the following settings into it:

```json
{
    "translate_tabs_to_spaces": true,
    "tab_size": 3,
    "default_line_ending": "unix",
}
```



# License

- [`LICENSE`][LICENSE]

```
MIT License

Copyright (c) 2021 Tristano Ajmone

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

# Credits

This package was built around the original [`unicon.sublime-syntax`][ST3 Syntax] taken from the Unicon repository (commit [`a26ccbc`][a26ccbc]):

- https://github.com/uniconproject/unicon/blob/master/config/editor/unicon.sublime-syntax

Explicit permission was granted to reuse the `unicon.sublime-syntax` file in this package under MIT License:

- [uniconproject/unicon#261]


<!-----------------------------------------------------------------------------
                               REFERENCE LINKS
------------------------------------------------------------------------------>

[Sublime Unicon]: https://github.com/tajmone/Sublime-Unicon "Visit the Sublime Unicon repository at GitHub"

[MIT License]: ./LICENSE "View MIT License file"

[Discussions]: https://github.com/tajmone/Sublime-Unicon/discussions "Go to Sublime Unicon repository Discussions"
[open an Issue]: https://github.com/tajmone/Sublime-Unicon/issues "Jump to the repository Issues"

<!-- Sublime Text -->

[Sublime Text 4]: https://www.sublimetext.com "Visit Sublime Text website"
[Sublime Text 3]: https://www.sublimetext.com/3 "Visit Sublime Text 3 homepage"

[Sublime Text Packages documentation]: https://www.sublimetext.com/docs/packages.html "Sublime Text documentation » Packages"

[v2key]: https://www.sublimetext.com/docs/syntax.html#compatibility "Sublime Text documentation » Syntax Definitions » Compatibility"

<!-- Unicon -->

[Unicon]: http://unicon.org "Unicon website"
[Get Unicon]: http://unicon.org/downloads.html "Go to the Unicon download page"

[Unicon repository]: https://github.com/uniconproject/unicon "Visit the Unicon repository at GitHub"

[recommended code styles conventions]: http://btiffin.users.sourceforge.net/up/tools.html#coding-conventions-and-style "Brian Tiffin's 'Unicon Programming Page' » Coding conventions and style"

<!-- upstream -->

[a26ccbc]: https://github.com/uniconproject/unicon/blob/a26ccbca46b19dd9aeb4704b029514b6b5666ce8/config/editor/unicon.sublime-syntax "View upstream syntax file from commit a26ccbc"

[ST3 Syntax]: https://github.com/uniconproject/unicon/blob/master/config/editor/unicon.sublime-syntax

[uniconproject/unicon#261]: https://github.com/uniconproject/unicon/issues/261 "Issue #261 — Permission to Reuse the Sublime Text Syntax in an MIT-Licensed Project"

<!-- project files -->

[.editorconfig]: ./.editorconfig "View EditorConfig settings file"
[.gitattributes]: ./.gitattributes "View Git attributes settings file"
[.gitignore]: ./.gitignore "View Git ignore settings file"
[.travis.yml]: ./.travis.yml "View Travis CI settings file"
[CONTRIBUTING.md]: ./CONTRIBUTING.md "Read the Contributors' Guidelines"
[LICENSE]: ./LICENSE "View MIT License file"
[SYNTAX_STATUS.md]: ./SYNTAX_STATUS.md "View document"
[validate.sh]: ./validate.sh "View source script for code style validation"

<!-- badges -->

[License badge]: https://img.shields.io/badge/License-MIT-blue
[Package badge]: https://img.shields.io/badge/version-1.0.0-yellow "Sublime Unicon package version"
[Unicon badge]: https://img.shields.io/badge/Unicon-13.2-yellow "Supported Unicon version (click for Unicon download page)"
[ST badge]: https://img.shields.io/badge/Sublime_Text-4109-yellow?logo=sublime-text&logoColor=FF9800 "Supported Sublime Text version (click to visit download page)"
[ST link]: https://www.sublimetext.com/download "Supported Sublime Text version (click to visit download page)"
[Travis badge]: https://img.shields.io/travis/com/tajmone/Sublime-Unicon/main?logo=travis
[Travis link]: https://travis-ci.com/tajmone/Sublime-Unicon "Travis CI: EditorConfig validation status"

<!-- people -->

[Tristano Ajmone]: https://github.com/tajmone "View Tristano Ajmone's GitHub profile"

<!-- EOF -->
