# Configurables for Write.as, WriteFreely, and the rest of the Musing Studio Suite

---

*Please note this has just been separated from [extratone/bilge](https://github.com/extratone/bilge) for the sake of clarity/use/my own sanity.*

# Technical Documentation (Writeas Blog)

## Documentation for my blog, [bilge.world](https://bilge.world).

I proudly use [Write.as](https://write.as) as my blog's CMS. I am relatively new to Git and GitHub, but it occurred to me that a repository would be a great place to track technical changes and even versions/revisions of drafts.

---

[![Writeas Customization](https://i.snap.as/xpwZqmy4.png)](https://guides.write.as/customizing/)


##  Installation (Bilge Theme)

To "install" my theme on your own Writeas blog, copy and paste the contents of [Custom CSS.css](https://github.com/extratone/bilge/blob/main/Custom%20CSS.css) and [Custom Javascript.js](https://github.com/extratone/bilge/blob/main/Custom%20Javascript.js) into the respective "Custom CSS" and "Custom Javascript" fields in your blog's customization menu. 

See: "[Customizing Writeas](https://guides.write.as/customizing/)"

---

![Bilge Three Point Oh Footer](https://i.snap.as/B3D5JvZ4.png)

## [Colophon](https://bilge.world/colophon)

*The Psalms* is proudly hosted by [Write.as](http://write.as/about) - a new sort of blogging content management system built atop [Markdown](https://daringfireball.net/projects/markdown/) and maintained by a company which [explicitly shares](https://write.as/principles) my commitment to a better, Open web. 

A somewhat-outdated version of this site's theme is [listed among others](https://write.as/themes/bilge) in Writeas' official themes list. The full, up-to-date CSS and JS can be found below and on in [this GitHub repository](https://github.com/extratone/bilge), which I created in November, 2020 as an experiment in using Git to track editorial changes. (*That means you can see [current in-progress drafts](https://github.com/extratone/bilge/tree/main/Drafts)!*)

- ~~Download the entirety of this blog in EPUB format **[here](http://bilge.world/.epub)**~~. <!--Unfortunately, this isn't working right now.-->
- Subscribe to this blog's RSS feed **[here](https://bilge.world/feed/)**.
- This blog is federated at **@b@bilge.world**.

### Typography

**Body Text**: [Adobe Caslon Pro](https://fonts.adobe.com/fonts/adobe-caslon)

**Nav/Headers/Other**: [Proxima Nova](https://fonts.adobe.com/fonts/proxima-nova) & Variations

### Colors

![The Psalms Colors](https://i.snap.as/yREEslm5.png)

- [Expired Sour Cream](https://colornames.org/color/fff4e6) #fff4e6
- [David Blue](https://colornames.org/color/00006b) #00006b
- [Red](https://colornames.org/color/ff0000) #ff0000
- [Alarmed Suburbanite](https://colornames.org/color/f43f32) #f43f32

### [CSS](https://github.com/extratone/bilge/blob/main/Custom%20CSS.css)

```css
@import url('https://use.typekit.net/kst2rrh.css');

body {
    font-family: adobe-caslon-pro, serif !important;
    font-weight: 400;
    font-style: normal;
    background-color: #FFF4E6;
}

/* old background-color: #f2f2f2 */

#blog-title a {
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 900;
    font-style: normal;
    /* font-style:bold !important; */
    color: #00006b;
}

header nav a {
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 900;
    font-size: 1.2em;
}

header p.description {
    /* font-style: italic; */
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 700;
    line-height: 200% !important;
    color: #00006b !important;
    font-size: 1em;
    margin-left: inherit;
    margin-right: inherit;
}

body#collection header {
    margin-bottom: 1em !important;
}


header nav a {
    color: #00006b;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 900;
    /* margin-bottom: 1em; */
}

body,
article {
    font-family: adobe-caslon-pro, serif !important;
    font-weight: 400;
    line-height: 155%;
    font-size: 1.1em !important;
    color: #000000;
    padding-left: 0.5rem;
    padding-right: 0.5rem;
    /* margin-top:1rem !important; */
}


body,
article a:link {
    color: #00006b;
}

body,
article a:visited {
    color: #FF0000;
}

h1 {
    color: #00006b !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 900;
    font-size: 2em !important;
}

h2 {
    color: #00006b !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 700;
    font-size: 1.4em !important;
}

h3 {
    color: #1c0021 !important;
    font-family: proxima-nova-extra-condensed, sans-serif;
    font-weight: 600;
    font-size: 1.3em !important;
}

h4 {
    color: #1c0021 !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-size: 1em !important;
}

h5 {
    color: #1c0021 !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-size: 1em !important;
}

h6 {
    color: #1c0021 !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-size: .85em !important;
}

code {
    /* background-color:#f7ff85 !important; */
    /* border: 1px solid #da2573 !important;
    border-radius: 1px !important; */
    font-size: 0.85em !important;
    color: #1c0021 !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 400;
    /* padding: 0px 0px 0px 0px !important; */
}

body #post pre, body#collection pre, body#post pre, body#subpage pre {
    background: #FFFdeb; !important;
    border: 1px solid #da2573 !important;
    border-radius: 1px !important;
    font-size: 0.85em !important;
    color: #1c0021 !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 400;
    /* padding: 0px 0px 0px 0px !important; */
}

.post-title a:visited,
.post-title a:link {
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 900;
    color: #00006b !important;
    font-size: 1.7rem !important;
}

body#post article time.dt-published,
body#subpage article time.dt-published {
    font-family: proxima-nova-condensed, sans-serif !important;
    color: #00006b !important;
    font-size: 1rem !important;
}

body footer nav {
    font-family: proxima-nova-condensed, sans-serif !important;
    color: #00006b;
}

blockquote {
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 400;
    color: #333333 !important;
    border-left: 2.5px solid #00006b !important;
}

table {
    background-color: #FFFdeb !important;
    font-size: 0.8em !important;
    line-height: 1.2em;
    color: #1c0021 !important;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 400;
    border: 1px solid #f43f32 !important;
    border-radius: 1px !important;
}

article table td, article table th {
    border: 1px solid !important;
    border-color: #da2573 !important;
}


.gist {
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 400 !important;
    font-size: 18px !important;
}

.gist .gist-meta {
    font-family: proxima-nova-extra-condensed, sans-serif !important;
    font-weight: 600 !important;
    color: #1c0021 !important;
}

.gist, .gist article, .gist article p {
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 400 !important;
}


.gist .gist-file .gist-data {
    background: #FFFdeb; !important;
    border: 1px solid #da2573 !important;
    border-radius: 1px !important;
    font-size: 0.85em !important;
    color: #1c0021 !important;
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 400;
}

.gist, .gist article, .gist article p {
    white-space: normal !important;
}

/* .gist .gist-hr {
    display: hide !important;
} */

hr {
    border: 2px solid red;
}


body footer a.home:link,
body footer a.home:visited {
    color: #00006b;
}

.action {
    font-family: proxima-nova-condensed, sans-serif;
}

nav#manage ul a {
    color: #00006b;
}

nav#paging a {
    color: #00006b !important;
    font-family: proxima-nova-condensed, sans-serif !important;
}


a.bt {
    background-color: #0d0d0d !important;
    color: #00006b !important;
}

a.hashtag {
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 700;
    color: #00006b !important;
}

body#collection #wrapper time,
body#subpage #wrapper time,
body#post article time.dt-published,
body#subpage article time.dt-published {
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 700;
    font-size: 0.95em;
    color: #00006b !important;
}


.custom-nav {
    text-align: center;
    font-size: 0.85em;
    text-transform: uppercase;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 700;
    color: red;
}

.custom-nav a:link,
.custom-nav a:visited,
.custom-nav a:hover,
.custom-nav a:active {
    color: #00006b;
}

.custom-nav a:hover,
.custom-nav a:active {
    text-decoration: underline;
}

#subscribe-btn {
    border: 1px #FF0000;
    background: #00006b;
    font-family: proxima-nova-condensed, sans-serif;
    font-weight: 700;
    font-size: 1em;
    color: #FFF4E6;
}

#emailsub {
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 700;
}

.footnote, .footnote-ref {
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 700;
    /* margin-left:2.5px; */
    color: #da2573 !important;
    font-size: 1.1em;
    text-decoration:underline #FF0000;
}

.footnote-ref {
    margin-left:25px;
}

.footnote-ref-text {
    font-family: proxima-nova-condensed, sans-serif !important;
    font-weight: 400;
    color: #1c0021 !important;
    font-size: 1em;
    border-top: #00006b dotted 1px;
}
```
### [Javascript](https://github.com/extratone/bilge/blob/main/Custom%20Javascript.js)

```javascript
var topP = document.createElement("p");
//topP.style.textAlign = "center";
topP.innerHTML = '<hr><div class="custom-nav"><a rel="me" href="https://mastodon.social/@DavidBlue">Mastodon</a> ※ <a href="https://twitter.com/NeoYokel">Twitter</a> ※ <a href="https://discord.gg/4hdQcVd">Discord</a> ※ <a href="https://github.com/extratone/bilge">GitHub</a> ※ <a href="https://gist.github.com/extratone/140a11428b5dd1dda500b3928e0438b1">License</a></div>';
var cont = document.getElementById("wrapper");
if (cont !== null) {
    // Add to blog index and tag pages
    cont.appendChild(topP);
} else {
    // Add to individual blog post page
    cont = document.getElementById("post-body");
    cont.insertAdjacentHTML("afterend", topP.outerHTML);
}

// src: https://platform.twitter.com/widgets.js

// src: https://hypothes.is/embed.js

window.hypothesisConfig = function () {
  return {
    "openSidebar": false, 
    "theme": "clean",
    branding: {
      appBackgroundColor: '#e6f7ff',
      ctaBackgroundColor: '#da2573',
      ctaTextColor: '#00006b',
      selectionFontFamily: 'Georgia, serif'
    }
  };
};

// Footnote hyperlinks in the body.
var notePattern = /\[\^(\d+)\]/g;
var noteText = "<a name=\"fn$1\"></a><sup><a class=\"footnote\" href=\"#fnref$1\">$1</a></sup>";

// Footnote references at the bottom.
var refPattern = /\[(\d+)\](.*)/g;
var refText = "<a name=\"fnref$1\"></a><sup><a class=\"footnote-ref\" href=\"#fn$1\">$1</a></sup><span class=\"footnote-ref-text\">$2</span>";

var postContent = document.getElementById("post-body").innerHTML;
postContent = postContent.replace(notePattern, noteText);
postContent = postContent.replace(refPattern, refText);
document.getElementById("post-body").innerHTML = postContent;
```
