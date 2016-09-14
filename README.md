[![Melpa Status](http://melpa.org/packages/ac-inf-ruby-badge.svg)](http://melpa.org/#/ac-inf-ruby)
[![Melpa Stable Status](http://stable.melpa.org/packages/ac-inf-ruby-badge.svg)](http://stable.melpa.org/#/ac-inf-ruby)

inf-ruby completion source for Emacs auto-complete package
==========================================================

This plugin provides an [auto-complete](http://cx4a.org/software/auto-complete/)
completion source for use in [inf-ruby](https://github.com/nonsequitur/inf-ruby) buffers.

Installation
=============

First, ensure `auto-complete` and `inf-ruby` are installed: I recommend
using packages from [MELPA][melpa].

You'll need both `auto-complete` and `inf-ruby` to be enabled and
working, so please consult the corresponding documentation is you have
any trouble with this.

Next, install `ac-inf-rub`. If you choose not to use the convenient
package in [MELPA][melpa], you'll need to add the directory containing
`ac-inf-ruby.el` to your `load-path`, and then `(require
'ac-inf-ruby)`.

`ac-inf-ruby` provides an `inf-ruby`-specific completion source,
so `auto-complete` needs to be told to use them when `inf-ruby-mode` is
active. To do this, put the following code in your emacs init file to

```el
(eval-after-load 'auto-complete
  '(add-to-list 'ac-modes 'inf-ruby-mode))
(add-hook 'inf-ruby-mode-hook 'ac-inf-ruby-enable)
```

If you want to trigger `auto-complete` using <kbd>TAB</kbd> in `inf-ruby` buffers, you
should bind it directly:

```el
(eval-after-load 'inf-ruby '
  '(define-key inf-ruby-mode-map (kbd "TAB") 'auto-complete))
```

Usage
=====

`ac-inf-ruby` should now automatically be enabled in new `inf-ruby` sessions.

Simply trigger auto-completion, and completion candidates supplied by
`inf-ruby` should be displayed, with the "r" symbol on the right hand side of the
completion pop-up.

[melpa]: http://melpa.org

Acknowledgements
================

`ac-inf-ruby` was written by [Steve Purcell](https://github.com/purcell).

<hr>

Author links:

[![](http://api.coderwall.com/purcell/endorsecount.png)](http://coderwall.com/purcell)

[![](http://www.linkedin.com/img/webpromo/btn_liprofile_blue_80x15.png)](http://uk.linkedin.com/in/stevepurcell)

[Steve Purcell's blog](http://www.sanityinc.com/) // [@sanityinc on Twitter](https://twitter.com/sanityinc)
