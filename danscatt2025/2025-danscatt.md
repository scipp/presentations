# ESS data reduction software overview

As European Spallation Source(ESS) is built in Lund,
data reduction software for ESS is developed at DMSC in Copenhagen.
Data reduction team(scipp) has built Python packages to support various instruments at ESS.
Those packages supports various scopes, which are data reduction applications for certain techniques,
or arbitrary data reduction for neutron experiments or even general data manipulation. This poster will show
our software from lower-level lower level data structure/computation cores to higher level applications.

## ESS*packages

| category | project name | description |
| -------- | ------------ | ----------- |
| Scientific SW Core | scipp | `Scipp` is the core project of all our data reduction software. <br>`Scipp` enriches raw NumPy-like multi-dimensional arrays of data by adding named dimensions and associated coordinates. Generic functionality of `Scipp` is provided in the scipp Python package. In addition, more specific functionality is made available in other packages below. [^1]  |
| Scientific SW Core | plopp | `plopp` supports scientific visualization using `scipp`. It provides various visualization from simple histogram to 3d instrument view and widgets with simple user interfaces. |
| Scientific SW Core | sciline | sciline is a workflow framework
using type hint based dependency injection. It comes with graph based workflow visualization and helps us to develop various workflows in a consistent way. |
| Generic Neutron Experiment Libraries | scippneutron | (scippneutron) hosts neutron related data structure and computation functionalities. For example, time-of-flight transformation to Q or (h,k,l) vectors. As ESS provides long-pulse source, scippneutron also have chopper tools that can be used to calculate more accurate wavelength from time of arrival. |
| Generic Neutron Experiment Libraries | scippnexus | (scippnexus) is an IO interface between scipp data structure and NeXus(hdf5) files. <br> Scippnexus can load neutron event data along with corresponding static information such as pixel geometries. |
| Generic Neutron Experiment Libraries | essreduce | (essreduce) provides generic workflows of neutron experiments data reduction dedicated to ESS. The generic workflows can be extended to be instrument/technique specific workflows. |
| Technique/Instrument Specific Data Reduction Libraries | ess* | The ess* packages provide instrument of technique specific functionalities. Some instruments are supported as a sub package of a technique specific packge. i.e. loki is under esssans. Here is the list of early instruments that each package supports. Some of packages also host workflows for external instruments out of ESS. |
| Technique/Instrument Specific Data Reduction Libraries | essreflectometry | ESTIA, OFFSPEC |
| Technique/Instrument Specific Data Reduction Libraries | essdiffraction | DREAM, POWGEN(SNS)  |
| Technique/Instrument Specific Data Reduction Libraries | esssans | LoKI, Sans2D(ISIS), ZOOM(ISIS) |
| Technique/Instrument Specific Data Reduction Libraries | essimaging | ODIN, Test Beam Line, YMIR |
| Technique/Instrument Specific Data Reduction Libraries | essnmx | NMX |
| Technique/Instrument Specific Data Reduction Libraries | essspectroscopy | BIFROST |
| Technique/Instrument Specific Data Reduction Libraries | esspolarization | Any instruments that can be used for polirization experiments. |
| Generic ESS Data Reduction Applications | beamlime | `beamlime` is a real time data reduction application that will be available for ESS experiments. It allows users to grab a better understanding of the current data acquisition at a glance. |
| Interface with Ohter Services | scitacean | Scitacean is a high level Python package for downloading and uploading datasets from and to SciCat.|
| Interface with Ohter Services | scitiff | Scitiff is a neutron imaging tiff format and metadata schema that also provides python IO interfaces. |

[^1]: https://scipp.github.io
