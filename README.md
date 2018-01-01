# Drupal

Drupal is an open source web content management system that allows you to quickly and easily create simple to complex sites that span everything from a simple blog to a corporate site, a social networking site or virtually anything you can dream up.

What you can build with Drupal is only limited by your imagination and the time you have to spend with the platform.

Open source platform

Learning Drupal is like learning anyy new technology.


## Chapter1. Introduction to drupal

*  Content Management Systems
*  Drupal

    * Free and opensource CMS written in PHP
    * Creator Dries Buytaert (Dutch)
    * Main Module called Drupal Core
    * Developed and Maintained By Drupal Community
    * You can also a large number of add-on-modules depending on your use
* Drupal Core
   * Core represents the `engine` that powers a Drupal Based Website, along with a number of out-of-box features.
    * It covers the basic functionalities required for a CMS Platform

* Contributed Modules
    * Large number of addon modules that are classified into different categories.
    * check the compatibility with your drupal version before using.

* Drupal Themes
    * Drupal component that defines how the pages are structured and viewed
    * includes off-the-shelf themes and third party themes.

* Creating Content
    * add content
    * default content types 
        * article ( time sensitive)
        * basic page ( static like about us )
    * create your own content types as you wish

## Chapter 2. Creating and Managing Content

* Understanding the basics
    * content can be of any type like image,text,video,product description,news story , blog post, wiki entry
* Creating content in Drupal
    * create an article ( image + tags in addition)
    * tags should be separated by comma
    * alternative text is important b/c it is useful for person with visual disabilities
* Teaser and Full nodes
    * default 600 char in teaser (can change )
* Editing Content
    * Quick Edit option on home page( Explore)
    * Revision Settings (Try Reverting)
    * Menu Settings
        * provide a menu link
        * Parent menu -- <main navigation>
        * Weight < decides the ordering of menu items >
    * Comment Settings
        * Open / Closed
    * Url settings
        * override the default urls as aliases
        * start as /about ( will be displayed as the url there after)
    * Promotion options
        * promoted to front page
        * sticky at top of list ( make it always appear on top of lists)
    * Authoring Option
        * data published and author info
    * Deleting the content
        * automatically remove menu items too
        * save and unpublish if not completed
    * Previewing the content
    * Find Content
        * mainly use the content list page
        * bulk editing can be done there.
## Chapter 3 - Creating and Managing Users

* Users,Roles and Permissions
    * Anonymous and Authenticated Users
    * Roles are for Authenticated Users
    * Roles can be designed based on your application requirements
        * can be department specific
        * can be function oriented
        * can be for handling different section of the website
    * User can be assigned to none,one or more than one role
    * Permissions need to be assigned to roles
* User Accounts
    * Drupal has a default system admin user created at the time of installation
    * User account Creation
        * Only administrator can create accounts
        * Visitors can create account without admin approval
        * Visitors can create account but requires admin approval
    * Configuring User Account Settings
        * check the options @ configuration >> account settings
* Creating Roles
    * Manage >> People >> roles
* Assigining permissions
    * Manage >> People >> permissions
* Creating User Account
    * try both
    * admin approval requires email functionality implemented.(** not working ** )
    
## chapter 4 - Taxonomy

* Most Powerful but often misinterpreted functionality in Drupal
* Used to Categorize content into different sections. 
* Taxonomy Overview
    * Taxonomy in Drupal is divided into two General Capabilities
        * Tagging -- Simple 
            * free form, but subjective to synonym and spelling problem.
        * Structured Taxonomy
            * Admin needs to create all words for categorize
            * Authors simply select the terms from the list created by Admin
            * It can be hierarchial 
* Creating Vocabularies
    * Tag vocabulary is there by default
    * Manage >> Structure >> Taxonomy
    * Create a vocabulary and add terms
    * Display order can be varied depending on the weights assigned.
* Assigning a Taxonomy Vocabulary to a Content Type
    * requires site admin to make changes to the corresponding content type
    * eg Article Content Type
    * Manage >> Structure >> Content Types >> Article >> Manage Fields
    * Add Field >> Taxonomy term 
    * Enter label
    * Allowed Number of Values to unlimited
    * save
    * Customize the Field
        * Help Text, Required, Default value <none>,Reference Type < Default> , Vocabulary List -- select the vocabulary created 
        * only items in this list will appear
* Selecting a Taxonomy term When Creating Content
    * auto complete...( No dropdown found )
* Creating Human & Search Engine Friendly Lists
    * add aliases to taxonomy terms 
* Hierarchial terms
    * Use relations while creating terms
    * need a mechanism to show all items categorized as children terms while selecting parent term..not by default
