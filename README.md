node-printer
============
<table>
  <thead>
    <tr>
      <th>Linux</th>
      <th>OS X</th>
      <th>Windows</th>
      <th>Dependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan="2" align="center">
        <a href="https://travis-ci.org/tojocky/node-printer"><img src="https://travis-ci.org/tojocky/node-printer.svg?branch=master"></a>
      </td>
      <td align="center">
        <a href="https://ci.appveyor.com/project/tojocky/node-printer"><img src="https://ci.appveyor.com/api/projects/status/9y800f36wla35ee7?svg=true"></a>
      </td>
      <td align="center">
        <a href="https://david-dm.org/tojocky/node-printer"><img src="https://david-dm.org/tojocky/node-printer.svg"></a>
      </td>
    </tr>
  </tbody>
</table>

This package native bind printers on POSIX and Windows OS from Node.js. It was tested on node.js, io.js and node-webkit.
if you have a problem, ask question to [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/tojocky/node-printer?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) or find/create a new [Github issue](https://github.com/tojocky/node-printer/issues)

### Reason:

I was involved in a project where I need to print from Node.JS. This is the reason why I created this project and I want to share my code with others.


### Features:

* no dependecies;
* native method wrappers from Windows  and POSIX (which uses [CUPS 1.4/MAC OS X 10.6](http://cups.org/)) APIs;
* compatible with node v0.8.x, 0.9.x and v0.11.x (with 0.11.9 and 0.11.13);
* compatible with node-webkit v0.8.x and 0.9.2;
* `getPrinters()` to enumerate all installed printers with current jobs and statuses;
* `getPrinter(printerName)` to get a specific/default printer info with current jobs and statuses;
* `getPrinterDriverOptions(printerName)` ([POSIX](http://en.wikipedia.org/wiki/POSIX) only) to get a specific/default printer driver options such as supported paper size and other info
* `getSelectedPaperSize(printerName)` ([POSIX](http://en.wikipedia.org/wiki/POSIX) only) to get a specific/default printer default paper size from its driver options
* `getDefaultPrinterName()` return the default printer name;
* `printDirect(options)` to send a job to a specific/default printer, now supports [CUPS options](http://www.cups.org/documentation.php/options.html) passed in the form of a JS object (see `cancelJob.js` example);
* `printFile(options)`  ([POSIX](http://en.wikipedia.org/wiki/POSIX) only) to print a file;
* `getSupportedPrintFormats()` to get all possible print formats for printDirect method which depends on OS. `RAW` and `TEXT` are supported from all OS-es;
* `getJob(printerName, jobId)` to get a specific job info including job status;
* `setJob(printerName, jobId, command)` to send a command to a job (e.g. `'CANCEL'` to cancel the job);
* `getSupportedJobCommands()` to get supported job commands for setJob() depends on OS. `'CANCEL'` command is supported from all OS-es.


### How to install:

from [npmjs.org](https://www.npmjs.org/package/printer)

    npm install printer

or [direct from git](https://www.npmjs.org/doc/cli/npm-install.html):

    npm install git+https://github.com/tojocky/node-printer.git

Ubuntu User :
You need to install libcups2-dev package
`sudo apt-get install libcups2-dev`


### How to use:

See [examples](https://github.com/tojocky/node-printer/tree/master/examples)

### Author(s):

* Ion Lupascu, ionlupascu@gmail.com

### Contibutors:

Feel free to download, test and propose new futures

### License:
 [The MIT License (MIT)](http://opensource.org/licenses/MIT)
