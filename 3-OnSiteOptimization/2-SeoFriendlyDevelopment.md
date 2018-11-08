# Crawlable AJAX
For websites that load dynamic content on the page without refreshing, Google recommends routing `_escaped_fragment_` in your GET query and pointing it to an HTML snapshot. 

The principal idea is that you want to render *HTML* for **GoogleBot** and *JavaScript* for **Visitors**.

* Modify the backend such that if the URL looks like `http://example.com/index.php`
then an HTML page **WITH** the JS code should be served

* If the URL looks like `http://example.com/index.php?_escaped_fragment_` then the backend should serve a page with the JS already executed (meaning no JS)

* Add `<meta name="fragment" content="*">` to all dynamic pages of the site where a simplified HTML page is served for crawlers

* Verify your special routing by sending both normal and modified GET reqeusts to the server and checking the *View Source* and *View Inspect*. 
    | GET Type | View Source | View Inspect |
    |---|---|---|
    | Normal | Contains JS | Only HTML | 
    | Modified | Only HTML | Only HTML | 

# Crawlable Pagination 
Note - Wordpress has several plugins (including Yoast SEO) that handle SEO-friendly pagination for you.

Like Canonical tags, here you mention 

`<link rel="next" href=[target url]/>` for the next page

and 

`<link rel="prev" href=[target url]/>` for the previous page.
