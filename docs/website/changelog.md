# Log of changes to the RP website

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