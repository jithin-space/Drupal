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

            
    
        
        
    


