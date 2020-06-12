
# Table of Contents

1.  [An Emacs Course](#orgf6db9ea)
    1.  [Introduction](#org77b6ef9)
    2.  [Setup](#org93d2a7a)
        1.  [Install the configuration and the course](#orgfbfa272)
        2.  [Start Emacs and let it install the required Emacs packages](#org73ff809)
        3.  [Start the course](#org4efe6f6)
    3.  [Planning of learning stages](#orge5e16ba)



<a id="orgf6db9ea"></a>

# An Emacs Course


<a id="org77b6ef9"></a>

## Introduction

I had used Emacs for many years in its most simple way - just as a
programming editor, just using the minimal set of exotic
commands. But when I discovered around 2009 what Emacs really is -
one of the most flexible and well documented programming
environments that happens to be a very good editor as well, I was
blown away.

Org mode was a revelation - the dream of every scientist (physical
chemistry was my original profession). A notebook where you could
write easy marked up text, math, you could calculate, and as a
programmer you could use all your programming languages inside of
the documents and produce graphics inline - too good to be
true. And then it is one of the best task management systems as
well. I fell in love, learned lisp - enjoined its different feel from
the C and scripting languages I knew - something that reminded me of
the joy of playing with the HP Scientific Calculators many year ago.

For a long time I entertained the hope of passing on the
knowhow. But it's not so easy, since the thing which makes Emacs so
great and efficient - its staggering flexibility - also makes it
tough to teach. Most long time users end up with configurations that
fit them like a glove. But other users will be very opinionated in regards
to the packages and optimizations that are used. There's a good number
of excellent meta-distributions around, like SpaceMacs or Doom. They
may be great for many users. I myself always stayed with my hand-written
config that I constantly adapted to more modern styles (which prevented
me from ever declaring the dreaded *Dot Emacs Bankruptcy*)

I now decided to make a first test run with a course that is based on
basic configuration of Emacs. I will start with an initial configuration
that already has a number of nice packages that will wet the appetite.
But the idea is not that learners shall adpot these exact configurations.
They should learn how the configuration works and how they can adapt
it. So, they by themselves will be able to make an informed decision about
whether they want to adopt one of the meta distributions, change the
present one, or just develop their own.

My big thanks goes to the whole Emacs community. One of the most
welcoming and helpful communities I had the pleasure to work with.
So many people have contributed to this products and I feel indebted
to all of them.


<a id="org93d2a7a"></a>

## Setup


<a id="orgfbfa272"></a>

### Install the configuration and the course

The Emacs configuration for the course you can find at
<https://github.com/dfeich/emacs-course-and-config>. 
It is best that you fork that repository and then clone your
forked copy to your (or a test user's) account's `~/emacs.d` directory on your
machine.

    git clone git@github.com:dfeich/emacs-course-and-config.git ~/.emacs.d
    
    # or if you made a fork
    
    git clone git@github.com:<YOUR-GITNAME>/emacs-course-and-config.git ~/.emacs.d

This repository contains the course in the form of Org mode task files.
It should be checked out into the `~/Documents/orgcourse` folder of your account.
The emacs configuration for the course contains settings that expect to
find the files under that location.

    git clone git@github.com:dfeich/emacs-course.git ~/Documents/orgcourse

If you check out to another location, you need to adapt the
definition in the Emacs configuration.

When you start Emacs with the new configuration for the first time, it
will download all the missing packages from GNU, MELPA, and Org. This
may take some minutes.

I use Emacs version 26.3 and Org version 9.x for this course.


<a id="org73ff809"></a>

### Start Emacs and let it install the required Emacs packages

When you start Emacs with the new configuration, it will download
the packages that are defined in the config. It may also have to
compile some extensions and pull in some OS packages (e.g. for the
PDF integration). If Emacs stops with an error message, this does
not necessarily mean that there is a big problem. Close it either
using your pointer or hit the CTRL-x CTRL-c key combination. Launch
it again and look whether it gets further. Since some downloaded
packages are replacing older versions of existing packages, it can
sometimes happen that depending on your current config Emacs ends
up in a state where the old package and the new package
conflict. Because what you are actually doing is **live-patching
it**! Emacs mostly deals very well with your exchanging its
cogwheels while its running, but for some more brutal changes it
may need some help.

If it fails repeatedly without progressing further then please
file an issue in this tracker, and I will try to help.


<a id="org4efe6f6"></a>

### Start the course

Once you have everything installed, start the first stage by typing

    emacs ~/Documents/orgcourse/agenda/course01-basics.org


<a id="orge5e16ba"></a>

## Planning of learning stages

This is what I am planning to cover. Let's see whether I'll be able to
pull through&#x2026;

The sequence beyond step 1 is up to change&#x2026; I will teach a small
number of work colleagues in this first round. I'll adapt to the
feedback I will get. All of this will be hands-on with prepared
documents for the lessons. The configuration will grow with the
material covered in the lessons - and I may leave holes for this
first round, since the coworkers know some items already.

1.  Basic Emacs and Org mode
    -   this is a big first stage, but I think that Org mode must be introduced
        early, because it is one of the principal features that immediately
        offers big benefits to new users
    -   minimal emacs lisp knowledge, just enough to understand the config
        in a rudimentary way and lose the fear of parentheses
    -   basic editing
    -   file management (dired)
    -   org mode as a basic task manager (org agenda, basic org file features)
    -   easier user interface with helm, smex, ido
    -   emacs package management
    -   how to use the info and help systems
    -   emacs daemon
2.  Emacs for higher productivity, programming and system management
    -   Magit - is there a better Git interface then this?
    -   Tramp (a killer feaure for users working on remote hosts. Loved by
        system administrators and developers)
    -   Org capture - create tasks and back-links from everywhere
    -   gpg for encrypting files
    -   dired revisited
    -   command execution from Emacs
    -   a look at some of the programming modes
    -   lsp-mode (a modern IDE interface in Emacs)
    -   linting (Syntax checking with flycheck)
3.  Authoring LaTeX, HTML, and other documents with Org mode
    -   write scientific documents containing math, preview the math
    -   do inline calculations with Calc
    -   include graphics and screenshots
    -   simple first steps with Org Babel to execute code and
        create graphics
4.  Org Babel for real
5.  Fast Presentations with LaTeX beamer through Org
6.  Integrating with your browser
    -   Use emacs to edit forms in browsers like Firefox or Chrome
        (through the daemon)
    -   org-protocol: transfer information from the browser to Emacs,
        e.g. mark some text in the browser and get it into emacs, or
        convert a web page to org mode and find it ready in your buffer!
7.  Emacs and email
    -   mu4e and mbsync to manage email
    -   integrate email with org mode task management, making
        efficient use of org capture and email links in workflows.
8.  Emacs for science
    -   helm-bitex
    -   org-ref
    -   org-babel
    -   org-noter and PDF management
    -   jupyter (maybe)

