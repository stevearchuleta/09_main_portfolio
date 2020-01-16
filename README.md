# portfolio_update

Project Title:
Updated Portfolio
Week 13 of 24 (Bootcamp HW Assignment)
Second Revision of Personal Portfolio

Getting Started:
   This is a static HTML template. It doesn't have any admin/back-end panel. It is created for beginning developers who know HTML.

Prerequsite:
   Use IDE or Text Editor; HTML5 & CSS3 for customization.

Folder Structure:
   Ashton: Main (root) folder
   css: Template style.css and style.scss and other plugins CSS files.
   fonts: Font Awesome (icons), et-line (icons), and font files.
   img: Images that are used in the template.
   js: Template scripts.js and other JS plugins.

Layout:
   Navbar
    Header
    Section Content
    Footer

~ NavBar Nav-scroll is used to mount the navigation to the top of the page when scrolling. Flex styling was used to vertically center the navigation. 

~ Header is the wrapper for the header content - this includes all the banner or slider content.

~ Section tag gives padding to both top and bottom.



Basic Customization
How To Edit Files

You can use whatever text editor you like, even default Text Editor in the OS. But we recommend to use the one with th syntax highlighting such as:

    Sublime
    Notepad++

How To Change Fonts

    If you are not satisfied with the default font, you can choose from hundreds ones from the Google Fonts. After you are happy with the selected font, click SEE SPECIMEN. You'll be redirected to to font detail. Then click Select this font. Popup window will show with text "1 Family Selected" - click it. Then you can customize your selection by clicking Customize. When you are done copy the text in import tab.
    For example @import url('https://fonts.googleapis.com/css?family=Poppins:300,400,500,600,700,800,900');
    Then open the helper.css file to change fonts and find the @import... element which loads the Google font and place your copied code.
    Final step is to change the font family in the helper.css file. Find body tag on the beginning of the file and font-family inside. Go back to Google Fonts page where you have chose your font and copy the line placed in the Specify in CSS. In this example it is font-family: 'Poppins', sans-serif;

How To Change Colors - Simple Way

There are two methods how to change the main color. 1st Just by replacing the HEX color value in the style.css (simple) and 2nd by installing koala or you can choose another compiler as well (advanced). Here is the simple way.

Let say, that you want to change the default red color to blue one:

    Add template to the koala
    Set style.sccs path to output pathstyle.css
    Now open the style.scss in your text editor, find Replace or Find and Replace function
    As original text enter the red color #ff0000 (template default color)
    As Replace with enter HEX value of blue color #0000ff

Font Awesome Icons

Font Awesome includes more than 900 icons that can be easily used on your site. For example you want the download link with the PDF icon.

    Go to Font Awesome Icons gallery and find the one you need. I our example it is file-pdf. Click the detail, then find and copy <i class="fas fa-file-pdf"></i>.
    Place the copied line to your link: <a href="file.pdf"><i class="fas fa-file-pdf"></i> Download File</a>
    Final result: Download File

Bootstrap Utilities

Template is using Bootstrap utilities very often. We think that it is better solution as writing all styles for every element into CSS file. It makes the style.css smaller and it is more flexible. You can find more about Bootstrap Utilities.
Advanced Customization
JavaScript

JavaScript (JS) files/plugins are located in the /js folder and in the HTML file they are called using <script></script> code. All JS files are located at the bottom of the HTML file. scripts.js file is the template's JS file that includes scripts for running other plugins.

Note: You will need to modify only scripts.js file. Read more about it in the Plugins section.
Styling the Background

You can easily change the color of the background without editing of the CSS/SCSS files. This can be applied to whole section or particular element as well.
Background Color

To change the background color of the element use bg-* class.

Example: Change the background color of the section to black.

<section class="bg-black">
<h2>This Section is Black</h2>
</section>

Background Image

To add the background image of the element. You can also add an opacity using opacity-medium

Example: Background image with the 75% opacity:

 <section class="cover-background" style="background-image: url('image path');">
     <div class="opacity-medium bg-extra-dark-gray"></div>
     <div class="container"><!--content--></div>
 </section>

Important! You can also change the opacity and color with changing of opacity-light | opacity-medium | opacity-full-dark | bg-extra-dark-gray | bg-black | bg-white classes.
Background particles

