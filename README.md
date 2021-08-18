# Symfony based HTML video web app

- Objective: Finish the provided application skeleton to create a *responsive* web application based in the Bootstrap 4 framework and Twig templates. Don't be afraid to ask if you are stuck (instead of banging your head against the wall). Sometimes a small hint will get you far. 


-  Required tools / environment: Git command line tool, PHP 7.2.5 or higher, Symfony 5.0.4 (available for Linux, macOS and Windows here https://symfony.com/download), Node.js 10.15.3 or higher, Yarn 1.15.2 or higher

- Clone (not fork) Git repository from https://github.com/TechcastGmbH/video-app.git

- To access the application start the server on the commandline, then find the application with the address http://localhost:8000

```
    symfony server:start
```

- in case of an error such as "failed to open stream ... no such file or directory ... bootstrap.php" or a server error 500 run `composer install` (or `php composer.phar install`) in the application directory

- You can find some template skeletons in the directory "templates". Please note that Twig templates can use some mechanisms for including/extending other templates such as https://twig.symfony.com/doc/2.x/tags/extends.html. It makes sense to include styles and js in the base template and extend the other two templates from it. 

- The CSS and JS get built with Yarn, for instance "yarn encore dev) (see https://symfony.com/doc/5.0/frontend/encore/simple-example.html for more information).

- Include the app CSS stylesheet in your template(s) so you have a central entrypoint for styling the site.

- Then include Bootstrap in your stylesheet so you can use the Bootstrap classes for styling. For this you need to change the configuration of the symfony app to make use of SASS instead of plain CSS (see https://symfony.com/doc/5.0/frontend/encore/simple-example.html). Be sure to install only version 7.0.1 of the sass-loader npm. Otherwise you will encounter the error "options has an unknown property 'outputStyle'". When you have compiled the SCSS with "yarn encore dev" you can restart the app and see the results. The HTML code should include the CSS while the app.js imports the app.scss file. Now you can include Bootstrap following this page: https://symfony.com/doc/current/frontend/encore/bootstrap.html (although the bootstrap npm is already installed).

- Change the provided templates to show a list of videos on the homepage (a textual link is ok). Each video should be linked to a detail page of a video that includes the Plyr video player to show the video. Also output the video title that is provided in the "videos" variable. (All data are hardcoded in the controllers so the app doesn't need a databases but usually you don't need to bother).

- The video files are provided in the directory "public/videofiles" and can be accessed in HTML through the path "/videofiles/...". 

- The JS and CSS files of the Plyr video player can be found in "public/static/" and referenced with "/static". Check the Plyr documentation for more info on how to initialize the video player.

- Create a three column layout with Bootstrap 4 grid that contains the player in the middle column on the desktop. On a mobile phone the player should extend over the whole width.

- Create an account in Github (if you don't have one) and create a new repository for your app. Configure the repository as a remote origin in your local directory and push your solution to the Github repo. 

- Please send us the link to the solution and a short documentation about what you did to achieve the goal and what where your experiences. Don't be afraid to talk about problems your encountered (we all do in our daily work). 


