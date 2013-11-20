# _Metify_

_Javascript class which allows Shopify store owners and/or developers the ability to block out product.content / product.description content._

_Currently Shopify store owners have little freedom of how their product "description" is displayed._
_For example if a store owner wishes to display a piece of the {{ product.description }} in several places on the product page he/she can not._ 
_With Metify you can create as many meta tags necessary to accomidate your paticular design theme and layout_

## Project Setup

_I only used Javascript for this project, so no need to depend on JQuery or any other frameworks._ 
_As long as the end-user's browser supports DOM you are good to go!_

1. _Add metify.js to the end of html `<body>` tag_
2. _Define your meta tags inside of your Shopify store products_

_To be placed inside of Shopify product description (example only)_
```HTML
<div class="metify" data-mf-meta-key="my-product-custom">
	<p> some custom content here! </p>
</div>
```


## License
