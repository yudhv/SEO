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
    4. **Link to the Original Source** - helps get extra backlinks and tells Googlebot that the content came from you first. Follow these steps:

        * Go to `Appearance`=>`Editor`=>`functions.php`
        * Add this function 
        ```
        function embed_rss($content) { 
            if(is_feed( ) ) $content .= "<p><a href=' ". get_permalink( ) ."' >' "; $content .= get_the_title( ) ."</a></p>";
            return $content; 
        }
        add_filter(' the_content' , ' embed_rss' ) ;
        ```

# Common Mistakes
* Content behind forms or paywalls
* Links inside javascript
* Links pointing to pages blocked by robots.txt (or meta robots tag)
* Links inside frame or iframes (although parseable by SEs, u must know what you're doing)
* Links inside Flash, Java, and other plug-ins
* Pages with hundreds of links on them are at risk of not getting crawled completely