Add the background particles effect into an element. Use <div id="particles-js"></div>

Example: Background image with the particles.

 <section class="cover-background" style="background-image: url('image path');">
        <!-- particles -->
        <div id="particles-js"></div>
        <div class="container"><!--content--></div>
 </section>

Parallax Background

Easy background parallax effect is done using data-background. You can also change the speed and overlay of the parallax effect and overlay by adding data-stellar-background-ratio="0.5" and data-overlay-dark="6".

<div class="bg-img no-transition" data-overlay-dark="6" data-background="image path" data-stellar-background-ratio="0.5">
        <div class="container"><!--content--></div>
</div>

Important! You can also implement particles effect in the parallax background as well with adding of <div id="particles-js"></div>
Form

Template uses Bootsrap form structure and brings some own styles.
Contact Form

Ashton comes with working email. You can use them for contact, subscribe or other forms that will collect the user's email address and send it to your receiving one.

Important! Contact form must have action="bat/rd-mailform.php"

Note: It is better to test email sending on live server. It does not work on a local machine.
Setup a path to PHP file

In your <form> element you need to specify a path to the .php file that will handle the email.

<form method="post" action="bat/rd-mailform.php" class="mailform off2">
    <input type="hidden" name="form-type" value="contact">
    <div class="row">
        <div class="col-md-4">
            <input type="text" name="name" placeholder="Your Name:" data-constraints="@LettersOnly @NotEmpty">
        </div>
        <div class="col-md-4">
            <input type="text" name="phone" placeholder="Telephone:" data-constraints="@Phone">
        </div>
        <div class="col-md-4">
            <input type="text" name="email" placeholder="Email:" data-constraints="@Email @NotEmpty">
        </div>
        <div class="col-md-12">
            <textarea name="message" rows="5" placeholder="Message:" data-constraints="@NotEmpty"></textarea>
        </div>
        <div class="mfControls col-md-12">
                <button type="submit" class="butn">Sumbit comment</button>
        </div>
    </div>
</form> 

Note: Necessary files are js/mailform, bat folder and css/plugins/mailform.css.
Setup a Receiving Email Address

You have to setup your own email address for email receiving. As a default it is addyour@emailhere and it is located in the bat/rd-mailform.php.
How to change the address:

Go to bat/rd-mailform.php and find $recipients = 'addyour@emailhere'; and change the address to your own.
Plugins

Here is the list of the JS plugins used in the template. Usually they are loaded from /js folder.
Important! Every JS plugin loaded from /js must be called BEFORE the scripts.js

<script src="js/jquery.min.js"></script>

<!-- Plugins from /js -->

<script src="js/scripts.js"></script>

Owl Carousel

This plugin is used for creating slider/carousels from list of images or even HTML elements. Carousel must be wrapped in owl-carousel class.

Example: Carousel with 3 visible slides, 30px margin, auto play, infinite loop and 5s pause.

<div class="owl-carousel owl-theme">
    <img src="img/1.jpg">
    <img src="img/2.jpg">
    <img src="img/3.jpg">
</div>

Javascript (file path - /js/scripts.js)

    $('.owl-carousel').owlCarousel({
        items:3,
        loop:true,
        margin: 30,
        mouseDrag:false,
        autoplay:true,
        smartSpeed:500
    });

All attributes you can use with owl-carousel

    items number of items in carousel. 1 item for fullscreen carousel
    nav show or hide navigation arrows. Default: 0
    dots show or hide navigation dots. Default: 0
    center center carousel. Default: 0
    loop infinite loop. Default: 0
    auto-width carousel will move according the slides width. Default: 0
    autoplay carousel will play automatically. Default: 0
    autoplay-timeout pause between slides in milliseconds. Default: 5000
    auto-height height of the carousel will automatically change according the slide height. Default: 5000
    fadeout fade effect between transitions. Default: 0

Utilities

Template is using Bootstrap Utilities along with custom ones. Here is the list of available custom utilities:
Borders

    border-all border for all side
    border-width-1 border width 1px
    border-color-white border color white
    border-none removes any border
    border-radius-5 5px border radius
    border-dotted border style
    border-top border on top
    border-right border on right
    border-bottomborder on bottom
    border-left border on left

