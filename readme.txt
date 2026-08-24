=== Polite Clean ===

Contributors: templatesell
Theme URI: https://www.templatesell.com/item/polite-minimal-blog-wordpress-theme/
Author URI: https://www.templatesell.com/
Tags: grid-layout, one-column, two-columns, three-columns, four-columns, left-sidebar, right-sidebar, custom-background, custom-logo, custom-menu, featured-images, threaded-comments, translation-ready, footer-widgets, custom-colors, custom-header, editor-style, rtl-language-support, theme-options, blog, news
Requires at least: 6.0
Requires PHP: 7.4
Tested up to: 7.1
Stable tag: 1.0.1
License: GNU General Public License v2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

A perfect theme for blog and magazine site. With masonry layout and multiple blog page layout, this theme is the awesome and minimal theme. It is a child theme of Polite. This theme has search option, off-canvas sidebar, multiple sidebar options, footer options, featured slider, promo boxed, footer widgets and many more. Besides that, this theme comes with added custom widgets for author information, featured posts, social icons, etc. It comes with primary color option to change the whole site color with a single click. More Details: https://www.templatesell.com/item/polite-grid/

== Description ==

A perfect theme for blog and magazine site. With masonry layout and multiple blog page layout, this theme is the awesome and minimal theme.
== Installation ==

1. In your admin panel, go to Appearance > Themes and click the Add New button.
2. Click Upload Theme and Choose File, then select the theme's .zip file. Click Install Now.
3. Click Activate to use your new theme right away.

== Changelog ==
= 1.0.1 - August 24 2026 =

Fixed
* The Customizer's font list was requested from the css2 endpoint using v1 syntax - families separated by "|" - plus a stray space before one of them. css2 requires "&family=" between families and rejects the pipe outright, so the request came back HTTP 400 with an error page and the dropdown that exists to show each option in its own typeface loaded no fonts at all. It is built from the theme's own font list now, joined the way css2 wants, and routed through the same WPTT loader the front end already uses, so it is cached locally rather than fetched from Google on every Customizer load
* The child stylesheet was enqueued under the handle 'polite-blog-style' - a different theme's name, copied in along with the rest of the file
* The parent's 'polite-style' handle was re-registered with no version, which makes WordPress substitute its own - the parent stylesheet was served as style.css?ver=7.1. It carries the parent's version now. The handle does still have to be registered here, because the parent enqueues it with get_stylesheet_uri(), which on a child install resolves to this theme's style.css
* The dynamic font rule read the font array without checking the stored key exists. The parent offers its own font list, so a value set or left over from the parent was an undefined array key; it falls back to the theme default now
* $parent_style was assigned and never used, and the stylesheet enqueue ended in a double semicolon
* A default string in this child theme was tagged with the parent's text domain, so a language pack for this theme could never translate it
* The child theme's text domain was loaded without being told where its language files are
* 'no-cotent' was a misspelling of the class the theme meant to output
* readme.txt gave the PHP requirement as 4.7, a PHP version that has never existed, and a stable tag that did not match the theme

Performance
* The reading-time counter ran the whole content pipeline on every post in the loop purely to count words: apply_filters( 'the_content' ) renders blocks, expands shortcodes, runs wpautop and resolves every oEmbed - and then do_shortcode() was called on the result a second time. It counts the raw content now, with strip_shortcodes(), which removes shortcode tags without executing them
* _n()'s third argument selects the plural form and has to be a number; it was being passed number_format_i18n(), which returns a formatted string

Other
* Added languages/polite-clean.pot
* Tested up to WordPress 7.1

= 1.0.0 - July 04 2022 =
* Initial Submission

== Credits ==
Polite Clean is a child theme of Polite by, Template Sell.
Polite Clean is distributed under the terms of the GNU GPL v2 or later.

Polite is free WordPress theme by, Template Sell.
Polite is distributed under the terms of the GNU GPL v2 or later.

== Screenshot Images [CCO License] ==
Image for theme screenshot, Copyright Ben White
License: CC0 1.0 Universal (CC0 1.0)
Source: https://stocksnap.io/photo/people-man-C2PM96LSJL

Image for theme screenshot, Copyright NastyaSensei Sens
License: CC0 1.0 Universal (CC0 1.0)
Source: https://stocksnap.io/photo/people-woman-1XSBGU6WE1

Image for theme screenshot, Copyright Kristin Hardwick
License: CC0 1.0 Universal (CC0 1.0)
Source: https://stocksnap.io/photo/woman-business-LERRJPTMHP

Image for theme screenshot, Copyright Pete Johnson
License: CC0 1.0 Universal (CC0 1.0)
Source: https://stocksnap.io/photo/woman-crops-ZQENDPB9UC