* Assigning More than one vocabulary
    * Add a second field to the content type as done previous

## Chapter 5- Content Types

* Most powerful feature of Drupal is its ability to create custom content types
* We have article and basic page content types by default.
* Defining Custom Content Types
    * Drupal 8 core has the ability to create custom content types
    * First we have to decide in advance what all fields the custom content type will have.
    * Manage>>Structure>>Content Types
    * Add Content Type.
        * name, description
        * title field Label
        * preview, explanation
        * publishing options
            * published , not promoted to front page
            * enable create new revision
        * Display options
            * Display author name and date info --yes
        * Menu Settings
            * Where in the menus the new content type will appear
            * keep default settings
            * save and manage fields
    * Customizing your content type
            * it will have body by default..change its label
            * adding fields
                * eg start date
                * type date
                * allowed number of values 1
                * save
                * label,help text , required,def value
                * save
                * eg end date
                * eg event venue
                * type text(formatted,long)
    * Other Field Types
        * Radio Buttons
            * key|value
            * key1|value1
            * type List(Text)
            * Number of values 1 ( if >1  it will be for checkbox)
            * To display as a radio button instead of a dropdown 
                * manage form display >> widget >> checkbox/radio

        * Check Box
            * Same as Radio
        * Select List
            * radio / check box without any display change
        * File Upload
            * Enable Display Field yes
            * Files Displayed By Default yes
            * For getting a link to the file while viewing the content type
            * upload destination public ( default) / or its subdirectories
        
        * Image Upload
        * Numeric
        * Entity Ref Field ( if the field is another content type)
        * Term Reference Field ( able to include taxonomy terms)
        * Text Area
            * one or more paragraphs
            * full html, restricted html , basic html 

    * Formatting the input form For a custom content type
        * Mange Form Display 
    * Formatting the output of a custom content type
        * Manage Display
        * Custom Display Settings
            * How the content is to be displayed on other view modes like RSS, Search Index, Search Results rather than Default/Teaser modes.
    * new (custom) view modes
        * structure>>Display Modes>> View Modes >> 'content'
        * **not understood what is that 

## Chapter 6- Using Drupal Themes

* Visual Layout and Presentation of your new drupal site is defined through a Drupal Component called theme

* A Theme Defines
    * Colors used on the page
    * Fonts Used
    * Placement of Image and graphics that are common to all pages
    * The layout of the page

* Drupal themes developed using
    * HTML,CSS, JS
    * Tags from twig templating Engine
* Default available themes
    * bartik
        * fig 6.1
        * 17 regions for placing contents in the layout
        * understanding layout terms is important

* How a drupal theme works

        * you can have stock themes/commercial thems to download&use
        * also create your own thems either
            * from some starter themes like (zen)
            * from scratch ( eg book for this `pro drupal development` )
* Finding a new theme
    * Bartik,Seven,Stark,Classy ( in Drupal 8 core)
    * Design the layout first before searching for a theme
        * decide on 
            * header/banner
            * horizontal menus
            * left and right side bars
            * footer
            * responsiveness
        * go to www.drupal.org/project/project_theme
            * specify the parameter
            * core compatibility is important
            * select a theme from the search results
* Installing a new theme
    * two ways
        * using link / upload feature -- if ftp and permissions are correct
        * extracting and manually placing the folder under `themes`  directory
    * you have to install and set as default for making it active
    * Manage >> Appearance >> Themes

* Configuration Option
    * Manage >> Appearance >> Settings
    * shortcut icon or `favicon` used in tabs 
    * change logos
* Administration Theme
    * you can use a different theme for site administration if the default theme is not good while administering content
    * you can specify it in Appearance >> Administration Theme

* Great Designs / Organizational applications of Drupal 
    * can be found in the following link
    * dri.es/tag/drupal-sites

## Chapter 7 -- Menus

There are three basic mechanisms in Drupal to provide navigational capabilities to your site
    * Text links embedded in the content
    * Images and Buttons that redirect
    * Menus
Here we will learn how to use Drupal's administrators interface for creating and managing menus.

* Ordering From  the Menu

six menus in the bartik theme by default

    * Admininstrative Menu
    * Administrative SubMenu
    * User Account Menu
    * Main Navigation Menu
    * Tools Menu
    * Footer Menu

The process of creating menus requires following three activities

    * creating a menu
    * creating links of the menu
    * assign a region where menu should be placed.

