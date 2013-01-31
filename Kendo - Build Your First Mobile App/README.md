# Build Your First Mobile Application

In this challenge, you will build your first mobile application.  Oh - and you get to keep the tools that you will use to build it.  

Members of the Kendo UI team will be present to assist you and register you for your free Kendo UI Mobile license.

## Step 1

[Download the Kendo UI Mobile framework](http://www.kendoui.com/download) for building performant cross-plaform mobile applications with HTML5.

## Step 2

Include the necessary files for creating a Kendo UI mobile application...

1. kendo.mobile.all.min.css (at the top of the page)
2. kendo.all.min.js, jquery.min.js (at the bottom of the page below the closing body tag)

Your page should look something like this...

    <!DOCTYPE HTML>
    <html lang="en-US">
    <head>
      <meta charset="UTF-8">
      <title></title>
      <link rel="stylesheet" href="css/kendo.mobile.all.min.css">
    </head>
    <body>
      
      <script src="js/jquery.min.js"></script>
      <script src="js/kendo.all.min.js"></script>

    </body>
    </html>

## Step 3

Tie into the Instagram API to display popular images and interact with them.

To get you started, use the following code:

    <!DOCTYPE HTML>
    <html lang="en-US">
    <head>
      <meta charset="UTF-8">
      <title></title>
      <link rel="stylesheet" href="css/kendo.mobile.all.min.css">
    </head>
    <body>
      
      <!-- a mobile view with a navbar and a listview
      <div data-role="view" id="" data-title="">
        <div data-role="navbar">Popular Images</div>
        <ul id="popular" data-role="listview" data-style="inset" 
            data-source="APP.popular" data-template="template"></ul>
      </div>
      
      <!-- the template for the listview results -->
      <script type="text/x-kendo-templ" id="template">
        <a href="\#">
          <img src="#: images.thumbnail.url #">
        </a>
      </script>
      
      <script src="js/jquery.min.js"></script>
      <script src="js/kendo.all.min.js"></script>
      
      <script>
        
        (function($) {
        
          window.APP = {};

          // sample client id. won't work after Monday. 
          // You should register for your own at instagram.com/developers
          var clientid = "e70cc03ee111421cba42068751ff75b1";

          // create a remote datasource for reading the instagram api
          APP.popular = new kendo.data.DataSource({
            transport: {
              read: {
                url: "https://api.instagram.com/v1/media/popular?client_id=" + clientid,
                dataType: "jsonp"
              }
            },
            schema: {
              data: "data"
            }
          });

          // create the mobile application
          var app = new kendo.mobile.Application(document.body);
        
        }(jQuery));
      
      </script>
    
    </body>
    </html>

## Go forth and be awesome

Hit up the docs and getting started guides at [docs.kendoui.com](http://docs.kendoui.com) and build something amazing.  Here are some ideas...

1. Add a details page so when you click on an item, it loads that picture in a details view along with any comments on the picture.

2. Use a [Kendo UI Mobile ScrollView](http://demos.kendoui.com/mobile/scrollview) instead of a ListView to display the images

3. Use a [Kendo UI Mobile SplitView](http://demos.kendoui.com/mobile/splitview) to display the images on the left side and their details on the right side.

## Help is all around you!

There will be 4 resident Kendo UI Mobile experts to sit and assist you with your application.  If you need help, just find someone with a Kendo UI shirt and ask them!
