Participant Center Reset
==============================
The goal behind this project is to apply a more logical and editable workflow to Charity Dynamic's PC reset. Ideally, web devs could use this more default version as the jumping off point for additional customizations, such as circular progress bars, etc.

##Setup
Most up-to date reset in folder 16.1.1. 2 versions are set up
* default_pc - this includes basic responsive reset and is meant to be a plug and play solution for non-custom PCs.
* custom_pc - this includes custom thermometer, badges, and 1-column layout. This version should be good as a jumping off point for more custom projects.

To get started, first copy the folder of the reset you want to use and place in your projects directory.

The reset was created using SASS and build tools for compiling purposes (both Grunt and Gulp workflows are set up, pick your poison), so you will need to have [Node](https://nodejs.org/en/) and Ruby (Mac users have this automatically, [PC folks go here](https://www.ruby-lang.org/en/documentation/installation/) installed on your machine. Here is some basic documentaiton on setting up [Gulp with SASS](https://travismaynard.com/writing/getting-started-with-gulp) or [Getting Started With Gulp](https://markgoodyear.com/2014/01/getting-started-with-gulp/)

[Install SASS](http://sass-lang.com/install)

Install gulp globally (if you have never done so). If these are already on your machine then no need:

	$ npm install -g gulp

Navigate to the folder where you placed the copy of the reset in your project directory:

	$ cd my-project/default_pc

Install gulp and the neccesaary dependencies locally:

	$ npm install --save-dev gulp gulp-ruby-sass gulp-autoprefixer gulp-minify-css gulp-rename gulp-scss-lint

To start gulp compiling and watching tasks type: 

	$ gulp


##Updating CSS for specific projects
Just update variables file in sass/theme directory. Here you can update font stack, font sizes, branded colers and margins. For more customizations than just basic styles you will need to either update the other core SASS files or create a override file and add its reference to the bottom of the custom.scss file

##Adding CSS
When you save any changes to a sass file will gulp is running it will compile it into css in the dist/styles folder. Use the minified version and ftp it up to the client's server. I suggest adding it to the Particpant Center folder you created in Luminate. Once this file is on hte server, you can inlcude it in the custom CSS file by adding @import into the Custom Styles section under Related Actions in the PC:

@import url('https://secure3.convio.net/cdbox/defaultResponsiveV16/css/custom.min.css?v=[[S55:0:10000:5]]")

##Front End Examples
Both examples can be accessed using westest as username and password.
* [Default PC](http://cdbox.convio.net/site/TR?fr_id=2860&pg=entry)
* [Custom Baseline PC](http://cdbox.convio.net/site/TR?fr_id=2990&pg=entry)
#   R e s p o n s i v e - P a r t i c i p a n t - C e n t e r  
 