# Documentation

## What this app is:

A two-sided, video-streaming marketplace platform that features credit card payment capabilities, user role management, complex user interfaces, and advanced database relationships.

You may visit the deployed version [here](https://flixter-frederic-hodges.herokuapp.com/).

![Flixter app screenshot](app/assets/images/flixter.PNG "Flixter app screenshot")
![Flixter app screenshot](app/assets/images/flixter2.PNG "Flixter app screenshot")
***
# Setup

## Prerequisites:
 
 The following tools should be installed on the system before following setup steps.
 
  - Git
  - Ruby 2.5.3
  - Rails 5.2.3
  
1. **Clone repo:**
       
        git@github.com:derfman9303/flixter.git
        
2. **On the command line, navigate to the Flixter directory**
        
        cd flixter

3. **Create the database**
        
        rails db:create db:migrate
        
4. **Install gems**
        
        bundle install

***
# Usage

## Start your server:

        rails server -b 0.0.0.0 -p 3000

You may now visit your app at http://localhost:3030


***
# Deployment

## Pushing to Heroku

If you would like, you may push your app up to Heroku by running the following commands:

        git init
        
        git add .
        
        git commit -am "initial commit"
        
        heroku create
        
        git push heroku master
 
 ***
# Notes
This app integrates with a third party API called Stripe to process creit card payments. for more information visit [their website.](https://stripe.com/)

If you only use this app locally, images can be saved to the database using the "carrierwave" gem. However, if you push your app to Heroku, you will run into errors using carrierwave to store images in the database. In this case, you will need to specify an AWS bucket for the "fog-aws" gem to use. For more information on how these gems work, visit their official documentation: [carrierwave](https://github.com/carrierwaveuploader/carrierwave) - [fog-aws](https://github.com/fog/fog-aws)
