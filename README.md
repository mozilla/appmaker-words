AppMaker -- why, what, how
==============

Note: this is as draft as draft gets.  Nothing expressed here is at the level of agreed upon, let alone committed to.  Just words.

Also, this language will be telegraphic, not ready for marketing purposes, etc.  It's primarily to establish
shared objectives and approach within the people who end up working on it.

Context
------

The world is going mobile; FirefoxOS and the capabilities of the HTML5 mobile app platform more broadly are becoming more competitive.  A new generation of folks is going to be exposed to the internet and the web platform through mobile devices.  In the mobile world, the equivalent of creating a home page in Web 1.0
could be creating your own web app.

Long term goals
------

AppMaker is a set of initiatives to see if that's possible -- can we make the ability to create a mobile app drastically more accessible to a brand new set of app creators who are not self-identified as developers, and are primarily motivated by something other than "desire to learn the web".  We expect their motivations will
range fromcreative satisfaction of "having made a thing that looks & feels real" to a desire to have an app to send to clients of an small neighborhood offline service business.

The grand goal of AppMaker is for millions of people to be able to create apps that give them utility or joy.  It need not be through the use of our software, although we expect that we'll h ave to build or assemble parts of that whole product experience, partner for parts of it, and work with many, many people to both get input into both what the product should be, how our stuff does or doesn't meet the needs of real people, and how to get the software in front of the right users.

What would users actually do
--------------

We're currently exploring two basic onboarding paths, and three "advanced" modes.

Creative path 1: Remixable apps

We have a hypothesis that there are some apps which, if they were made "remixable", would satisfy many use cases. Remixing in this context refers to the ability of end-user to take an existing app (built with that capability built in)
and do the "mobile" equivalent of copy & paste: on the device, take the app and make a new app that is customized by the user, and republished at a new endpoint from where it can be distributed anew.  (there are issues of credit
and licensing to deal with -- we'll build in and assume licensing models that encourage this act of remix; removing the ability to remix can be done downstream).

We are identifying several such template remixable apps, which will help us identify the challenges to making remixable apps, and test whether both the specific apps and the notion of remixable apps have user appeal.

Creative path 2: Author new apps on desktop for use on phone only

Web technology has matured enough that most browsers are now capable of fluid, interactive "wysiwyg" tools. We will make an in-browser tool that lets users layout simple components in a layout simulator on a desktop configuration, with minimal "hooking up" of components and minimal navigational support, so that a novice can experience the full cycle of layout / configure / deploy, and make an app that they created.

We'll do this by asserting many hard constraints which tools aimed at professional developers can't afford to. Phone screens to a first approximation can be thought of having similar form factors, varying mostly in pixel
count and small aspect ratio variations.  We will simplify the generic problem of making a broadly responsive authoring environment (which would need to deal with very different UI patterns for phones, tablets, desktops, TVs) and lean on
a prescriptive proportional layout model, a default widget set and skin, and generally limited capabilities.

Upleveling 1: 

If people want to create new lego blocks, we want to provide a level of compositionality which is not quite at the level of raw HTML/JS, as that requires a lot of formal programming knowledge.  We will be exploring at least
two approaches: a 'wires and boxes' programming model, such as MeeMoo; a 'block language' like Waterbear (a webby  version of MIT's Scratch).

Upleveling 2:

This is all just HTML/JS/CSS, so we will have ways to look at / edit their code in a more traditional web authoring environment like Thimble (or JSfiddle or ...)

Approach
-------

We're starting by assembling a set of technologies which we think may play a role in the overall offering, and exploring how they need to be tweaked to better fit together.  Both complementing and testing some of the assumptions behind that initial thought will be user testing, prototyping and generally trying out whether the assembly makes sense.

The key components we've identified so far are:

* HTML5 + WebAPIs + Open Web App spec.  FirefoxOS is showing that we can use web technologies defined somewhat broadly to implement experiences that feel "appy".  The WebRT ("Web Runtime") is the set of APIs that these apps
need (broadly: HTML5 + device APIs and app manifest and the like, all en route to standardization but not yet ubiquitous).

* A place to publish and get apps.  The Firefox Marketplace (marketplace.firefox.com) is the canonical such place, but we will probably be playing with other app distribution endpoints especially for user and tech testing
scenarios.

* A higher-level language for lego-block-like assembly of "parts of apps".  We're pretty excited about Web Components and will be figuring out how to build on the shoulders of projects like the Web Components standard, x-tags,
Polymer (http://www.polymer-project.org/) and others to identify an abstraction layer that is "good enough" for our users' needs.  This is a hard problem, and we'll be very happy if we find 80% solutions.

* A place to publish these lego blocks.  We'll probably start with a fork of the MakeAPI (URL to spec?) that's used by the Webmaker project, with plans to merge that fork back in mainline once it's proven its worth. 

* A layout tool.  Our users  should be able to go a website, use an appropriately easy and simple tool to create a set of web assets which when deployed through an 'appstore' does what they want.  This layout tool will import components and assets from the makeAPI at first, although the intent is to have other asset stores.

Assumptions
----------------

We'll be targeting the web stack that Mozilla is currently building.  The intent is for this to be ubiquitous, but one fight at a time.  We'll focus on mobile, where we expect FirefoxOS will have the best early API support, but where Android (and the WebRT delivered as part of Firefox for Android) will have the most penetration for a while to come.  We will thus be targeting users with Android phones capable of running whatever version of Firefox for Android will have the WebRT capabilities built in.




Summer 2013
----------

