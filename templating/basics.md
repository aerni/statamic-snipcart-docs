# Basics

## Example

This is a simple example of a section that displays all products:

<pre class="language-html"><code class="lang-html"><strong>&#x3C;section>
</strong><strong>    {{ collection:products }}
</strong>        &#x3C;div>
            &#x3C;h2>{{ title }}&#x3C;/h2>
            &#x3C;div>{{ price }}&#x3C;/div>
            &#x3C;div>{{ snipcart:buy }}&#x3C;/div>
        &#x3C;/div>
    {{ /collection:products }}
&#x3C;/section>
</code></pre>

## Multi-Site

Snipcart doesn't fully support multiple localizations. The only localizable field supported by Snipcart is a product's price. You may localize a few other fields such as a product's title and description. But those fields are solely for templating purposes and will fall back to the product's root locale when getting the Snipcart button attributes.

