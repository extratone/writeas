# Write.as eBook Add-on
- [eBook Add-on](https://discuss.write.as/t/ebook-add-on/1271)
matt | 2021-11-17 15:46:16 UTC | #1

Today we're launching a new Labs feature, [**eBook Export**](https://write.as/extend/ebook-preview)! This lets readers download your entire blog or a group of hashtagged posts as an eBook.

This is an early look at the feature with just the basics (see below). But we're releasing it now so you can try it out and help us improve it for everyone.

We're also trying something a little different this time. Since this is a feature we think people will find really useful as it grows, we're charging a small one-time fee ($10) for it. This means you can get it even without a Pro subscription, and as a bonus, you won't have to pay anything else as the feature gets better over time (and the price increases).

This acts as a kind of a "mini crowdfunding campaign" for us. Your contribution will show us how important the feature is, and help fund development, while giving you immediate access to what we've created so far.

(Of course, if this is something you *really* want to give feedback on, but can't afford right now, I totally understand. Just let us know @old-support and we'll give you access.)

## How-to

Once you've enabled eBook export, you can add `.epub` to your blog URLs to download the collection of posts as an ePub file. For example, you can download our official blog here: https://write.as/blog/.epub

If you want all posts tagged `#Updates`, you'd find that here: https://write.as/blog/tag:Updates.epub

### Uses

This only enables new download URLs on all of your blogs. Next, you might want to create a new static page titled "Downloads" and link to the various blog-generated eBooks you'd like to make available to readers.

## Future

Our goal is to make this add-on into a full eBook creator, with just enough customization to be widely useful, but not so much that it becomes unwieldy. Some future options we can imagine today:

* Export as PDF and plain HTML files (with table of contents, cover, etc.)
* Respect blog's *Display Format* setting for post ordering and whether or not to show dates
* Display the exported date
* Cover customization
* Edit metadata like author name, description, etc.
* A few different layout options

## Feedback

What do you think so far? What would you like to see next?

We plan to build this entirely around your feedback, so please feel free to share any thoughts you have!

-------------------------

matt | 2020-04-15 18:54:11 UTC | #2



-------------------------

DeaconPatrick | 2020-04-15 19:09:11 UTC | #3

Wow! This looks fantastic. Excellent for three of my four sites. I need to puzzle out the details when I have time. Thanks!

-------------------------

matt | 2020-04-15 19:13:40 UTC | #5

Taking a look at what happened -- just a second.

-------------------------

DeaconPatrick | 2020-04-15 19:49:00 UTC | #6

I want to make a pinned post/title go directly to a link (which I've yet to successfully do). Can I do this? How? The link for the whole blog is CatholicHalos.org.epub, correct?

-------------------------

DeaconPatrick | 2020-04-15 20:02:07 UTC | #7

Initial impressions:

- I love that it puts first posts first. Great call, even on a blog that shows most recent posts at the top.
- Great and simple look and feel the the eBook.
- .mobi files as request for future (vote for, presuming it's already on the list)
- Overall impression: simple and elegant and easy. Thank you!

With abandon,
Patrick

-------------------------

cjeller1592 | 2020-04-15 20:04:33 UTC | #8


[quote="DeaconPatrick, post:6, topic:1271"]
The link for the whole blog is CatholicHalos.org.epub, correct?
[/quote]

Close! The entire link will be https://catholichalos.org/.epub

[quote="DeaconPatrick, post:6, topic:1271"]
I want to make a pinned post/title go directly to a link (which I’ve yet to successfully do). Can I do this? How?
[/quote]

You can do this! What you'll do is first create an empty post titled "Ebook" and pin it to your blog. Then go to your blog's _Customize_ settings. Scroll down to "Custom JavaScript" and add the following:

```JavaScript

const pinned = document.querySelector('a[href*="https://catholichalos.org/ebook"]');
pinned.href = 'https://catholichalos.org/.epub';


```
Once you save the changes, the pinned "Ebook" page should go directly to the correct ebook link!

-------------------------

DeaconPatrick | 2020-04-15 20:20:39 UTC | #9

Old dog, new tricks! All three blogs in need of ebook options now ebooked! Thanks @cjeller1592 and @matt!

With abandon,
Patrick

-------------------------

tmo404 | 2020-04-15 20:36:27 UTC | #10

Nice! Been looking forward to this feature for a long time, as I want to make *some* sort of book out of the TMO blog. I will definitely be using this, and providing feedback very soon :)

-------------------------

DeaconPatrick | 2020-04-15 20:36:53 UTC | #11

Oops. I saw it backwards. Is it possible to have a setting so that posts publish to the eBook in Chronological order rather than the order they appear on the blog from top to bottom?

-------------------------

matt | 2020-04-16 16:39:43 UTC | #12

Yep! Definitely makes more sense that way. Just sent out some new changes:

* Posts in the eBook are now in chronological order
* Pinned posts will show up first, before other blog posts

-------------------------

processimagining | 2020-04-16 16:51:06 UTC | #13

Tried using the feature, receive this: 404 page not found
or

{"code":500,"error_msg":"This is an unhelpful error message for a miscellaneous internal error."}

-------------------------

DeaconPatrick | 2020-04-16 16:54:36 UTC | #14

Yes, what worked on my blogs yesterday now gives: "{"code":500,"error_msg":"This is an unhelpful error message for a miscellaneous internal error."}" Something broke.

-------------------------

matt | 2020-04-16 16:55:58 UTC | #15

Can you both try again @processimagining and @DeaconPatrick? Should work now -- just working out some kinks with our update process.

-------------------------

DeaconPatrick | 2020-04-16 17:09:37 UTC | #16

Works for me now! Thank you, @matt! Chronological order and pinned posts first looks great! Wish list: Table of contents?

-------------------------

matt | 2020-04-16 17:36:25 UTC | #17

Definitely, table of contents would be a nice addition. Will get that on the list.

-------------------------

egoecho | 2020-04-16 20:41:58 UTC | #18

Wow, this looks really promising and a very nice addition. Great! I will def try this as soon as (and come back with nothing but cheers or wish list thingies, or both!).

-------------------------

mistynotes | 2020-04-17 07:51:37 UTC | #19

This looks very good! And it is very smart to offer all those people the opportunity to bundle all their poems or proza in an ebook.

Is it possible to extend the css for ebooks a little, just as it is customizable for the website? I know one can do this manually in for example the ebook editor of Calibre. (I tried this, and it works.) But it would be nice to be able to style the ebook a little more, so that it is automatically updated everytime the ebook is generated.

-------------------------

DeaconPatrick | 2020-04-17 17:36:17 UTC | #20

Further suggestions:
- categorize pinned posts as "front matter" and posts as "chapters" (this is the language used on Pressbooks.com, perhaps industry standard?). Some of my pinned posts are front, others back matter, but putting them all as front covers it without adding complexity. Come to think of it, they could all be back matter too.
- Set "landing page" when first opening it to the first chapter, skipping the front matter.

-------------------------

scott | 2020-04-18 02:11:10 UTC | #21

First off, thanks to @matt and the team for adding this feature to Write.as. I got really excited when I read the email from @cjeller1592 . And, in the last 24 or so hours, a few of the little annoyances that I noticed have been fixed.

I just wanted to share a couple or three thoughts and things I've noticed while playing with the EPUB export today:

1. Would it be possible to exclude pinned pages from the output?

2. Is there a way to use a site's custom CSS to format the EPUB, and then fall back to the CSS file that EPUB generator uses?

3. Matt's original announcement in the forum mentioned that the EPUB export is better suited to text-only blogs/sites. But I noticed that with one or two of the desktop ebook readers I used, images on a page display. But when I open an EPUB in the Sigil ebook editor, this message displays:

    ![sigil-writes.as-epub|516x197](upload://2FT3IiQcCkaRHJ5tPLsLXp5bKn.png) 

    That error is caused by the img tag on pages, which isn't properly formed (either in the EPUB or on Write.as). The closing / of the tag is missing in both. In Sigil and one of the EPUB readers I tested, an error message displays at the top of a page containing an image.

4. When then EPUB downloads (at least when using Firefox), the file name is the first word of a site's or blog's name/title and the .EPUB extension isn't added to the file name. I know there's nothing you can do about that, but just a heads up.

I plan to keep fiddling (including on my phone and a tablet). But this is a great addition to Write.as, and as others have pointed out looks really promising.

-------------------------

matt | 2020-04-18 18:21:56 UTC | #22

Thanks for the feedback, everyone! Here's what I'm gathering so far:

* We'll need to offer customization around pinned posts: include at front, include at back, exclude completely. Would anyone want to include only *certain* pinned posts, as opposed to the whole bunch?

* We should include custom blog CSS with the ebook. I would like to keep this as simple as possible, so I'd prefer to avoid this upcoming suggestion, but would anyone want a separate custom stylesheet for the ebook?

To address some questions / feedback:

[quote="DeaconPatrick, post:20, topic:1271"]
Set “landing page” when first opening it to the first chapter, skipping the front matter.
[/quote]

@DeaconPatrick, do you mean this would exclude all front matter in the ebook? Or that we might somehow tell the ereader to open to the first chapter?

[quote="scott, post:21, topic:1271"]
Matt’s original announcement in the forum mentioned that the EPUB export is better suited to text-only blogs/sites. But I noticed that with one or two of the desktop ebook readers I used, images on a page display.
[/quote]

Images are fetched remotely, so they will show up on internet-connected devices. But the goal is to include them in the ebook itself, so you can read it completely offline.

[quote="scott, post:21, topic:1271"]
That error is caused by the img tag on pages, which isn’t properly formed (either in the EPUB or on Write.as). The closing / of the tag is missing in both.
[/quote]

This is fixed now, though testing with Sigil still brings up some other errors for me. We'll keep working at 100% correctly-formatted files.

[quote="scott, post:21, topic:1271"]
When then EPUB downloads (at least when using Firefox), the file name is the first word of a site’s or blog’s name/title and the .EPUB extension isn’t added to the file name.
[/quote]

This is fixed too -- just needed to adjust the HTTP headers to work with spaces.

-------------------------

scott | 2020-04-18 20:37:59 UTC | #23

That's some fine, fast work there!

>Images are fetched remotely, so they will show up on internet-connected devices. But the goal is to include them in the ebook itself, so you can read it completely offline.

That actually seems to depend on the ebook reader, too. The images show up when using Calibre's ebook reader and in Sigil, but not in Foliate (there's just an empty rectangle). But at least the nasty malformed HTML tag message isn't there!

Thanks for all the work that you and the team are putting into this feature, @matt!

-------------------------

DeaconPatrick | 2020-04-18 21:08:43 UTC | #24

Set landing page to first chapter: Generally when I open an eBook for the first time, it opens to the first chapter (Kindle Paperwhite). This happens because it automatically (I think?) skips anything marked as front matter, while still retaining the front matter.

-------------------------

mistynotes | 2020-04-20 11:24:33 UTC | #25

> We should include custom blog CSS with the ebook. I would like to keep this as simple as possible, so I’d prefer to avoid this upcoming suggestion, but would anyone want a separate custom stylesheet for the ebook?

Although one could argue  that an ebook is not a blog and needs a little bit different css, I am ok with having the option to include the customized blog css in the generated ebook.  It is always possible to make some changes afterwards. Thanks again for this great feature!

-------------------------

egoecho | 2020-04-20 20:52:30 UTC | #26

First: I am very happy with the new feature, still playing around with it, but looks good already.

In addition:

* yes, I would def like to exclude (some) pinned posts;
* also (if possible) to have an option to *only* use a certain tag, even if the post itself has more tags. For example, if I tagged a post with both prose and poetry, the option the generate an eBook with only one of them;
* and.... in the output remove the tag (so it will not appear in the output)...?

-------------------------

dino | 2020-04-27 04:36:49 UTC | #27

Would there be some stats or an indication that people have actually downloaded the ebooks?

-------------------------

veyne | 2020-05-20 04:52:33 UTC | #28

So I've tried it (on my mobile). Typed the adress, got an epub instantly (without having to rename it to add the .epub extension).

The result is nearly flawless : each post is a "chapter", and the formatting is top notch. 

Much to my surprise, with the android App Librium you can play videos inside the book.

I still haven't tested it on desktop, but overall impression is fantastic.

On a side note, I've been looking for FOSS android epub apps, but there are almost always none (correct me if I'm wrong).

Also, but it is unavoidable: each reader has its preset rules and formatting is different on different readers (gotta do with it). 

Finally I agree with these points mentionned by Deacon Patrick and scott:

* (*selected*) pinned posts as front matter and posts as chapters
* Set landing page to the 1st chapter

I'm not sure about custom css (complicated to implement and it won't be used by many; plus I might be wrong but you can edit the CSS yourself "manually").

