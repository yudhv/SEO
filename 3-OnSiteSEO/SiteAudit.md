# The Chronological Process
## 1. Crawling
### Step 0: Browse your website like an SE
* Use [Browseo](http://browseo.net) to view the site without JS and CSS masking your links
* Stuff to check for here:
    * Can you see all the menu links?
    * Do all of the menu items and links appear as plain text? Are all the links clickable?
    * Does this reveal any text that was previously hidden? (Hidden text can send a red flag to Googlebot. It might not always be malicious, but it shouldn’t be there.)
    * Is your sidebar or widgets content all the way at the top? Remember, your most important links and content should be at the top of the HTML.
### Step 1: Run Screaming Frog and crawl the site
* The 500 URL limit can be bypassed by crawling sub-directories in pieces
* BONUS: Here, you can also filter out the pages with specific HTML in them (ex=> get all pages that open a link in a new tab)
### Step 2: Check page level: Pages buried too deep within the site are neither good for users, nor SEO. 
* After the crawl, sort the pages by "Level" (one of the columns)
* Now we have a sorted list of pages that need to be linked in the upcoming posts (to reduce the link-level)
* Export as CSV
* Note - The [CrossLinker plugin](http://wordpress.org/extend/plugins/cross-linker/) for Wordpress helps you to always internally cross-link all posts
### Step 3: Check for Crawl Errors
* Click on "Response Codes" =>  "Client Error 4xx" (drop down)
* Export as CSV
### Step 4: Find & Fix Long Titles
* Title tags and meta descriptions have a recommended length. It pays to adhere to the same.
* Click on "Page Titles"=>"Over 70 Characters" (drop down)
* Export as CSV
* TIP: Use the "=LEN(E3)" to calculate length of the titles in a new column
### Step 5: Find & Fix Long Descriptions
* Click on "Meta Descriptions"=>"Over 156 Characters" (drop down)
* Export as CSV
### Step 6: Check Indexation Settings
* Click on "Meta & Canonical"
* Check for:
    * Missing Canonical Tags (to eliminate duplicates)
    * Incorrect Canonical tags (pointing to a different page)
    * Pages that should be indexed, but have "noindex" meta
    * Pages that shouldn't be indexed, but have "index" meta
### Step 7: Check and eliminate search URLs and thin pages
* Thin pages: Pages with very little content on them (mostly used to target KWs)
* If you have 1000s of thin pages targeting lots of KWs but no content, google considers the domain low quality
* Only keep the most popular search URLs that have category-style landing page content on them

## 2. KW research & Targeting (Use the dedicated note)
* Make a long and broad list
    * Use KWs from competitors
    * Use KWs from auto complete and related searches on Google itself
    * Use semantically connected terms (like common questions)
* Get volume, difficulty and CTR opportunity
    * Volume: get from KW Planner 
    * Difficulty: not paid (as is shown by KW Planner) but organic difficulty/competition
    * CTR Opportunity: Note CTR stealing feature snippets (answer boxes, knowledge graphs) and their effect on organic 
* Prioritize by importance, difficulty, and volume
    * Importance is the subjective factor here. Only you may know which searches are best
## 3. Accessible content aimed at delighting searchers
* Don't just serve your content; satisfy searchers. Key is to put the searcher's goals above your business' goals; selflessness in content
* Use low engagement to identify poorly performing URLs: ex=>Bounce rate, Time on site, Pages per visit
## 4. KW Use + On-Page optimization
* Title, URL, Meta Description, Headlines, and Content (all still matter)
* Target all the KWs having the same intent on 1 URL: ex=>best smartphones, best smartphones 2018, best mobile phones
## 5. Snippet, Markup, and Schema
* This involves all different ways you can customize your SERP result (not just feature snippets but even regular results)
* Check Schema.org
* Compare types of results in your KW SERPs
* Identify "feature snippet" opportunities: **15% of searches have a feature snippet**
## 6. Alternative Formats & Engines
* Youtube=>Video: Even if you're not doing videos, check the YouTube search volume for your KWs to see if you need to get into video or not
* FB/Insta=>Images/News
* Maps=>Local
* Amazon=>E-Commerce
* Images/News/Apps: Different content domains have different mediums that are most prominent
## 7. Links & Amplification
* Before creating content, ask "who will help amplify and why?": the specific list of people/entities (bloggers, outlets, etc) that would be willing to share your content
* Choose a flywheel; reduce friction with smart hacks: 
    * Flywheel (or link flywheel) is a link building process which is cyclical and self-sustaining. 
    * Hacks refer to one-to-one manual link building through outreach. 
    * Smart Hacks are the same as hacks, but are done in the service of a flywheel, i.e approach only those who deliver continuously (not just once)
    * amplifier ex=>news/press, content marketing, partnerships, embedded content
## 8. Conversion Optimization
* Find the funnel/path to attract, to draw back, and to close
    * Conversions always happen over multiple visits, never single 

# Site Redesign
In-order to not lose any traffic in the process of redesigning one's website, one has to have a self-audit to monitor the effects of the redesign. 

Here are the common things to monitor: 
## 1. Monitor No. of Pages Indexed
Google `site:sitename.com`

## 2. Monitor Cache Date
Google `cache:sitename.com`

## 3. Monitor Page Rank
Use the (SEOquake Toolbar)[http://www.seoquake.com/] to check your page rank. Keep in mind, this is a *loose metric*

## 4. Monitor Domain Authority (DA)
Use (SEOmoz toolbar)[http://www.seomoz.org/seo-toolbar]. This metric will have a delay. 

## 5. Monitor "Not Found" Errors
Use Google Search Console to monitor the number of "Not Found" Errors.

## BONUS - 5 questions to ask for any website
1. What value does your business create that helps solve searcher's queries?
2. What is unique about the value you provide? (It can be better than existing, or different than existing, etc)?
3. Who is going to amplify your value and why? (bloggers, social media users, press, etc)?
4. What is your conversion process? (This is where your funnel comes in)?
5. How do you expose your value in a way that SEs can crawl, index, understand (contextual), and show off (feature snippets, desc, etc)?

