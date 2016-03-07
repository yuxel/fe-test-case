There are 2 PSD files in zip; one for desktop, one for mobile responsive design

Lets keep desktop design on resolutions >= 960px and mobile version < 960px

on desktop design:
* there is a logo at top center, which should be a link
* signin/register etc links at top right (which are helvetica)
* centered category links below them which are RopaSans (https://www.google.com/fonts/specimen/Ropa+Sans)
* a search input, which has a "search" icon at right, and have a dropdown menu
    - if the input's length is >= 3, then you should open this dropdown (you can just show it without an effect) and send request to http://test.sonsuzdongu.com/query.php?keyword=[KEYWORD HERE] . ie: http://test.sonsuzdongu.com/query.php?keyword=skirt
    - this is a mock service and it returns you the response about ~1 seconds, so its better to show a "loading.gif" in that dropdown. You can choose any loading.gif.
    - When response comes from server, put suggestion links, which are "terms" on response.
    - if the input's length is < 3 or the XHR result is an empty array you should kill all ongoing XHR requests and close the dropdown
* and an image carousel slider below this input field. you can use images from http://lorempixel.com/940/375/fashion/?someRandomStrings to fit in that place. And implement a carousel slider with these images. The design of this carousel (like arrows, and dots) are not so important at this level. We just want a working carousel. You can use any library/plugin you want.


on mobile design:
* there's a hamburger menu which wraps all navigation links at left top. Just wrap these links into hamburger menu. You dont have to make this hamburger menu work when we click on it. Just hide navigation elements and show an hamburger menu for this case.
* "your bag" link on desktop version becomes an icon at right top on mobile design.
* signin/register & stores comes after the logo
* search field comes after these links. Make sure that dropdown which you've implemented on desktop version to NOT WORK on mobile. So we should have just an input field on mobile. We have to prevent sending requests and dropdown menu to open on mobile version.
* and a responsive carousel below them.


In this test case, I want to see you to implement;

* design with valid/semantic HTML5 and SASS/Less. You can use any framework you want on JavaScript side (Angular, jQuery, etc). Include this framework with *bower*
* use grunt/gulp tasks to compile less/sass, combine them into one css
* use grunt/gulp tasks to combine javascript files into one js files
* logo, search icon, basket icon and hamburger menu icon (on mobile page) should be in "sprite" file. so, use grunt/gulp tasks to automate this process (see grunt-spritesmith for details)
* use a plugin for the image carousel and use bower to include this plugin
* document the code you've written with comments


Take your time to build this test case. You can send the result anytime you want. But please keep track time and tell us how much time you spent on this case.
