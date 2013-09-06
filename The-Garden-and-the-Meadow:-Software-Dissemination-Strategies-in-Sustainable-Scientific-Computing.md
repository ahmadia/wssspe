# The Garden and the Meadow: Software Dissemination Strategies in Sustainable Scientific Computing [DRAFT for Submission](http://wssspe.researchcomputing.org.uk/)

## Aron Ahmadia, U.S. Army Research and Development Center

## Acknowledgements

Thanks to [Greg Wilson](http://third-bit.com/), [Jed Brown](http://59a2.org/research/), [Andy Terrel](http://andy.terrel.us/vita/), and [Patrick Wagstrom](http://academic.patrick.wagstrom.net/) for helpful discussion and contribution of several points.

## Introduction 

### Scientific Software Infrastructure

Scientific software infrastructure encompasses the entire space of digital products which enable or accelerate scientific discovery.  Much of today's scientific software infrastructure is general-purpose, that is, it is not primarily designed for or used by scientists.  For example, there are very few components in today's most commonly used operating systems that are specifically intended for use by scientists.  Although it is commonly recognized that industry trends in hardware development drive scientific hardware infrastructure, industry trends in software infrastructure development have similar far-reaching effects on scientific software development.

### Cathedrals and Bazaars

In 1999, Eric S. Raymond released the essay ["The Cathedral and the Bazaar: Musings on Linux and Open Source by an Accidental Revolutionary"](http://www.catb.org/esr/writings/homesteading/).  The essay contrasted two different open source development models.  The first model, which was more common at the time, was the cathedral, characterized by long release cycles, single-developer or small development teams, and closed access to development repositories.  The new model, the bazaar, was characterized by short release cycles, community-driven development, and open access to development repositories.  The essay (and the underlying reality of the advantages of the bazaar model over the cathedral model) was incredibly influential in the open source movement.  Shortly afterward, many prominent open source projects (GNU Emacs, GCC)  switched from the cathedral model to the bazaar model.

Unfortunately, many of the developers of open source scientific software seem to have missed this development.  A number of influential open source scientific software projects such as [CESM](http://www.cesm.ucar.edu/working_groups/Software/secp/repo/) and [FLASH](http://flash.uchicago.edu/site/flashcode/) still follow the cathedral model.  This essay is not about cathedrals and bazaars, however, the use of a metaphorical dichotomy is apt for describing another challenge for sustainable scientific software development.  This essay examines and defines a bifurcation in how software is digitally disseminated, either in the form of walled gardens, or freely accessible meadows.

### Gardens and Meadows

Today's digital marketplaces have undergone a steady revolution in distribution.  Audio, video, text, and software applications are increasingly distributed digitally, accompanied by a meandering trend towards increased digital rights and fewer restrictions.  Despite this, the majority of today's digital content exists in a metaphorical *garden*, it has been restricted from sharing, modification, or reuse.  A recent development in the licensing of digital media is the set of [Creative Commons Licenses](http://creativecommons.org/about), which provide a simple, standardized way to grant public permission to share and use digital content.  Media that is distributed with explicit permission for sharing, modification, and reuse exists in a *meadow*.  Today's most famous meadow is [Wikipedia](http://www.wikipedia.org/), a free encyclopedia licensed under the Creative Commons Attribution-ShareAlike License.  

Recently, there has been a strong push to move publicly funded research data and papers from gardens into meadows.  The most prominent collection of manuscripts in the scientific meadows is Cornell University Library's [arXiv](http://arxiv.org/), which accepts public domain, Creative Commons Attribution, and Attribution-Noncommercial-ShareAlike licensed content.  The arXiv also accepts articles that it has been granted a non-exclusive and irrevocable license to distribute.  Although this class of article does not completely meet the definition of a meadow, this compromise appears to be agreeable to most scholars, publishers, and curators.

Today's scientific software infrastructure, ranging from operating systems to shell scripts, can be similarly categorized into gardens and meadows.  We propose the following formal definition of a scientific software garden.  

### Garden

Any scientific software infrastructure that possesses at least one of the following three attributes is released 'into' a garden:

R1.  Access to inspect, modify, or use the software is restricted by a non-OSI license.  
R2.  Access to build the software is restricted to a non-free environment.
R3.  Access to run the software is restricted to hardware supplied by a particular vendor.

### Meadow

Any scientific software infrastructure uninhibited by R1, R2, or R3 is part of a meadow.

## Some illustrating examples

### Numerical Computing Environments

#### Gardens

* MATLAB

#### Meadows

* Traditional Programming Languages (C, C++, Fortran)
* Octave
* Scilab
* Scientific Python Stack
* Julia

### Analytical Environments

#### Gardens

* Mathematica
* Magma

#### Meadows

* Sage

### Parallel Computing Interfaces

#### Gardens

* CUDA

#### Meadows

* MPI
* OpenMP
* OpenCL

### Debugging Environments

#### Gardens

* Totalview
* DDT

#### Meadows

* GDB

*Jed points to ParMETIS and TetGen as examples of walled gardens that are almost meadows.*

## Discussion

###
**GVW: right now, they're *all* effectively gardens because of lack of skills among scientists --- a meadow you can't get into is a garden as far as you're concerned.  Cf. Berlin's distinction between positive and negative liberty.**

### The importance of the garden

#### Allows industry to participate in the acceleration of scientific innovation

### The limitations of the garden

#### Decreases the impact of research funding by stifling reuse
#### Decreases trust in algorithms and implementations
#### Discourages citizen science
#### Discourages automation and integration 

## References

[Troubling Trends in Scientific Software Use](http://www.sciencemag.org/content/340/6134/814)
[Scientiﬁc software production: incentives and
collaboration](http://herbsleb.org/web-pubs/pdfs/howison-scientific-2011.pdf)
[A Vision and Strategy for Software for Science, Engineering, and Education: Cyberinfrastructure Framework for the 21st Century](http://www.nsf.gov/publications/pub_summ.jsp?ods_key=nsf12113)

