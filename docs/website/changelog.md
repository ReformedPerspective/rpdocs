# Log of changes to the RP website

## Past Articles Page - April, 2022

The 'Past Articles' page shows a list of all the main Categories on the site and lists all the articles under those categories. You can link to the list of articles and then out to the article page from here.

This page is linked at /past-articles

## Bootstrap Upgraded to latest - Oct., 2022

Bootstrap was updated to the latest version of Bootstrap 4.

## New Voice of the Church Page - Dec., 2022

A new page for all the Voice of the Church data was created. All data is hosted in our PCloud public folder so that the Dreamhost shared host doesn't fill up.

The page allows filtering by the Speaker and Series titles and allows sorting by Title, Series, Minister, Scripture, Date, and Type. It uses json data on PCloud retrieved from the VOTC data on Sermon Audio, and links to the VOTC mp3s, and, when applicable, PDFs and videos.

## New Ads setup - April, 2023

The following steps were taken to enable the new Ads at the bottom of the articles.

1. Create an 'Ad-New' Category that is a sub-category of Advertisements
    1. Set this category as 'exempt' from *Recent News* and *Front Page* in the [Benchpress settings](benchpress.md#benchpress-options).

        **NOTE**: A post with the 'Ad-New' Category must be published first before the it will show up in this list and can be selected.

2. Create an 'expires' Tag
    1. Hide this tag from the *Front Page* in the same way

3. Install the *PublishPress Future* plugin to allow setting an expiry date

4. Create an adArea() function in BP_modules and call it from the articlePage() function in the Page Controller

5. Set up a way for Categories to show the description at the top of the first page of results. Just add a description to the Category and then enable that category in Benchpress Options.

## Add Doc. Comments to Functions - June, 2023

All files were gone through and documentation comments were added for functions and other things. This helps IDEs see and show documentation for things while coding.

## Add 'Highlighted Links' Minister

A new widget was added to the front page highlighting the latest devotional and Manna podcast.

## Switch to Cloudflare Turnstile - Dec., 2023

Captchas were switched to Cloudflare Turnstile instead of ReCaptcha.

Because of this change, spam emails went down to 0.

## New 'Free Books' Module Created - Jan., 2024

A new module for Free Books was added. It is slowly being populated with content by Jon. When he's ready we can link to it somewhere.

## Change Donate Page to Bambora for Credit Cards - March, 2024

The Donate page was reconfigured to use Bambora instead of Square for credit card processing.

## Add Aria and Alt to Images - Aug., 2024

Add arial-label and alt text to images all over the site. Includes any descriptions typed in inside the Wordpress media upload interfaces.

## Prefer WebP Images  - Sept., 2024

Code to convert jpg/png to webp was implemented using the WebP Express plugin and a function to get the relevant webp for images was created.

## Remove Mobile Page Code - Sept., 2024

Extra 'Mobile' page code was removed and css adjusted for responsive performance on all screen sizes. Many redundant Bootstrap classes were removed and optimized.
