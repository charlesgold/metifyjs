# _Metify_

_Javascript class which allows Shopify store owners and/or developers the ability to block out product.content / product.description content._

_Currently Shopify store owners have little freedom of how their product "description" is displayed._
_For example if a store owner wishes to display a piece of the {{ product.description }} in several places on the product page he/she cannot._ 
_With Metify you can create as many meta tags necessary to accommodate your particular design theme and layout_

## Setup

_I only used Javascript for this project, so no need to depend on JQuery or any other frameworks._ 
_As long as the end-user's browser supports DOM you are good to go!_

1. Add metify.js to the end of html `<body>` tag
2. Setup `{{ product.description }}` `<div>` holder in your product.liquid template.
3. Obviously using your theme of choice, feel free to place the "meta-value" tags which will accept the "meta-keys" values.
4. Define your meta tags inside of your Shopify store products.


## How-to use

Add metify.js to your document, just before `</body>`
```HTML
<script src="metify.js"></script>
<script>
 //Initialize metify.js class
 var myMetify	=	metify();
 
 /*
 * you could also pass in your own shopify product.description holder class.
 * example:
 * var myMetify	=	metify('raw-shopify');
 */
</script>
</body>
```

Example of `<div>` holder inside of product.liquid template.
```HTML
<div class="mf-product-raw" style="display:none;">
	{{ product.description }}
</div>
```

```HTML
<!-- html from selector with attribute data-mf-meta-key="my-product-custom" will be placed below -->
<div id="my-product-custom"></div>
```

To be placed inside of Shopify product description (example only)
```HTML
<div class="metify" data-mf-meta-key="my-product-custom">
	<p> some custom content here! </p>
</div>
```


## License
