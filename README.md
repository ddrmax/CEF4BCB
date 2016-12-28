# CEF4BCB

Component / Wrapper Classes for the Chromium Embedded Framework
  
This project is based on Dcef3 / capi / CEF

# FAQ:

### What is CEF4BCB?

CEF4BCB provide a simple method to develop a chromium browser based app in c++ builder instead of using the TWebBrowser (IE based) VCL Component.

### Which versions of CEF are supported?

CEF4BCB only support CEF3

Cef3 version: 3.2883.1539

other branches comming soon (older and newer)

Component like in DCEF comming soon

### Which platforms are supported?

Windows, VCL

Test in Delphi 2009, It seems to work on Delphi 2010 and Newer

will try to compile into these versions of C++ builder:

C++ builder 6 personal

c++ builder 2006 Turbo Explorer

c++ builder 2009 professional

c++ builder XE4 professional

c++ builder 10.1 Starter

### How to use it?

first use implib on libcef.dll (implib -a libcef.lib libcef.dll)

add CEF4BCB.h into your code

add CEF4BCB * Browser to your .h

add Browser = new CEF4BCB to your form constructor

on your formshow  set the handle (like a TPanel)

Call the init

in oncanclose call the Shutdown procedure (will terminate the thread and call cefshutdown)

use it like the TChromium or TWebBrowser

# State of implementation of the CEF3 API

To be updated:

Launch the browser in external window or embeded into a form

use standard functions like go back, go next, reload , stop loading, etc...

use javascript like in the devleloper console (but no return values for now)

WebGL is working (but some chrome experiment doesnt work)

no download support

# Known bugs

access violation when closing the app because of a weird problem implying the reference counter (because we cannot use atomic like in the libcefdll wrapper from CEF 

# License

To be Specified.
 
# Links:

[Dcef3](https://github.com/hgourvest/dcef3)

[cefcapi](https://github.com/cztomczak/cefcapi)

[chromiumembedded](https://bitbucket.org/chromiumembedded/cef)

[DcefBrowser](https://github.com/bccsafe/DcefBrowser)
