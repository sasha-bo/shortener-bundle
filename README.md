# shortener-bundle (Symfony)

Provides shorten_text and shorten_html twig filters, which shorten (cut) 
plain text or html to the $length, preventing braking words and tags.

Read [sashabo/shortener](https://packagist.org/packages/sashabo/shortener)
readme for retails.

### Installation

`composer require sashabo/shortener-bundle`

Then add the bundle to your config/bundles.php:

```php
SashaBo\Shortener\SymfonyBundle\SashaBoShortenerBundle::class => ['all' => true],
```

### Usage

`{{ 'Lorem ipsum dolor sit amet'|shorten_text(25, '...') }}`

`{{ '<u>Lorem <i>ipsum</i> dolor sit amet</u>'|shorten_html(25, '...') }}`

results:

Lorem ipsum dolor sit...

&lt;u&gt;Lorem &lt;i&gt;ipsum&lt;/i&gt; dolor sit...&lt;/u&gt;



