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

<<<<<<< HEAD
## Typography - Specific to SR

Fonts, I don't like generate appear of Gentium book. 

What about Cormorant Garamond with the current headers? It's really light but might work with the headers? (Actually, its pretty nice. I like it.) 
Worth a try, but I think Libre Baskerville might be better overall for book text. I wish it had a bold italics style though. 

Man, I really need a typeface with a small caps style too. I might have to fake the small caps, which is not ideal, but...

Algerian might be an interesting font for headers. 

Ibm plex serif is quite good for body text. 
=======
### Book.json

or something like that. If there was a json doc for the booik. then we would have the pages all layed out. can link to the files and such. Not sure how that might interaactwith webpack. but it is an interesting thought. 

book: title
- Section : name, directory? 
  - Page : file
  - page : file

easy to make a nav from. 

if a page doesn't have a file, we can show empty, that's easy
if a file doesn't have a page we don't show it. 
does mean we have to layout the entire format of the book. 

Also makes it harder to have arbitrary levels of nav
the overall nature of the data is important. 

Basically just the book structure, serialized. 
Simple enough. Except, we have to fill in the content. 

##### Consider writing a custom loader for this nonsense

```json
{
  Title: "The Title of My Book",
  Pages: [],
  Sections: [ {
     Name: "The Name of my Section"
     Sections
   }
  ]
}
```

#### Interacting with webpack

It would be pretty easy to take the book.json and the paths and match them up by path with the content from webpack require. We can even include a json schema for the book.

##### I did kinda want to keep this from needing much config though.  

I don't think there is any other reliable way to get files in a particular order. So, book.json it is.




## Typography
>>>>>>> 0bf56c2d772cefcf5088537d3daf3b45906cefac

