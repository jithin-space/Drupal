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

            
    
        
        
    


