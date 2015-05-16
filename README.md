Simple compiler for *Modelleertaal*
==========================================

[![Travis Status](https://travis-ci.org/tomkooij/modelleertaal.svg)]
(https://travis-ci.org/tomkooij/modelleertaal)

Modelleertaal to javascript compiler in javascript/jison.

Modelleertaal is  the language used for "natuurkundig modelleren" 
 (dynamical models in  high school physics in NL). 
The language is a subset of "CoachTaal" which is a ALGOL-like (i.e. Pascal) 
 with the keywords translated into Dutch.
```
 Note that keywords start with a capital (and are in dutch).
 Statements are not ; terminated
 Comments start with '


   Example:
     Als (a == 0) En Niet(b == Waar) Dan Stop       'modelleertaal

   In Pascal:
     If (a = 0) AND !(b = True) then Halt(0);

   Real world example (SysNat model 9):
     'model 9 parachutesprong
     'modelregels
     Fwr = k * v^2
     Fres = Fzw - Fwr
     a = Fres/m
     dv = a * dt
     v = v + dv
     dy = v * dt
     y = y + dy
     h = h0 - y
     t = t + dt
     als h < 400 dan k = 0.6 * (400 - h) eindals
     als h < 350 dan k = 30 eindals

Extensions to the language:
CoachTaal (and Pascal) use ':=' as the assign keyword. We also allow '='
 because our textbook and exams use '='. Use '==' for comparison.
C/Java style comments are allowed
```

This was originally based on git://github.com/zaach/zii-jsconf2010-talk.git

Installation
============

Node.js using npm and grunt:

```
npm install -g grunt-cli
npm install 
grunt 
```

Usage
=====

Node.js:
```
node run
```
