---
layout: page
title: HDF5 Files
permalink: /hdf5-files/
---

The Gadgetron framework is used to process many different types of data and it is cumbersome to add specific read and write routines for all these different kinds of data. Consequently we have chosen to use the generic HDF5 file format. A detailed description of this format can be found at <http://www.hdfgroup.org/HDF5/>.

The HDF5 file format is much like a file system. Data can be organized hierarchically into groups (like folders in a filesystem) and each file can contain multiple groups and datasets. Each dataset can be an array of any type, e.g. an array of images. There is a generic tool `hdfview` which can be used to view the files. It is available on all the platforms supported by the Gadgetron framework. HDF5 files can also be read easily in newer versions of Matlab.

As an example of a HDF5 file with MRI raw data can be found at <https://gadgetrondata.blob.core.windows.net/gadgetrongithubio/files/testdata/>. Download the file `gadgetron_testdata.h5`. When opened with `hdfview`, it should look like the figure below. As seen, the file contains 4 groups of data. Each group consists of some data and an XML configuration for the Gadgetron.

<img src="http://gadgetron.sf.net/figs/hdfview_mri_testdata.png" style="width: 400px;" />

HDF5 Files can also be used to store images. Several of the Gadgetron clients included with the framework save images in HDF5 files. An example of viewing the output of a reconstruction can be seen below.

<img src="http://gadgetron.sf.net/figs/hdfview_image_view.png" style="width: 400px;" />

Images saved by Gadgetron clients are saved as arrays in the HDF5 files. Due to the array storage conventions in the Gadgetron environment, the first dimension is the slowest varying dimension in the arrays and the last dimension is the fastest varying dimension. That means that an array with 10 images with dimensions 128x128 would be stored in a variable in the HDF5 file with dimensions 10x1x128x128 as seen above. 

To display the images, right click on the data and choose settings as illustrated below.

<img src="http://gadgetron.sf.net/figs/hdfview_image_view_setting.png" style="width: 400px;" />

The HDF5 files can also be read with Matlab. The images in the file above could be read with:

    >> images = h5read('out.h5','/2012-05-11 10:57:48/data_0');
    >> size(images)

    ans =

       128   128     1    10

    >> imagesc(images(:,:,1,1));colormap(gray) 