Font Size

    font-size11 to font-size20 11px to 20px font size
    font-size22 to font-size50 22px to 50px font size - Just even font size
    font-size100 100px font size
    font-size130 130 screen font size
    md-font-size11 to font-size20 medium screen 11px to 20px font size
    md-font-size22 to font-size50 medium screen 22px to 50px font size - Just even font size
    md-font-size100 medium screen 100px font size
    md-font-size130 medium screen 130 screen font size
    sm-font-size11 to font-size20 small screen 11px to 20px font size
    sm-font-size22 to font-size50 small screen 22px to 50px font size - Just even font size
    sm-font-size100 small screen 100px font size
    sm-font-size130 small screen 130 screen font size

Important! If you add md and sm prefix before the class it will be consider for medium and small screens.
Font Weight

    font-weight-100 font weight 100
    font-weight-200 font weight 200
    font-weight-300 font weight 300
    font-weight-400 font weight 400
    font-weight-500 font weight 500
    font-weight-600 font weight 600
    font-weight-700 font weight 700
    font-weight-800 font weight 800
    font-weight-900 font weight 900

Font Color

    text-white white text color
    text-black black text color
    text-pink-color pink text color

Divider

    divider-full divide the items in a list with 1px border

Margin

    margin-one-all 1% margin to all side
    margin-10px-all margin 10px to all side
    no-margin remove margin
    no-margin-top remove margin from top
    no-margin-right remove margin from right
    no-margin-bottom remove margin from bottom
    no-margin-left remove margin from left
    margin-10px-top margin 10px top
    margin-10px-right margin 10px right
    margin-10px-bottom margin 10px bottom
    margin-10px-left margin 10px left
    margin-10px-lr margin 10px left and right
    margin-10px-tb margin 10px top and bottom
    md-margin-10px-all for medium screen - margin 10px to all side
    sm-margin-10px-all for small screen - margin 10px to all side

Important! If you add md and sm prefix before the class it will be consider for medium and small screens.
No Gutters

Removes padding from col*. Apply on row class

    no-gutters removes padding from cols

Overflow

    overflow-hidden overflow hidden
    overflow-visible overflow visible
    overflow-auto overflow auto
    md-overflow-hidden medium screen overflow hidden
    md-overflow-visible medium screen overflow visible
    md-overflow-auto medium screen overflow auto
    sm-overflow-hidden small screen overflow hidden
    sm-overflow-visible small screenoverflow visible
    sm-overflow-auto small screen overflow auto

Position

    position-inherit position inherit
    position-relative position relative
    position-absolute position absolute
    position-fixed position fixed

Important! If you add md and sm prefix before the class it will be consider for medium and small screens.
Opacity

    opacity1 .1 opacity
    opacity2 .2 opacity
    opacity3 .3 opacity
    opacity4 .4 opacity
    opacity5 .5 opacity
    opacity6 .6 opacity
    opacity7 .7 opacity
    opacity8 .8 opacity
    opacity9 .9 opacity

Padding

Although, Bootstrap has p*-0 utility, but sometimes you need to remove just one side of padding and it is not possible with the same Bootstrap's padding utility.

    padding-one-all 1% padding to all side
    padding-10px-all padding 10px to all side
    no-padding remove padding
    no-padding-top remove padding from top
    no-padding-right remove padding from right
    no-padding-bottom remove padding from bottom
    no-padding-left remove padding from left
    padding-10px-top padding 10px top
    padding-10px-right padding 10px right
    padding-10px-bottom padding 10px bottom
    padding-10px-left padding 10px left
    padding-10px-lr padding 10px left and right
    padding-10px-tb padding 10px top and bottom
    md-padding-10px-all for medium screen - padding 10px to all side
    sm-padding-10px-all for small screen - padding 10px to all side

Important! If you add md and sm prefix before the class it will be consider for medium and small screens.
Shadow

    box-shadow box shadow
    box-shadow-light light shadow
    box-shadow-dark dark shadow
    box-shadow-large large shadow

Width

    width-10px 10px width
    width-10 10% width
    md-width-10px medium screen 10px width
    md-width-10 medium screen 10% width
    sm-width-10px small screen 10px width
    sm-width-10 small screen 10% width

