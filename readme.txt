=== SEO BreadCrumb ===
Contributors:redsnow_
Tags: breadcrumb, topic path, microdata
Requires at least: 3.1
Tested up to: 3.6
Stable tag: 1.0.0

Adds the function to display breadcrumbs navigation.

== Description ==
This plugin adds the function to display breadcrumbs (topic path) navigation. You can use display styles, lots of parameters of styles and original plugin hooks of breadcrumbs navigation, and you can customize navigations flexibly.
Forked "[Prime Strategy Bread Crumb](http://wordpress.org/plugins/prime-strategy-bread-crumb/ "WordPress breadcrumb plugin")" 

= Examples =
**Default**<br />
Template Tag<br />
`
<?php if (function_exists('bread_crumb')) bread_crumb(); ?>
`
Output Sample<br />
`
<div id="breadcrumb" class="bread_crumb">
    <div itemscope itemtype="http://data-vocabulary.org/Breadcrumb">
        <a href="http://www.example.com/" itemprop="url">
            <span itemprop="title">Home</span>
        </a>  &gt; 
    </div>
    <div itemscope itemtype="http://data-vocabulary.org/Breadcrumb">
        <a href="http://www.example.com/?cat=2" itemprop="url">
            <span itemprop="title">Seminar</span>
        </a>  &gt; 
    </div>
    <div itemscope itemtype="http://data-vocabulary.org/Breadcrumb">
        <a href="http://www.example.com/?cat=4" itemprop="url">
            <span itemprop="title">Tokyo</span>
        </a>  &gt; 
    </div>
</div>
`

**List types**<br />
Template Tag<br />
`
<?php if (function_exists('bread_crumb')) bread_crumb('type=list'); ?>
`
Output sample<br />
`
<div id="breadcrumb" class="bread_crumb">
    <ul>
        <li itemscope itemtype="http://data-vocabulary.org/Breadcrumb" class="level-1 top">
            <a href="http://www.example.com/" itemprop="url">
                <span itemprop="title">トップページ</span>
            </a> &gt; 
        </li>
        <li itemscope itemtype="http://data-vocabulary.org/Breadcrumb" class="level-2 sub">
            <a href="http://www.example.com/?cat=2" itemprop="url">
                <span itemprop="title">Seminar</span>
            </a> &gt; 
        </li>
        <li itemscope itemtype="http://data-vocabulary.org/Breadcrumb" class="level-3 sub">
            <a href="http://www.example.com/?cat=4" itemprop="url">
                <span itemprop="title">Tokyo</span>
            </a> &gt; 
        </li>
    </ul>
</div>
`
= Special Thanks =


== Installation ==

1. Upload SEO Bread Cumb plugin folder you downloaded to the plugin directory.
2. Go to the plugin menu of Admin, and activate "SEO Bread Crumb" plugin.
3. Add a template tag "bread_crumb" of page navigation to the place where you would like to display breadcrumbs navigation in your theme. See below about parametes you can specify by template tags.

= Parameters =

**type**<br />
If you specify "string", output strings instead of list.
Default: list

**home_label**<br />
Texts displayed on front page.
Default: home

**search_label**<br />
Texts displayed on search results.
Default: Search Results of "%s" (%s : search strings)

**404_label**<br />
Texts displayed on 404 page.
Default: 404 Not Found

**category_label**<br />
Texts displayed on categories.
Default: %s (%s is a category label.)

**tag_label**<br />
Texts displayed on tags.
Default: %s (%s is a tag label)

**taxonomy_label**<br />
Texts displayed on taxonomies.
Default: %s (%s is a taxonomy label)

**author_label**<br />
Texts displayed on authors' page.
Default: %s (%s is author's name)

**attachment_label**<br />
Texts displayed on attachments.
Default: %s (%s is an attachment's name)

**year_label**<br />
Texts displayed on Yearly Archives.
Default: %s (%s is a year)

**month_label**<br />
Texts displayed on Monthly Archives. 
Default: %s (%s is monthly-display-type specified on date format)

**day_label**<br />
Texts displayed on Daily Archives.
Default: %s (%s is a day)

**post_type_label**<br />
Texts displayed on custom post type archives.
Default: %s  (%s is custom post type label)

**joint_string**<br />
If you specify "string" on type, strings between texts.
Default: " &amp;gt; " ( > )

**navi_element**<br />
Name of wrapper elements. You can select div or nav.
Default: none (no element)

**elm_class**<br />
Name of wrapper class. If no wrapper element and type is "list", name of "ul" class will be displayed.
Default: bread_crumb

**elm_id**<br />
Name of wrapper id. iF no wrapper element and type is "list", name of "ul" id will be displayed.
Default: none (no id)

**li_class**<br />
Name of class added to li if type is "list".
Default: none (no class)

**class_prefix**<br />
prefix added to each class.
Default: none (no prefix)

**current_class**<br />
Name of class added to breadcrumbs navigation on current page where you see.
Default: current

**indent**<br />
Number of tab indent. Default: 0

**echo**<br />
Output or not. Default: true (output).
If you specify 0 or false, return values as PHP.

**disp_current**<br />
current page Output or not. Default: false (not).
If you specify 0 or false, return values as PHP.

== Changelog ==
= 1.0.0 =
* Opening to the public.

== Screenshots ==
1. Output Sample of a breadcrumbs navigation

== Links ==
