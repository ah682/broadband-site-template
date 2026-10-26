# SupaBroadband WordPress theme

An Astra child theme for a broadband comparison site. It includes plan listings,
filters, comparison tables, enquiry pages and a mock speed-test widget.

## Install

Start with a working WordPress installation and the Astra parent theme.

1. Copy `app/public/wp-content/themes/astra-child/` into your WordPress
   `wp-content/themes/` directory.
2. Activate **Astra Child** under **Appearance → Themes**.
3. Set permalinks to **Post name** under **Settings → Permalinks**.
4. Create the pages and add plans using the [theme setup guide](app/public/wp-content/themes/astra-child/README.md).

The enquiry page renders its page content, so it can use a Contact Form 7 shortcode.
Configure that plugin separately if you want to receive enquiries.

## Theme files

The child theme contains templates for the homepage, plans, comparison, enquiry,
contact, getting started, cookies and terms pages. Plan fields and shortcodes live
in `functions.php`; filtering and sorting live in `assets/js/filter-sort.js`.

CSS is split into variables, base styles, components, sections, pages and utilities
under `assets/css/`. Edit the child theme rather than the Astra parent theme.
