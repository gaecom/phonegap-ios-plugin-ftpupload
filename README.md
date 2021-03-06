# Ftp Upload for PhoneGap #

Ftp Upload plugin that works out of the box with Cordova/PhoneGap 3.x.x `plugin add` interface.

Only for file upload. Other functions are not covered yet. Basic FTP functions are from Apple's sample [SimpleFTPSample](https://developer.apple.com/library/IOs/samplecode/SimpleFTPSample/Listings/Read_Me_About_SimpleFTPSample_txt.html#//apple_ref/doc/uid/DTS40009243-Read_Me_About_SimpleFTPSample_txt-DontLinkElementID_16)

## Installation ##

  You can use Cordova/PhoneGap 3.x.x `plugin add` interface to install:
  <pre>
  phonegap local plugin add https://github.com/gokce/phonegap-ios-plugin-ftpupload.git
  </pre>

## Usage in javascript ##

  <pre>
  window.plugins.ftpUpload.sendFile(successCallback, failCallback, "address", "username", "password", "filepath");
  </pre>
  
  * address can be either full: "ftp://127.0.0.1" or just ip or domain "127.0.0.1"
  
  * filepath should be fullpath. You can check [File Plugin](http://docs.phonegap.com/en/3.0.0/cordova_file_file.md.html#File) for more details on how to get fullpath.

### FailCallback returns fail message, that you can capture: ###
  <pre>
    failCallback = function(e) {
        console.log(e);
    }
  </pre>
  can output:
  <pre>
    {"message":"Stream open error","code":9}
  </pre>
  
  Check XCode console for mode detailed debugging.

## LICENSE ##

Copyright (c) 2013 Gökce Taskan

The MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.