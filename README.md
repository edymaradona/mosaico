# Mosaico - Responsive Email Template Editor

Mosaico is a JavaScript library (or maybe a single page application) supporting the editing of email templates.
The great thing is that Mosaico itself does not define what you can edit or what styles you can change: this is defined by the template. This makes Mosaico very flexible.


![Mosaico Screenshot](res/img/screenshot.png)


At this time we provide a single template to illustrate some best practice examples: more templates will come soon! Please get in touch with us if you want to make your email html template "Mosaico ready".

### Live demo
On https://mosaico.io you can see a live demo of Mosaico: the live deploy has a custom backend (you don't see it) and some customization (custom Moxiemanager integration, customized onboarding slideshow, contextual menu, and some other small bits), but 95% of what you see is provided by this library. You will also see a second working template there: we are still working to open source it. Stay tuned!

#### News

Subscribe to our newsletter to get updates: http://mosaico.voxmail.it/user/register

### More Docs from the Wiki

[Mosaico Basics](https://github.com/voidlabs/mosaico/wiki)

[Developer Notes](https://github.com/voidlabs/mosaico/wiki/Developers)

### Build/Run  [![Build Status](https://travis-ci.org/voidlabs/mosaico.svg)](https://travis-ci.org/voidlabs/mosaico)

You need NodeJS v6.0 or higher + ImageMagick

this may raise warnings about Knockout, ignore them. It will probably fail on some colorpicker dependency, just run it again and will work:
```
  npm install
```
if you don't have it, install grunt-cli globally
```
  npm install -g grunt-cli
```
compile and run a local webserver (http://127.0.0.1:9006) with incremental build and livereload
```
  grunt
```
*IMPORTANT* in order to use image uploading/processing feature in Node you need imageMagick installed in your environment.
e.g. running "convert" and "identify" on the command line should output imageMagick command line help (if you are on Windows and install imageMagick 7.x then make sure to install ["legacy utilities"](https://github.com/aheckmann/gm/issues/559)).

*NOTE* we have reports that default Ubuntu node package have issues with building Mosaico via Grunt. If you see a ```Fatal error: watch ENOSPC``` then have a look at https://github.com/voidlabs/mosaico/issues/82

### Docker

We bundle a small Dockerfile based on centos7 to test mosaico with no need to install dependencies.
```
docker build -t mosaico/mosaico .
docker run -p 9006:9006 mosaico/mosaico
```
then open a browser to point to the port 9006 of your docker machine IP.

### Serving via Apache PHP or Django or something else?
First you have to build it using grunt, then you can read (https://github.com/voidlabs/mosaico/wiki/Serving-Mosaico).

*Access Interpreting* wrote a sample [PHP backend](https://github.com/ainterpreting/mosaico-php-backend) so you can start from there if you want to use Mosaico with an Apache/PHP backend.

*Ryan Nowakowski* wrote a [Python/Django backend](https://github.com/tubaman/django-mosaic) and also wrote a [test-suite in Python](https://github.com/tubaman/mosaico-server-tests) to help testing Mosaico backends

*Matt Gordon* wrote a sample [ASP.NET Core backend](https://github.com/gordon-matt/Mosaico.NetCore) and a sample [ASP.NET MVC5 backend](https://github.com/gordon-matt/Mosaico.Mvc5) so you can start with those if you want to use Mosaico with a .NET backend.

*Cameron Dutro* wrote a [Rails engine](https://github.com/camertron/mosaico-rails) and also wrote a [RoR application](https://github.com/camertron/mosaico-example) that can be used as a starting point.

*Ahmed Rehan* implemented a featured [CodeIgniter](https://github.com/ar27111994/Mosaico-CodeIgniter-Ion-Auth) backend implementing email queue and auth.

### OpenSource projects including/using Mosaico

[MailTrain](https://github.com/Mailtrain-org/mailtrain) is a full featured newsletter web application written in Node and support email editing via Mosaico since their 1.23.0 release.

[GoodEnough's Mosaico](https://github.com/goodenough/mosaico-backend) born as a Mosaico fork, now have become a full web application product built around Mosaico editing targeting agencies.

### Are you having issues with Mosaico?

See the [CONTRIBUTING file](https://github.com/voidlabs/mosaico/blob/master/CONTRIBUTING.md)

### Contact Us

Please contact us if you have ideas, suggestions or, even better, you want to collaborate on this project ( feedback at mosaico.io ) or you need COMMERCIAL support ( sales at mosaico.io ) . Please DON'T write to this email to get free support: use Git issues for that.
