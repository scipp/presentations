# Oral Presentation - Scitiff

## Power Point File Location

It's under `/scipp_data/presentations/ICNS-imaging-ppt` in `NextCloud`.
It also has other png/mov or vector files used for the presentation.

## Demo

Demo notebooks are under `/scipp_data/presentations/ICNS-imaging-ppt/scitiff-demo`.

The notebook may need copying `small_ymir_images.hdf` from ess public file server.

# Poster Presentation - WFM

The PDF file is under `/scipp_data/presentations/ICNS25_Sun_Neil.pdf` in `NextCloud`.

# Report - After ICNS

> Author: Sun

It was interesting and motivating to see various fields of science that use neutron in different ways.

There are still a lot of work going on to improve existing neutron instruments and methodologies as well as exploring new novel ideas about utilizing full potential of each facilities.

I was mostly interested in biology topics and historical heritage studies.
There were also many different various topics.

I could categorize the session topics like below:

| Category | Topics(Fields) |
| -------- | -------------- |
| science - experiment methodology | Instrumentation, Facility Updates, Neutron Technologies, Sample Environments, Polarization |
| science - study subject | Functional Materials(?), Magnetic Structure/Materials, Food Science, Universe Essentials and Socienty, Quantum Chemistry, Spin Phonon, Membranes, Biology, Energy Research(like batteries), Electronic Properties, Superconductivity, Polymers |
| software - Algorithm/Dev/UI/UX | SW Design, Imaging SW Symposium, Magnetic SAS data analysis, ORSO, Tools for Coherent Excitations |
| politics | Facility Updates, Facility Roadmaps, User Needs |

**I went through the program and categorized the session titles. It may missing some and I didn't use exact same words if it has overlapping words or numberings. The full list is in their [web page](https://www.icns2025.dk/programme/final-programme)**

### Imaging Symposium Review - User Community Observation

An imaging experiment is very either simple as they only need a very rough structural information or they need extreme amout of information in a case like high resolution tomography.

Therefore I had an impression that there are two different expectations about data reduction SW performance:
  - No need of high performance(speed) as it would still be a fraction of time compared to the neturon exposure time itself. Preserving more precision and error-prone/easy-to-understand approach is more appreciated than faster processing.
  - GPU and parellel processing required. Otherwise can't process the data at all.

So often imaging technique users write their own disposable script or use existing pricy solutions.
There was no intermediate level of performance/code quality needed.
GPU/parellel processing is mandatory in some cases and not needed at all in other cases.

We had a chance to present our `scitiff` project as a sustainable strategy of data handling.
Another related talk was about using `scicat`.

The `scitiff` could draw positive interest(I think) from audiences there.

Here are some notes I took from the discussion about `scitiff`:
(It may also contain just my own interpretation/impression/opinion, not something we openly discussed about.)

  - I had to remind the audiences a couple times that `scitiff` is not a new tiff format and does not touch any low-level tiff format.
    It is merely adding a plain text metadata piggy-bagging on `ImageJ` metadata.
    The mission is to build a very easy human redable standard way of preserving physical dimension/information of the data that everyone can contribute in the community.
  - Some people may be using `scicat` to store such information but I think it's kind of abusing scicat.
  - It seems like people agree that we need something like `scitiff` at least, even if they don't use our solution.
  - There is a high demand of GUI based interface.

### WFM Poster session

I also presented the WFM stitching method using MC simulations in the poster session.

The poster was in a very dark corner in the end of the room but still had a few visitors :D

A couple of scientists were interested if we have validated the methodology with the real data. I think they didn't mean the validation of the software but the validation of the physical choppers if they work as nicely as the simulation.

It is indeed one of our requirements from instrument scientists.

There was another engineer/scientist from DTU Space who work on the chopper.
She was interested in our chopper simulation methods and visualization/analysis tools.
(I forgot what exactly we discussed about :D....)

### User Needs Meeting - Needs for Centralized Online Space for Neutron Community

In the `User Needs` meeting, there was a discussion about lacking centralized source of information for neutron community.

There are some newsletters for smaller part of neutron society or individual neutron facilities/instruments but there is no centralized online space for various smaller sources or different fields.

Some groups from different fields could benefit from other fields but it was not so easy for them to find relevant information.

Also, for a potential user, or someone who want to try neutron as their study methodology, will have an entry barrier as they have to know someone who have a good overview/understanding of neutron community/technology.

I think it should be big facilities obligation to maintain such space/information.

Someone pointed out that the smaller facilities were not acknowledged enough and closing one by one despite of their importance to the potential users and contribution to the community.

As ESS representative mentioned that we don't want a lot of users, but the right users, ESS maybe be maintaining the centralized online space for all neutron community so that any users can easily tell which facility/technique they can benefit from their science cases...?

There are not so many of neutron facilities in the world...!
