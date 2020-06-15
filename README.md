# phantom-browserless
Splunk Phantom App for [Browserless/chrome](http://github.com/browserless/chrome) & [Browserless.io](http://browserless.io)

This will allow you to perform local screenshotting when using the docker or github app. Additionally you can use the broswerless.io service. 

# Features
* Get Screenshot - Provides the ability to take a screenshot of a URL using a headless chrome browser. Supports JPEG and PNG
* Get PDF - Provides the ability print a webpage as PDF (supports several Chrome PDF Print Settings)
* Get Content - Provides the ability to get the download of the HTML source of a URL provided

# Installing browserless as docker
> See more options on browserless.io's [full documentation site](https://docs.browserless.io/docs/docker.html).

If docker is already installed  `docker run -p 3000:3000 browserless/chrome`

# Install phbrowserless on phantom
1. Download and extract phbrowserless to you phantom server
1. cd to this new directory
1. `phenv python3 /opt/phantom/bin/py3/compile_app.pyc -i`
    > If python2 is needed `phenv python2.7 /opt/phantom/bin/compile_app.pyc -i`
1. Procced to Phantom UI for configuration

# Configure phbrowserless
1. Navigate to Apps in the Phantom UI
1. Select Unconfigured apps and look for "Browserless"
1. Click the "CONFIGURE NEW ASSET" button
1. Provide an asset name
1. Click asset settings
1. Provide the url for your docker host `http://(hostname/ip):3000` if you are using browserless.io use http://chrome.browserless.io and don't forget to provide the Token. 
    > Token's can be used for self hosted instances as well, follow the instructions provided by browserless.io for how.
1. Click Save 
1. Click Test Connectivity. 
