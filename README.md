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

options for handling non-XML `.ppt` or Mac keynote (`.key`) formats

* convert `.ppt` or `.key` to `.pptx` using [LibreOffice](https://www.libreoffice.org/)

  ** .ppt to .pptx **
  ~~~
  libreoffice --headless --convert-to pptx filename.ppt
  ./pptx2txt.sh filename.pptx
  ~~~

  ** .key to .pptx ** (LibreOffice 5.x or newer)
  ~~~
  libreoffice --headless --convert-to pptx filename.key
  ./pptx2txt.sh filename.pptx
  ~~~
