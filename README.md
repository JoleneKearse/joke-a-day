# Joke a Day

I finally tried out **HTMX**! This is a simple app using making calls to the **Joke API** right in the **HTML**! I followed this [tutorial](https://www.sitepoint.com/htmx-introduction/) on SitePoint. And it goes on, but I decided to make my button into an *apple* to carry on the theme.

![Screenshot showing: Joke a Day, a button in the shape of an apple saying cure me and the introduction.](/screenshots/screenshot.png)

HTMX was very simple to get started. You can install it or use the CDN:
```html
<script src="https://unpkg.com/htmx.org@1.9.4"></script>
```

The API call was dead simple to make just
```html
hx-get="https://v2.jokeapi.dev/joke/Any?format=txt&safe-mode&type=single"
```
within my button element.

Then 
```html
hx-target="#joke-container"
```
to send the response elsewhere (rather than replacing the button, as is the default behaviour).

My main challenge was making the apple shape, but this [YouTube video by Coder ACB](https://www.youtube.com/watch?v=oe4Wc1fH1AY&t=65s) was awesome!

And no effort at all was spent on **accessibility**, but I managed to clear the boards in my Lighthouse testing.

![100 scores in every category](/screenshots/lighthouse.png)