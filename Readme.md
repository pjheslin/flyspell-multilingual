# Flyspell-extras

NB. I have not been keeping these packages up to date and they probably need some updating to work with current versions of Emacs.

This is a set of Emacs packages that attempt to make flyspell (on -the-fly spellchecking) work better with multilingual texts.  The idea is that the dictionary in use should change when there is an indication in the text that the language has changed, such as my means of a babel command in a LaTeX file or an xml-lang attribute in an XML file.

## ispell-multi.el
ispell-multi.el enables Emacs to keep a number of ispell processes alive in order to spell-check text efficiently in multiple languages, and it provides a hook that tells flyspell to switch languages depending on the value of a particular text property.

It provides the infrastructure on which flyspell-xml-lang.el and flyspell-babel.el are built, and it is a prerequisite for them.

## flyspell-xml-lang.el
flyspell-xml-lang.el will switch the current language dictionary used by flyspell (an Emacs package that highlights misspelled words as you type) to match the language declared by the xml:lang attribute of the current XML document element. The dictionary currently in force is shown in the modeline.

## flyspell-babel.el
flyspell-babel.el is a package that switches the language used by the flyspell spell-checker according to the Babel commands in a Latex file. It can be customized to take into account non-standard language-switching commands, and you can switch off spell-checking for languages for which you don't have a dictionary.
