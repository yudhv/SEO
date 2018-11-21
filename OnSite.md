(PageOptimization)
# Keyword Usage
## Summary
* In the title tag at least once. Try to keep the keyword phrase as close to the beginning of the title tag as possible
* Once prominently near the top of the page.
* At least two or three times, including variations, in the body copy on the page. Perhaps a few more times if there's a lot of text content.
* At least once in the alt attribute of an image on the page. This not only helps with web search, but also image search.
* Once in the URL
* At least once in the meta description tag. Note - this does not get used by SEs for rankings, but helps attract clicks on SERP
* Do NOT use keyword in link anchor text pointing to other pages on your site (called keyword cannibalization)

## Title
* Keep length < 65-75 characters as that is what SEs show on SERP
* Place important keywords close to the front
* Try adding branding in the title if possible
* It must be descriptive, readable, compelling and attention-grabbing

## Meta-Tags - <META NAME="ROBOTS" CONTENT="NOINDEX, NOFOLLOW">
* Meta Robots - Used to control search engine crawler activity on a per-page level
    * index/noindex - use if you wanna stop SEs from indexing (default: index)
    * follow/nofollow - use to stop SEs from crawling this page (default: follow)
    * noarchive - use to stop SEs from save a cached copy of this page
    * nosnippet - use to stop SEs from displaying description in SERP
    * noodp/noydir - use to tell SEs to take desc from DMOZ or Yahoo Directory
* Meta Description - Short description of a page's content shown on SERP
    * Very important 
    * SEs cut these after 160 characters, so stay within this limit
    * Do not include this if page targets multiple keywords. In this case the SEs will create the search snippet from other elements on the page. Valid tactic
    * Keep it readable, compelling
    * Include imp keywords as Google bolds them on SERP

