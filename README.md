# PR3DATOR Twitter

### Introduction
“Pr3dator Twitter” is a web application that handles twitter data through websocket. Application basically uses Maven to build a Camel route in an OSGi bundle, that can be deployed on Apache Karaf. This application is primarily built from example camel-example-twitter-websocket-blueprint available at Camel distribution. We have implemented major API’s available to perform various twitter functions.


### Build
You will need to install this example first to your local maven repository with:
  mvn install

### Run with Karaf
This example requires running in Apache Karaf / ServiceMix

	karaf

To install Apache Camel in Karaf you type in the shell (as an example here we make use of
Camel version 2.15.2):

	feature:repo-add camel 2.15.2

First you need to install the following features in Karaf/ServiceMix with:

  feature:install camel
	feature:install camel-twitter
	feature:install camel-websocket

Then you can install the Camel example:

	install -s mvn:org.apache.camel/camel-example-twitter-websocket-blueprint/2.15.2

Then open a browser to see  twitter application in the web page

	http://localhost:9090
<http://localhost:9090>
To stop the example run from Karaf/ServiceMix shell:
  stop <bundle id>

To view logs:
 log:display

To view deploy status:
 list

