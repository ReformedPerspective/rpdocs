# Reformed Perspective App

The RP App is delivered via a platform called [Subsplash](https://www.subsplash.com/) which specialized in church websites and apps. They have a number of products which integrate together, but we are just using their Mobile App product. We access the configuration options for the App via the [Subsplash Dashboard](https://dashboard.subsplash.com).

The Mobile App configuration is accessed from the Dashboard by clicking on *Apps* in the left sidebar, and then *Mobile App*. It is set up as a series of '*Screens*' or '[*Tabs*](index.md#bottom-buttons-tabs)' which are shown at the top of the Dashboard interface.

There is some other functionality in the Subsplash Dashboard, such as [Push notifications](pushnotifications.md), [Analytics](analytics.md),[Account Settings](account.md), and other [Settings](settings.md).

## Home Screen Layout

**NOTE**: This 'layout' is the same as the layout available for any of the custom screens or tabs, except that most of the options for the Home screen are enabled.

---

### Header

At the top of the App home screen is an optional *Header* section. This, when turned on, can be a static image (1920 x 692 - 10MB Max.) or a Carousel with up to 5 items. These items can be any of the *Library* items available. We are currently using the Static Image **<sup>\*</sup>** option with the RP Banner.

The Header is configured using the *Design* widget to the right of the Mobile App page. In addition, the *Items* shown on the home screen can have the following properties configured there:

- Layout: can be *Rows*, *Grid* **<sup>\*</sup>**, or *Stacked*
- Item titles: can be *Below* or *Off* **<sup>\*</sup>**. The reason for this choice is that our square icons have a title built in. We don't control the size or font of these titles anyway, so it's better (if more cumbersome) this way.
- Item images: can be *Square* **<sup>\*</sup>** or *Wide*.
- Margins: *On* **<sup>\*</sup>** or *Off*.
- Shadows: *On* **<sup>\*</sup>** or *Off*.

### Content

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

### Bottom buttons (Tabs)

There are some small buttons in a bar at the bottom of the home screen. They take you to various different app screens some of which have the same kind of properties as the home screen, including a Header, Content. These are, currently:

- Home: Tab. Takes you to the [home screen](index.md#home-screen-layout)
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

## Tab Types

- Media: audio and video content
- Event: calendar of events
- Bible: bible reading plan
- Giving: for the Subsplash *Giving* product
- Build your own tab: uses custom or smart list items
- Subtabs: up to 4 subtabs pointing to lists
- Browser: internal *browser* tab
- Blog: RSS feed to blog or other resource

## Library Item Types and Options

- Lists: These are just lists of other items. A list can be any combination of other items. It can even be a list of lists.
- Media Series:
- Event:
- Song:
- RSS: Has a Title and Subtitle and links to an RSS feed. Either *Reader* or *Rows* layout.
    - Reader: This layout uses a repeating pattern of 6 tiles to show the Featured image and summary of each item of an RSS feed.
- Media Item:
- Calendar:
- Album:
- Link: Has a Title and Subtitle and can be any one of the following:
    - Website: Link to external web page. Will open in mobile browser.
    - Video: Link to Youtube or Vimeo video
    - App link: Opens URL inside the app. There are limitations to how well this works.
    - Contact: Link to an email address or phone number. Will open with whatever is configured on the device.
    - Page: Link to custom Subsplash page. (i.e. SnapPages) <sup>\**</sup>
    - Giving or payments: Link to Donation or Store URL
- Fill In Notes: This seems to be a custom web page or a collection of custom pages designed for people to fill in like sermon notes? I'm not sure what this is for or how to use it properly.

Library items can have artwork associate with them, and this artwork will show up in various parts of the App, depending on which size artwork is relevant. The sizes are:

- Square: This is a 1024 x 1024 icon. We used this a lot.
- Wide: A 1920 x 1080 graphic often used as a background image.
- Banner: A 1920 x 692 suitable for banners.

<sub><sup>\*</sup> = our current setting for this option</sub><br>
<sub><sup>\**</sup> = we don't use this</sub>
