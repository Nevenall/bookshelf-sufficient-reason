# Design Notes

## Page Order

There is currently no way to order pages. They'll be sorted according to whatever the filesystem decides. 
So, it may behoove us to include some configuration of page order. Perhaps a simple json file that is essentially a manifest.
It describes the pages and organization of the book. And we can read our nav from that.

### What if it's out of sync?

the proverbial question. What if it is? we can show blank pages if there's no content yet.
If something is on the file system, but doesn't appear in the json, we can ignore it. 

## Single .md Mode

It might also be interesting to be able to navigate a single markdown file. Where each top level header becomes a folder node. Though that would be a different structure. Because a top level node can be a page. More like *blades in the dark* where each top level header becomes it's own page. 

We can either programmatically break up the file into chunks. That may make the most sense. Or try to inject some kind of nav links into the headers. 
acutally, a file splitting pre-processor probably makes the most sense. It's a side task to make `BookShelf` compatible chunks. 

## Typography - Specific to SR

Fonts, I don't like generate appear of Gentium book. 

What about Cormorant Garamond with the current headers? It's really light but might work with the headers? (Actually, its pretty nice. I like it.) 
Worth a try, but I think Libre Baskerville might be better overall for book text. I wish it had a bold italics style though. 

Man, I really need a typeface with a small caps style too. I might have to fake the small caps, which is not ideal, but...

Algerian might be an interesting font for headers. 

Ibm plex serif is quite good for body text. 



### Paragraphs

in general the paragraphs in sr are short. And very often just one sentence, rather then running text, which means that indented paragraphs look a little odd. there is a bit of running text, but not all that much., 

### typography frame

I'm tempted to replace the typography frame so we can separate the generic default typographic styles from the per-book customizations based on #page. 

Also, should put the typographic styles in a separate file. 

