# Wordpress Setup

The reformedperspective.ca site is connected to wordpress.com using the *tech* account via the Wordpress Jetpack plugin. Stats can be seen in the admin interface and in the wordpress.com account.

## Plugins

The following plugins are in use on the rp.ca website:

- **[(Simply) Guest Author Name](https://wordpress.org/plugins/guest-author-name/)**: Add authors to posts without having them as users
- **[Aksimet Anti-Spam: Spam Protection](https://wordpress.org/plugins/akismet/)**: Spam protection for comments <sup>*</sup>
- **[All In One WP Security](https://wordpress.org/plugins/all-in-one-wp-security-and-firewall/)**: Security analyzer and administration tool
- **[Basic User Avatars](https://wordpress.org/plugins/basic-user-avatars/)**: Locally-stored avatar images
- **[Classic Editor](https://wordpress.org/plugins/classic-editor/)**: Allows use of Classic editor depending on user preference
- **[Jetpack](https://wordpress.org/plugins/jetpack/)**: Security, performance, analytics, etc.
- **[Jetpack Boost](https://wordpress.org/plugins/jetpack-boost/)**: Site optimization and analysis
- **[Page Links To](https://wordpress.org/plugins/page-links-to/)**: Makes a page link to custom URL <sup>!</sup>
- **[PublishPress Future](https://wordpress.org/plugins/post-expirator/)**: Expires page/post after timeout
- **[Scheduled Post Trigger](https://wordpress.org/plugins/scheduled-post-trigger/)**: Try to publish unpublished scheduled posts
- **[WP Mail SMTP](https://wordpress.org/plugins/wp-mail-smtp/)**: Configure SMTP mail sending
- **[WP Super Cache](https://wordpress.org/plugins/wp-super-cache/)**: Generates static html files generator
- **[Yoast Duplicate Post](https://wordpress.org/plugins/duplicate-post/)**: Clone posts

<sup>*</sup> it may be possible to get rid of this plugin
<sup>!</sup> should get rid of this plugin

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
