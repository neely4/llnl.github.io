---
title: RADIUSS Policies & Guidelines
layout: info
---

## {{ page.title }}
{: .page-header}

<!--
Prepared by LLNL under Contract DE-AC52-07NA27344.

This document was prepared as an account of work sponsored by an agency of the United States government. Neither the United States government nor Lawrence Livermore National Security, LLC, nor any of their employees makes any warranty, expressed or implied, or assumes any legal liability or responsibility for the accuracy, completeness, or usefulness of any information, apparatus, product, or process disclosed, or represents that its use would not infringe privately owned rights. Reference herein to any specific commercial product, process, or service by trade name, trademark, manufacturer, or otherwise does not necessarily constitute or imply its endorsement, recommendation, or favoring by the United States government or Lawrence Livermore National Security, LLC. The views and opinions of authors expressed herein do not necessarily state or reflect those of the United States government or Lawrence Livermore National Security, LLC, and shall not be used for advertising or product endorsement purposes.

LLNL-TR-781103

IM #975025
-->


#### About

The [RADIUSS](https://hpc.llnl.gov/radiuss) project promotes and supports a broad set of open source
software developed over many years at [Lawrence
Livermore National Laboratory (LLNL)](https://www.llnl.gov) for use
outside of their primary funding organization and within the broader
scientific research community. With these libraries and tools we
cover a wide range of features a team would need to develop a modern
scientific simulation code, particularly when targeting High Performance
Computing (HPC). Each of these products are used in applications that
support the LLNL science mission, and will be supported and
continuously developed for the foreseeable future. These are not
research projects that will simply vanish if a lead
developer finds other interests - but well-supported software backed
by programs and sponsors, and supplemented with support through the RADIUSS
project for broader use and external engagement.

As part of the RADIUSS project, these open source products 
follow a set of policies and guidelines (listed below) based on best
practices learned and adopted through years of research and
development supporting production software running on the
worlds largest supercomputers. Some of these policies were derived
directly or indirectly from other similar documents [^bss] [^xsdk] [^sl]
[^wsc] listed at the
bottom of this page. By sharing these policies publicly, we
hope to encourage others to adopt similar standards for the
betterment of the open source software community, and welcome a
[dialogue](mailto:radiuss-request@llnl.gov) on where we could
improve. 

These policies and guidelines are not meant to be a comprehensive set
of recommendations for good software quality assurance (SQA) practices
(although many of them do promote that). Instead, these are policies
that we feel are particularly important for developers of open source
software to follow. We strongly believe that open source software will
not succeed by just being "put out there". These policies are our
attempt to capture the things we feel are most important to a
successful open source project, beyond just good SQA practices that
any software engineer would promote.

We intend to continuously evolve these policies and guidelines
in the future. In particular, tools mentioned are not eternal and
best practices evolve rapidly, demanding flexibility in our approaches. However, we
attempted to make these recommendation as generic as possible, so that
they could apply to the various types of projects RADIUSS supports,
and likewise may serve to others. While we try not to interfere in project's
management, with found it important and relevant to focus our support
effort on a subset of fundamental tools, so that knowledge and
practices can easily be shared, and for the sake of interoperability.  

RADIUSS and the Projects it covers are open-source and primarily (or
by now, exclusively) use
[GitHub](https://github.com) for repository management. These policies and guidelines are
themselves part of the [GitHub repository](https://github.com/LLNL/llnl.github.io) that automates the
building and updating of [LLNL's Software
Portal](https://software.llnl.gov), to which you are welcome to submit an
issue or pull request to help us evolve these policies.

---

#### Legend
[![Generic badge](https://img.shields.io/badge/M.section-N-blue.svg)]() Designates a __Mandatory__ point (Policy)

[![Generic badge](https://img.shields.io/badge/R.section-N-9cf.svg)]() Designates a __Recommended__ point (Guideline)


---

>**Headline-only format follows. Click on any header or badge icon for more detailed description**

#### [Licensing](/radiuss/policies/licensing/)

[![Generic
badge](https://img.shields.io/badge/M.lic-1-blue.svg)](/radiuss/policies/licensing/)&emsp;New projects must use an [OSI](https://opensource.org/licenses)-approved, permissive open-source license (e.g., Apache, MIT, or BSD 3-Clause)

[![Generic badge](https://img.shields.io/badge/M.lic-2-blue.svg)](/radiuss/policies/licensing/) &emsp;Provide a list of dependencies and their associated licenses in SPDX format.

[![Generic badge](https://img.shields.io/badge/R.lic-3-9cf.svg)](/radiuss/policies/licensing/) &emsp;Consider moving to an [OSI](https://opensource.org/licenses)-approved, permissive open-source license for existing projects.

&nbsp;

#### [Documentation](/radiuss/policies/documentation)

[![Generic badge](https://img.shields.io/badge/M.doc-1-blue.svg)](/radiuss/policies/documentation/) &emsp;Publish documentation in a web-based form.

[![Generic badge](https://img.shields.io/badge/M.doc-2-blue.svg)](/radiuss/policies/documentation/) &emsp;Provide a concise description of the project.

[![Generic badge](https://img.shields.io/badge/M.doc-3-blue.svg)](/radiuss/policies/documentation/) &emsp;Version control documentation consistent with and alongside your source code.

[![Generic badge](https://img.shields.io/badge/M.doc-4-blue.svg)](/radiuss/policies/documentation/) &emsp;Provide a reliable way to contact the development team.

[![Generic badge](https://img.shields.io/badge/R.doc-5-9cf.svg)](/radiuss/policies/documentation/) &emsp;Produce Web and PDF documentation from a readable plain-text format.

[![Generic badge](https://img.shields.io/badge/R.doc-6-9cf.svg)](/radiuss/policies/documentation/) &emsp;Provide and maintain example codes along with documentation.

&nbsp;

#### [Build](/radiuss/policies/build)

[![Generic badge](https://img.shields.io/badge/M.bui-1-blue.svg)](/radiuss/policies/build/) &emsp;Package your installation and provide automated builds of dependencies via ([Spack](https://spack.io/)).

[![Generic badge](https://img.shields.io/badge/R.bui-2-9cf.svg)](/radiuss/policies/build/) &emsp;Compilable projects (e.g. those written in C++ and/or Fortran) must be buildable with [CMake](https://cmake.org). 

[![Generic badge](https://img.shields.io/badge/R.bui-3-9cf.svg)](/radiuss/policies/logging-debugging/) &emsp;Provide build options for production (optimized) and debug deployments.

&nbsp;

#### [Version Control](/radiuss/policies/version-control)

[![Generic badge](https://img.shields.io/badge/M.ver-1-blue.svg)](/radiuss/policies/version-control/) &emsp;The source code must be version controlled using [Git](https://git-scm.com).

[![Generic badge](https://img.shields.io/badge/M.ver-2-blue.svg)](/radiuss/policies/version-control/) &emsp;Provide a transparent, online contribution process based on pull requests and issues collection.

&nbsp;

#### [Testing and Continuous Integration](/radiuss/policies/tests-ci)

[![Generic badge](https://img.shields.io/badge/M.tes-1-blue.svg)](/radiuss/policies/tests-ci/) &emsp;Use regression tests in the development process.

[![Generic badge](https://img.shields.io/badge/M.tes-2-blue.svg)](/radiuss/policies/tests-ci/) &emsp;Provide a test suite for verifying correctness of build and installation.

[![Generic badge](https://img.shields.io/badge/M.tes-3-blue.svg)](/radiuss/policies/tests-ci/) &emsp;Provide a development test suite along with the source code for external contributors.

[![Generic badge](https://img.shields.io/badge/M.tes-4-blue.svg)](/radiuss/policies/tests-ci/) &emsp;Use continuous integration (CI).

[![Generic badge](https://img.shields.io/badge/R.tes-5-9cf.svg)](/radiuss/policies/tests-ci/) &emsp;Continuously check compatibility with different compilers and versions.

[![Generic badge](https://img.shields.io/badge/R.tes-6-9cf.svg)](/radiuss/policies/tests-ci/) &emsp;Ensure code quality/health in an automated manner.

&nbsp;

#### [Portability](/radiuss/policies/portability)

[![Generic badge](https://img.shields.io/badge/M.por-1-blue.svg)](/radiuss/policies/portability/) &emsp;Give best effort at portability to common HPC platforms and compiling toolchains.

[![Generic badge](https://img.shields.io/badge/R.por-2-9cf.svg)](/radiuss/policies/portability/) &emsp;Support Apple MacOS (Xcode) and Microsoft Windows (Visual Studio).

&nbsp;

#### [Packaging](/radiuss/policies/packaging)

[![Generic badge](https://img.shields.io/badge/M.pac-1-blue.svg)](/radiuss/policies/packaging/) &emsp;Version and build characteristics must be easily accessible.

[![Generic badge](https://img.shields.io/badge/M.pac-2-blue.svg)](/radiuss/policies/packaging/) &emsp;Use a limited, unique, and well-defined symbol, macro, library, and include file namespace.

[![Generic badge](https://img.shields.io/badge/M.pac-3-blue.svg)](/radiuss/policies/packaging/) &emsp;Use MPI in a way that is compatible with other products.

&nbsp;

---

#### References

[^bss]: [Better Scientific Software](https://bssw.io)
[^xsdk]: [xSDK Community Policies](https://xsdk.info/policies)
[^sl]: [Smart Libraries: Best SQE Practices for Libraries with Emphasis on Scientific Computing](https://www.osti.gov/biblio/936460)
[^wsc]: [Weapons Simulation and Computing (WSC) Software Guildelines](https://lc.llnl.gov/confluence/display/WSCSOFT/WSC+Software+Guidelines) (internal LLNL access only)