# Yii Combined Pager

**This project ABANDONED, because I don't code in Yii1 anymore! There is no wiki, issues and no support. There will be no future updates. Unfortunately, you're on your own.**

This is an extremely simple extension that is combining both CListPager and CLinkPager in one, allowing your users to select page of CGridView they want to go to by either clicking on a page button (CLinkPager) or selecting page from a drop down list (CListPager).

_Please note: This extension was created for a specific purpose, not for a public domain, so you might find some changes in its code that do not necessary will suit your needs. There are some fixes to some things in base classes that I found wrong (for example - making disabled buttons by only changing their class, but still allowing user to click them), but you may disagree with me. In that case, fill free to drop any additional code out of original extension._

There are some Polish texts hard-coded into this extension. You need to throw them away or change them to use Yii:t for translating purposes. I know that this is a very bad manner and sorry that I wasn't able to do this myself, but I haven't got enough time for doing this when developing this extension.

Unfortunately, do to above circumstances, symbol used to separate CLinkPager from CListPager (mdash) is also hard coded, you have to change it manually.

## Requirements

Since this is a descent from a standard paging class, you do need only framework, even with a very old version of it.

## Usage

This is a standard paging component so to use it in a very base manner, all you have to do, is to extend your CGridView configuration with the following line:

~~~php
'pager'=>array('class'=>'CombinedPager')
~~~

Yii, of course must be informed to load proper extension, so you can either add a line like this before your CGridView widget definition:

~~~php
Yii::import('ext.CombinedPager.CombinedPager');
~~~

(providing correct path to the place, where you unpacked this extension.

This is a good approach, if you are using only one or just a few CGridViews with this paging component. If tyou have them more, it is better to force Yii to autoload this extension upon startup by adding following line to your application configuration:

~~~php
//Autoloading model and component classes
'import'=>array
(
        'application.models.*',
        'application.components.*',
        'application.extensions.*',
        'ext.CombinedPager.CombinedPager'
),
~~~

Since this extension descents from CLinkPager, you can use with it any configuration, you would normally use with CLinkPager. For example:

~~~php
'pager'=>array
(
        'class'=>'CombinedPager',
        'maxButtonCount'=>25,
        'header'=>''
)
~~~

**This project ABANDONED, because I don't code in Yii1 anymore! There is no wiki, issues and no support. There will be no future updates. Unfortunately, you're on your own.**
