# Read-03 >> Structure web pages with HTML

## Chapter 17 - HTML5 Layout Hints:
- Traditional HTML Layout is a bunch of div tags that have attributes indicates the roll of each div tag.
- New HTML 5 layout create elements that indicate the type of the content inside it.
- `<header>` tag usully contain the title and `<footer>` contain links and copyrights info.
- `<nav>` tag used to contain navigational links.
- `<article>` tag used to contain a section of the page.
- `<aside>` tag contain general inforamtio about the page or the section, usually links or glossary.
- `<section>` tag used to split up the article or the page to differenct topics.
- `<hgroup>` tag used to group the heading tags (h1-h6) so they can be treated as one heading.
- `<figure>` and `<figcaption>` tags used to contain the media contents (images, videos, graphs).
- `<div>` tag can be used instead of all the above and add a class name to it according to the content type.


## Chapter 8 - Extra Markup Hints:
- There is three versions of HTML:
  - HTML 4 Released 1997.
  - XHTML 1.0 Released 2000.
  - HTML5 Released 2000.
- each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using.
  > " it should be the first thing in a document.There must be nothing before it, not even a space."  
- Add comments to your source code is good if you want to update certin things in the future, and it's not visible to the user in the browser. ex: `<!-- this is comment -->`.  
- Giving an element a unique identity (id attribute) allows you to style it differently than any other instance of the same element on the page. ex: `<p id="p1">`.
- Class attribute let you identify several elements as being different from the other elements on the page. ex: `<p class="important">`.
- Examples of block elements are `<h1>, <p>, <ul>, <li>`.
- Examples of inline elements are `<a>, <b>, <em>, <img>`.
- `<iframe>` tag used to show another page like (video, google maps..etc).
- `<meta>` tag used in the `<head>` only, and it contains information about your page.
- Escape characters can let you include symbols. ex: `&copy;` for copu rights symbol.


[Back to home page](../README.md)