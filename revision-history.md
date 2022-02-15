---
layout: page
title: Revision History
permalink: /revision-history/
---

### Version 2.5

Version 2.5 contains a number of extension and enhancements to the Gadgetron. In particular, a toolbox, named Gadgetron Plus or GtPlus is added to the package. GtPlus toolbox implements the complete reconstruction workflow for ISMRMRD data format and different parallel imaging modes (embedded, interleaved, seperate etc.). Multiple linear and non-linear reconstruction algorithms are implemented in this toolbox. The data accumulation and reconstruction triggering scheme are extended to support on-the-fly reconstruction. Another major extension is to extend the Gadgetron to support cloud computing. This feature is named as GtPlus Cloud. A non-exhaustive list of changes can be found below:

-   The GadgetMessageAcquisition, GadgetMessageImage, etc. (previously used to describe MRI raw data and images) have been replaced with the corresponding classes from the ISMRMRD library.

-   There is now a Gadgetron configuration file (`gadgetron.xml`) used to control the port number of the Gadgetron when starting. That makes it easier to maintain the same port for a given installation without supplying it on the command line.

-   The dependency on TinyXML has been almost entirely removed. We are now using a class representations of headers and configuration generated with CodeSynthesis XSD (<http://www.codesynthesis.com/products/xsd/>).

-   All XML representations now have schema definitions to make it easier to validate configuration files etc.

-   New toolbox functionality.

-   Various bug fixes.

-   Note in particular that we now use 'size_t' to denote [NDArray](https://gadgetron.github.io/api_master//class_gadgetron_1_1_n_d_array.html) dimension sizes etc. Users writing custom gadgets will need to update their code accordingly.

### Version 2.0

Mainly numerous interface changes and upgrades to the toolboxes. 
Much new functionality for systems without a GPU.

### Version 1.1

Version 1.1 contains multiple bug fixes, optimizations and some structural changes. Most notably, the Gadgetron now uses the proposed ISMRM Raw Data format (<http://ismrmrd.github.io>) throughout the MRI specific Gadgets. A non-exhaustive list of changes can be found below:

-   The GadgetMessageAcquisition, GadgetMessageImage, etc. (previously used to describe MRI raw data and images) have been replaced with the corresponding classes from the ISMRMRD library.

-   There is now a Gadgetron configuration file (`gadgetron.xml`) used to control the port number of the Gadgetron when starting. That makes it easier to maintain the same port for a given installation without supplying it on the command line.

-   The dependency on TinyXML has been almost entirely removed. We are now using a class representations of headers and configuration generated with CodeSynthesis XSD (<http://www.codesynthesis.com/products/xsd/>).

-   All XML representations now have schema definitions to make it easier to validate configuration files etc.

-   New toolbox functionality.

-   Various bug fixes.

### Version 1.0

First release of the Gadgetron
