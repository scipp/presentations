# ESS data reduction software overview

As the European Spallation Source (ESS) is built in Lund,
data reduction software for ESS is developed at DMSC in Copenhagen.
Here is an overview of various software packages that our Data reduction team has built to support various instruments at ESS and other neutron source experiments data reduction.

| category | project name | description |
| -------- | ------------ | ----------- |
| Scientific SW Core | scipp | `Scipp` is the core project of all our data reduction software. <br>- Numpy like multi dimensional arrays data structure and computational functionalities<br>- Physical units and coordinates<br>- Physical properties propagation along computation (units, errors, masks, etc... only if possible)<br>- Flexible binning of data without losing original information<br>- String formatting and HTML data representation (can be rendered in jupyter notebooks)|
| Scientific SW Core | plopp | `plopp` - Scientific visualization tool (using `scipp`).<br>- Various automatic plotting (1,2,3d histogram, line plots etc...)<br>- Ipywidgets (data slicer, 3d instrument view)|
| Scientific SW Core | sciline | sciline - Workflow framework for consistent way of data reduction routine development.<br>- Type-hint-based dependency injection.<br>- Visualization of workflow as a graph.<br>- Reproducibility support.|
| Generic Neutron Experiment Libraries | scippneutron | - (scippneutron) Neutron related data structure and computation functionalities.<br>- Neutron related coordinate transformation graphs, <br>i.e. time-of-flight transformation to wavelength, Q, (h,k,l), etc...<br>- Chopper data structure, visualization and computation tools for long pulse|
| Generic Neutron Experiment Libraries | scippnexus | - (scippnexus) Python IO interface between scipp data structure and NeXus(hdf5) files <br>- Loading dataset with physical attributes using scipp data structure<br>- Loading neutron event data (NXevent) along with corresponding static information<br>- Resolving transformation chains (NXtransformation)<br>- Coordinate based data slicing|
| Generic Neutron Experiment Libraries | essreduce | - (essreduce) Generic data reduction workflows dedicated to ESS. The generic workflows can be extended to be instrument/technique specific workflows. |
| Technique/Instrument Specific Data Reduction Libraries | ess* | The ess* packages provide instrument/technique specific functionalities and workflows. Some instruments are supported by a sub package of a higher level technique specific packge. i.e. loki is under esssans. Here is the list of early ESS instruments/techniques that each package supports. Many of packages can save reduced data into relevant format. <br>*Some of packages also has example workflows for external instruments out of ESS in the documentation <br>*Some instruments uses multiple ess* packages if they use multiple techniques. i.e. esspolarization will be used by all instruments that provide polarization experiments. |
| Technique/Instrument Specific Data Reduction Libraries | essreflectometry | ESTIA, OFFSPEC |
| Technique/Instrument Specific Data Reduction Libraries | essdiffraction | DREAM |
| Technique/Instrument Specific Data Reduction Libraries | esssans | LoKI |
| Technique/Instrument Specific Data Reduction Libraries | essimaging | ODIN, Test Beam Line, YMIR |
| Technique/Instrument Specific Data Reduction Libraries | essnmx | NMX |
| Technique/Instrument Specific Data Reduction Libraries | essspectroscopy | BIFROST |
| Technique/Instrument Specific Data Reduction Libraries | esspolarization | Any instruments that can be used for polirization experiments. |
| Generic ESS Data Reduction Applications | beamlime | - Real time data reduction framework/application.<br>- Real time visualization of event counts along physical coordinates<br>- Visualization integrated in NICOS<br>- Selection of region of interest |
| Interface with Ohter Services | scitacean | -  High level Python package for down/uploading datasets from/to SciCat|
| Interface with Ohter Services | scitiff | - (Scitiff) Neutron imaging tiff format and metadata schema |

[^1]: https://scipp.github.io
