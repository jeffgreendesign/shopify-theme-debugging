# shopify-theme-debugging

## General tips

- Include the relative URL of the file as a comment at the top of the file. Example: `<!-- /sections/product.liquid -->`. This can help you on the front-end determine what template file is generating what code.
- Use the [Shopify Cheat Sheet](https://www.shopify.com/partners/shopify-cheat-sheet) to quickly find documentation for Shopify tags, filter, and objects.

## Specific cases

### Objects

Use an inline style tag with the object in a `console.log()` or `console.dir()`:

```liquid
<script>
  console.dir({{ product | json }});
</script>
```

### Strings

Include the liquid tag in a wrapping element with a border to quickly debug a tag value: 

```liquid
<p style="border: 1px solid red;">{{ product.handle }}</p>
```
