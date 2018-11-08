## Content
* Provide alt-text for images
* Supplement search boxes with navigation and crawl-able links
* Supplement Java and Flash plug-ins with text on the page
* Provide transcripts for video and audio content
* Use Rich Snippets to allow SEs to add more value to your SERP results, like ratings, dates etc. Check schema.org, google, and mozbar for usage and verification info. 
* Use Pingomatic to automatically ping Google, Yahoo, Bing whenever you publish new content. This will tell them that your content is original, and copycats will be prohibited
* Use tools like Google Cache, SEO-browser, and MozBar to see what content is indexable by search engines
* Do not let any page become an orphan (without any page linking to it)

## Canonicalization
* It is the practice of organizing content in such a way that every unique piece has one, and only one, URL 
* Duplicate content is a great problem in SEO. ex => same content offered as HTML and print-optimized pages
* Taking multiple pages and "301-redirecting" them relieves the problem
* SEs will combine them into a single strong page, and create stronger relevancy and popularity signal overall, thus positively impacting the original ranking
* Use canonical tags within the page that contains duplicate content, with the target pointing to the master URL that you wanna rank for.
* Canonical tag can also point to other domain's URLs
* Example Code: `<link rel="canonical" href=[target url]/>`


## Common Mistakes
* Content behind forms or paywalls
* Links inside javascript
* Links pointing to pages blocked by robots.txt (or meta robots tag)
* Links inside frame or iframes (although parseable by SEs, u must know what you're doing)
* Links inside Flash, Java, and other plug-ins
* Pages with hundreds of links on them are at risk of not getting crawled completely


## Keyword Usage
* In the title tag at least once. Try to keep the keyword phrase as close to the beginning of the title tag as possible
* Once prominently near the top of the page.
* At least two or three times, including variations, in the body copy on the page. Perhaps a few more times if there's a lot of text content.
* At least once in the alt attribute of an image on the page. This not only helps with web search, but also image search.
* Once in the URL
* At least once in the meta description tag. Note - this does not get used by SEs for rankings, but rather helps attract clicks by searchers on SERP
* Do NOT use keyword in link anchor text pointing to other pages on your site (called keyword cannibalization)


## On-Page Optimization
### Title
* Keep length < 65-75 characters as that is what SEs show on SERP
* Place important keywords close to the front
* Try adding branding in the title if possible
* It must be descriptive, readable, compelling and attention-grabbing
### Meta-Tags - <META NAME="ROBOTS" CONTENT="NOINDEX, NOFOLLOW">
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
### URL
* Use empathy here. Think if it gives a rough description to u as a user
* Shorter is better. It'll be easier to share and copy, and will look good in the top bar
* Use KWs but not too much. If page targets mutliple KWs, then keep the best ones
* Use static URLs - Using technologies like mod_rewrite for Apache and ISAPI_rewrite for Microsoft,  transform dynamic URLs like this https://moz.com/blog?id=123 into a more static version like this: https://moz.com/blog/google-fresh-factor. Even single dynamic parameters in a URL can result in lower overall ranking and indexing
* Use hyphens to separate words - Not all web applications accurately interpret separators like underscores (_), plus signs (+), or spaces (%20), so use hyphens(-)