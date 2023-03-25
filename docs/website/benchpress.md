# Benchpress Theme

The Benchpress theme is a custom Wordpress theme, written in PHP, that does all the of the heavy lifting for the rp.ca website. I handles all of the custom pages and takes over most of the functionality for rendering articles and other web pages for the entire rp.ca site. All customization is done there (i.e. `wp-content/themes/benchpress`).

There are a few things that are done via plugins, but just about everything is done via Benchpress. Plugins will be discussed [elsewhere](wordpress.md#plugins).

## The Page Hierarchy

The website is managed by a variety of hierarchical 'controller' modules containing functions that are called as needed by the various pages. Normally, for a given page, that starts something like this:

```PHP
<?PHP
   get_header();
   $BP_pageController->specificPageModule();
   get_footer();
?>
```

Then, the page controller calls the module controller methods for the various parts of the relevant page. This could look a bit like this:

```PHP
public function specificPageModule(){
   $BP_modules = $this->MC;
   $BP_modules->startFullMain();
   $BP_modules->pageContent();
   $BP_modules->endMain();
}
```

Although it could be a lot more complicated with various methods being called along with the logic required to render the page properly under various circumstances.
