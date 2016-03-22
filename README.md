pptx2txt.sh
===========

command line bash shell script to convert PowerPoint `.pptx` format to text on Mac, Linux or Unix

~~~
USAGE: pptx2txt.sh [options] PPTX_FILENAME

OPTIONS:

  -v, --verbose     verbose output including filename and slide number heading

  -h, --help        display this help message

~~~

redirect output to a text file
~~~
./pptx2txt.sh [options] PPTX_FILENAME > output.txt
~~~

handing non-XML `.ppt` format

* manually save as `.pptx` format, e.g. with [LibreOffice](https://www.libreoffice.org/)

* convert `.ppt` to `.pptx` using `unoconv` (Linux/Unix)
~~~
sudo apt-get install unoconv
unoconv --doctype=presentation --format=pptx --output=tmp.pptx PPT_FILENAME
./pptx2txt.sh tmp.pptx
~~~
