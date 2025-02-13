# SMC Blog

This is the repository for the blog of the [Aalborg University Copenhagen](https://www.aau.dk/en) international master's programme in [Sound and Music Computing](https://www.smc.aau.dk).

To learn how to use the blog, and much more, visit our **[Full Documentation and Guides.](https://github.com/SMC-master/Guides/wiki/How-to-use-the-SMC-Blog)**

<br>

# Quick User Guide

1. [Serve the Blog Locally](#1-serve-the-blog-locally)
2. [Post Layout](#2-post-layout)
   - [Post File Naming and Storage](#post-file-naming-and-storage)
   - [Frontmatter](#frontmatter)
3. [Multi-media](#3-multi-media)
   - [Media File Naming and Storage](#media-file-naming-and-storage)
   - [Embedding Links](#embedding-links)
   - [Embedding Images](#embedding-images)
   - [Embedding Slideshow](#embedding-slideshow)
   - [Embedding Videos](#embedding-videos)
   - [Embedding Audio](#embedding-audio)
4. [Tables](#4-tables)
   - [Standard HTML Tables](#standard-html-tables)
   - [Responsive HTML Tables](#responsive-html-tables)
   - [Markdown Tables](#markdown-tables)
5. [Improvements and Issues](#5-issues-and-improvements)

## 1. Serve the Blog Locally

You can build the SMC blog and visualize it in the browser locally on your machine by installing [Jekyll](https://jekyllrb.com/docs/installation/).

Once you have your Jekyll environment set up, you can serve from the root blog folder using this command in the terminal:

```
bundle exec jekyll serve
```

<br>

## 2. Post Layout

Every blog post markdown file should share the same general layout and folder placement.

<br>

### Post File Naming and Storage

**Drafts**
Posts placed in the `_posts_drafts` will not be published on the blog. Use this folder for drafts and collaboratory efforts. **NB!** Files in the drafts folder are frequently deleted (once every semester) for maintenance reasons.

**Ready Posts**
Posts placed in the `_posts` folder are automatically published to the blog once you push the repo to GitHub, given they have correct file names and front matter.

All posts must share the same filename syntax, whitespaces in the filename are not allowed:

```
YYYY-MM-DD-UiOusername-shortVersionOfTitle.md
```

Example:

```
2022-04-02-aleksati-5g-nmp.md
```

<br>

### Frontmatter

The top of every blog post markdown file must include _frontmatter_. The frontmatter includes important information related to your blog post.

```markdown
---
layout: post
title: "Title of the blog post"
date: YYYY-MM-DD HH:MM:SS Z
categories: category-name
author: Name1 Surname1, Name2 Surname2
image: /assets/image/featured_image.jpg
keywords: comma, separated, list, of, keywords
excerpt: "A short summary, typically copy-pasting the first paragraph of the blog post."
---
```

Example:

```markdown
---
layout: post
title: "5G Networked Music Performances - Will It Work?"
date: 2022-04-11 10:30:00 +0200
categories: networked-music
author: Aleksander Tidemann
image: /assets/image/2022_04_01_aleksati_5g_telenor_logo.png
keywords: SMC, uio, networked music performances, telematic music, 5g, telenor research, lola, jacktrip, audio latency, video latency
excerpt: "In collaboration with Telenor Research, we explored the prospects of doing networked music performances over 5G. Here are the preliminary results."
---
```

<br>

## 3. Multi-media

### Media File Naming and Storage

All media files must share the same filename syntax, whitespaces in the filename are not allowed:

```
YYYY_MM_DD_UiOusername_filename.extension
```

Example:

```
2019_04_19_aleksati_blog_header.jpg
```

You can store files in the appropriate sub-folder of `./assets/` in the GitHub blog repo, given that the files are less than 300KB in size. Files above 300KB must be stored in the equivalent sub-folder of the [UiO Vortex blog folder](https://www-adm.uio.no/english/studies/programmes/SMC-master/blog/assets/?vrtx=admin).

- Path to GitHub blog repo media `/assets/images/filename.extension`
- Path to UiO Vortex folder media - `https://www.uio.no/english/studies/programmes/SMC-master/blog/assets/images/filename.extension`

For more details on storing and sharing media files, visit the ["Embedding and Storage of Files" section](https://github.com/SMC-master/Guides/wiki/How-to-use-the-SMC-Blog-%E2%80%90-Embedding-and-Storage-of-Files) in the SMC Guides.

<br>

### Embedding Links

Links are text that redirects the reader to a different web address. To add links, use this simple markdown syntax:

```
[text](url)
```

Example:

```
[Blix Solutions AS](https://www.blix.com/servers/)
```

<br>

### Embedding Images

The best way to embed images and figures to a blog post is to use and wrap a HTML `<img>` element inside a `<figure>` container:

```HTML
<figure style="float: none">
   <img
      src="PATH-TO-IMAGE"
      alt="Alternative Text"
      title="Image Title"
      width="auto" />
   <figcaption>Caption Text</figcaption>
</figure>
```

The `style="float: none"` can be used to specify the horizontal alignment of the figure and the caption. To do this, simply specify `right`, `left` or `none` (for middle) in the space following `float: `.

It is also possible to add images using Markdown:

```markdown
![Alternate Text](PATH-TO-IMAGE "Image Title")
```

<br>

### Embedding Slideshow

To embed more than one image at a particular place, you can combine multiple images into a slideshow. To add a slideshow to your blog post, use the following HTML structure:

```HTML
<div class="slideshow-container" id="ID-OF-MY-SLIDESHOW">
  <div class="mySlides fade">
    <!-- Insert Figure with Img -->
  </div>
  <div class="mySlides fade">
    <!-- Insert Figure with Img -->
  </div>
  <div class="mySlides fade">
    <!-- Insert Figure with Img -->
  </div>
</div>
```

**NB!** It is important that to specify a unique ID property for every slideshow container. Use a clear and informative name.

You can add as many slideshow items as you want, just remember to wrap each item in a div with "mySlides fade" class names:

```html
<div class="mySlides fade">
  <!-- Insert Figure or other content -->
</div>
```

Each slideshow has a max height of 480px. Therefore, to ensure the best possible user experience, make all slideshow images should have a height equal to or larger than 480px.

<br>

### Embedding Videos

The best way to embed videos in a blog post is to wrap an `<video>` element inside a `<figure>` container. Videos should be in .mp4 format.

```HTML
<figure style="float: none">
  <video width="auto" controls>
    <source src="PATH-TO-VIDEO" type='video/mp4'>
  </video>
  <figcaption>Caption Text</figcaption>
</figure>
```

To embed videos upload on third party platforms such as Youtube or Vimeo use the `<iframe>` element inside a `<figure>` container.

```HTML
<figure style="float: none">
  <iframe src="PATH-TO-VIDEO" width="auto" frameborder="0" allowfullscreen>
  </iframe>
  <figcaption>Caption Text</figcaption>
</figure>
```

Usually you can copy the `<iframe>` element with all fields precompiled directly from the third party platform (select Share -> Embed), for example:

```HTML
<figure style="float: none">
  <iframe
    src="https://www.youtube.com/embed/WGTF7fL8w-Q"
    width="100%"
    height="315"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  >
  </iframe>
  <figcaption>Caption Text</figcaption>
</figure>
```

<br>

### Embedding Audio

The best way to embed audio to a blog post is to use our custom [WaveSurfer](https://wavesurfer-js.org/) audio widget. Simply add a `<div></div>` to your post with a waveform class and the path to your audio:

```HTML
<div class="waveform" path="PATH-TO-AUDIO"></div>
```

With additional features: 

```HTML
<div class="waveform" path="PATH-TO-AUDIO" color="#56BBCC" splitChannels></div>
```

By default, each waveform gets assigned a color. However, you can add a custom color to your waveform through the color attribute. You can also choose to see each audio channel individually in a vertical fashion by using the splitChannels flag. If not specified, a normal waveform style is used. 

You can also create a simpler audio player by wrapping a `<audio/>` element inside a `<figure/>` container.

```HTML
<figure style="float: none">
  <audio controls>
    <source src="PATH-TO-AUDIO" type="audio/mpeg">
    Alternate Text
  </audio>
  <figcaption>Text Caption</figcaption>
</figure>
```

<br>

## 4. Tables

There are three ways to embed tables to your blog post. let's build one table using all three methods. This is what we will create:

<table>
  <tr>
    <!-- Another Row -->
    <td>hey</td>
    <td>hey</td>
    <td>hey</td>
  </tr>
  <tr>
    <!-- Another Row -->
    <td>hey</td>
    <td>hey</td>
    <td>hey</td>
  </tr>
</table>

<br>

### Standard HTML Tables

The standard way to create HTML tables is to use the `<table />` element. You will find a bunch of resources online detailing how to use and customize such tables.

```HTML
<table>
  <tr>
    <!-- Row -->
    <td>hey</td>
    <td>hey</td>
    <td>hey</td>
  </tr>
  <tr>
    <!-- Another Row -->
    <td>hey</td>
    <td>hey</td>
    <td>hey</td>
  </tr>
</table>
```

<br>

### Responsive HTML Tables

The best way to add a table to a blog post is to use responsive tables. Responsive tables are great because they will resize and re-organize themselves to fit different media screens. In other words, your tables will look good both on mobile and desktop devices.

To use responsive tables, wrap multiple `<div class="Rtable-cell"/>` inside a `<div class="Rtable Rtable--3cols Rtable--collapse" />` container, like so:

```HTML
<div class="Rtable Rtable--3cols Rtable--collapse">
  <!-- Column one -->
  <div style="order:1;" class="Rtable-cell">Hey></div>
  <div style="order:2;" class="Rtable-cell">Hey</div>

  <!-- Column two -->
  <div style="order:1;" class="Rtable-cell">Hey</div>
  <div style="order:2;" class="Rtable-cell">Hey</div>

  <!-- Column three -->
  <div style="order:1;" class="Rtable-cell">Hey</div>
  <div style="order:2;" class="Rtable-cell">Hey</div>
</div>
```

In the container, specify the number of columns with the `Rtable--3cols` class.

In every cell, specify an `"order:"` style attribute. This number represents the vertical order of the cells in the table, from top to bottom.

Compare the top table with the table below. Both are the same table, only the HTML is arranged differently. This HTML arrangement will affect how the table responds to smaller screen sizes. To learn more about how this works and how to customize these kinds of responsive tables, visit [this great resource](https://css-tricks.com/accessible-simple-responsive-tables/).

```HTML
<div class="Rtable Rtable--3cols Rtable--collapse">
  <!-- Row one -->
  <div style="order:1;" class="Rtable-cell">hey</div>
  <div style="order:1;" class="Rtable-cell">hey</div>
  <div style="order:1;" class="Rtable-cell">hey</div>

  <!-- Row two -->
  <div style="order:2;" class="Rtable-cell">hey</div>
  <div style="order:2;" class="Rtable-cell">hey</div>
  <div style="order:2;" class="Rtable-cell">hey</div>
</div>
```

<br>

### Markdown Tables

We can also use markdown to generate tables in a blog post.

```markdown
| Hey | Hey | Hey |
| --- | --- | --- |
| Hey | Hey | Hey |
```

Some websites allow you to generate the markdown code automatically, like [this page](https://www.tablesgenerator.com/markdown_tables).

<br>

## 5. Issues and Improvements

Fixing bugs, improving existing features or adding new ones are activities continuously carried out by users of the SMC Blog. If you find anything wrong or if you have suggestions, open an issue in the blog repository and include appropriate labels. If you [open an issue](https://github.com/SMC-master/SMC-master.github.io/issues), you should also take the lead or contribute towards resolving it.

For more information about the blog and how to use it, visit our **[Full Documentation and Guides.](https://github.com/SMC-master/Guides/wiki/How-to-use-the-SMC-Blog)**.
