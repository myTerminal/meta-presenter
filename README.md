# meta-presenter

[![MELPA-Stable](http://stable.melpa.org/packages/meta-presenter-badge.svg)](http://stable.melpa.org/#/meta-presenter)
[![MELPA](http://melpa.org/packages/meta-presenter-badge.svg)](http://melpa.org/#/meta-presenter)
[![Marmalade](https://img.shields.io/badge/marmalade-available-8A2A8B.svg)](https://marmalade-repo.org/packages/meta-presenter)  
[![License](https://img.shields.io/badge/LICENSE-GPL%20v3.0-blue.svg)](https://www.gnu.org/licenses/gpl.html)
[![Gratipay](http://img.shields.io/gratipay/myTerminal.svg)](https://gratipay.com/myTerminal)

A simple multi-file presentation tool for Emacs

## Installation

### Manual

Save the file *meta-presenter.el* to disk and add the directory containing it to 'load-path' using a command in your '.emacs' file like:

    (add-to-list 'load-path "~/.emacs.d/")
    
The above line assumes that you've placed the file into the Emacs directory '.emacs.d'.

Start the package with:

    (require 'meta-presenter)

### MELPA-Stable / MELPA / Marmalade

If you have MELPA-Stable, MELPA or Marmalade added as a repository to your Emacs, you can just install *meta-presenter* with

    M-x package-install meta-presenter RET

## Usage

Create a directory that contains slides to be presented stored as files. Name the files as the slide number followed by an underscore, followed by the name of the slide. Below are some examples:

*   1_introduction.md
*   2_getting-started.md
*   3_advanced-features.md

Create a separate title slide for the presentation, start the presentation mode while viewing the file. For example, if the directory containing your slides contains a *title.md* file, you can run `meta-presenter-start-presentation` while having the file open in the buffer where you would like the presenation to start. When the presentation starts, you'll be taken to a buffer named *slide-show.md*.

In order to move to the next slide press `C-c C-v`, to move back to the previous slide press `C-c C-x`.

As the slides are not read-only, you could perform annotations on them. To revert the changes press `C-c C-c`.

You can also enable animations for slide transitions which is currently experimental and not optimized. To enable animations, just evaluate the below line.

    (setq meta-presenter-enable-animations t)
