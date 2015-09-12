moe-flycheck-mode-line.el
===========================

Emacs minor-mode to change [moe-theme][moe-theme] mode-line color according to
the [Flycheck][flycheck] status.

I am a complete beginner in elisp, so the code can be full of bugs. Use it at
your own risk, and please help me to improve it

Idea and code shamelessly stolen from [flycheck-color-mode-line][flycheck-color-mode-line].


Configuration
-------------

Put this code in your init file:

	(require 'moe-flycheck-mode-line)

	(eval-after-load "flycheck"
	  '(add-hook 'flycheck-mode-hook 'moe-flycheck-mode-line-mode))


Credits
------

- [Sylvain Benner][syl20bnr] for the idea and code from the excellent [flycheck-color-mode-line][flycheck-color-mode-line].
- [hiroko][kuanyui] for [moe-theme][moe-theme] the best emacs theme ever!


[flycheck]: http://github.com/flycheck/flycheck
[kuanyui]: https://github.com/kuanyui
[moe-theme]: http://github.com/kuanyui/moe-theme.el
[syl20bnr]: http://github.com/syl20bnr
[flycheck-color-mode-line]: http://github.com/flycheck/flycheck-color-mode-line
