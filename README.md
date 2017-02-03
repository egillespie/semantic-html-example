## What are Semantics?

In the early days of the web, things looked pretty... boring.

![Boring old website](https://i.imgur.com/noYC03g.jpg)

Images, an `h1` here or there, walls of text, probably a table, and lots and lots of links. Now imagine if every website were created using only the elements you've learned up until now.

TERRIFYING.

We've come a long way since then: pages are colorful, interactive, and full of information you want to share. Not only that, but it's actually _easier_ to find and share information now than it was twenty years ago.

We might thank search engines and social media for that. They certainly helped a lot, but they didn't do it alone. The web itself changed. *Semantic elements* were added to HTML to make it easier for computers to understand all of the webpages that us humans create.

### Syntax vs semantics

When you write HTML, there is a specific way you have to type tags so that your web browser can show a page properly:

``` {.html}
<a href="/">Stupendous Content</a>
```

You learned about syntax highlighting in a previous lesson. All of those colorful letters and special characters make up the *syntax* of HTML, but what those elements say about their content is *semantics*.

This is true in spoken languages, too. Syntax is _how_ you say something. Semantics is the _meaning_ of what you say.

Consider this example:

``` {.txt}
I love cats
👁️ ❤️️ 🐈
```

Both lines mean the same thing, but how we stated it is different. The syntax changed, but the semantics did not.

It works the other way around, too:

``` {.txt}
Aren't you happy!
Aren't you happy?
```

By simply replacing the exclamation with a question mark, the meaning of the sentence changed from excitement to one of concern.

In written or typed languages, we can use punctuation, *bold letters*, _italics_, ALL CAPS, and other text decorations to change the meaning of what we say. When we're talking, we use the inflection of our voice and body language.

Semantics are important for us to understand each other properly. If we say the right words in the wrong way, it can be confusing, get us in trouble, or make us seem creepy.

![Romantic vs creepy message](https://i.imgur.com/i79Ho0o.jpg)

## Organizing your content

Semantics are important on the web, too. Organizing content and presenting it properly on a webpage makes it easy to understand and skim, which makes you more likely to read it.

Take blog articles for example. You can recognize one the moment the page appears and most of them are organized in the same way.

![Blog example](https://i.imgur.com/vl9qJfx.jpg)

Without much thought, you know what the title of an article is, who wrote it, how to navigate between pages, and where the article begins and ends.

~~~ {.note}
### Semantics: not just for people

Do you know who else cares about how your content is organized? Search engines! In fact, take a look at Google's mission:

<blockquote>
To organize the world’s information and make it universally accessible and useful.
</blockquote>

Search engines, social media, screen readers, blog rollers, product comparison tools, and all sorts of other software are looking at the content you put on the web everyday.

It's becoming increasingly important to give your HTML proper semantic meaning. Take it from the inventor of the World Wide Web:

![](http://i.imgur.com/SS3Pi0v.jpg)

We'll explain how as we explore semantic HTML in 3... 2... 1...
~~~

### Semantic HTML Elements

Let's take a closer look at the semantic elements used in the example above. There are nine of them:

* `main`
* `article`
* `header`
* `section`
* `figure`
* `figcaption`
* `aside`
* `footer`
* `nav`

One of the nice things about semantic HTML elements is that their names pretty much describe what they do and even give you a clue about where they go.

Try it out. Which elements do you think were used for the different parts of Ralph's blog post?

### `main`

The `main` element literally means _the main content_ of the page. There should only be one of them inside your `body` element.

If the purpose of your page is to list links and short content for a bunch of blog posts, it should all go inside a `main` element. If your page is a single blog post, the whole post -- title and all -- should go inside `main`.

But doesn't that mean `main` is basically the same thing as `body`? Nope!

There are things that shouldn't go in your `main` element: logos, copyright information, your site's navigation, sidebars, and anything else that will exist on every page of your website.

~~~ {.note}
Search engines create relationships between different content on your site to help people find relevant information.

If you have an "About Me" link on every page, don't put it in `main`. If you make Google think there's a strong relationship to your "About Me" page, it could start appearing higher in search results than more important content you care about! 😱
~~~

## The anatomy of an article

On the web, an article is any content that can be read, start to finish, entirely independent of any other content. These include:

* tutorials
* blog posts
* short stories
* product reviews
* news... articles 😉

Articles typically have a title followed by one or more blocks of related content (sometimes broken up into chunks or lists to make the article easier to read) and extra information about the piece such as the author and date.

Look at [any](https://medium.com/@zackkelly/5-life-changing-things-i-learned-from-doing-improv-e398342238e7#.nf9n9sn04) [random](https://artplusmarketing.com/12-haikus-26d0acd8fcb4#.3r1z8bw6o) [article](https://medium.com/@sheamatthewfisher/macbeth-in-klingon-35e88cf50479#.o49f5mxo6) on Medium and you'll see that same basic structure.

### `article`

The `article` element wraps all of the content, title and all. The idea behind an `article` is that you can take everything inside it, give it to someone else, and they'll still be able to understand it.

Putting a whole blog post inside an `article` makes sense, but if you only put an excerpt or the first paragraph of a post in an article, the reader wouldn't be able to make sense of it without more information.

You can also have as many `article` elements on a page as you want.

~~~ {.note}
Much like search engines downplay relationships between your `main` content and everything else, the content in two `article` elements on the same page are not considered strongly related.
~~~

### `header`

If your content has a title, author, date, feature image, or anything else that you want to include at the beginning of your content, `header` is the place to do it.

``` {.html}
<header class="page-header">
  <h1>Rambling Ralph</h1>
  <div class="author">By Ralph Wiggum</div>
  <div class="post-date">January 1, 1998</div>
</header>
```
~~~ {.result}
![](http://i.imgur.com/rj6cTpg.jpg)
~~~

Typically `header` will be one of the first elements inside your `article`, but `header` elements aren't just used for articles. You can use `header` elements in your `body`, `main`, or anywhere else that you may want to put a title or introductory content.

### `section`

A section is a portion of your content that may have a theme or topic of its own, but doesn't provide all of the details or lacks some context to be shared on its own. Like a chapter in a book or Ralph's ode to Lisa.

``` {.html}
<section>
  <h2>Lisa</h2>
  <p>There's the key!  Dear wife, if I could take but one treasure with me to the next life, it would be your tender kiss.  I'm Idaho!  I won! I won!  I ated the purple berries... oooh, oohh</p>
</section>
```
~~~ {.result}
![Ralph's ode to lisa](https://i.imgur.com/lauteEA.jpg)
~~~

The `section` element is fairly generic. You don't have to put them inside `article` elements, they can go anywhere inside the `body` that makes sense to you. You can also have more than one of them inside an `article` to break up your content.

A good rule here is to avoid using a `section` when something more specific will work.

### `footer`

The `footer` element is similar to `header`: it can be used in an `article` or outside of one and is used to hold any information that you would like readers to see at the end of your content.

``` {.html}
<footer>
  <nav>
    <input type="button" class="prev">Prev Post</button>
    <input type="button" class="next">Next Post</button>
  </nav>
</footer>
```
~~~ {.result}
![Footer navigation](https://i.imgur.com/5sFI0X3.jpg)
~~~

This might include related articles, some info about the author, copyright information, or navigation buttons.

## Navigation and content that _pops_

So far we've covered a lot of semantic tags that are great for organizing your content, and while organized walls of text are all well and good, we want more!

![Two versions of the Mona Lisa](https://i.imgur.com/U6OJh0r.png)

We want beautiful content. And we want to know how to find more of it!

### `figure` and `figcaption`

Magazines, newspapers, books, the web... they're full of figures and captions. Pictures, code snippets, and graphs are all fairly common types of figures that you'll see while reading and the caption is usually a brief description or photo credit.

The thing about figures is that they're supposed to add a little flavor to the surrounding content, but readers should still be able to get by without them. This isn't a strict rule, but it's a good one to follow when you can.

``` {.html}
<figure class="thumbnail">
  <img src="ralph.jpg">
  <figcaption>Why do people run from me?</figcaption>
</figure>
```
~~~ {.result}
![Figure of ralph](https://i.imgur.com/1NGEMQl.jpg)
~~~

The `figure` element can be sprinkled into your content wherever you find appropriate. `figcaption`, on the other hand, should always be the first or last element inside of a `figure`.

Anything else that goes inside a `figure` is up to you! In a previous lesson you learned how to add tables, video, audio, and embedded content from places like YouTube. They're all good fits.

And, of course, images. 😛

~~~ {.note}
### Style your semantic HTML

`figure` is the only semantic HTML element in this lesson that has any styles applied to it by default (there is a small margin around it that makes it look indented).

Semantic HTML is all about _meaning_, not appearance. Elements like `figure`, `header`, and `footer` tell someone to think about your content differently, but if you want them to _look_ different, you will have to add your own styles!
~~~

### `aside`

An aside is usually a piece of information related to the content around it. It can be a quote that you want to highlight, some words of caution about a topic, or even a deeper dive into a subject.

``` {.html}
<aside>
  <blockquote>The rat symbolizes obviousness!</blockquote>
</aside>
```
~~~ {.result}
![Aside element example](https://i.imgur.com/mYy8aEa.jpg)
~~~

Asides are usually brief, but they don't have to be! You can put a whole mini-article inside of one if you want. That means inside an `aside` element, you can use all sorts of other elements like `h2`, `p`, and `blockquote`.

Like figures, asides should not be required reading for your content, but they should stand out and help break up and improve its overall quality of your content.

### `nav`

It's pretty rare to find a page on the web that doesn't have a navigation bar _somewhere_ on the page. Usually it's hanging out at the very top, in a sidebar, or in a menu somewhere.

Wherever you want to place a set of links on your site to make navigation easier, use a `nav` element to group them all together.

Besides providing an easy way for readers to move from page to page on your site, the location of a `nav` element on a page can also help people understand where links will take them.

``` {.html}
<nav>
  <input type="button" class="prev">Prev Post</button>
  <input type="button" class="next">Next Post</button>
</nav>
```
~~~ {.result}
![Nav element example](https://i.imgur.com/5sFI0X3.jpg)
~~~

For example, putting the same `nav` element at the top of every page helps readers find the most important pages on your site, like "Home" or "About" pages. If you put a `nav` element in the `header` or `footer` of an article, the links are usually to more articles.

~~~ {.note}
Search engines LOOOOOVE links. Links inside a `nav` that is also inside an `article` will get preferred treatment from Google and the likes than any other URLs found on the page.

That's one reason why many blogs have a group of "Related Posts" beside or below an article.
~~~

## The real power of the semantic web

Sure, all of these semantic HTML elements give _meaning_ to the different parts of your webpage, but why does that matter? I mean, couldn't we just put everything in `div` tags and call it a day?

Technically, you _could_, but wow, you would be missing out on some cool benefits and maybe even losing money or traffic!

![Reference to 2001: A Space Odyssey](https://i.imgur.com/gRIXjm3.jpg)

The real power of the semantic web is it helps _computers_ understand your content.

### Search Engine Optimization

Search engines like Google are forever scouring the web for new information that help people find what they're looking for.

If you make a website, you can tune your content so that it appears higher up in search results. That process is called Search Engine Optimization, or *SEO*. Using semantic HTML elements is only one of many types of SEO, but it's one that you have complete control over.

Let's say you have a personal blog. If you use semantic HTML, Google can easily tell that your "2½-Minute Taco Lasagna" recipe has very little to do with your post about software architecture.

Both articles appear on your homepage and they even share some of the same keywords.

![The evolution of software architecture](https://i.imgur.com/VAZ0ODp.png)

If you didn't use semantic HTML, Google would have to guess about what information on the page is related to everything else. And if Google can't understand your site, what are the chances you'll show up at the top of someone's search for "lasagna code?"

Fortunately, you separated your content into different `article` elements, embedded links to related articles using `nav`, and put images in `figure` elements with relevant captions. Google can easily use the context of a search and the semantics of your articles to give someone exactly the links they went looking for.

The payoff: you finally out-rank that spaghetti taco recipe because you used semantic HTML!

![Spaghetti tacos](https://i.imgur.com/exOkcS7.jpg)

Bon appétit! 🍝
