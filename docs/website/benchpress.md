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

## Benchpress Configuration Pages

Here is an explanation of the various Benchpress theme options found in the Wordpress Dashboard:

### Benchpress Options

This is the main Benchpress configuration page with a number of settings that control how things look on the site:

#### Front Page Options:

- Exclude the following **categories** from **recent news**:
    - This options prevents certain categories (toggled using Ctrl+click) from showing up in the 'recent' list on the front page.
- Exclude the following **categories** from **front page**:
    - Similarly, this option prevent the selected categories from showing up in the sections lower down on the front page
- Exclude the following **tags** from **front page**:
    - This does the same with tags

#### Footer Options:

These are URLs that serve as links for the various social media icons on the right of the footer at the bottom of the site pages.

#### Top-Level Category Options:

Since Categories are hierarchical, there are a set of 'top level' categories. These are used in the [RP site Menu](rp_ca.md#Menu) to show links to the various sections of the site. The options here allow us to configure a set of SVG icons for those links or to hide the category from the menu entirely using the 'Hidden' checkbox.

### Sub Pages

The [RP site menu](rp_ca.md#Menu) has two main rows of links, the Category links, mentioned above, and the Sub Page links. This settings allows us to:

- Add links using the form at the bottom
- Remove them using the red 'Delete' button on each card
- Edit them with the green 'Edit' button, which populates the form at the bottom and allows us to resubmit the changes.
- Re-order them with the green and red arrows at the top of each card

### Book Review Categories

This page allows us to re-order the Book Review sub-categories by dragging them with the mouse using the up/down arrows on the left. This specifies the order that the sections (and the links) on the [Book Reviews page](https://reformedperspective.ca/category/book-reviews) show up.

### Movie Review Categories

This page does the same thing as above with the Movie Reviews categories.

### Top Level Categories

This page works similarly to the last two pages, but affects the order of the categories in the [main menu](rp_ca.md#menu). Notice the existence of 'Placeholder' in the list. This is a stand-in for the Past Articles page, since *it* is not a Category page at all.

### Manage Contacts

This page is for managing the contacts that show up on the [Contacts page](https://reformedperspective.ca/contact). It is possible to Add, Remove, and Re-order the items here.

It's very important to realize that the actual 'username' is required to add an item to the contacts list. The username may not be obvious. It can be found by finding the user in question on the [Users page](https://reformedperspective.ca/wp-admin/users.php) and copying the name as it is found in the right-most 'Username' column.

### Miscellaneous Options

#### Category Descriptions

The ability to show a description at the top of the first page of results for a category can be configured here.

1. Make sure there's a description available for the category.
2. Select the category from the dropdown list and click the 'Select Category' button.

**NOTE**: You can add hyperlinks to the description just by using `<a href="https://...">Your text</a>`

#### Motto and Tagline

The RP motto can be set here. It is used in the header of the site underneath the logo.

The site Tag Line is used on banners where something shorter than the motto is needed. It can be set in the Wordpress site settings under *General* or in the Appearance settings under *Customize*.
