Nikita Tchayka

# How to get cool icons for the Spacemacs file tree

The icons that come with Spacemacs for the file tree are quite "classic". In fact, that theme is called `classic`.

We can make them prettier by doing some simple changes to our `.spacemacs` file:

1. Add to your `additional-packages` section the `all-the-icons` package
2. In your `user-config` function, add the following code:
```elisp
  (require 'all-the-icons)
  (setq all-the-icons-color-icons t)
  (setq all-the-icons-for-buffer t)
  (setq neo-theme 'icons)
```
3. Restart spacemacs.

You now should have something that looks like [this](https://imgur.com/a/r2CZnF3).