* Creating a New Menu

    * Manage >> Structure >> Menus >> AddNew
    * Manage >> Structure >> Menus >> Edit Menu >> Add Link
    * it needs to added to a region inorder to make it visible
    * Manage >> Structure >> Block Layout 
    * Find a block and add the menu & upon saving new menu will appear in the specified block
    * Each theme ships with a number of inbuilt blocks and you can use them right now

* Adding an item to a Menu
    * link to an existing element on our site like  a  page , a content item, list of contents associated with a taxonomy term etc.
    * link to a page that is external to our site

    * Adding Content Item to a Menu

        * Best practice is to use content creation form ( or other element creation forms such as a panel page or a view).
        * adv. drupal automatically removes the item from the menu upon deleting
        * if you use menu administration form, you will need to remove manually.  Here you can create a menu item .
        * Adding a Content Item to a Menu

            * Use create/edit content option and provide a menu link option to create the link
        * Adding a menu item for an external page

            * Manage >> structure >> Menus >> Edit Menu
            * add link ( http://www.google.com for eg)
        

## Chapter 8 -- Drupal Blocks

* commonly called `widgets` that can be assigned to different regions
* Blocks
    * block is any self-contained piece of content.
    * blocks can be
        * come with built in core
        * come as contributed modules
        * create custom blocks from scratch
* Making Blocks appear on Page
    * Needs to be placed in regions
    * Spot the blocks in the figure 8.1 (excercise)
* Finding the List of available blocks
    * Manage >> Structure >> BlockList
    * Try to place available blocks in different regions
    * Rearranging Blocks
* Reassign & Deactivating Blocks
    * at the end of a block ( need scrolling)
* Configuring Blocks
    * eg who's online block
    * display title uncheck
    * which pages to show
    * which roles to show
    * <front>   for front page
* Using Blocks from Contributed Modules
    * download and enable and install the module (eg Wunderground )
    * it will automatically appear in the block list
* Creating Custom Blocks
    * you can write html and js code 
    * Manage >> Structure >> custom block library >> Add Custom Block
    * create a block and place it to an available region

## Chapter 9 -- Views

* Another killer module views
* Views provides an easy to use interface for selecting and displaying lists of content on your website.
* Examples--view textbook

* The views module

    * core module and enabled during installation
    * Creating your first view
        * Manage >> structure >> views
        * add new
        * A set of views already available.
        * parameters
            * View name
            * Description
            * View Settings
                * defines what type of content is going to be rendered by the view
                * select article in our case
                * tagged with -- leave-- for limiting the number of articles with some tags
                * sorted by -- Unsorted -- will cover later
            * Page settings
                * tick `create a page`
                * provide the ability to create a list of content and have that list available as a stand alone page on your site accessible through a URL
                * page title .. keep default
                * enter a URL path ..keep default
                * Display format -- unformatted list of teasers.
                *  Use a pager -- check
            * Block settings
                * allow our view to create a block
                * display format as an unformatted list of titles(linked) 
                * items/block to 3
                * use a page --uncheck
            * Save

    * configure the created view

        
        * edit the view created earlier
        * Displays List
        *  For this view, we have a Page and a Block displays
        * One of the powerful features of Views is the ability to have a single view render multiple displays
        * A single view can be used to create several different types of displays  that each display the views content in slightly different formats.
        * Let's get two display working
        * Page Display
        * list complete articles
        * Display Name-- change
        * Title -- change ( displayed at top of output generated by views for this display)
        * Format section -- we have the option to generate a list using different output formats like Grid,HTML list, Table,Unformatted list etc.. select unformatted list.
        * This page (override ) should be selected when changing the value to something other than "unformatted list".
        * show parameter defines how we want to handle the content that we are going to display.
        * Two most common options are Content and Fields
            * Content : Displays the complete entity
            * Fields :  Displays specific fields from the entity that you are rendering.
            * Here we select, Content and display content as teasers.( if we want full...select 'default')
        * FIELDS--no option since we use show 'Content'
        * Filter Criteria
        * Sort Criteria
            * add -- search title -- use `Content:title`
            * This page override --- Apply (this display)
            * specify the sorting order
            * expose this option to site visitors-- unchecked
            * check the preview
        * Every view display that is defined as Page must have a unique URL
            * specify the path ( /all-articles)
        * Menu Fields
            * add it to the "Main Navigation"
            * No menu >> Normal Menu entry >> entr tile & description
            * select "Main Navigation"
        * Who can view
            * Access Restrictions ( None,permission,Role)
            * Keep default
        * Header
            * enables you to add several things to the top of the view
            * eg..an introductory para,another block,output of another view or several other elements.
            * add>> Global: text area -- for intro para
        * Footer
            * Similar to Header
        * No Results Behaviour settings
        *  Use pager for pagination
        * Advanced
            *Contextual Filters
            * powerful configuration option that allows you to utilize values passed in the URL to filter content that is returned by the view.
            * % -- for url parameter
            * single view can be used to display any article by any category in our taxonomy vocabulary.
            * not using now
            * Relationships
            * combine two different content types according to a criteria.
            * Event Content Type & Venue content type
            * not using now

            * save and test your results.

        * Block Display
        * Edit the block display of the newly created view
        * Display Name -- Recent Articles Block
        * Title ----
        * Format --- Unformatted List
        * Show --- Fields
        * Fields --- title
        * Filter Criteria --leave both ( Content Publishing Status & Content Type criteria ).
        * Sort Criteria
            * add --- search Date -- use `Content: Post date`o            * apply (this display)
            * Sort descending
        * limit the number
            * check to make sure that the value for User pager is set to `Display a specified number of items | 3 items`
        * Save
        * Place the block in a region

    * Filtering
        * list articles tagged with a specific tag--- Behind the scenes, Drupal is using Views to generate this list.
        * we can do that here from our all-articles view using filtering
        * add a new filter criteria
            *  Content: Tags (field_tags)
            * Apply (this display ) for all articles page
            * Select the type of interface we wish to provide
                * Dropdown
                * Autocomplete field
            * Select dropdown , Save and Continue
            * configure the fillter and how it will work
                * Expose this filter to visitors , to allow them to change it
                * Filter type to expose --- Single filter
                * Label- Select one or more tags
                * Operator -- Is one of
                * Allow multiple selections
                * save-- test the output

    * Advanced view output
        * Creating RSS Feeds
            * Create a new display for our current view
            * display type--- Feed
            * URL --- rss/all-articles
        * Creating Tables
            * new display-- blocks type
            * Format-- Table
            * Sortable option for each fields
            * Grouping Field Nr.1 -- group results
            * Add other fields too ( Add button in fields section )

    * Views Add-on Modules
            * Views Slideshow
            * Calendar
            * JCarousel
            * Draggable views
            * GMap
            * Views data export
            * Many more...


## Chapter 10 -- Creating Pages

* Foundation for creating pages
    * Each theme provides its set of regions for placing the content
    * Here we use the regions provided by the default bartik theme
    * You can also use starter themes suchas Zen and design the exact layout that you need
    * What we do here
        * Create an article and note down its url for future use
        * we need to display a custom  block that need to be appear only on a specific page 
            * Mange >> Block Layout
            * Add custom block ( DrupalCon 2015 Los Angles )
            * add description and body 
            * save
            * This block to be placed in Featured Top Region for only the article created above
            * place the block
            * show for listed pages add ( /node/8 -- url noted above)
            * save and view the page

* Creating Landing Pages            
                
    * several pieces of content and several blocks eg. Home page
    * what we do here
        * create a basic page content with just title as a landing page
        * create two taxonomies and terms inside it
            * Event with DrupalCon Los Angels as term
            * Subject with Things to do & restaurants as terms
        * add custom fields to the article content type so that user can enter articles about `things to do` in `DrupalCon Los Angles`
            * Structure >> Content types >> Manage Fields for article content type
            * add two fields of type entity reference and specify the respective vocabularies in the field settings.
            * check with the screen shot in the textbook

        * create a view that //filled later

            * add view ( Name articles ..article type to render )
            * save and edit
            * first display
                * teaser list of latest five articles
                * add display of type block
                * Display name -- Latest articles
                * Title--make it none by editing to empty
                * Fields -- content-- and in teaser mode
                * Use pager -- Display specified number of items | 5
                * save
            * Second display
                * Featured Article block -- randomly select an article and display full article on the page
                * block display..this block override
                * show settings to teaser
                * Sort criteria -- random of global category
                * delete the default post date (desc ) sort criteria
                * Use pager : items 1 
            * assign the two blocks that we created to the page what to do around los angels
                * assign Featured article to sidebar second
                * show for listed pages ( /node/8 )
                * assigne Latest articles to content region
                * save
            * add three additional featured article blocks by creating three additional articles for restaurants around Los Angels
                * add restaurants to subjects vocabulary
                * create three contents ( Article type ) with fields restaurant 
                * upload each of them an image of the restaurants
                * create a new block in the article view
                    * display name  -- featured restaurant 1
                    * blank out the existing title
                    * show -- fields
                    * add field link click -- and select -- Content: Image Appears in : article
                    * This block override
                    * Uncheck the create a label box
                    * link image to select list -- Content
                    * apply this display
                    * filter criteria -- search for term ( Content: Has taxonomy term ) -- select Subject -- selection type -- Dropdown  -- check Show hierarchy in dropdown"
                    * apply..seletct restaurants next -- apply (this display)
                    * Use pager -- items 1
                    * save button and new block is created.
                * Add two more blocks
                    * use duplicate feature
                    * change the display name to Featured restaurant 2
                    * use pager -- offest 1
                    * use pager -- offset 2 to third block
                    * save
            * place the blocks in Featured bottom first,second and third regions respectively.
            * submit to see the result.

## Chapter 11 -- Drupal Modules

* Finding Contributed Modules
    * go to drupal modules page
    * select a module from specific category
    * also check this site drupalmodules.com
* Downloading and Installing a Module
    * three ways
    * Downloading the module files to your server
        * Download the tar/zip file
        * upload/move it to servers module directory
        * unzip it there
        * go to drupal administration page to enable the module ( Manage >> Extend )
    * Using the Install new module feature
        * copy the tar/zip url from web
        * paste it in after clicking on Install new module
        * click on install module
    * Using Drush
        * will be covered in later chapter
* Configuring Modules and Setting Permissions
    * Some modules may have some configurations and settings
    * Better to check both configuration and permission upon installing a module
        * Manage >> People >> Permissions
        * Manage >> configuration >> (find something related to the module eg . google analytics ,or search & metadata link )
        * Read the configuration settings of the respective modules

* Enabling a Module -- Manage >> Extend
* Upgrading a Module -- Manage >> Reports >> Available Updates
* Uninstalling a Module 
    * Extend >> list / update / uninstall
    * remove the file from modules directory if no caution or dependency
    * depency can be found in the module's .info.yml file

* Top 11 Modules

    * views ( integrated into drupal 8 core )
    * Layout ( handling regions as you wish )
    * Rules ( eg sending an automated mail upon an event )
    * Display suite ( Drag and drop interface for content placing )
    * Nicemenus ( single level menus with special dropdown and flytext handling)
    * Pathauto ( automatically generates search engine friendly urls)
    * Webforms ( able to create and give form processing functionalities)
    * Backup and Migrate ( automatic backup of drupal database / data )
    * Date ( Date and calendar etc)
    * Library ( Useful when  using external js libraries )
    * Drupal Commerce ( ubercart / Drupal commerce )

    

# Chapter 12-- Anatomy of a Module

* Your first drupal module
    * that just displays hello world
    * step1: creating the Module's director
        * under modules>>custom>>hello (folder)
    * step2: Create the Module's info file
        * hello.info.yml
        * meta data ---displays at extends page
        * name,type,description,package,version,core
    * step3: Create the Module File
        * hello.module
        * function hello_hello_world (convention)
        * funtion t() -- translates if multilingual
    * step4: Create the Module's Routing File
        * symfony based
        * MVC & Routing Model
        * help.routing.yml
            * path,defaults,requirements
    * step5: Create the Module's Controller
        * PSR-4 & use of namespaces
        * src/Controller inside main module folder
        * within that HelloController.php
        * syntax
    * save all files & goto extends page & enable the module
    * /hello -- you could see the page (** I couldn't find anything **)
    * all modules follows the same convention & try to look into the core of other modules
                        
            






















## Installing Drupal in Debian Stretch

### Install Requirements

    * update the repository
        * `apt-get update`
    * install apache and php7.0 dependencies 
         * `apt-get install apache2 php7.0 php7.0-common php7.0-gd  php7.0-mbstring php7.0-xml`
    * install composer ( php dependency manager )
        * apt-get install composer
    * install database
        * apt-get install mysql-server php7.0-mysql phpmyadmin 
    * Download Drupal core using Composer
        * cd /var/www/html
        * composer create-project drupal-composer/drupal-project:8x-dev <directory_name> --stability dev --no-interaction
        * //will download core into the folder specified
    * configure apache2
        * sites-available/000-default.conf
            DocumentRoot /var/www/html/<directory>/web
            <Directory /var/www/html/<directory>/web >
                AllowOverride All
            </Directory>
        * a2enmod rewrite
        * chown -R www-data:www-data /var/www/html
    * configure database
        * mysql -u root -p
        * create user 'admin'@'localhost' identified by 'space123';
        * grant all privileges on *.* to 'admin'@'localhost' with grant option;
        * flush privileges;
        * exit
        * mysql -u admin -p
        * create a database for drupal using phpmyadmin
    * complete drupal installation
        * go to localhost and complete installation

            
    
        
        
    


