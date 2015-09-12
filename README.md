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


Customization
-------------

You can choose any of [moe-theme mode-line themes][moe-theme-mode-line-themes],
or any other declared by you.

Defaults are:
* Flycheck default/no error: 'green
* Flycheck warning: 'orange
* Flycheck error: 'red
* Flycheck info: 'blue
* Flycheck check failed: 'purple


The themes can be customized in the customization group `flycheck-faces`:

	M-x customize-group
	moe-flycheck-mode-line

or:

	M-x moe-flycheck-mode-line-customize

or, in your `init.el`:

	(setq moe-flycheck-mode-line-error 'red)

Credits
-------

- [Sylvain Benner][syl20bnr] for the idea and code from the excellent [flycheck-color-mode-line][flycheck-color-mode-line].
- [hiroko][kuanyui] for [moe-theme][moe-theme] the best emacs theme ever!


[flycheck]: http://github.com/flycheck/flycheck
[kuanyui]: https://github.com/kuanyui
[moe-theme]: http://github.com/kuanyui/moe-theme.el
[moe-theme-mode-line-themes]: https://github.com/kuanyui/moe-theme.el#colorful-mode-line-and-powerline
[syl20bnr]: http://github.com/syl20bnr
[flycheck-color-mode-line]: http://github.com/flycheck/flycheck-color-mode-line
