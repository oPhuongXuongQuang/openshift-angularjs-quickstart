openshift-angularjs-quickstart
==============================

This git repository helps you get up and running quickly a AngularJS
installation on OpenShift.  The AngularJS project name used in this repo
is 'openshift' but you can feel free to change it.

Running on OpenShift by RHC
---------------------------

Create an account at http://broker.ose.hi.inet/ or contact with [support team](#mailto://engapa@aurigae.com).

Install the RHC client tools if you have not already done so:
    
    sudo gem install rhc

Create a web application

    rhc app create -a angularjs -t jbossews-2.0

Add this upstream repo

    cd angularjs
    git remote add upstream -m master git://pdihub.com/egp30/openshift-angularjs-quickstart.git
    git pull -s recursive -X theirs upstream master

Then push the repo upstream

    git push

Here, the application url will be displayed, so pay special attention.
	
That's it, click on the link. You can now checkout your application at:

    http://angularjs-$yournamespace.ose.hi.inet

Running on OpenShift by Web console
-----------------------------------

Create an account at http://broker.ose.hi.inet/ or contact with [support team](#mailto://engapa@aurigae.com).

Login on web console :  http://broker.ose.hi.inet/

On section 'Create application' select the AngularJS quickstart and follow the steps

Here, the application url will be displayed, so pay special attention.
	
That's it, click on the link. You can now checkout your application at:

    http://angularjs-$yournamespace.ose.hi.inet

Store JSON for use it on web console (Only Administrator of PDI-OpenShift)
--------------------------------------------------------------------------

In order to add this quickstart to available quickstarts on web console you shoud add this entry to file ´´/etc/openshift/quickstarts.json´´ :

    {"quickstart": {
    "id":"1",
    "href":"https://broker.ose.hi.inet/quickstarts/angularjs",
    "name":"AngularJS on OpenShift",
    "summary":"This git repository demonstrates how to use AngularJS on OpenShift using Tomcat7.",
    "body":"<p>This git repository demonstrates how to use AngularJS on OpenShift using Tomcat7.",
    "cartridges":"jbossews-2.0",
    "website":"http://angularjs.com",
    "tags":"partner, tomcat, javascript",
    "language":"Web",
    "initial_git_url":"https://pdihub.com/egp30/openshift-angularjs-quickstart.git",
    "provider":"partner",
    "admin_tags":[]
    }}

