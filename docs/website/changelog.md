# Log of changes to the RP website

## New Ads setup - April, 2023

The following steps were taken to enable the new Ads at the bottom of the articles.

1. Create an 'Ad-New' Category that is a sub-category of Advertisements
   1. Set this a exempt from *Recent News* and *Front Page* in the [Benchpress settings](benchpress.md#benchpress-options).
2. Create an 'expires' Tag
   1. Hide this from the *Front Page* in the same way
3. Install the *PublishPress Future* plugin to allow setting an expiry date
4. Create an adArea() function in BP_modules and call it from the articlePage() function in the Page Controller