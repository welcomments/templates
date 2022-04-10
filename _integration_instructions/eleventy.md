Add this to **.eleventy.js**:

```javascript
// ...
const { EleventyRenderPlugin } = require("@11ty/eleventy");

module.exports = function (eleventyConfig) {
  // ...

  // Add plugins
  // ...
  eleventyConfig.addPlugin(EleventyRenderPlugin);
  // ...

  // Welcomments configuration
  const absoluteUrl = "https://<YOUR WEBSITE HERE>";
  eleventyConfig.addFilter("absoluteUrl", (path) => `${absoluteUrl}${path}`);
  eleventyConfig.addFilter("objectValues", (object) => object ? Object.values(object) : []);
  eleventyConfig.addFilter("whereUnset", (array, key) => array.filter(item => !item[key] || item[key] === ""));
  eleventyConfig.addFilter("where", (array, key, value) => array.filter(item => item[key] === value));
  eleventyConfig.addFilter("interpolate", (a, b) => `${a}${b}`);
  eleventyConfig.addFilter("markdownify", (value) => markdownLibrary.render(value));
  eleventyConfig.addFilter("sortBy", (array, key) => array.slice().sort((a, b) => a[key] - b[key]));
};
```

It's important to replace `<YOUR WEBSITE HERE>` with the url of your production website, such as `https://example.com`.

Then, add the following snippet to your _post template file_.

```
{% set welcomments_config = {welcomments: welcomments, website_id: "YOUR-WEBSITE-ID-HERE"} %}
{% renderFile "./_includes/welcomments/comments.liquid", welcomments_config %}
```

The location of this file can differ based on the Eleventy starter you're using.

Here are some examples where this file could be:
* `_includes/layouts/post.njk`
* `_includes/post.liquid`