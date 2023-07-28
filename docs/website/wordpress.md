# Wordpress Setup

The reformedperspective.ca site is connected to wordpress.com using the *tech* account via the Wordpress Jetpack plugin. Stats can be seen in the admin interface and in the wordpress.com account.

## Plugins


## Benchpress Theme

The theme used for the rp.ca site is a [custom theme called Benchpress](benchpress.md).

## Shortcodes

Shortcodes are a way to get extra functionality into pages and posts without effort on the part of the content creators.

In addition to the default Wordpress shortcodes:

- `[caption][/caption]` - wraps captions around content (enclosing)
- `[gallery]` - shows image gallery (self-closing)
- `[audio]` - embeds and plays audio file (self-closing)
- `[video]` - embeds and plays video file (self-closing)
- `[playlist]` - embeds multi-media playlist
- `[embed][/embed]` - wraps embedded item (enclosing)

we have some custom ones. These are found in the Benchpress 'shortcodes.php' file:

- `[BP_getAllSaved]` - shows page of articles saved by user (self-closing)
- `[BP_getAllHistory]` - shows page of user's view history (self-closing)
- `[BP_fontSize][/BP_fontSize]` - allows custom font size for text (enclosing)
    - takes the 'size' property, which can be 'smaller' (default) or 'larger'
        - e.g. `[BP_fontSize]Some nice text[/BP_fontSize]`
        - e.g. `[BP_fontSize size=larger]Some more nice text[/BP_fontSize]`
    - also works with the font size slider by checking and adding 2px or subtracting 2px from the size of the regular paragraph text
    - only use to enclose complete lines. This might be expanded at some point to allow use in the middle of lines.

Here are some resources on how to use and make shortcodes:

- [WordPress Shortcodes: A Complete Guide (Smashing Magazine)](https://www.smashingmagazine.com/2012/05/wordpress-shortcodes-complete-guide/)
- [WordPress Shortcodes (WordPress Codex)](https://codex.wordpress.org/Shortcode)
