[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![MELPA](https://melpa.org/packages/ffmpeg-player-badge.svg)](https://melpa.org/#/ffmpeg-player)
[![MELPA Stable](https://stable.melpa.org/packages/ffmpeg-player-badge.svg)](https://stable.melpa.org/#/ffmpeg-player)

# ffmpeg-player
> Play video using ffmpeg.

[![CI](https://github.com/jcs-elpa/ffmpeg-player/actions/workflows/test.yml/badge.svg)](https://github.com/jcs-elpa/ffmpeg-player/actions/workflows/test.yml)

## 📝 Acknowledge

This package will output video into images (in frame). This might causes
many I/O times and disk space (Even though these frames will eventually get 
cleaned up). I would like to mention you all the information and consequences
before you use this package.

*See [melpa/6560](https://github.com/melpa/melpa/pull/6560) for more information.*

## External Program

This package uses these following programs, make sure these program are added
to your path.

* [ffmpeg](https://www.ffmpeg.org/)
* [ffplay](https://www.ffmpeg.org/) - Bundle with `ffmpeg`.

## 🔌 Capability

Base on `ffplay`'s website.

> ffplay is a very simple and portable media player using the FFmpeg libraries
and the SDL library. It is mostly used as a testbed for the various FFmpeg APIs.

Hence, I have encounter some issues synchronize video and audio. Try move the
timeline by pressing `<left>` or `<right>` key multiple times could resolve
such an issue.

## 🔧 Usage

You can play the video by calling function `ffmpeg-player-video`.

```el
(ffmpeg-player-video (expand-file-name "./test/1.avi"))
```

And here is the control of the media.

* <kbd>space</kbd> - Pause/Unpause.
* <kbd>up</kbd> - Increase volume by 5.
* <kbd>down</kbd> - Decrease volume by 5.
* <kbd>left</kbd> - Backward timeline 10 seconds.
* <kbd>right</kbd> - Forward timeline 10 seconds.
* <kbd>m</kbd> - Mute/Unmute.
* <kbd>r</kbd> - Replay.

## 📝 Todo List

- [ ] Play youtube video through url.

## 🛠️ Contribute

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)
[![Elisp styleguide](https://img.shields.io/badge/elisp-style%20guide-purple)](https://github.com/bbatsov/emacs-lisp-style-guide)
[![Donate on paypal](https://img.shields.io/badge/paypal-donate-1?logo=paypal&color=blue)](https://www.paypal.me/jcs090218)
[![Become a patron](https://img.shields.io/badge/patreon-become%20a%20patron-orange.svg?logo=patreon)](https://www.patreon.com/jcs090218)

If you would like to contribute to this project, you may either
clone and make pull requests to this repository. Or you can
clone the project and establish your own branch of this tool.
Any methods are welcome!

### 🔬 Development

To run the test locally, you will need the following tools:

- [Eask](https://emacs-eask.github.io/)
- [Make](https://www.gnu.org/software/make/) (optional)

Install all dependencies and development dependencies:

```sh
$ eask install-deps --dev
```

To test the package's installation:

```sh
$ eask package
$ eask install
```

To test compilation:

```sh
$ eask compile
```

**🪧 The following steps are optional, but we recommend you follow these lint results!**

The built-in `checkdoc` linter:

```sh
$ eask lint checkdoc
```

The standard `package` linter:

```sh
$ eask lint package
```

*📝 P.S. For more information, find the Eask manual at https://emacs-eask.github.io/.*

## ⚜️ License

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.

See [`LICENSE`](./LICENSE.txt) for details.
