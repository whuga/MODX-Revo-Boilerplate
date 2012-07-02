#MODX Revolution Boilerplate basics

A bunch of stuff to quickly get some sensible basics into a new [MODX Revolution](http://modx.com/) install. There's a folder for each type of resource. Simply make a new resource of that particular type and copy in the code.

I'll probably try and set up a transport package for this at some point to make it even easier to use.


##Templates

###BaseTemplate

Used by default in MODX, very basic HTML structure. Pulls in a head and foot chunk.

###Article & ArticleContainer

For sites using Articles, you'll definitely want new templates for the layout in that section. These two templates have sane defaults and ensures all repeated code is pulled out into head, foot & articleSidebar chunks.


##Assets

###CSS

I use LESS just about all the time. The files in here can be put straight into /assets/templates/{TEMPLATEFOLDERNAME}

Includes the HTML5 Boilerplate normalise CSS (with a few tweaks), Internet Explorer HTC behaviour file for border-box bos-sizing method, clearfixes, classes, and basic print styles. 

###js

Includes Modernizr for YepNope and making people think that old versions of Internet Explorer are futuristic. Kind of. Also includes jQuery 1.7.2 for fallback should the CDN download fail, and jQuery Easing for nicer animations.


##Chunks

###head and foot

Beginning and end of the templates. I've added two placeholders - [[+bodyClass]] and [[+template]].

[[+bodyClass]] is useful for complex sites and when passed into the [[$head]] will add that class name to the body tag. Can help save a bunch of extra templates (sometimes).

[[+template]] help make your [[$head]] & [[$foot]] more generic and easier to chuck into a new site without messing too much. See the BaseTemplate template for how to use.

###standardSidebar

Chuck everything in here that you would have in your aside. 

###articleSidebar

Contains most things that were pulled out of the stock Articles templates but are repeated on both container and article template. Nicely wrapped in an aside

###contactEmail and contactForm

Install the FormIt extra, and with these two simple chunks you can easily drop a working contact form on any page with little to no customisation required.


##Snippets

###copyYears

Works out the copyright for the footer.

###currentUrl

Clue is in the name

###formatSearchUrl

Some preformatting for passing to the SimpleSearch on the Page Not Found error page.


##Content Pages

###Page Not Found

Requires SimpleSearch extra, formatSearchUrl and currentUrl snippets. Does a lookup for what page you tried to access and shows results in a list (if any).

###robots.txt

Disallows access to a bunch of MODX folders to SpiderBotMonkeys. Also points out the URL of the sitemap (edit this to your URL). You'll need to install the GoogleSiteMap extra to make the sitemap.xml file

###humans.txt

You can pretty much do what you want in this file, but point out developer, designer, technology used, etc.


##Extras

I generally use the following extras most of the time:

* Ace (code editor). A lot better than CodeMirror
* Articles. This in turn installs a load of extras it needs
* Big Brother. A Google Analytics dashboard widget.
* FormIt. For form sending/validation, etc
* getResourceField. Useful for grabbing one bit of data from one single page. Kind of get resources, but blinkered.
* getResources. Useful for all kinds of things.
* GoogleSiteMap. Generates XML sitemaps for Spiders, etc
* [JSONDerulo](http://modx.com/extras/package/jsonderulo23). Pulls in and outputs JSON feeds for common social feeds.
* phpThumbOf. Crop, thumbnail and alter images automagically.
* SimpleSearch. For use on the Page Not Found error page.
* UltimateParent. Searches up branches to find parent pages at a chosen level. I use this for the bodyClass placeholder mostly.
* Wayfinder. Makes menus easy.