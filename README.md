# openjdk9-builds
There should be OpenJDK 9 binaries. How about these?

## So you don't have to

tl;dr version: See the Releases tab on this Github project for binaries. See
the REVISION file to know what tag or revision the binaries were built with.

This project uses OpenJDK 9's beta sources and builds them for (at the moment)
Windows 32-bit and 64-bit. The exact revision of OpenJDK source used is in the
file in this directory called `REVISION`. Every attempt will be made to use
as-stable-as-possible revisions, mostly by only using permanent tags in the
OpenJDK Mercurial repo. See the Releases tab of this project for the actual
binaries, bundled similarly to alexkasko's openjdk-unofficial-builds project.
I owe a great deal of thanks to alexkasko for inspiration and taking the first
steps to package OpenJDK (6 and 7) in a usable form. I also absolutely need to
thank [Ludovic Hochet](http://lhochet.blogspot.fr/2015/05/building-java-9-on-with-visual-studio.html)
for providing detailed instructions on how to build such a complex piece
of software on Windows.



# README from OpenJDK source

README:
  This file should be located at the top of the OpenJDK Mercurial root
  repository. A full OpenJDK repository set (forest) should also include
  the following 7 nested repositories:
    "jdk", "hotspot", "langtools", "nashorn", "corba", "jaxws"  and "jaxp".

  The root repository can be obtained with something like:
    `hg clone http://hg.openjdk.java.net/jdk9/jdk9 openjdk9`

  You can run the get_source.sh script located in the root repository to get
  the other needed repositories:
    `cd openjdk9 && sh ./get_source.sh`

  People unfamiliar with Mercurial should read the first few chapters of
  the Mercurial book: http://hgbook.red-bean.com/read/

  See http://openjdk.java.net/ for more information about OpenJDK.

Simple Build Instructions:

  0. Get the necessary system software/packages installed on your system, see
     http://hg.openjdk.java.net/jdk9/jdk9/raw-file/tip/README-builds.html

  1. If you don't have a jdk8 or newer jdk, download and install it from
     http://java.sun.com/javase/downloads/index.jsp
     Add the `/bin` directory of this installation to your PATH environment
     variable.

  2. Configure the build:
       bash ./configure

  3. Build the OpenJDK:
       make all
     The resulting JDK image should be found in `build/*/images/j2sdk-image`

where make is GNU make 3.81 or newer, /usr/bin/make on Linux usually
is 3.81 or newer. Note that on Solaris, GNU make is called "gmake".

Complete details are available in the file:
     http://hg.openjdk.java.net/jdk9/jdk9/raw-file/tip/README-builds.html
