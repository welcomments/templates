The Hugo template is tested with Hugo 0.64.0.

**If you're using Netlify**, set HUGO_VERSION to 0.64.0 or higher in the environment variables section of your Netlify site.

Set the base url for your Hugo site in the config file:

**config.toml:**
```
baseURL = "https://mysite.com"
```

Add the following snippet to your "single post layout file".

The location of this file can differ based on the theme you're using.

Here are some examples where this file could be:
* `themes/<theme-name>/layouts/_default/single.html`
* `themes/<theme-name>/layouts/posts/single.html`
* `themes/<theme-name>/layouts/post.html`

```
{{ partial "welcomments/comments" (dict "context" . "websiteId" "<%= website_id %>" ) }}
```