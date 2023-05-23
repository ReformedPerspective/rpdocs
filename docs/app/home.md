# Home Screen Layout

**NOTE**: This 'layout' is the same as the layout available for any of the custom screens or tabs, except that most of the options for the Home screen are enabled.

---

## Header

At the top of the App home screen is an optional *Header* section. This, when turned on, can be a static image (1920 x 692 - 10MB Max.) or a Carousel with up to 5 items. These items can be any of the *Library* items available. We are currently using the Static Image **<sup>\*</sup>** option with the RP Banner.

The Header is configured using the *Design* widget to the right of the Mobile App page. In addition, the *Items* shown on the home screen can have the following properties configured there:

- Layout: can be *Rows*, *Grid* **<sup>\*</sup>**, or *Stacked*
- Item titles: can be *Below* or *Off* **<sup>\*</sup>**. The reason for this choice is that our square icons have a title built in. We don't control the size or font of these titles anyway, so it's better (if more cumbersome) this way.
- Item images: can be *Square* **<sup>\*</sup>** or *Wide*.
- Margins: *On* **<sup>\*</sup>** or *Off*.
- Shadows: *On* **<sup>\*</sup>** or *Off*.

## Content

This section is just the main part of the home screen which shows the large, square buttons (since we have this set to *Grid* and *Square*). These can be any of the items in the App *Library* and will use (obviously) the square icons associated with each. The items are ordered vertically in a single list in the settings, but are shown in rows that wrap down and have a length that depends on the screen size. These icons are taken from a Library *List* and the order can be set. Currently the home screen is using the *Learn* list, which contains:

|Item Name|Icon Label|Icon Description|Library Type|URL|Layout|
|----|-----|----|----|---|-----|
|Nearer to God|DEVOTIONAL|Open book with cross|Website|https://reformedperspective.ca/devotional-app||
|Manna Podcast|MANNA|Open book with jar|Website|https://www.mannapodcast.ca/||
|RealTalk Podcast|REAL TALK|Real Talk logo|Website|https://www.realtalkpodcast.ca/||
|Recent Posts|RECENT POSTS|Folded newspaper|RSS Feed|https://reformedperspective.ca/category/news,rp-app/feed|Reader|
|Past Articles|PAST ARTICLES|Star|List (see [Past Articles](pastarticles.md))|||
|Book Reviews|BOOK REVIEWS|Book with star|RSS Feed|https://reformedperspective.ca/category/book-reviews/feed|Reader|
|Movie Reviews|MOVIE REVIEWS|Clapperboard with Play button|RSS Feed|https://reformedperspective.ca/category/movie-reviews/feed|Reader|

The current list for this screen can be changed using the *Advanced* widget to the right under *Design*.

## Bottom buttons (Tabs)

There are some small buttons in a bar at the bottom of the home screen. They take you to various different app screens some of which have the same kind of properties as the home screen, including a Header, Content. These are, currently:

- Home: Tab. Takes you to the [home screen](home.md#home-screen-layout)
- Book of Praise: Tab. Uses the [*Book of Praise Content List*](bookofpraise.md) list.
- Bible: Bible reading plan screen. Can choose a default *Reading plan*, and a start date.
- More: This is a special page that can have:
    - Banner Slideshow: Up to 4 banner (1536 x 560) images. Currently just the RP banner.
    - Map: Has pins for as many configurable locations as we wish to add. I think the current pins are all CanRef churches
    - Additional Links: Links to external, associated sites.
    - Description: (1000 char. limit)

**Current *additional links***:

|Name|Title|URL|
|---|---|---|
|Facebook|Facebook Page|https://www.facebook.com/ReformedPerspectiveMagazine|
|Twitter|EMPTY||
|Website|Our Website|https://reformedperspective.ca|
|Update|EMPTY||
|Store|EMPTY||

**Current *description***:

```text
Reformed Perspective is all about equipping Christians and building Christ's Church. 

We serve you by providing resources to learn about the gospel, love God, and live out Jesus' redemptive work in your life.

We're affiliated with the Canadian and American Reformed Churches.

Give us feedback!  
Send mail to: info@reformedperspective.ca
```

These tabs can be managed using the *Manage tabs* button at the top-right of the Mobile App configuration page. The title of the tab should be short, depending on how many of these tabs there are (mobile screens have limited width). The Subsplash *info* dialog says to use "19 characters/3 tabs, 14/4, and 11/5" as a guideline.

### Tab Types

- Media: audio and video content
- Event: calendar of events
- Bible: bible reading plan
- Giving: for the Subsplash *Giving* product
- Build your own tab: uses custom or smart list items
- Subtabs: up to 4 subtabs pointing to lists
- Browser: internal *browser* tab
- Blog: RSS feed to blog or other resource

<sub><sup>\*</sup> = our current setting for this option</sub><br>
<sub><sup>\**</sup> = we don't use this</sub>