Anyway, that's a much welcome addition to the tools available, thanks!

-------------------------

veyne | 2020-05-30 05:53:38 UTC | #29

Made a first try. In order to exclude to post announcing the possibility to download the epub, I used a # that I put in all posts except the epub post. However, if your blog is called X and the # is, for instance "book1", then the cover generated will look like that:

Book1

By X

If you don't use the tag, the cover will be your blog name in big bold letters.

There are two workarounds so far, probably more: 

* Someone else used this trick: creating another blog dedicated to the epub and without the posts you want to exclude

* Or, if you use the tag method, I think you'd get a better cover if your tag is capitalized and contain invisible HTML characters in order to replace spaces:
for instance: tag: FIRST YEAR IN CANADA.

There are multiple ways to createb invisible characters, just gotta find which ones work.

-------------------------

triptych | 2020-08-09 19:32:01 UTC | #30

I love the idea of this. I know there are sites like LeanPub that use this as their main feature. ( ePub plus others like .mobi, pdf)
My asks would be:
support epub, .mobi, pdf 
Allow a way to auto updated all the "exported" formats so say you edited a post it would 
1) version all the exports
2) create new files 
3) notify all "subscribers" that there was a new version posted.

-------------------------

ariadnemm | 2021-06-20 15:29:31 UTC | #31

