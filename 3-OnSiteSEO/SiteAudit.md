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

# Local SEO 
Always start with knowing what SEO work was done in the past. This will help you with knowing what potential damage has been done and give ideas on how to improve the site.

[This spreadsheet](https://docs.google.com/spreadsheets/d/1AQvfF26DZvXN2PJAGv0TuW_EYg4eQ0O5nxDgy2cW2fE/edit?usp=sharing) can be used to track most Local SEO factors mentioned below. It has 5 tabs:

* Current Info - allows you to record the information the customer submits and compare it against the Google My Business information you find. Helps with reporting findings
* Questions to ask - questions you can ask your clients up front that may save a lot of time in the long run
* Competitor information - You can use this tab to track your competitors and compare your metrics side by side
* Top 50 citations audit - a list of the top 50 citation sources as provided by [Whitespark](https://whitespark.ca)
* Audit steps - an **audit checklist** for the more advanced user with some small notes on what to check for


## Local SEO Audit Steps

## 1. Google My Business page audit
1. Locate the proper Google My Business (GMB) page 
2. Find and destroy duplicate GMB listings 
3. **Ensure the local listing is not penalized**
    * How to find out - If your main KW set SERP has your business listing in Maps, but not in the local searches below, you're penalized. Check with a penalty expert .....
4. Ensure the GMB page is associated with the business' domain
5. Ensure the GMB listing is verified - it doesn't have "claim this business" mentioned
6. Ensure that the correct business name is used
    * It's crucial that the Business Name, Address, and Phone Number are as consistent as possible across the web. Google also now permits a one word descriptor of your business in the name of the business.
7. **Proper category association**
    * Make sure your primary category is the one that most closely represents your most important keyword
8. Proper URL
    * If single location, use home page
    * If multiple locations, separate landing pages
9. Use an Introduction Description that is unique (google your description to confirm) and over 250 words if possible
10. Profile should be 100% GMB complete
11. Map & Search photos should be used
12. Business Hours mentioned
13. Schedule a Google Trusted Photographer search
    * From the Google My Business page click the "Add Virtual Tour" link

## 2. Website & landing page audit
1. Crawlable NAP (Name, Address, Phone Number) on landing page
2. **Site Structure** 
    * Is there a page for every specific service (and location and practitioner, if applicable)?
    * Does the homepage form the nucleus of the site, with a ton of useful detail on the page, and plenty of links to relevant subpages?
    * Is the blog on the same domain? 
    * Does the landing page URL structure follow this format:
    
        http://www.YourSite.com/locations/Denver
3. Crawlable Business Hours on landing page
4. Use Landing Page content
    * Go for at least 400 words
    * Use [Miriam Ellis article](https://moz.com/blog/local-landing-pages-guide) for tips
    * Ask local operators for content if you have multiple locations. This ensures a unique content flavor each time
5. Ensure your landing page is **indexed** by pasting \*[landingPageURL]\* in Google
6. Optimize landing page meta title and description
    * Title - Use *business name, keyword,* and *location* (including city and state)
    * Description - May or may not show in SERP. Helps improve CTR.
    * Use [Matt Cutts' guidelines](https://moz.com/blog/local-landing-pages-guide) for details
7. Use heading tags (h1,h2,etc) and test using MozBar page analysis feature
8. Add driving directions and embed a map on landing page
    * Have them in a text format as well as an embedded map with landmark pictures
    * Go to classic Google Maps and grab the embed code after searching for your business
9. Add Payment Info on landing page with acceptable payment forms
10. Add Customer reviews on landing page in schema with the `hReview` tag
11. Add alt text to location images with state/city/street info
12. Get the Domain Authority (DA) and Page Authority (PA) with MozBar for competitive comparison later
13. Add NAP to `hCard` schema so Google can crawl and understand what it means
14. Load time of landing page below 3.5 sec at 1.5mbps
15. Add KML file on domain name
    * Follow [Geo Map Site Generator](http://www.geositemapgenerator.com/)
    * Add all your locations to the KML file
    * Reference KML through your XML site map
16. Add address to the footer as well
17. Ensure no content is keyword stuffed (means adding irrelevant KWs)
18. **Ensure mobile friendliness** 
    * Use Browserstack and PageSpeed insigths to verify mobile responsiveness

## 3. Citation analysis
Citations are different than backlinks. They refer to your business having presence on popular business directories like Yelp, YellowPages, etc.

This allows your business to be seen as more authentic by Google (less so since Pigeon update) and also allows for reviews 

1. Check Data Aggregators
    * Data Aggregators are the data holders that submit your business information to other directories
    * Make sure your business appears on the top 5 data aggregators for your country
    * Ex=> The main data aggregators in the United States are Infogroup, Localeze, Acxiom, and Factual
2. Check top 50 citations from the afore-mentioned spreadsheet
    * Ensure the top 50 citations for your industry are live, correct, and don't have duplicates
    * Identify other high-quality citation sources. For example => 

        **Attorneys**: Lawyers.com, Martindale.com, Avvo.com

        **Restaurants**: Yelp.com, TripAdvisor.com, OpenTable.com
3. Verify you're on Apple Maps

## 4. Organic link & penalty analysis
### **NOTE: Do NOT go for high link number. It is completely irrelevant. Only link quality matters now**
1. Ensure there is no manual web spam action
* Make this a top priority if Google penalises your domain. 
* Check through Google Search Console by going to `manual actions` tab
2. Check for algorithmic penalties
* Check out Moz's [guide](https://moz.com/google-algorithm-change) to algorithm changes
* **Easy Method**: Use the [Panguin tool](http://panguintool.barracuda-digital.co.uk/) to align your traffic trends with Google updates. 
3. Check the number of links (domain and page)
* Use MozBar to get these numbers for **you and your competition**
* The number CAN help if to see if you have a lot less or a lot more than your competitors. 
* A lot more could mean you might have spammy links. 
* A lot less means either your competition has spammy links, or you need to add more links yourself
4. Anchor text of links
5. Link velocity
6. Does a disavow exist

## 5. Review analysis
Reviews are important but hard to get
1. GMB reviews
2. Identify top 3rd party review sites

## 6. Social analysis
1. FB reviews
2. Foursquare | Swarm audit
3. Youtube audit

## 7. Competition analysis
1. Competition identification
2. Competition analysis

## 8. Ongoing strategy


