[![Project Status: Inactive - The project has reached a stable, usable state but is no longer being actively developed; support/maintenance will be provided as time allows.](http://www.repostatus.org/badges/latest/inactive.svg)](http://www.repostatus.org/#inactive)

UnobfuscateJs
=============

jQuery plugin for defuscating obfuscated email addressess.

Usage in a ATK14 project
------------------------

UnobfuscateJs was originally developed for ATK14 Framework. In the ATK14 Framework there is a helper no_spam for distorting email addresses to prevents robotic scraping. The ObfuscateJs normalizes their appearance again.

Package installation:

    npm install --save unobfuscatejs

Include source file among vendor scripts in the project, e.g. using Gulp in gulpfile.js:

    var vendorScripts = [
      "node_modules/jquery/dist/jquery.js",
      "node_modules/bootstrap/dist/js/bootstrap.js",
      "node_modules/atk14js/src/atk14.js",
      "node_modules/unobfuscatejs/src/jquery.unobfuscate.js"
    ];

In the application script this should be added for every page:

    $( ".atk14_no_spam" ).unobfuscate( {
      atstring: "[at-sign]",
      dotstring: "[dot-sign]"
    } );
