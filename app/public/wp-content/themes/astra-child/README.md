# SupaBroadband theme setup

This Astra child theme adds broadband plans, comparison pages and enquiry forms to
WordPress. The theme files are already laid out in this directory; copy the whole
`astra-child` folder into your WordPress site's `wp-content/themes/` directory.

## Set up the pages

Install the Astra parent theme, then activate **Astra Child** under
**Appearance → Themes**.

1. Create a blank page named **Home**. Under **Settings → Reading**, select
   **A static page** and choose it as the homepage. `front-page.php` supplies the
   layout.
2. Create a **Broadband Plans** page with the slug `broadband-plans` and select the
   **Broadband Plans** template.
3. Create an **Enquiry** page with the slug `enquiry` and select the **Enquiry Form**
   template. Add a Contact Form 7 shortcode to the page content after installing
   and configuring that plugin.
4. Set permalinks to **Post name** under **Settings → Permalinks**.

Templates for comparison, contact, getting started, cookies and terms pages are
also included. Review their text and contact details when setting up your own site.

## Add plans

Open **Broadband Plans → Add New** in the WordPress dashboard. Enter a title, then
fill in the provider, speed, monthly price, contract length and setup fee. A featured
image can be used as the provider logo. Publish the plan to show it in the listing.

For a local demo, an example plan could use 67 Mbps, £24.99 per month, a 24-month
contract and a £9.99 setup fee. Add a few plans with different speeds and prices to
try the filters and comparison table.

## Customize

- Change colours in `assets/css/variables/colors.css` and typography in
  `assets/css/variables/typography.css`.
- Edit component and page styles in the corresponding `assets/css/` folders.
  `functions.php` enqueues the modular stylesheets.
- Edit `header.php` and `footer.php` for the site header, links and footer text.
- Edit page templates to change their headings, copy and layout.
- `assets/js/filter-sort.js` handles plan filtering, sorting and selection.

The `[speed_test_widget]` shortcode shows an animated mock speed test with generated
results. The `[comparison_table]` shortcode displays plans; use
`[comparison_table limit="3"]` to limit how many appear.

## Check the setup

Open the homepage and plan listing on desktop and a narrow screen. Try the speed
and contract filters, both sort orders and **Reset All**. Select a plan and check
that its details appear on the enquiry page. Test form delivery through your
configured form plugin.

If plans are missing, check that they are published and that the listing page uses
the **Broadband Plans** template. If filtering is not working, check the browser
console and confirm that `assets/js/filter-sort.js` and jQuery load. For missing
styles, check stylesheet requests in the browser and clear any page or asset cache.
