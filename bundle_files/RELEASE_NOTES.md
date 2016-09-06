4.6.0 (2016-09-07)
==================

The main changes since bundle release 4.5.0.1 are:

pvDataJava (6.0.2)
------------------

* Fixed issue with PVStructure's equals() method
* Unit tests for equality of Structures/PVStructures added
* PVAuxInfo has been removed
* Field name validation has been added
* Fixed truncation in BitSet::or_and
* Extra postPut() in ConvertFactory.copyScalar array removed

pvAccessJava (5.0.2)
--------------------

* Duplicate channel response from the same server warning removed
* Server "all providers" support
* ServerContextImpl.startPVAServer method added
* "pvAccess" provider name deprecated, use "pva" instead
* Server-side channel destroy
* pipeline: ackAny parameter percentage support
* PVGet utility monitor support
* pvDS code removed
* pipeline support added

pvDatabaseJava (4.2.2)
----------------------

* Move examples to exampleJava.
* Add support for channelRPC.
* Add removeRecord and traceRecord.

normativeTypesJava (0.2.2)
--------------------------

* __TODO__

pvaClientJava (4.2.2)
---------------------

* The examples are moved to exampleJava.
* Support for channelRPC is now available.

exampleJava (4.2.2)
-------------------

* Move all example code to exampleJava.
* Make each example is a separate Maven module.
* Simplify documentation structure by moving docs to the parent.


4.5.0.1 (2016/02/05)
====================

The main change since release 4.5.0 is:

pvDataJava (5.0.3)
------------------

* Fixed buffer overflow in PVUnion.serialize() (issue #5)

The versions of the other modules and their dependencies have been updated,
but are otherwise unchanged.

See individual RELEASE_NOTES.md in each module for more.


4.5.0 (2015/10/16)
==================

The following are the MAIN changes to the EPICS v4 software suite, since release 4.4.0. See individual RELEASE_NOTES.md in each module for more.

pvDataJava (5.0.2)
------------------
* New template versions of Structure::getField
* Printing of structure and union arrays modified
* minStep field added to Control
* Changes to access specifiers in Display and PVDisplay


pvAccessJava (4.1.2)
--------------------
* Async RPC service.


pvDatabaseJava (4.1.2)
---------------------
This is the first release of pvDatabaseJava, an EPICS V4 record/database framework for providing services over pvAccess.


normativeTypesJava (0.1.2)
--------------------------
This is the first release of normativeTypesJava.

* This release provides support through wrapper classes and builders for the
following Normative Types:
    * NTScalar
    * NTScalarArray
    * NTEnum
    * NTMatrix
    * NTURI
    * NTNameValue
    * NTTable
    * NTAttribute
    * NTMultiChannel
    * NTNDArray
    * NTContinuum
    * NTHistogram
    * NTAggregate
    * NTUnion
    * NTScalarMultiChannel

* Release 0.1 therefore implements fully the
[16 Mar 2015 version](http://epics-pvdata.sourceforge.net/alpha/normativeTypes/normativeTypes_20150316.html)
 of the normativeTypes specification.
* Each type has a builder and a class for testing compatibility and wrapping
  existing structures.
* Utility classes NTField and NTPVField for standard structure fields and
  NTUtils and NTID for type IDs.
* Unit tests for all the implemented types and other classes, providing
  extensive coverage for all the Normative Types (except NTNDArray).


pvaClientJava (4.1.3)
--------------------
pvaClientJava is the successor to easyPVAJava, a synchronous API for pvAccess.

* pvaClient uses exceptions to report most problem instead
  of requiring the client to call status methods.


easyPVAJava (4.1.2)
--------------------

* EasyPVA automatically starts ChannelProvider for both Channel Access and pvAccess.
* EasyMultiChannel is now implemented
* Support for monitors is now available both for EasyChannel and EasyMultiChannel.


directoryService (0.4.2)
-----------------------

(No significant changes)


exampleJava (4.0.5)
------------------

(No significant changes)
