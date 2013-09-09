% The Garden And the Meadow: Software Dissemination Strategies in Sustainable Scientific Computing
% Aron Ahmadia, U.S. Army Engineer Research and Development Center

This article is currently in public review for [WSSSPE](http://wssspe.researchcomputing.org.uk/).  Comments and discussion welcome at its [Issues](https://github.com/ahmadia/wssspe/issues) page. 

## Acknowledgements

Thanks to [Greg Wilson](http://third-bit.com/), [Jed Brown](http://59a2.org/research/), [Andy Terrel](http://andy.terrel.us/vita/), and [Patrick Wagstrom](http://academic.patrick.wagstrom.net/) for helpful discussion and contribution of several points.  This article was written collaboratively on [GitHub](https://github.com/ahmadia/wssspe).

## Introduction 

### The Scientific Software Infrastructure Ecosystem

Scientists spend a surprising amount of time developing and using software.  A [2009 survey study](http://dl.acm.org/citation.cfm?id=1556928) reported that scientists spend an average of 40% using software and 30% developing it.  A [2011 survey](http://liberty.princeton.edu/Publications/sc11_survey.pdf) conducted at Princeton reported a similar observation.  Despite this consumption of research effort, the [USA's National Science Foundation Advisory Committee for CyberInfrastructure Task Force on Software for Science and Engineering](https://www.nsf.gov/cise/aci/taskforces/TaskForceReport_Software.pdf) noted:

> [NSF-Funded scientific] software infrastructure has evolved organically and inconsistently, with its development and adoption coming largely as by-products of community responses to other targeted initiatives

Scientific software infrastructure encompasses the entire space of digital products which enable or accelerate scientific discovery.  Much of today's scientific software infrastructure is general-purpose, that is, it is not primarily designed for or used by scientists.  For example, there are very few components in today's most commonly used operating systems that are specifically intended for use by scientists.  Although it is commonly recognized that industry trends in hardware development drive scientific hardware infrastructure, industry trends in software infrastructure development have similar far-reaching effects on scientific software development.

### Cathedrals and Bazaars

In 1999, Eric S. Raymond released the essay ["The Cathedral and the Bazaar: Musings on Linux and Open Source by an Accidental Revolutionary"](http://www.catb.org/esr/writings/homesteading/).  The essay contrasted two different open source development models.  The first model, which was more common at the time, was the cathedral, characterized by long release cycles, single-developer or small development teams, and closed access to development repositories.  The new model, the bazaar, was characterized by short release cycles, community-driven development, and open access to development repositories.  The essay (and the underlying reality of the advantages of the bazaar model over the cathedral model) was incredibly influential in the open source movement.  Shortly afterward, many prominent open source projects such as GNU Emacs and GCC switched from the cathedral model to the bazaar model.

Unfortunately, many of the developers of open source scientific software seem to have missed this development.  A number of influential open source scientific software projects such as [CESM](http://www.cesm.ucar.edu/working_groups/Software/secp/repo/) and [FLASH](http://flash.uchicago.edu/site/flashcode/) still follow the cathedral model.  This essay is not about cathedrals and bazaars, however, the use of a metaphorical dichotomy is apt for describing another challenge for sustainable scientific software development.  This essay proposes defining this bifurcation in how software is digitally disseminated, either in the form of walled gardens, or freely accessible meadows.

### Gardens and Meadows

Today's digital marketplaces have undergone a steady revolution in distribution.  Audio, video, text, and software applications are increasingly distributed digitally, accompanied by a meandering trend towards increased digital rights and fewer restrictions.  Despite this, the majority of today's digital content exists in a metaphorical *garden*, it has been restricted from sharing, modification, or reuse.  A recent development in the licensing of digital media is the set of [Creative Commons Licenses](http://creativecommons.org/about), which provide a simple, standardized way to grant public permission to share and use digital content.  Media that is distributed with explicit permission for sharing, modification, and reuse exists in a *meadow*.  Today's most famous meadow is [Wikipedia](http://www.wikipedia.org/), a free encyclopedia licensed under the Creative Commons Attribution-ShareAlike License.  

Recently, there has been a strong push to move publicly funded research data and papers from gardens into meadows.  The most prominent collection of manuscripts in the scientific meadows is Cornell University Library's [arXiv](http://arxiv.org/), which accepts public domain, Creative Commons Attribution, and Attribution-Noncommercial-ShareAlike licensed content.  The arXiv also accepts articles that it has been granted a non-exclusive and irrevocable license to distribute.  Although this class of article does not completely meet the definition of a meadow, this compromise appears to be agreeable to most scholars, publishers, and curators.

Today's scientific software infrastructure, ranging from operating systems to shell scripts, can be similarly categorized into gardens and meadows.  We propose the following formal definition of a scientific software garden.  

### Garden

Any scientific software infrastructure that possesses either of the following two attributes is released 'into' a garden:

R1.  Access to inspect, modify, or use the software is restricted by a non-OSI license.  
R2.  Access to build or run the software is restricted to a non-freely available environment.  

### Meadow

Any scientific software infrastructure uninhibited by R1 or R2 is part of a meadow.

### Exemplars

There are many exemplars of both gardens and meadows in scientific computing infrastructure.  Starting at the level of operating systems, Windows and OS X are gardens, while Linux-based operating systems are usually meadows.  

At a slightly higher level, almost all numerical programming environments are released into meadows.  These range from traditional programming languages such as C, C++, and Fortran, to newer high-productivity languages such as [Chapel](http://chapel.cray.com/download.html), [X10](http://x10-lang.org/x10-development/building-x10-from-source.html), and [Julia](http://julialang.org/).  A notable exception is MATLAB, a commercial numerical computing environment that provides a garden-walled core engine and development environment, but strongly encourages contributions to [MATLAB Central](http://www.mathworks.com/matlabcentral/FX_transition_faq.html).  New contributions to MATLAB Central all satisfy R1.  If the contributions can be adapted to Octave or Scilab, two engines in the meadows that are compatible with much of the MATLAB language, they also satisfy R2 and have effectively been released into meadows. Two important final community projects in the meadows are the [Scientific Python stack](http://www.scipy.org/stackspec.html), and the [R](http://www.r-project.org/) programming language and development environment.  Beyond their core environments, both the R and Scientific Python communities possess a strong tradition of releasing into the meadows, with participation and support from both academia and industry.

In the closely related arena of software for mathematical analysis, Mathematica and Magma are two well-known examples of gardens.  [Sage](http://www.sagemath.org/) is a notable meadow in this domain, constructed as an amalgam of 89 other meadows, including many software packages from Scientific Python and R.

A final example of gardens and meadows in high performance computing comes from the recent emergence of heterogeneous computing languages.  An early notable heterogeneous computing language, Brook, was released as a meadow 2003.  Four years later, Nvidia released CUDA, strongly influenced by Brook, as a garden in 2007.  The OpenCL standard, which can be considered as a derivative alternative to the CUDA language, was released as a meadow in 2008.  

## Discussion

### The Importance of the Industrial Garden

Industrial gardens have demonstrated an important role in the dissemination of scientific research.  For example, the MATLAB programming environment has been transformational in the promotion of wide reuse of scientific software. [LAPACK](http://www.mathworks.com/company/newsletters/articles/matlab-incorporates-lapack.html), [FFTW](http://www.mathworks.com/help/matlab/ref/fftw.html) and [SuiteSparse](http://www.cise.ufl.edu/research/sparse/SuiteSparse/) are examples of meadows projects that have been incorporated into the MATLAB garden.   

### Limitations of the Garden

Unfortunately, software infrastructure developed within gardens (as opposed to being incorporated into them from meadows) have several limitations, most notably barriers to reuse.  A notable example is [CVX](http://cvxr.com/cvx/), a GPL-licensed MATLAB-based modeling system for disciplined convex programming.  Despite its free licensing, it is impossible to use CVX in embedded computers or massively parallel environments, or in any situation where MATLAB is not otherwise available.  Although there have been several attempts to reimplement CVX in other programming environments, CVX's advances in disciplined convex programming remain restricted to use within the MATLAB garden.

Beyond limitations to reuse, constrained access to software infrastructure decreases trust in algorithms and their implementations.  It is not sufficient to grant access to software restricted to temporary peer review.  Bugs are frequently found in software projects throughout their lifecycle.  Access to the source does not guarantee that a software is bug-free, but it does improve independent verification, and as a consequence, trust.  

The limitations in access to scientific software gardens also discourages the role of citizens in the development of sustainable scientific software infrastructure.  This is especially important because many scientists are not formally trained in even the basic principles of software engineering.  Scientific software infrastructure properly released into the meadows has been integrated into larger software projects, improving quality, reuse, and sustainability.  Beyond the earlier MATLAB examples, another notable example of this is the [LLVM](http://llvm.org/) compiler infrastructure project, which was released into the meadows as part of Chris Lattner's UIUC Master's thesis in 2003, and which has since gained significant industry support and use, including incorporation as the default compiler in new version of OS X.

## Closing Thoughts

Despite the growing success of the meadow model for scientific software dissemination, there remains a cultural entrenchment among many scientists to release their software into gardens.  This may be attributed to the negligence of funding bodies and review panels in rewarding the efforts of scientists who release scientific software into meadows.  It may also be attributed to several other reasons, several which have been outlined by Randy LeVeque in [Top Ten Reasons To Not Share Your Code (and why you should anyway)](http://www.siam.org/news/news.php?id=2064).  Broader attention to this issue is needed as part of our commitment to improving the sustainability of scientific infrastructure.

## Further Reading

[Troubling Trends in Scientific Software Use](http://www.sciencemag.org/content/340/6134/814)  
[Scientiﬁc software production: incentives and
collaboration](http://herbsleb.org/web-pubs/pdfs/howison-scientific-2011.pdf)  
[A Vision and Strategy for Software for Science, Engineering, and Education: Cyberinfrastructure Framework for the 21st Century](http://www.nsf.gov/publications/pub_summ.jsp?ods_key=nsf12113)  
[Best Practices for Scientific Computing](http://arxiv.org/pdf/1210.0530v3.pdf)
