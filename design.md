# BookShelf Design Document

Vue 
Vue cli 
Webpack 4
Vuetify


## Touch enabled page turning

Vuetify supports touch events. 


## Niggling bits

The vuetify framework seems to be reflowing the text when the drawer is closed. Hopefully once we start filling out the css that will go away.

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