Important! If you add md and sm prefix before the class it will be consider for medium and small screens.
Z-Index

    z-index-1111 z-index 111
    z-index-111 z-index 111
    z-index-1 z-index 1
    z-index-2 z-index 2
    z-index-3 z-index 3
    z-index-4 z-index 4
    z-index-5 z-index 4
    z-index-0 z-index 0
    z-index-minus2 z-index -2

Other Utilities

    no-letter-spacing no letter spacing
    letter-spacing-1 letter spacing 1
    letter-spacing-2 letter spacing 2
    letter-spacing-3 letter spacing 3
    letter-spacing-4 letter spacing 4
    letter-spacing-5 letter spacing 5

    display-block display block
    display-none display none
    display-inline-block display inline block
    display-inline display inline
    display-inherit display inherit
    display-table display table
    display-table-cell display table cell

Credits

Template is using third party plugins. Here is the list of third party plugins:
Third Party Plugins (Attribution)

    jQuery (MIT License)
    Mailform (MIT License)
    PHP Mailer (GNU Lesser General Public License)
    Animate CSS (MIT License)
    Bootstrap (MIT License)
    Fontawesome (MIT License)
    Magnific Popup (MIT License)
    OwlCarousel (MIT License)
    scrollIt (MIT License)
    Isotope (MIT License)
    Counterup (GNU Lesser General Public License)
    Parallax (MIT License)
    jQuery Appear (MIT License)
    Particles (MIT License)


______________________________________________________________________________________________________

Week 13 of 24 (Bootcamp HW Assignment)
Overview

Now that you've had some practice with HTML and have a project to share, you'll be updating your portfolio page and other materials to build toward being employer competitive.

If you are opting out of career services, this is still a required assignment. Part of being a web developer means being a part of a community. Having a place to share your projects is necessary if you're applying for jobs, but is still critical on your journey as a developer.


Before you Begin



Pin some repos that you want to share


Navigate to your GitHub Profile

Click "Customize your pinned repositories"
Click the "Repositories you contribute to" checkbox (this will allow you to "pin" Project 1 even if you aren't the "owner")
Click the checkboxes for your project and 2-3 homework assignments that you would like to share
Make sure each of these projects is deployed and add a link to the deployed project in their README files



Revisit your portfolio page


Open up your old portfolio page
Read through the rest of the homework requirements and decide whether you can update your existing portfolio page or if you want to start fresh now that you've had some more HTML/CSS practice (you may also want to change it to be a single page instead of multiple pages or you might even want to consider using a paid theme)





Required: Update your Portfolio Site -- Employer Ready

To receive a passing grade on this assignment, you should meet all of the content and design requirements listed below as well as all of the requirements listed under "Polish Your Portfolio & Github" in the "Employer Ready" section of the Employer Ready vs. Employer Competitive Checklist. These two sets of requirements should be mostly the same.


Content

Your updated site should have the following content:


Your name
Links to your GitHub profile & LinkedIn page as well as your email address and phone number
A link to a PDF of your resume

List of projects. For each project make sure you have the following:


Project title
Link to the deployed version
Link to the code on GitHub





Design

The content of your portfolio page is a lot more important than the aesthetics. That said, there are a couple basic requirements your portfolio page should meet:


Mobile-friendliness: you don't need advanced responsive styles, but you should ensure that your portfolio page is still readable on different screen sizes
Readability: make sure the font size is large enough to read, and that the colors don't cause eye strain.



Suggested: Update Portfolio -- Employer Competitive

To receive an "A" on this assignment, you should also meet the following requirements
to ensure your portfolio site will help you be employer competitive.


Competitive Content


At least 3 deployed projects

External content:


Update your LinkedIn with the projects you've worked on so far
Update the README for each project you linked to with a description of the problem,
how you solved it, and some information about your technical approach
Suggested: refactor some of your code from earlier assignments to make them more readable





Competitive Design

Unfortunately, this is where it gets a little bit subjective. Your site should look
"polished." Here are a few guidelines on what that means:


Mobile-first design: you should be proud to pull out your phone and share
your portfolio site with a friend, family member, or someone at a meetup.
Polish: choose a color palette for your site so it doesn't just look like
the default bootstrap theme or an unstyled HTML site.
Images: add a meaningful screenshot for each of your projects


If you want a slick-looking site, but don't feel good about your CSS skills,
check out CV, Resume, and Portfolio site templates on ThemeForest