I love this feature!
It works well on my main blog.

But I just I tried this with a private blog and I got the following error:
`{"code":500,"error_msg": "This is an unhelpful error message for a miscellaneous internal error."}`

Does anyone know what might be the error?

-------------------------

matt | 2021-11-17 15:46:17 UTC | #33

Hey @ariadnemm, really glad you like it! I'll need to take a look at this internally to see what might've caused it.

Could you share the name of the blog that's giving you this error in a private message to @support? Or could you try downloading the .epub again and let me know once you've done that, so I can look up the error?

-------------------------

ariadnemm | 2021-11-17 15:46:17 UTC | #35

Yes, I sent a private message to @support. Thanks!

-------------------------

matt | 2021-06-29 14:43:39 UTC | #36

I appreciate it! It looks like this was a wider issue that didn't just affect private blogs. It was limited to one of our backend servers, which means it would've happened occasionally, depending on where your request landed. But this is fixed for everyone now!

-------------------------

jas | 2021-10-06 10:42:16 UTC | #37

This looks cool!

And, as someone who quickly realised he could *not* format his own ebook (i.e. convert from MS Word to ePUB), if this effectively enables me to self-format in an easy way, this would be especially handy.

In general, I also *love* the idea of being able to convert my blog posts to a book format, as I have a feeling I might publish some kind of memoir/journal of my blog posts as some point.