## Content
* Provide alt-text for images
* Supplement search boxes with navigation and crawl-able links
* Supplement Java and Flash plug-ins with text on the page
* Provide transcripts for video and audio content
* Use Rich Snippets to allow SEs to add more value to your SERP results, like ratings, dates etc. Check schema.org, google, and mozbar for usage and verification info. 
* Use [Pingomatic](http://pingomatic.com/) to automatically ping Google, Yahoo, Bing whenever you publish new content. This will tell them that your content is original, and copycats will be prohibited
* Use tools like Google Cache, SEO-browser, and MozBar to see what content is indexable by search engines
* Do not let any page become an orphan (without any page linking to it)

## URL
* Use empathy here. Think if it gives a rough description to u as a user
* Shorter is better. It'll be easier to share and copy, and will look good in the top bar
* Use KWs but not too much. If page targets mutliple KWs, then keep the best ones
* Use static URLs - Using technologies like mod_rewrite for Apache and ISAPI_rewrite for Microsoft,  transform dynamic URLs like this https://moz.com/blog?id=123 into a more static version like this: https://moz.com/blog/google-fresh-factor. Even single dynamic parameter in a URL can result in lower overall ranking and indexing
* Use hyphens to separate words - Not all web applications accurately interpret separators like underscores (_), plus signs (+), or spaces (%20), so use hyphens(-)

# How Google measures UI of a site
* Engagement Metrics
    * Google uses Google Analytics data to gauge user-engagement on a website 
    * So, the way visitors engage with your site will affect your rankings
    * Ex - If users go back as soon as they arrive from Google, your site will suffer
* Machine Learning
    1. The Panda update in 2011
    2. Google used human evaluators to manually rate thousands of sites, searching for low quality content
    3. Google then incorporated machine learning to mimic the human evaluators
    4. The end result was a seismic shift that rearranged over 20% of all results
    5. More about Panda [here](https://moz.com/blog/beat-google-panda) and [here](https://moz.com/blog/duplicate-content-in-a-post-panda-world)
* Links
    * higher quality sites earn more links than their less useful, lower quality peers

## Common traits in Google-certified UX sites
* Easy to use, navigate, and understand
*  Provide direct, actionable information relevant to the query
*  Professionally designed and accessible to modern browsers
*  Deliver high quality, legitimate, credible content

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


(SiteOptimization)
# Canonicalization
* It is the practice of organizing content in such a way that every unique piece has one, and only one, URL 
* Duplicate content is a great problem in SEO. ex => same content offered as HTML and print-optimized pages
* Taking multiple pages and "301-redirecting" them relieves the problem
* SEs will combine them into a single strong page, and create stronger relevancy and popularity signal overall, thus positively impacting the original ranking
* Use canonical tags within the page that contains duplicate content, with the target pointing to the master URL that you wanna rank for.
* Canonical tag can also point to other domain's URLs
* Example Code: `<link rel="canonical" href=[target url]/>`

# RSS Feeds
This assumes you have Feedburner (the most popular RSS tool)
* In-order to have all sites point to your Feedburner feed, you'll need to change the href value of the rss link tag in the header.php file (Wordpress) like so:

    `<link rel="Alternate" type="application/rss+xml" title="<?php bloginfo('name');?>RSS Feed" href="http://feeds.feedburner.com/sitename.com" />`
* In Feedburner, now you have a number of low-hanging fruits (features):
    
    1. **Activate SmartFeed** - helps make your feed compatible with any reader
    2. **Activate FeedFlare** - helps put links at the bottom of your feed (like FB share, email, bookmark). Remember adding "personal" flares as well.
    3. **Activate Pingshot** - helps notify reading services when there's an update
    4. **Link to the Original Source** - helps get extra backlinks and tells Googlebot that the content came from you first. Follow these steps for Wordpress:

        * Go to `Appearance`=>`Editor`=>`functions.php`
        * Add this code 
        ```
        function embed_rss($content) { 
            if(is_feed( ) ) $content .= "<p><a href=' ". get_permalink( ) ."' >' "; $content .= get_the_title( ) ."</a></p>";
            return $content; 
        }
        add_filter(' the_content' , ' embed_rss' ) ;
        ```
    5. **Create Thank You** - Go to `Optimize`=>`BrowserFriendly`=>`Content Options` and "Enable" the personal message
    6. **Time Your RSS Emails** - Go to `Publicize`=>`Email Subscriptions`=>`Delivery Options`
    7. **Redirect Wordpress RSS to Feedburner** - Install and activate the [tentbloggers plugin](http://wordpress.org/extend/plugins/tentbloggers-feedburner-rss-redirect-plugin/). Then enter your Feedburner URL for "Your Feedburner Address" and "Comment Feeds" fields.

# Video Sitemaps
Video content gets noticed and indexed much faster with Video Sitemaps
Follow these steps to generate one - 
1. Create an empty XML file
    * Save it in the root directory of your website. The name of the file does not matter.
2. Paste this into the XML 
    ```
    <url>
    <loc>http://www.quicksprout.com/videos/neil-patel-video-1.html</loc> <video:video>
    <video:thumbnail_loc>http://www.quicksprout.com/thumbs/thumbnail.jpg</video:thu mbnail_loc>
    <video:title>Advanced SEO for Bloggers</video:title> <video:description>An exclusive video with SEO expert Neil Patel. Drive ridiculous amounts of leads to your blog and learn the 7 secrets of conversion rate optimization.</video:description> <video:content_loc>http://www.quicksprout.com/video.flv</video:content_loc> </video:video> </url>
    ```
3. Submit your sitemap to Google Search Console
    * Yuo can also submit it by adding the following line to robots.txt

        `Sitemap: http://www.example.com/sitemap_video.xml`

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

# .HTACCESS hacks


# Common Mistakes
* Content behind forms or paywalls
* Links inside javascript
* Links pointing to pages blocked by robots.txt (or meta robots tag)
* Links inside frame or iframes (although parseable by SEs, u must know what you're doing)
* Links inside Flash, Java, and other plug-ins
* Pages with hundreds of links on them are at risk of not getting crawled completely