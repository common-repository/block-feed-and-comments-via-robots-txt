=== Block Feed and Comments via robots.txt ===
Contributors: apasionados
Donate link: https://apasionados.es/
Author URI: https://apasionados.es/
Tags: robots, robots.txt, crawler, robot, bot, seo
Requires at least: 4.0.1
Tested up to: 6.3
Requires PHP: 7.1
Stable tag: 1.2.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Blocks some Feed and Comment resources in order to avoid spam bots

== Description ==

This plugin adds lines to the virtual robots.txt file that WordPress creates automagically if the file is not present physically on the server to block resources related to feeds and comments from being indexed by search engines.

> Please be aware of what this plugin does exactly: If you activate the plugin it will add some lines to the robots.txt file to tell search engine bots to **not to crawl and index** parts of this website.

This plugin blocks all resources related to feeds and comments from being indexed by search engines.

**Please only activate this plugin if you know what you're doing**.

= What can I do with this plugin? =

This plugin adds the necessary lines to the virtual robots.txt file that WordPress creates automagically to block to block Feeds and Comments resources.

= What ideas is this plugin based on? =

None. We needed a fast solution to add these lines to the robots.txt file and this was the solution we coded.

= What is the robots.txt file? =

The robots.txt file is a plain text file located at the root folder of a domain (or subdomain) which tells web crawlers (like Googlebot) what parts of the website they should access and index.

The first thing a search engine crawler looks at when it is visiting a page is the robots.txt file and it controls how search engine spiders see and interact with the web pages.

= System requirements =

PHP version 7.1 or greater.
We require 7.1 or higher because we believe that everybody should be running a modern PHP version. When releasing this plugin [Wordpress recommends PHP 7.4 or higher](https://wordpress.org/about/requirements/).

= How to get this plugin in your Language! =
This first release is avaliable in English and Spanish. In the "languages" folder we have included the necessary files to translate this plugin.

If you would like the plugin in your language and you're good at translating, please use the [native WordPress Translation](https://translate.wordpress.org/) functionality.

New to Translating a plugin? First read through the [Translator Handbook](https://make.wordpress.org/polyglots/handbook/tools/glotpress-translate-wordpress-org/), then select your locale at [Translating WordPress](https://translate.wordpress.org/) and finally search for this plugin to translate it.

= Further Reading =
You can access the description of the plugin in Spanish at: [Block Feed and Comments via robots.txt en espa&ntilde;ol](https://apasionados.es/blog/).

== Screenshots ==

1. Lines that the plugin adds to the virtual robots.txt file that WordPress creates.

== Installation ==

1. First you will have to upload the plugin to the `/wp-content/plugins/` folder.
2. Then activate the plugin in the plugin panel. There are no settings.

== Frequently Asked Questions ==

= Why did you make this plugin?  =
We created this plugin to be able to append the lines to block Feed and Comment resources in order to avoid spam bots without having to upload a robots.txt file.

= Does Block Feed and Comments via robots.txt make changes to the database? =
No. The plugin doesn't write any options or settings to the database.

= How can I check out if the plugin works for me? =
Install and activate. Have a look at the content of the robots.txt file in root of the domain.

= How can I remove Block Feed and Comments via robots.txt? =
You can simply activate, deactivate or delete it in your plugin management section. There are no options stored in the database so you can delete it also via FTP and everything will be removed.

= What happens if there is a physical robots.txt file on the server? =
**This plugin makes changes to the virtual robots.txt file generated automagically by WordPress and doesn't work with a physical robots.txt file**. In order to use this plugin you need to remove the physical robots.txt file from your server. Please delete the robots.txt file via FTP or Server Panel before using this plugin. **We check this on activation (and only on activation)**. If we find a physical robots.txt file the plugin can't be activated until the file is removed. Please keep in mind that we only check it on plugin activation and after activation we don't check it any more; so if you upload a robots.txt file to the root of the domain once the plugin is activated, the plugin will have no effects but you will not receive a warning.

= What happens if WordPress is installed in a subdirectory? =
**WordPress must be installed in top-level directory of the web server.** Please note that the robots.txt must be in the top-level directory of your web server. If WordPress is installed in a subdirectory this plugin will not be effective because the robots.txt file generated by WordPress in the subdirectory will be ignored by the bots. Please note that we don\'t check this. You can read more about the robots.txt standard here [robotstxt.org: How to create a /robots.txt file and Where to put it](http://www.robotstxt.org/robotstxt.html).

= Are there any known incompatibilities? =
Please don't use it with *WordPress MultiSite*, as it has not been tested.

The plugin has similar functionality as the [Virtual Robots.txt](https://wordpress.org/plugins/pc-robotstxt/) and the [Better Robots.txt – Index, Rank & SEO booster](https://wordpress.org/plugins/better-robots-txt/) plugin; **both are not compatible with our plugin** as they remove all the virtual WordPress robots.txt content and create their own. The directives our plugin creates are not added to the robots.txt file these plugins generate as they don't use the standard functions of WordPress to append information to them.

= What Feed and Comment Resources does this plugin block? =
* `Disallow: /feed/`
* `Disallow: /feed/$`
* `Disallow: /comments/feed`
* `Disallow: /trackback/`
* `Disallow: */?author=*`
* `Disallow: */author/*`
* `Disallow: /author*`
* `Disallow: /author/`
* `Disallow: */comments$`
* `Disallow: */feed`
* `Disallow: */feed$`
* `Disallow: */trackback`
* `Disallow: */trackback$`
* `Disallow: /?feed=`
* `Disallow: /wp-comments`
* `Disallow: /wp-feed`
* `Disallow: /wp-trackback`
* `Disallow: */replytocom=`

= Are there any server requirements? =
Yes. The plugin requires a PHP version 7.1 or higher and we recommend using PHP version 7.4 or higher. The plugin has been tested with PHP up to 7.4. When releasing this plugin [Wordpress recommends PHP 7.4 or higher](https://wordpress.org/about/requirements/).

= Do you make use of Block Feed and Comments via robots.txt yourself? = 
Of course we do. That's why we created it. ;-)

== Changelog ==

= 1.2.0 (04/04/2023) =
* Added Data Sanitization/Escaping according to WordPress Developer Guidelines

= 1.1.0 (02/09/2020) =
* Updated translation text domain to match plugin slug ("Since WordPress 4.6 the Text Domain header is optional because it must be the same as the plugin slug" - More info at [Text Domains](https://developer.wordpress.org/plugins/internationalization/how-to-internationalize-your-plugin/#text-domains)).

= 1.0.0 (25/08/2020) =
* First official release.

== Upgrade Notice ==

= 1.2.0 =
UPDATED: Added Data Sanitization/Escaping

== Contact ==

For further information please send us an [email](https://apasionados.es/contacto/index.php?desde=wordpress-org-block-feeds-comments-robots-txt).