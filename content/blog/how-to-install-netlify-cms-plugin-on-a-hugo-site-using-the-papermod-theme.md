---
Title: Installing Netlify CMS plugin on a Hugo site using the Papermod theme
description: Learn how to install Netlify CMS plugin on a Hugo site using the
  Papermod theme.
dateString: February 2023
draft: false
tags:
  - Netlify CMS
  - HUGO
  - PaperMod Theme
  - Installation
weight: 100
cover:
  image: /blog/sugarcrm-lamp-installation/cover.png
title: how to install Netlify CMS plugin on a Hugo site using the Papermod theme
date: 2023-02-11T21:24:46.984Z
---
# Introduction
To install the Netlify CMS plugin on a Hugo site using the Papermod theme, you will need to follow these steps:

## 1.  Clone the Papermod theme repository to your local machine:
    
 ``` 
   git clone https://github.com/kishaningithub/hugo-papermod-theme` 
 ```

## 2.  Create a new Hugo site using the Papermod theme:
    
      
    hugo new site my-hugo-site
    cd my-hugo-site
    git clone https://github.com/kishaningithub/hugo-papermod-theme themes/hugo-papermod-theme 
    
## 3.  In your Hugo site's `config.toml` file, add the following line to specify the Papermod theme:
    
    makefileCopy code
    
    `theme = "hugo-papermod-theme"` 
    
## 4.  Create a new `static` directory in your Hugo site:
    
    javascriptCopy code
    
    `mkdir static` 
    
## 5.  Download the latest version of Netlify CMS from the official repository:
    
    bashCopy code
    
    `curl https://cdn.jsdelivr.net/npm/netlify-cms@2.13.2/dist/netlify-cms.js > static/netlify-cms.js` 
    
## 6.  Create a new `admin` directory in your Hugo site:
    
    bashCopy code
    
    `mkdir admin` 
    
## 7.  Create a new `index.html` file in the `admin` directory with the following content:
    
       
    `<!DOCTYPE html>
    <html>
    <head>
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Content Manager</title>
    </head>
    <body>
      <script src="https://identity.netlify.com/v1/netlify-identity-widget.js"></script>
      <script src="/netlify-cms.js"></script>
    </body>
    </html>` 
    
## 8.  In your Hugo site's `config.toml` file, add the following lines to configure Netlify CMS:
    
       
    `baseURL = "https://your-site.com"
    [backend]
      name = "git-gateway"
    [mediaLibrary]
      name = "cloudinary"
      config = {
        cloud_name = "your-cloud-name",
        api_key = "your-api-key",
        api_secret = "your-api-secret"
      }` 
    
## 9.  Push your Hugo site to a Git repository.
    
## 10.  Deploy your Hugo site to Netlify, connecting it to your Git repository.
    
## 11.  In the Netlify CMS dashboard, go to the `Settings` tab and enable the `Identity` and `Git Gateway` services.
    
## 12.  Access the Netlify CMS by visiting `https://your-site.com/admin`.
    
# Conclusion
You should now have Netlify CMS installed and configured on your Hugo site using the Papermod theme.