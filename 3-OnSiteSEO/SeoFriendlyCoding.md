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

# Error Handling
Having a single error page instead of several across the domain is also good practice
### Step 1 - Create an Error Page
* Create a single PHP or Node file that handles different REDIRECT_STATUS codes to served different pages. A PHP example - 
```
<?php switch($_SERVER["REDIRECT_STATUS"] ) { 
    case 400:
        $title = "400 Bad Request"; 
        $description = "The request can not be processed due to bad syntax";
        break;
    case 401: 
        $title = "401 Unauthorized"; 
        $description = "The request has failed authentication";
        break;
    case 403: 
        $title = "403 Forbidden"; 
        $description = "The server refuses to response to the request";
        break;
    case 404: 
        $title = "404 Not Found"; 
        $description = "The resource requested can not be found.";
        break; 
    case 500: 
        $title = "500 Internal Server Error"; 
        $description = "There was an error which doesn' t fit any other error
        message"; 
        break; 
    case 502: 
        $title = "502 Bad Gateway"; 
        $description = "The server was acting as a proxy and received a bad
        request."; 
        break; 
    case 504: 
        $title = "504 Gateway Timeout"; 
        $description = "The server was acting as a proxy and the request timed
        out."; 
        break;
} ?>
```
### Step 2 - Configure .htaccess
* You’ll need to redirect all error codes to the error page. Add the following lines to .htaccess
```
ErrorDocument 400 /error.php 
ErrorDocument 401 /error.php 
ErrorDocument 403 /error.php 
ErrorDocument 404 /error.php 
ErrorDocument 500 /error.php 
ErrorDocument 502 /error.php 
ErrorDocument 504 /error.php
```

# Crawlable Pagination 
Note - Wordpress has several plugins (including Yoast SEO) that handle SEO-friendly pagination for you.

Like Canonical tags, here you mention 

`<link rel="next" href=[target url]/>` for the next page

and

`<link rel="prev" href=[target url]/>` for the previous page.