# Paige

Powerful, pliable pixel perfection. An advanced Hugo theme. [Try it out.](https://willfaught.com/paige)

<img src="https://github.com/willfaught/paige/raw/master/images/screenshot.jpg">

Paige is designed to put your content front and center,
avoiding the typical clutter.
The look is seamless and smooth, scalable and readable, portable and efficient.
The layout is minimal and responsive,
using verticality and white space to focus and delineate parts of the page.
The implementation is flexible and extensible.
It's a versatile canvas that serves most web needs.

Welcome to the last Hugo theme you'll probably ever need.

## Features

- Accessibility
- Analytics
- Automatic switching between light and dark color schemes
- Blog
- Bootstrap
- Comments
- Customizable
- Dark color scheme
- E-mail protection
- Facebook sharing
- Header links
- Landing page
- Light color scheme
- Math typesetting
- Menu
- Minimal design
- Multiple authors
- Multiple languages
- RSS with full content
- Responsive
- Right-to-left languages
- SEO
- Safari and Firefox Reader View support
- Search
- Sections
- Single column
- Social links
- Table of contents
- Twitter sharing

## Community

Get started by [starring](https://github.com/willfaught/paige/stargazers)
and [following](https://github.com/willfaught/paige/watchers) the project.

If you find a problem or have a suggestion,
please share it by [creating an issue](https://github.com/willfaught/paige/issues/new).
Feedback is encouraged and appreciated.

If you have a fix or improvement,
please share it by [creating a pull request](https://github.com/willfaught/paige/compare).

If you make a customization or alteration,
please share it by [posting code or screenshots](https://github.com/willfaught/paige/discussions/8).

## Get started with Hugo

1. [Install Hugo](https://gohugo.io/installation/).

    For Homebrew on Mac:

    ```sh
    $ brew install hugo
    ```

2. Create a site:

    ```sh
    $ hugo new site yourproject
    ```

3. Create a post:

    ```sh
    $ cd yourproject
    $ hugo new my-post.md
    ```

See [Hugo's quick start guide](https://gohugo.io/getting-started/quick-start/) for more information.

## Install

### Option 1: Use a Hugo module

Example `config.yaml`:

```yaml
module:
  imports:
  - path: "github.com/willfaught/paige"
```

Install:

```sh
$ cd yourproject
$ hugo mod init github.com/youraccount/yourproject
$ hugo mod get github.com/willfaught/paige
```

Update:

```sh
$ cd yourproject
$ hugo mod get -u
```

### Option 2: Use a Git subtree

Example `config.yaml`:

```yaml
theme: "paige"
```

Install:

```sh
$ cd yourproject
$ git subtree add --prefix themes/paige --squash https://github.com/willfaught/paige master
```

Update:

```sh
$ cd yourproject
$ git subtree pull --prefix themes/paige --squash https://github.com/willfaught/paige master
```

### Option 3: Use a Git submodule

Example `config.yaml`:

```yaml
theme: "paige"
```

Install:

```sh
$ cd yourproject
$ git submodule add https://github.com/willfaught/paige themes/paige
$ git submodule update --init --recursive --remote
```

Update:

```sh
$ cd yourproject
$ git submodule update --recursive --remote
```

### Option 4: Use a copy

Example `config.yaml`:

```yaml
theme: "paige"
```

Install:

```sh
$ cd yourproject
$ git clone https://github.com/willfaught/paige themes/paige
$ rm -rf themes/paige/.git
```

Update:

```sh
$ cd yourproject
$ rm -rf themes/paige
$ git clone https://github.com/willfaught/paige themes/paige
$ rm -rf themes/paige/.git
```

## Run

```sh
$ cd yourproject
$ hugo mod npm pack
$ npm install
$ hugo server -D
```

## Configure

### Parameters

There is a single parameter object with sensible defaults that can be overridden in site or page parameters:

```yaml
paige:
  analytics:
    chartbeat: # See https://chartbeat.com
      account_id: "" # Example is "123456"
      domain: "" # Example is "example.com"
    clicky: # See https://clicky.com
      account_id: "" # Example is "123456"
    fathom: # See https://usefathom.com
      account_id: "" # Example is "123456"
    finteza: # See https://finteza.com
      account_id: "" # Example is "123456"
      script_url: "" # Example is "https://example.com/script.js"
    hotjar: # See https://hotjar.com
      account_id: "" # Example is "123456"
    matomo: # See https://matomo.org
      account_id: "" # Example is "123456"
      host_url: "" # Example is "https://example.com"
    mixpanel: # See https://mixpanel.com
      token: "" # Example is "123456"
    plausible: # plausible.io
      account_id: "" # Example is "123456"
    woopra: # See https://woopra.com
      domain: "" # Example is "example.com"
    yandex: # See https://metrica.yandex.com
      account_id: "" # Example is "123456"
  color: "#0d6efd" # Bootstrap primary color; theme color for Safari and Windows
  color_scheme: "" # Always use this color scheme without automatic switching; must be "", "light", or "dark"
  comments:
    cactus: # See https://cactus.chat
      account_id: "" # Example is "123456"
    commento: # See https://commento.io
      script_url: "" # Example is "https://example.com/script.js"
    hyvor: # See https://hyvor.com
      account_id: "" # Example is "123456"
    intensedebate: # intensedebate.com
      account_id: "" # Example is "123456"
    isso: # See https://isso-comments.de
      script_url: "" # Example is "https://example.com/script.js"
    remark42: # See https://remark42.com
      host_url: "" # Example is "https://example.com"
      site_id: "" # Example is "123456"
    replybox: # See https://getreplybox.com
      account_id: "" # Example is "123456"
    utterances: # See https://utteranc.es
      github_repo: "" # Example is "example/foo"
  credit:
    data:
      hide: false # Don't credit this project in a data attribute
    link:
      hide: false # Don't credit this project in the footer
  header:
    menu:
      breakpoint: "sm" # Bootstrap breakpoint at which to display all menu items
      style: "pills" # Must be "links" or "pills"
  home:
    blurb: "" # Displayed below the greeting
    greeting: "" # Displayed below the image
    image:
      raw: false # Do not copy or process the file
      stretch: false # Stretch the image fully horizontally if true; center the image otherwise
      url: "" # Local or remote resource glob
  list:
    authors:
      class: "mb-0 text-center text-secondary"
      hide: false
    content:
      show: false
    date:
      class: "mb-0 text-center text-secondary"
      format: ":date_long" # Hugo date format
      hide: false
    date_header:
      class: "h5 text-center"
      hide: false
    description:
      class: "mb-0 text-center"
      hide: false
    pages:
      hide: false
    reading_time:
      class: "mb-0 text-center text-secondary"
      hide: false
    section:
      class: "mb-3 w-100"
    summary:
      class: "fst-italic mb-0 text-center"
      hide: false
    terms:
      hide: false
      inner_class: "badge text-bg-secondary text-decoration-none"
      outer_class: "mb-0 text-center"
    title:
      class: "mb-0 text-center"
      hide: false
  main:
    metadata:
      authors:
        class: "text-center text-secondary"
        hide: false
      date:
        class: "text-center text-secondary"
        format: ":date_long" # Hugo date format
        hide: false
        lastmod:
          hide: false
      description:
        class: "lead text-center"
        hide: false
      git:
        commit_url_prefix: "" # Example is "https://github.com/willfaught/paige/commit/"
      max_width: ""
      reading_time:
        class: "text-center text-secondary"
        hide: false
      section:
        class: "paige-metadata w-100"
      terms:
        hide: false
        inner_class: "badge text-bg-secondary text-decoration-none"
        outer_class: "text-center"
      title:
        class: "display-5 fw-bold text-center"
        hide: false
    table_of_contents:
      class: "border mb-3 pe-3 ps-3 pt-3 rounded"
      hide: false
      max_width: ""
    content:
      class: "mw-100 paige-content"
      hide: false
      max_width: ""
  math: false # Enable math typesetting
  rss:
    hide_page: false
    managing_editor: ""
    web_master: ""
  search:
    hide_page: false
  social:
    examplesite:
      bootstrap_icon: "" # Example is "example-icon"
      name: "" # Example is "Example"
      url: "" # Example is "https://example.com/username"
```

The assigned values shown are the default values.

If you set `paige.credit.data.hide` or `paige.credit.link.hide`, please credit this project in a post to help others find it.

### Site parameters

Optional site parameters:

```yaml
authors:
  michael_bluth:
    name: "Michael Bluth"
    default: false # Credit this author in pages that have no authors parameter
```

### Page parameters

Optional page parameters:

```yaml
authors:
- "michael_bluth" # Credit the corresponding author in the site parameters
- author: "michael_bluth" # Credit the corresponding author in the site parameters
- name: "Michael Bluth" # Credit this author
link: "https://youtu.be/dQw4w9WgXcQ" # The reference for an anchor around the title
```

### Minimal look

By default, everything is shown. If you want a more minimal look, try the following:

```yaml
paige:
  list:
    authors:
      hide: true
    date:
      hide: true
    reading_time:
      hide: true
    summary:
      hide: true
    terms:
      hide: true
  main:
    metadata:
      reading_time:
        hide: true
      terms:
        hide: true
    table_of_contents:
      hide: true
```

## Layouts

The `paige/search` layout provides full site search.

Example `config.yaml`:

```yaml
outputs:
  home: ["html", "json", "rss"]
```

Example `content/search.md`:

```yaml
---
layout: paige/search
title: Search
---
```

## Shortcodes

### Figure

The `paige/figure` shortcode provides a figure with content.

```
{{< paige/figure
    caption="My caption"
    float="left"
    height="10rem"
    horizontal="center"
    maxheight="10rem"
    maxwidth="10rem"
    number=0
    numbered=false
    vertical="center"
    width="10rem"
>}}
My content
{{< /paige/figure >}}
```

Inner content: Required. String. Markdown. The content.

Parameters:

<dl>
    <dt><code>caption</code></dt>
    <dd>Optional. Position 0. String. Markdown. Descriptive text below the content.</dd>
    <dt><code>float</code></dt>
    <dd>Optional. String. Float to one side of its container. Must be <code>start</code> or <code>end</code>.</dd>
    <dt><code>height</code></dt>
    <dd>Optional. String. CSS value. Total height.</dd>
    <dt><code>horizontal</code></dt>
    <dd>Optional. String. Horizontal alignment. Must be <code>start</code>, <code>center</code>, or <code>end</code>. Default is <code>center</code>.</dd>
    <dt><code>maxheight</code></dt>
    <dd>Optional. String. CSS value. Maximum total height.</dd>
    <dt><code>maxwidth</code></dt>
    <dd>Optional. String. CSS value. Maximum total width.</dd>
    <dt><code>number</code></dt>
    <dd>Optional. Integer or string. Figure number. Displayed with the caption.</dd>
    <dt><code>numbered</code></dt>
    <dd>Optional. Boolean. Number the figure automatically. Displayed with the caption.</dd>
    <dt><code>vertical</code></dt>
    <dd>Optional. String. Vertical alignment. Must be <code>start</code>, <code>center</code>, or <code>end</code>. Default is <code>center</code>.</dd>
    <dt><code>width</code></dt>
    <dd>Optional. String. CSS value. Total width.</dd>
</dl>

### Quote

The `paige/quote` shortcode provides a figure with a quotation.

```
{{< paige/quote >}}
My content
{{< /paige/quote >}}
```

Inner content: Required. String. Markdown. The quotation.

Parameters:

It has the parameters of the `paige/figure` shortcode.

### Code

The `paige/code` shortcode provides a figure with code.

```
{{< paige/code
    caption="My caption"
    lang="html"
    options="linenos=true"
>}}
<!doctype html>
<html lang="en">
<body>
  <p>Test</p>
</body>
</html>
{{< /paige/code >}}
```

Inner content: Required. String. The code.

Parameters:

<dl>
    <dt><code>caption</code></dt>
    <dd>Optional. String. Markdown. Descriptive text below the code.</dd>
    <dt><code>lang</code></dt>
    <dd>Optional. Position 0. String. Chroma language code. Defaults to <code>plaintext</code>. See the <a href="https://gohugo.io/content-management/syntax-highlighting/#list-of-chroma-highlighting-languages">codes</a>.</dd>
    <dt><code>options</code></dt>
    <dd>Optional. String. Hugo highlight options. See the <a href="https://gohugo.io/content-management/syntax-highlighting/#highlight-shortcode">options</a>.</dd>
</dl>

It has the other parameters of the `paige/figure` shortcode.

### Image

The `paige/image` shortcode provides a figure with an image.

```
{{< paige/image
    alt="My alt" >}}
    caption="My caption"
    link="https://github.com/willfaught/paige"
    method="resize"
    options="550x webp picture Lanczos"
    raw=false
    src="me.jpg"
    title="My title"
>}}
```

Inner content: None.

Parameters:

<dl>
    <dt><code>alt</code></dt>
    <dd>Optional. String. Plain text. Image alt.</dd>
    <dt><code>caption</code></dt>
    <dd>Optional. String. Markdown. Descriptive text below the image.</dd>
    <dt><code>link</code></dt>
    <dd>Optional. String. URL. Image link.</dd>
    <dt><code>method</code></dt>
    <dd>Optional. String. Hugo image processing method. Must be <code>crop</code>, <code>fill</code>, <code>fit</code>, or <code>resize</code>. Must be specified with <code>options</code>. See the <a href="https://gohugo.io/content-management/image-processing/#image-processing-methods">methods</a>.</dd>
    <dt><code>options</code></dt>
    <dd>Optional. String. Hugo image processing options. Must be specified with <code>method</code>. See the <a href="https://gohugo.io/content-management/image-processing/#image-processing-options">options</a>.</dd>
    <dt><code>raw</code></dt>
    <dd>Optional. Boolean. Whether to reference an image without copying it. Default is <code>false</code>.</dd>
    <dt><code>src</code></dt>
    <dd>Required. Position 0. String. URL. Image source.</dd>
    <dt><code>title</code></dt>
    <dd>Optional. String. Plain text. Image title.</dd>
</dl>

It has the other parameters of the `paige/figure` shortcode.

### Gallery

The `paige/gallery` shortcode provides a figure with a collection of images.

```
{{< paige/gallery
    align="center"
    caption="My caption"
    height="10rem"
    images="*.jpg"
    justify="center"
    maxheight="10rem"
    maxwidth="10rem"
    method="resize"
    options="550x webp picture Lanczos"
    type="list"
    width="10rem"
/>}}

{{< paige/gallery >}}
    {{< paige/gallery
        caption="My caption"
        height="10rem"
        image="me.jpg"
        maxheight="10rem"
        maxwidth="10rem"
        method="resize"
        options="550x webp picture Lanczos"
        raw=false
        width="10rem"
    />}}
    {{< paige/gallery
        caption="My caption"
        height="10rem"
        image="you.jpg"
        maxheight="10rem"
        maxwidth="10rem"
        method="resize"
        options="550x webp picture Lanczos"
        raw=false
        width="10rem"
    />}}
{{< /paige/gallery >}}
```

Inner content: Optional. String. HTML. Must be other uses of this shortcode.

Parameters:

<dl>
    <dt><code>align</code></dt>
    <dd>Optional. String. Cross axis alignment. Must be <code>baseline</code>, <code>center</code>, <code>end</code>, <code>start</code>, or <code>stretch</code>. Must not be used when nested.</dd>
    <dt><code>caption</code></dt>
    <dd>Optional. String. Markdown. Descriptive text below the image or images.</dd>
    <dt><code>height</code></dt>
    <dd>Optional. String. CSS value. Image height.</dd>
    <dt><code>image</code></dt>
    <dd>Optional. String. Page, site, or remote image glob. Only used in the inner content of this shortcode.</dd>
    <dt><code>images</code></dt>
    <dd>Optional. Position 0. String. Page, site, or remote images glob. Default is all image page resources.</dd>
    <dt><code>justify</code></dt>
    <dd>Optional. String. Main axis space distribution. Must be <code>around</code>, <code>between</code>, <code>center</code>, <code>end</code>, <code>evenly</code>, or <code>start</code>. Must not be used when nested.</dd>
    <dt><code>maxheight</code></dt>
    <dd>Optional. String. CSS value. Maximum image height.</dd>
    <dt><code>maxwidth</code></dt>
    <dd>Optional. String. CSS value. Maximum image width.</dd>
    <dt><code>method</code></dt>
    <dd>Optional. String. Hugo image processing method. Must be <code>crop</code>, <code>fill</code>, <code>fit</code>, or <code>resize</code>. Default is <code>resize</code>. See the <a href="https://gohugo.io/content-management/image-processing/#image-processing-methods">methods</a>.</dd>
    <dt><code>options</code></dt>
    <dd>Optional. String. Hugo image processing options. Default is <code>550x webp picture Lanczos</code>. See the <a href="https://gohugo.io/content-management/image-processing/#image-processing-options">options</a>.</dd>
    <dt><code>raw</code></dt>
    <dd>Optional. Boolean. Whether to reference an image without copying it. Default is <code>false</code>.</dd>
    <dt><code>type</code></dt>
    <dd>Optional. String. Type of layout. Grid and list layouts use the horizontal axis as the main axis, and the vertical axis as the cross axis. Must be <code>grid</code> or <code>list</code>. Default is <code>list</code>.</dd>
    <dt><code>width</code></dt>
    <dd>Optional. String. CSS value. Image width.</dd>
</dl>

It has the other parameters of the `paige/figure` shortcode.

### Vimeo

The `paige/vimeo` shortcode provides a responsive Vimeo video.

```
{{< paige/vimeo
    autopause=true
    autoplay=false
    background=false
    byline=true
    color="00adef"
    controls=true
    description="My description"
    dnt=false
    fullscreen=true
    keyboard=true
    loop=false
    muted=false
    pip=false
    playsinline=true
    portrait=true
    quality="auto"
    speed=false
    texttrack=false
    time="1m2s"
    title=true
    transparent=true
    video="644036051"
>}}
```

Inner content: None.

Parameters:

<dl>
    <dt><code>autopause</code></dt>
    <dd>Optional. Boolean. Enable playing more than one Vimeo video on the same page. Default is <code>true</code>.</dd>
    <dt><code>autoplay</code></dt>
    <dd>Optional. Boolean. Autoplay the video. Default is <code>false</code>.</dd>
    <dt><code>background</code></dt>
    <dd>Optional. Boolean. Autoplay the video. Hide the controls. Loop the video. Mute the video. Default is <code>false</code>.</dd>
    <dt><code>byline</code></dt>
    <dd>Optional. Boolean. Show the author. Default is configured per video.</dd>
    <dt><code>color</code></dt>
    <dd>Optional. String. Hex code. Control color. Default is <code>00adef</code>.</dd>
    <dt><code>controls</code></dt>
    <dd>Optional. Boolean. Show the controls. Default is <code>true</code>.</dd>
    <dt><code>description</code></dt>
    <dd>Optional. String. Plain text. Screen reader content. Default is <code>Vimeo video</code>.</dd>
    <dt><code>dnt</code></dt>
    <dd>Optional. Boolean. Do not track session data. Default is <code>false</code>.</dd>
    <dt><code>fullscreen</code></dt>
    <dd>Optional. Boolean. Enable full screen. Default is <code>true</code>.</dd>
    <dt><code>keyboard</code></dt>
    <dd>Optional. Boolean. Enable keyboard input. Default is <code>true</code>.</dd>
    <dt><code>loop</code></dt>
    <dd>Optional. Boolean. Loop the video. Default is <code>false</code>.</dd>
    <dt><code>muted</code></dt>
    <dd>Optional. Boolean. Mute the video. Default is <code>false</code>.</dd>
    <dt><code>pip</code></dt>
    <dd>Optional. Boolean. Show the picture-in-picture control. Default is <code>false</code>.</dd>
    <dt><code>playsinline</code></dt>
    <dd>Optional. Boolean. Play inline instead of full screen on mobile devices. Default is <code>true</code>.</dd>
    <dt><code>portrait</code></dt>
    <dd>Optional. Boolean. Show the author's profile image. Default is configured per video.</dd>
    <dt><code>quality</code></dt>
    <dd>Optional. String. The resolution. Must be <code>auto</code>, <code>240p</code>, <code>360p</code>, <code>540p</code>, <code>720p</code>, <code>1080p</code>, <code>2k</code>, or <code>4k</code>. Default is <code>auto</code>.</dd>
    <dt><code>speed</code></dt>
    <dd>Optional. Boolean. Show the speed controls. Default is <code>false</code>.</dd>
    <dt><code>texttrack</code></dt>
    <dd>Optional. String. Language code and optionally a locale code (e.g. <code>en</code>, <code>en-US</code>). Use the corresponding subtitles. Default is <code>false</code>.</dd>
    <dt><code>time</code></dt>
    <dd>Optional. String. Duration (e.g. <code>0m</code>, <code>1m2s</code>). Start time. Default is <code>0m</code>.</dd>
    <dt><code>title</code></dt>
    <dd>Optional. Boolean. Show the title. Default is configured per video.</dd>
    <dt><code>transparent</code></dt>
    <dd>Optional. Boolean. Use a transparent background instead of a black one. Default is <code>true</code>.</dd>
    <dt><code>video</code></dt>
    <dd>Optional. Position 0. String. Video ID.</dd>
</dl>

It has the parameters of the `paige/figure` shortcode.

See [Vimeo documentation](https://vimeo.zendesk.com/hc/en-us/articles/360001494447-Player-parameters-overview) for more detail.

### YouTube

The `paige/youtube` shortcode provides a responsive YouTube video.

```
{{< paige/youtube
    autoplay=false
    controls=true
    end=20
    fullscreen=true
    list=PL2WkvfelorAFjpzGUWc4OWAWmiJpwL97L
    loop=true
    mute=true
    start=10
    title="My title"
    video="dQw4w9WgXcQ"
>}}
```

Inner content: None.

Parameters:

<dl>
    <dt><code>autoplay</code></dt>
    <dd>Optional. Boolean. Automatically play the video.</dd>
    <dt><code>controls</code></dt>
    <dd>Optional. Boolean. Show video controls. Default is <code>true</code>.</dd>
    <dt><code>description</code></dt>
    <dd>Optional. String. Plain text. Screen reader content. Default is <code>YouTube video</code>.</dd>
    <dt><code>end</code></dt>
    <dd>Optional. Integer. Elapsed seconds. Stop the video here.</dd>
    <dt><code>fullscreen</code></dt>
    <dd>Optional. Boolean. Enable full screen. Default is <code>true</code>.</dd>
    <dt><code>list</code></dt>
    <dd>Optional. String. Playlist ID.</dd>
    <dt><code>loop</code></dt>
    <dd>Optional. Boolean. Loop the video.</dd>
    <dt><code>mute</code></dt>
    <dd>Optional. Boolean. Mute the video.</dd>
    <dt><code>start</code></dt>
    <dd>Optional. Integer. Elapsed seconds. Start the video here.</dd>
    <dt><code>video</code></dt>
    <dd>Optional. Position 0. String. Video ID.</dd>
</dl>

It has the parameters of the `paige/figure` shortcode.

## Customize

### Include

| If this file exists in the site    | It is included at               |
| ---------------------------------- | ------------------------------- |
| `partials/paige/body-first.html`   | The beginning of the body tag   |
| `partials/paige/body-last.html`    | The end of the body tag         |
| `partials/paige/footer-first.html` | The beginning of the footer tag |
| `partials/paige/footer-last.html`  | The end of the footer tag       |
| `partials/paige/head-first.html`   | The beginning of the head tag   |
| `partials/paige/head-last.html`    | The end of the head tag         |
| `partials/paige/header-first.html` | The beginning of the header tag |
| `partials/paige/header-last.html`  | The end of the header tag       |
| `partials/paige/main-first.html`   | The beginning of the main tag   |
| `partials/paige/main-last.html`    | The end of the main tag         |

### Override

Most code is in partials that are included by the layouts.
Elements can be added, changed, or removed easily by overriding the corresponding layout or partial.

For example, the layouts
`home.html`, `list.html`, `single.html`, `taxonomy.html`, and `term.html`
include the partial `paige/article.html`.
`paige/article.html` includes the partials `paige/metadata.html`, `paige/toc.html`, and `paige/content.html`.
To change the page title for those layouts, change `paige/metadata.html`.
To change the page title for `single.html`,
replace the use of `paige/article.html` in `single.html` with the use of
`paige/metadata.html`, `paige/toc.html`, and `paige/content.html`,
then replace that use of `paige/metadata.html` with your own design.

### Define

These optional CSS names can be defined how you want:

<dl>
    <dt><code>#paige-container</code></dt>
    <dd>The outermost element in the body.</dd>
    <dt><code>#paige-copyright</code></dt>
    <dd>The copyright in the footer.</dd>
    <dt><code>#paige-credit</code></dt>
    <dd>The credit in the footer.</dd>
    <dt><code>#paige-footer</code></dt>
    <dd>The footer element in the container.</dd>
    <dt><code>#paige-header</code></dt>
    <dd>The header element in the container.</dd>
    <dt><code>#paige-main</code></dt>
    <dd>The main element in the container.</dd>
    <dt><code>#paige-pages</code></dt>
    <dd>The page list in the list and term layouts.</dd>
    <dt><code>#paige-pagination</code></dt>
    <dd>The pagination links in the list and term layouts.</dd>
    <dt><code>.paige-article</code></dt>
    <dd>The page article.</dd>
    <dt><code>.paige-authors</code></dt>
    <dd>The page authors.</dd>
    <dt><code>.paige-content</code></dt>
    <dd>The page content.</dd>
    <dt><code>.paige-date</code></dt>
    <dd>The page date.</dd>
    <dt><code>.paige-date-header</code></dt>
    <dd>The date headers in list and term layouts.</dd>
    <dt><code>.paige-description</code></dt>
    <dd>The page description.</dd>
    <dt><code>.paige-draft</code></dt>
    <dd>Applied to the title of draft pages in the list and term layouts.</dd>
    <dt><code>.paige-expired</code></dt>
    <dd>Applied to the title of expired pages in the list and term layouts.</dd>
    <dt><code>.paige-future</code></dt>
    <dd>Applied to the title of future pages in the list and term layouts.</dd>
    <dt><code>.paige-metadata</code></dt>
    <dd>The page metadata section.</dd>
    <dt><code>.paige-modified</code></dt>
    <dd>Applied to the title of modified pages in the list and term layouts.</dd>
    <dt><code>.paige-page</code></dt>
    <dd>A page in the pages in the list and term layouts.</dd>
    <dt><code>.paige-published</code></dt>
    <dd>Applied to the title of published pages in the list and term layouts.</dd>
    <dt><code>.paige-summary</code></dt>
    <dd>The page summary.</dd>
    <dt><code>.paige-reading-time</code></dt>
    <dd>The page reading time.</dd>
    <dt><code>.paige-terms-inner</code></dt>
    <dd>The page terms.</dd>
    <dt><code>.paige-terms-outer</code></dt>
    <dd>The container of the page terms.</dd>
    <dt><code>.paige-title</code></dt>
    <dd>The page title.</dd>
    <dt><code>.paige-toc</code></dt>
    <dd>The page table of contents.</dd>
    <dt><code>.paige-unpublished</code></dt>
    <dd>Applied to the title of unpublished (draft, expired, future) pages in the list and term layouts.</dd>
</dl>

## Design

The HTML author is the page authors.

The HTML description is the page description.

The HTML keywords is a union of the page keywords, tags, and categories.

The HTML title is the page title, followed by a middle dot, followed by the site title.
If one is missing, the other is used without the middle dot.
For the home page, the title is the page title, or the site title otherwise.

The HTML body can have a header, a body, and a footer.
The header has the menu, the page title, the page description, the page authors, and the page date.
The body has the page content.
The footer has the copyright notice and the theme link.

The page title and description can be Markdown. Markup is stripped for HTML and RSS titles.

The page title is displayed in an `h1` tag, so page content headers must start with `h2`.

The page date is the publish date.

## Implementation

The following NPM packages are used:

- Bootstrap 5.3.0-alpha1
- Bootstrap Icons 1.10.3
- KaTeX 0.16.4

The files are checked into in the repository.

Bootstrap JS and SCSS files can be loaded manually at `paige/bootstrap`,
e.g. `paige/bootstrap/alert.js` and `paige/bootstrap/_alert.scss`.

Hugo names, HTML names, CSS names, and JavaScript names that begin with "paige" capitalized in any way are reserved.

## Credits

Photo by [Sergey Pesterev](https://unsplash.com/photos/JV78PVf3gGI).

## Project

Created by [Will Faught](https://willfaught.com).
Released under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
Hosted at https://github.com/willfaught/paige.
