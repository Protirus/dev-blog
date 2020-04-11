---
layout: post
title: Using the REST Generator in Workflow 7.6
author: Alex Hedley
category: general
tags: [general]
---

In this Article I will explain how to use the REST Generator within [Workflow](http://www.symantec.com/connect/workflow-servicedesk) 7.6.

Follow up articles

- [Using the REST Generator (GET) in Workflow 7.6 with Mobility Suite](about:/Blog/Detail/2)
- [Using the REST Generator (Headers) in Workflow 7.6 with Mobility Suite](about:/Blog/Detail/3)

I'm going to be using the RESTful APIs available in to us from [http://swapi.co/](http://swapi.co/). The Star Wars API.

A little background:

> REST or Representational State Transfer is an architecture style or design pattern used as a set of guidelines for creating web services which allow anything connected to a network (web servers, private intranets, smartphones, fitness bands, banking systems, traffic cameras, televisions etc.) to communicate with one another via a shared common communications protocol known as Hypertext Transfer Protocol (HTTP). The same HTTP verbs (GET, POST, PUT, DELETE etc.) used by web browsers to retrieve and display web pages, audio/video files, images etc. from remote servers and post data back to them when performing actions like filling out and submitting forms are used by all of the aforementioned devices/services to communicate with one another.

Link: http://en.wikipedia.org/wiki/Representational_state_transfer

---

To Test an APIs you could use a Chrome Plugin called Postman [http://www.getpostman.com/]

Or on a Mac there is an App you can get called Cocoa Rest Client [http://mmattozzi.github.io/cocoa-rest-client/]

---

Most APIs will require a Key to use them, but don't share it, luckily the Star Wars API doesn't need one.

---

Now go to your Workflow Server.

Open Workflow Manager.

File | New Project and create a new Forms (Web).png Forms (Web) Project.

Give this a name (POC_JSON_WEB).

We will be using this later to display our results.

Now back in the main Workflow Manager window click on

File | New Project and create a new Int.png Integration Project.

Give this a name (POC_JSON_SW_INT).

Scroll down to Enterprise Resources and choose 'REST Generator' and give it a name: "StarWars"

Put in your

- Base URL: http://swapi.co/api/
- Namespace: StarWars

then click Next.

Click Add.

Give it a name: "Planets"

You can change the Method to any of the following:

- GET
- PUT
- POST
- DELETE

Click on the ellipse (…) below 'Response Content'.

Choose "JSON"

Then in Create choose "Create From Request"

Click Next

The response is then shown, click Next.

You will then see the Data Type that has been created, you edit this if necessary. Click Finish.

You will see the chosen Data Type, click OK.

Now you can click Finish and save your new Integration Project.

You can see what was generated for you.

Back to your Web Forms Project.

Add the Library to this.

You can now call the INT and display the results in a Web Form.

And your Web Page

And there you have a way of retrieving data from an API and displaying it in a Web Form.

---

**Symantec**

- [Using the REST Generator in Workflow 7.6](https://www-secure.symantec.com/connect/articles/using-rest-generator-workflow-76)
- [Using the REST Generator (GET) in Workflow 7.6 with Mobility Suite](https://www-secure.symantec.com/connect/articles/using-rest-generator-get-workflow-76-mobility-suite)
- [Using the REST Generator (Headers) in Workflow 7.6 with Mobility Suite](https://www-secure.symantec.com/connect/articles/using-rest-generator-headers-workflow-76-mobility-suite)
