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
    * Identify other high-quality citation sources. Check Google Analytics Referral traffic for ideas. Example: 

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
    * Your anchor text profile (or **link profile**) should look natural
    * Anchor text correlates heavily with SEO penalties
    * It's always detrimental to have the exact same anchor text (even if it is relevant) across multiple inbound links
5. Link velocity
    * It is the speed with which you gain inbound links
    * The link velocity should seem natural
    * If you gained all your links overnight, then you almost always will be penalized by Google
    * Review any spikes in your link velocity and remove them
6. Does a disavow exist
    * Disavow list is a list of inbound links that you acknowledge being bad links
    * Every client site has bad links, but most do not have a disavow list that Google can read
    * Every Penguin (the algo that strictly checks link profile) update takes your disavow into consideration
    * Update this list every month

## 5. Review analysis
Reviews are important but hard to get. Even if you rank on the top, bad overall reviews and ratings will pretty much nullify all other SEO efforts.

The three factors to look for are **Positive sentiment**, **Uniqueness**, and **User's Importance** (like whether it is a Yelp Elite user)
1. GMB reviews
    * Try to go for at least 10 reviews here (>4 stars), unless you're a restaurant in which case you'll need more
    * The key is they need to be honest, come naturally over time, and posted from the customer's own devices
2. Identify top 3rd party review sites
    * Check Referral traffic in Google Analytics to identify 3rd party review sites
    * Also check for low referral traffic for your top citations. Maybe it would point to low quality reviews
    * Ensure you have 5-10 reviews with 4+ star average rating across the top 5 review sites

## 6. Social analysis
Social is important as it allows you to add NAP, check ins from your customers, and gives brand consistency
1. FB reviews - Check for the following
    * Ensure the Facebook NAP is correct.

    * Are the best possible photos used for the cover photo and profile image?

    * Is the page completely filled out and linked to their website?

    * Are they active and posting regularly?

    * Do they have any business check ins?

    * Do they have reviews and do they meet the criteria mentioned in the review section?
2. Foursquare | Swarm audit
    * Used mostly for checkins
    * Having a social presence here can help alert users of your business and allow them to check in 
    * You can also take advantage of this by having **check in deals** among other offers
3. Youtube audit
    * Add NAP in the description and link it to the landing page
    * Add Geo Tags
4. Instagram audit
    * Have influencers add NAP in the description
    * Point it to your Insta Business profile 
    * Add landing page link to your profile's Bio

## 7. Competition analysis
**Important Warnings Ahead**

* Remember that this is **NOT A NUMBERS GAME**
* Wrong mindset - "Well they're not doing it so I'm not going to do it" 
* Right mindset - "Lets be the least imperfect"
* Do this only to get some ideas on low-hanging fruits. A road map of what you can do moving forward.
* Start by getting a list of top 3-7 competitors in your niche, with their NAP+W (?) info

1. Domain Authority
2. Page Authority of Landing Page
3. Number of links from root domain
4. Number of links from unique domains
5. Number of citations (both detected and undetected)

## 8. Ongoing strategy