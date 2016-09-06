EPICS V4 Java Implementation README
===================================

This README is a guide to the Java implementation of EPICS V4. 

*Status:* This README is up-to-date with respect to release 4.6.0 of EPICS 
V4.
<br/>
*Author:*
Greg White, SLAC, 28-Oct-2015
<br/>
*Modified:*
<br/>
Dave Hickin, Diamond, 01-Feb-2016: Update for 4.5.0.1<br/>
Ralph Lange, ITER, 06-Sep-2016: Refactor and update for 4.6.0


Prerequisites
-------------

The EPICS V4 Java bundle requires recent versions of the following software:

1. Java SDK v1.7 (Java 7) or later.


Contents
--------

The distribution download tar (or zip) archive of the Java implementation of 
EPICS v4.6.0 contains:

* **`epics-core`**
<br/>
The jar files of Java executables, sources and Javadoc API documentation for 
all core software modules of EPICS V4, 
and the CAJ and JCA libraries that support Channel Access operations through 
the pvAccess API "Channel Provider" interface.

* **`example-modules`**
<br/>
The complete source directory structures (Maven projects) for the example 
applications demonstrating the use of EPICS V4.

* **`example-libs`**
<br/>
All external libraries (dependencies) that are needed by the example modules.


Usage
-----

The jars in `epics-core` are mainly for educational purposes, or for importing 
into IDEs when creating non-Maven Java projects using EPICS V4.

`example-modules` contains examples as Maven projects.
These will download all dependencies through the Maven mechanism using 
dedicated Maven repositories. 
They do not use the jars from the distribution download tar/zip archive.

### IDE Use

Simply open the `exampleJava` aggregator project (or any of the individual 
modules/projects in the subdirectories) in your IDE. 
All common Java IDEs (Eclipse, NetBeans, ...) support Maven projects.

Build the project using your IDE.

### Command Line Use

Change into the project directory of the `exampleJava` aggregator module 
(or any of the individual modules). The project directory is the directory 
that contains the POM (`pom.xml` file). In that directory, run

    mvn install


Source Repositories
-------------------

The upstream source code repositories of all modules are kept on 
[GitHub/epics-base](https://github.com/epics-base).


Further Information
-------------------

For more information visit the 
[EPICS V4 Project Website](http://epics-pvdata.sourceforge.net), 
where you will find

* [Getting Started Guide](http://epics-pvdata.sourceforge.net/gettingStarted.html) - 
  Build instructions and links to detailed information.
* [Developer's Guide](http://epics-pvdata.sourceforge.net/informative/developerGuide/developerGuide.html) -
  Reference Manual for developing applications with EPICS V4.
* [Documentation page](http://epics-pvdata.sourceforge.net/literature.html) -
  Overview documents and API documentation for all modules.

For the individual modules, the documentation sources are part of the upstream 
source repositories. Each module provides

* An overview in `README.md`
* A `documentation` directory, containing
    * the module specific documentation, and
    * the release notes in `RELEASE_NOTES.md`.