-------------------------

DavidBlue | 2022-02-21 13:20:20 UTC | #38

![Generic Server Error](https://user-images.githubusercontent.com/43663476/154961871-cda6612b-d29a-44bf-a60c-81e472788928.png)

I’ve been getting this generic server error when trying to download .epub files from `bilge.world/.epub` and `bilge.writeas.com/.epub` though these two still work:
- `chaff.writeas.com/.epub`
- `extratone.com/.epub`

Could this be a domain error or perhaps my Bilge has simply gotten Too Big?

-------------------------

matt | 2022-02-21 13:53:05 UTC | #39

Thanks for the heads up! I'm not sure what the root cause is, though it looks like we're not gracefully handling the error, which caused this. I'll get a fix in and then we can figure out what exactly is causing it.

-------------------------

justinf | 2022-02-25 01:10:32 UTC | #40

Two notes. I am trying this feature but can't use it at present because:

**1. Every other page has some error on it. Here is an example:**

“This page contains the following errors:
error on line 31 at column 11: Opening and ending tag mismatch: hr line 0 and article
Below is a rendering of the page up to the first error.”

**2. The Post Signature field is included on every post.** 
Can that get excluded? Doesn't seem appropriate to have that published for every post.

-------------------------

matt | 2022-02-25 21:20:20 UTC | #41

[quote="justinf, post:40, topic:1271"]
1. Every other page has some error on it.
[/quote]

I'd guess that this might have to do with some HTML in the posts -- I think the epub format works best with the valid HTML we render. Taking a look at your posts, this might be from the post signature? So...

[quote="justinf, post:40, topic:1271"]
2. The Post Signature field is included on every post.
[/quote]

I'll change this behavior. Agreed that it probably doesn't make sense to include in the ebook. Hopefully that'll also fix issue #1.

-------------------------

justinf | 2022-02-28 02:22:21 UTC | #42

The error is a result of the images at the top of every blog post I assume. Still exists - thought snap.as images would be supported.

-------------------------

DavidBlue | 2022-03-04 17:35:57 UTC | #43

This would make sense because I’ve started to use GitHub as an image host on the blog that’s not working to reduce my load on Snap.as. (A nono, I know, but it’s just so tempting lol.)

-------------------------

socialvida | 2022-03-05 23:59:19 UTC | #44

Sorry it´s compatible this format with Amazon E-reades with .mobi extension?

-------------------------

matt | 2022-03-07 16:33:38 UTC | #45

[quote="justinf, post:42, topic:1271, full:true"]
The error is a result of the images at the top of every blog post I assume. Still exists - thought snap.as images would be supported.
[/quote]

I think it's actually from the signature HTML, based on this message:

```text
Opening and ending tag mismatch: hr line 0
```

It's saying there's an opening `<hr>` tag without a closing `</hr>` tag to match it. Snap.as images should work just fine in the ebooks! Assuming you're using Markdown to include them, or valid XHTML `<img />` tags.

-------------------------

matt | 2022-03-07 16:35:04 UTC | #46

Right now, we only export .epub files. We might support the .mobi format in the future though.

-------------------------

socialvida | 2022-03-07 16:50:50 UTC | #47

ahhh ok!
thanks!

-------------------------

jamiecropley | 2022-04-29 14:53:51 UTC | #48

I asked this here before realising this entire topic existed, apologies: https://discuss.write.as/t/is-there-a-way-to-disable-ebooks-for-a-specific-blog-but-have-it-enabled-on-another/5365

-------------------------

Kroeber | 2022-05-13 22:06:30 UTC | #49

Hi, was this feature disabled?
I cannot get it to work.

Not with by blog: https://write.as/kroeber/.epub
Not with the example provided: https://write.as/blog/.epub

It stopped working at least months ago.

-------------------------

PaoloAmoroso | 2022-06-26 12:27:13 UTC | #50

@Kroeber I can download the ebook from [my blog](https://journal.paoloamoroso.com) but the generated ePub file doesn't validate and Google Play Books rejects it with an error. For example, the Draft2Digital ePub validator returns a thick wall of errors:

```
ERROR(RSC-005): .tmp.tmpfjo5g478.epub/EPUB.package.opf(8,24): Error while parsing file: character content of element "dc:date" invalid; must be a string with length at least 1 (actual length was 0)

ERROR(CSS-001): .tmp.tmpfjo5g478.epub/EPUB.css.epub.css(1,405): The 'unicode-bidi' property must not be included in an EPUB Style Sheet.

ERROR(RSC-005): .tmp.tmpfjo5g478.epub/EPUB.xhtml.section0024.xhtml(38,20): Error while parsing file: attribute "align" not allowed here; expected attribute "about", "accesskey", "aria-activedescendant", "aria-atomic", "aria-autocomplete", "aria-busy", "aria-checked", "aria-colcount", "aria-colindex", "aria-colspan", "aria-controls", "aria-current", "aria-describedby", "aria-details", "aria-disabled", "aria-dropeffect", "aria-errormessage", "aria-expanded", "aria-flowto", "aria-grabbed", "aria-haspopup", "aria-hidden", "aria-invalid", "aria-keyshortcuts", "aria-label", "aria-labelledby", "aria-level", "aria-live", "aria-modal", "aria-multiline", "aria-multiselectable", "aria-orientation", "aria-owns", "aria-placeholder", "aria-posinset", "aria-pressed", "aria-readonly", "aria-relevant", "aria-required", "aria-roledescription", "aria-rowcount", "aria-rowindex", "aria-rowspan", "aria-selected", "aria-setsize", "aria-sort", "aria-valuemax", "aria-valuemin", "aria-valuenow", "aria-valuetext", "autocapitalize", "class", "colspan", "content", "contenteditable", "datatype", "dir", "draggable", "headers", "hidden", "id", "inlist", "is", "itemid", "itemprop", "itemref", "itemscope", "itemtype", "lang", "ns1:type", "ns2:alphabet", "ns2:ph", "onabort", "onautocomplete", "onautocompleteerror", "onblur", "oncancel", "oncanplay", "oncanplaythrough", "onchange", "onclick", "onclose", "oncontextmenu", "oncuechange", "ondblclick", "ondrag", "ondragend", "ondragenter", "ondragexit", "ondragleave", "ondragover", "ondragstart", "ondrop", "ondurationchange", "onemptied", "onended", "onerror", "onfocus", "onfocusin", "onfocusout", "oninput", "oninvalid", "onkeydown", "onkeypress", "onkeyup", "onload", "onloadeddata", "onloadedmetadata", "onloadstart", "onmousedown", "onmouseenter", "onmouseleave", "onmousemove", "onmouseout", "onmouseover", "onmouseup", "onpause", "onplay", "onplaying", "onprogress", "onratechange", "onreset", "onresize", "onscroll", "onseeked", "onseeking", "onselect", "onsort", "onstalled", "onsubmit", "onsuspend", "ontimeupdate", "ontoggle", "onvolumechange", "onwaiting", "onwheel", "prefix", "property", "rel", "resource", "rev", "role", "rowspan", "scope", "slot", "spellcheck", "style", "tabindex", "title", "translate", "typeof", "vocab", "xml:base", "xml:lang" or "xml:space" (with xmlns:ns1="http://www.idpf.org/2007/ops" xmlns:ns2="http://www.w3.org/2001/10/synthesis")

ERROR(RSC-005): .tmp.tmpfjo5g478.epub/EPUB.xhtml.section0024.xhtml(39,20): Error while parsing file: attribute "align" not allowed here; expected attribute "about", "accesskey", "aria-activedescendant", "aria-atomic", "aria-autocomplete", "aria-busy", "aria-checked", "aria-colcount", "aria-colindex", "aria-colspan", "aria-controls", "aria-current", "aria-describedby", "aria-details", "aria-disabled", "aria-dropeffect", "aria-errormessage", "aria-expanded", "aria-flowto", "aria-grabbed", "aria-haspopup", "aria-hidden", "aria-invalid", "aria-keyshortcuts", "aria-label", "aria-labelledby", "aria-level", "aria-live", "aria-modal", "aria-multiline", "aria-multiselectable", "aria-orientation", "aria-owns", "aria-placeholder", "aria-posinset", "aria-pressed", "aria-readonly", "aria-relevant", "aria-required", "aria-roledescription", "aria-rowcount", "aria-rowindex", "aria-rowspan", "aria-selected", "aria-setsize", "aria-sort", "aria-valuemax", "aria-valuemin", "aria-valuenow", "aria-valuetext", "autocapitalize", "class", "colspan", "content", "contenteditable", "datatype", "dir", "draggable", "headers", "hidden", "id", "inlist", "is", "itemid", "itemprop", "itemref", "itemscope", "itemtype", "lang", "ns1:type", "ns2:alphabet", "ns2:ph", "onabort", "onautocomplete", "onautocompleteerror", "onblur", "oncancel", "oncanplay", "oncanplaythrough", "onchange", "onclick", "onclose", "oncontextmenu", "oncuechange", "ondblclick", "ondrag", "ondragend", "ondragenter", "ondragexit", "ondragleave", "ondragover", "ondragstart", "ondrop", "ondurationchange", "onemptied", "onended", "onerror", "onfocus", "onfocusin", "onfocusout", "oninput", "oninvalid", "onkeydown", "onkeypress", "onkeyup", "onload", "onloadeddata", "onloadedmetadata", "onloadstart", "onmousedown", "onmouseenter", "onmouseleave", "onmousemove", "onmouseout", "onmouseover", "onmouseup", "onpause", "onplay", "onplaying", "onprogress", "onratechange", "onreset", "onresize", "onscroll", "onseeked", "onseeking", "onselect", "onsort", "onstalled", "onsubmit", "onsuspend", "ontimeupdate", "ontoggle", "onvolumechange", "onwaiting", "onwheel", "prefix", "property", "rel", "resource", "rev", "role", "rowspan", "scope", "slot", "spellcheck", "style", "tabindex", "title", "translate", "typeof", "vocab", "xml:base", "xml:lang" or "xml:space" (with xmlns:ns1="http://www.idpf.org/2007/ops" xmlns:ns2="http://www.w3.org/2001/10/synthesis")

ERROR(RSC-005): .tmp.tmpfjo5g478.epub/EPUB.xhtml.section0024.xhtml(45,20): Error while parsing file: attribute "align" not allowed here; expected attribute "about", "accesskey", "aria-activedescendant", "aria-atomic", "aria-autocomplete", "aria-busy", "aria-checked", "aria-colcount", "aria-colindex", "aria-colspan", "aria-controls", "aria-current", "aria-describedby", "aria-details", "aria-disabled", "aria-dropeffect", "aria-errormessage", "aria-expanded", "aria-flowto", "aria-grabbed", "aria-haspopup", "aria-hidden", "aria-invalid", "aria-keyshortcuts", "aria-label", "aria-labelledby", "aria-level", "aria-live", "aria-modal", "aria-multiline", "aria-multiselectable", "aria-orientation", "aria-owns", "aria-placeholder", "aria-posinset", "aria-pressed", "aria-readonly", "aria-relevant", "aria-required", "aria-roledescription", "aria-rowcount", "aria-rowindex", "aria-rowspan", "aria-selected", "aria-setsize", "aria-sort", "aria-valuemax", "aria-valuemin", "aria-valuenow", "aria-valuetext", "autocapitalize", "class", "colspan", "content", "contenteditable", "datatype", "dir", "draggable", "headers", "hidden", "id", "inlist", "is", "itemid", "itemprop", "itemref", "itemscope", "itemtype", "lang", "ns1:type", "ns2:alphabet", "ns2:ph", "onabort", "onautocomplete", "onautocompleteerror", "onblur", "oncancel", "oncanplay", "oncanplaythrough", "onchange", "onclick", "onclose", "oncontextmenu", "oncuechange", "ondblclick", "ondrag", "ondragend", "ondragenter", "ondragexit", "ondragleave", "ondragover", "ondragstart", "ondrop", "ondurationchange", "onemptied", "onended", "onerror", "onfocus", "onfocusin", "onfocusout", "oninput", "oninvalid", "onkeydown", "onkeypress", "onkeyup", "onload", "onloadeddata", "onloadedmetadata", "onloadstart", "onmousedown", "onmouseenter", "onmouseleave", "onmousemove", "onmouseout", "onmouseover", "onmouseup", "onpause", "onplay", "onplaying", "onprogress", "onratechange", "onreset", "onresize", "onscroll", "onseeked", "onseeking", "onselect", "onsort", "onstalled", "onsubmit", "onsuspend", "ontimeupdate", "ontoggle", "onvolumechange", "onwaiting", "onwheel", "prefix", "property", "rel", "resource", "rev", "role", "rowspan", "slot", "spellcheck", "style", "tabindex", "title", "translate", "typeof", "vocab", "xml:base", "xml:lang" or "xml:space" (with xmlns:ns1="http://www.idpf.org/2007/ops" xmlns:ns2="http://www.w3.org/2001/10/synthesis")

ERROR(RSC-005): .tmp.tmpfjo5g478.epub/EPUB.xhtml.section0024.xhtml(46,20): Error while parsing file: attribute "align" not allowed here; expected attribute "about", "accesskey", "aria-activedescendant", "aria-atomic", "aria-autocomplete", "aria-busy", "aria-checked", "aria-colcount", "aria-colindex", "aria-colspan", "aria-controls", "aria-current", "aria-describedby", "aria-details", "aria-disabled", "aria-dropeffect", "aria-errormessage", "aria-expanded", "aria-flowto", "aria-grabbed", "aria-haspopup", "aria-hidden", "aria-invalid", "aria-keyshortcuts", "aria-label", "aria-labelledby", "aria-level", "aria-live", "aria-modal", "aria-multiline", "aria-multiselectable", "aria-orientation", "aria-owns", "aria-placeholder", "aria-posinset", "aria-pressed", "aria-readonly", "aria-relevant", "aria-required", "aria-roledescription", "aria-rowcount", "aria-rowindex", "aria-rowspan", "aria-selected", "aria-setsize", "aria-sort", "aria-valuemax", "aria-valuemin", "aria-valuenow", "aria-valuetext", "autocapitalize", "class", "colspan", "content", "contenteditable", "datatype", "dir", "draggable", "headers", "hidden", "id", "inlist", "is", "itemid", "itemprop", "itemref", "itemscope", "itemtype", "lang", "ns1:type", "ns2:alphabet", "ns2:ph", "onabort", "onautocomplete", "onautocompleteerror", "onblur", "oncancel", "oncanplay", "oncanplaythrough", "onchange", "onclick", "onclose", "oncontextmenu", "oncuechange", "ondblclick", "ondrag", "ondragend", "ondragenter", "ondragexit", "ondragleave", "ondragover", "ondragstart", "ondrop", "ondurationchange", "onemptied", "onended", "onerror", "onfocus", "onfocusin", "onfocusout", "oninput", "oninvalid", "onkeydown", "onkeypress", "onkeyup", "onload", "onloadeddata", "onloadedmetadata", "onloadstart", "onmousedown", "onmouseenter", "onmouseleave", "onmousemove", "onmouseout", "onmouseover", "onmouseup", "onpause", "onplay", "onplaying", "onprogress", "onratechange", "onreset", "onresize", "onscroll", "onseeked", "onseeking", "onselect", "onsort", "onstalled", "onsubmit", "onsuspend", "ontimeupdate", "ontoggle", "onvolumechange", "onwaiting", "onwheel", "prefix", "property", "rel", "resource", "rev", "role", "rowspan", "slot", "spellcheck", "style", "tabindex", "title", "translate", "typeof", "vocab", "xml:base", "xml:lang" or "xml:space" (with xmlns:ns1="http://www.idpf.org/2007/ops" xmlns:ns2="http://www.w3.org/2001/10/synthesis")

ERROR(RSC-005): .tmp.tmpfjo5g478.epub/EPUB.xhtml.section0024.xhtml(50,20): Error while parsing file: attribute "align" not allowed here; expected attribute "about", "accesskey", "aria-activedescendant", "aria-atomic", "aria-autocomplete", "aria-busy", "aria-checked", "aria-colcount", "aria-colindex", "aria-colspan", "aria-controls", "aria-current", "aria-describedby", "aria-details", "aria-disabled", "aria-dropeffect", "aria-errormessage", "aria-expanded", "aria-flowto", "aria-grabbed", "aria-haspopup", "aria-hidden", "aria-invalid", "aria-keyshortcuts", "aria-label", "aria-labelledby", "aria-level", "aria-live", "aria-modal", "aria-multiline", "aria-multiselectable", "aria-orientation", "aria-owns", "aria-placeholder", "aria-posinset", "aria-pressed", "aria-readonly", "aria-relevant", "aria-required", "aria-roledescription", "aria-rowcount", "aria-rowindex", "aria-rowspan", "aria-selected", "aria-setsize", "aria-sort", "aria-valuemax", "aria-valuemin", "aria-valuenow", "aria-valuetext", "autocapitalize", "class", "colspan", "content", "contenteditable", "datatype", "dir", "draggable", "headers", "hidden", "id", "inlist", "is", "itemid", "itemprop", "itemref", "itemscope", "itemtype", "lang", "ns1:type", "ns2:alphabet", "ns2:ph", "onabort", "onautocomplete", "onautocompleteerror", "onblur", "oncancel", "oncanplay", "oncanplaythrough", "onchange", "onclick", "onclose", "oncontextmenu", "oncuechange", "ondblclick", "ondrag", "ondragend", "ondragenter", "ondragexit", "ondragleave", "ondragover", "ondragstart", "ondrop", "ondurationchange", "onemptied", "onended", "onerror", "onfocus", "onfocusin", "onfocusout", "oninput", "oninvalid", "onkeydown", "onkeypress", "onkeyup", "onload", "onloadeddata", "onloadedmetadata", "onloadstart", "onmousedown", "onmouseenter", "onmouseleave", "onmousemove", "onmouseout", "onmouseover", "onmouseup", "onpause", "onplay", "onplaying", "onprogress", "onratechange", "onreset", "onresize", "onscroll", "onseeked", "onseeking", "onselect", "onsort", "onstalled", "onsubmit", "onsuspend", "ontimeupdate", "ontoggle", "onvolumechange", "onwaiting", "onwheel", "prefix", "property", "rel", "resource", "rev", "role", "rowspan", "slot", "spellcheck", "style", "tabindex", "title", "translate", "typeof", "vocab", "xml:base", "xml:lang" or "xml:space" (with xmlns:ns1="http://www.idpf.org/2007/ops" xmlns:ns2="http://www.w3.org/2001/10/synthesis")

ERROR(RSC-005): .tmp.tmpfjo5g478.epub/EPUB.xhtml.section0024.xhtml(51,20): Error while parsing file: attribute "align" not allowed here; expected attribute "about", "accesskey", "aria-activedescendant", "aria-atomic", "aria-autocomplete", "aria-busy", "aria-checked", "aria-colcount", "aria-colindex", "aria-colspan", "aria-controls", "aria-current", "aria-describedby", "aria-details", "aria-disabled", "aria-dropeffect", "aria-errormessage", "aria-expanded", "aria-flowto", "aria-grabbed", "aria-haspopup", "aria-hidden", "aria-invalid", "aria-keyshortcuts", "aria-label", "aria-labelledby", "aria-level", "aria-live", "aria-modal", "aria-multiline", "aria-multiselectable", "aria-orientation", "aria-owns", "aria-placeholder", "aria-posinset", "aria-pressed", "aria-readonly", "aria-relevant", "aria-required", "aria-roledescription", "aria-rowcount", "aria-rowindex", "aria-rowspan", "aria-selected", "aria-setsize", "aria-sort", "aria-valuemax", "aria-valuemin", "aria-valuenow", "aria-valuetext", "autocapitalize", "class", "colspan", "content", "contenteditable", "datatype", "dir", "draggable", "headers", "hidden", "id", "inlist", "is", "itemid", "itemprop", "itemref", "itemscope", "itemtype", "lang", "ns1:type", "ns2:alphabet", "ns2:ph", "onabort", "onautocomplete", "onautocompleteerror", "onblur", "oncancel", "oncanplay", "oncanplaythrough", "onchange", "onclick", "onclose", "oncontextmenu", "oncuechange", "ondblclick", "ondrag", "ondragend", "ondragenter", "ondragexit", "ondragleave", "ondragover", "ondragstart", "ondrop", "ondurationchange", "onemptied", "onended", "onerror", "onfocus", "onfocusin", "onfocusout", "oninput", "oninvalid", "onkeydown", "onkeypress", "onkeyup", "onload", "onloadeddata", "onloadedmetadata", "onloadstart", "onmousedown", "onmouseenter", "onmouseleave", "onmousemove", "onmouseout", "onmouseover", "onmouseup", "onpause", "onplay", "onplaying", "onprogress", "onratechange", "onreset", "onresize", "onscroll", "onseeked", "onseeking", "onselect", "onsort", "onstalled", "onsubmit", "onsuspend", "ontimeupdate", "ontoggle", "onvolumechange", "onwaiting", "onwheel", "prefix", "property", "rel", "resource", "rev", "role", "rowspan", "slot", "spellcheck", "style", "tabindex", "title", "translate", "typeof", "vocab", "xml:base", "xml:lang" or "xml:space" (with xmlns:ns1="http://www.idpf.org/2007/ops" xmlns:ns2="http://www.w3.org/2001/10/synthesis")
[...]
```

-------------------------

Kroeber | 2022-06-26 13:11:52 UTC | #51

Hi @ [PaoloAmoroso](https://discuss.write.as/u/PaoloAmoroso)

I can open your downloaded epub file with no issues with Calibre. 
Maybe in Calibre you can then format it in a way Google Books can accept it.

The problem I am facing with [my blog](https://write.as/kroeber/.epub), is that the feature simply does not work. All I see is this:

![image|690x184](upload://eSfPxsIX7XvyDy3LUnqVNJf0YVx.png)

-------------------------

PaoloAmoroso | 2022-06-26 14:14:16 UTC | #52

@Kroeber Thanks for the feedback. I'd prefer downloaded ePub files to validate and open in at least a few major ereading apps and platforms rather than having to edit the files. I confirm the issues with your blog.

-------------------------

PaoloAmoroso | 2022-06-26 14:28:52 UTC | #53

I was able to open my blog's ePub file with [BookFusion](https://bookfusion.com).

The ePub generation feature works remarkably well. Aside from MathJax and the broken rendering of part of a post, all formatting is preserved. I second the feedback of others in this thread about book organization and metadata.

-------------------------

Kroeber | 2022-06-26 21:10:17 UTC | #54

This is disappointing for me. I have subscribed to this feature for years. It stopped working several months ago. And I cannot get support for it. I don't know what to do.

-------------------------

matt | 2022-06-27 16:09:48 UTC | #55

@Kroeber I'm going to look into the issues you're having today. Sorry it's taken so long for me to get to it.

@PaoloAmoroso Besides the first two errors, I'm assuming the other ones are from some custom HTML inserted into one of your posts. The epub format is a little picky, and we simply output whatever custom HTML you might've inserted, so that could be the cause here.

-------------------------

PaoloAmoroso | 2022-06-27 17:19:43 UTC | #56

@matt I actually don't remember having ever inserted any HTML in my posts, only Markdown. But my blog does have custom CSS:

```css
article pre code {
    white-space: pre !important;
}
article pre {
    overflow-x: scroll;
}

body footer nav {display:none}
```

-------------------------

matt | 2022-06-27 18:11:50 UTC | #57

When you open up the ebook, what post shows up as chapter 24? Based on this error: 

```text
[...] section0024.xhtml(38,20): Error while parsing file: attribute "align" not allowed here [...]
```

It seems there might be an element or two with an `align` attribute in that one post (all errors are from `section0024.xhtml`).

-------------------------

PaoloAmoroso | 2022-06-27 19:09:23 UTC | #58

The 24-th TOC entry is [this post](https://journal.paoloamoroso.com/collecting-and-reading-vintage-computer-manuals-and-books), which has pretty plain formatting. The previous one is [this](https://journal.paoloamoroso.com/test-driving-write-as-on-a-tablet) and the following one [this](https://journal.paoloamoroso.com/putting-twitter-aside-and-focusing-on-blogging). The source of all these posts includes only Markdown.

-------------------------

Kroeber | 2022-06-27 21:37:15 UTC | #59

Thanks matt.

-------------------------

playgroundtourist | 2022-07-09 07:04:04 UTC | #60

I would love to see this feature, as I just had the plan to write a book for myself. When I click on the demo link I only get a literally unhelpful http 500 message. I'd donate if I could see that at least the demo works.

-------------------------

jamiecropley | 2022-07-30 23:23:29 UTC | #61

If you really need an ebook format urgently this might be helpful: https://pandoc.org/

-------------------------

