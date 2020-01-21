---
title: Packaging
layout: info
---

### {{ page.title }}
{: .page-header}
[Back to Policies and Guidelines home](/radiuss/policies/)

---

#### Legend

[![generic badge](https://img.shields.io/badge/M.section-N-blue.svg)]() Designates a __mandatory__ point (policy).

[![generic badge](https://img.shields.io/badge/R.section-N-9cf.svg)]() Designates a __recommended__ point (guideline).

&nbsp;

---

[![Generic badge](https://img.shields.io/badge/M.pac-1-blue.svg)]() **Version and build characteristics must be easily accessible.**

**Details:** Each product API must include a way to return the current version number of the software and indicate which configure/CMake and compiler options were used to build the package. For development versions of the software, each package must provide the current commit ID in the repository.

**Rationale:** This allows users to make an inventory of what they have, which can aid debugging and configuration management. 

***Ref:** Smart Libraries Practice 10 / xSDK M8*

---

[![Generic badge](https://img.shields.io/badge/M.pac-2-blue.svg)]() **Use a limited, unique, and well-defined symbol, macro, library, and include file namespace.**

**Details:** For example, there should be no publicly visible include files with generic names such as `utils.h`, a package named `libutil.a`, or macros named YES or TRUE. Namespacing of include files can be handled either by prepending installed include files with a package name (e.g.,`<XXXutils.h>`) or by placing and referencing all installed include files in a subdirectory with a package name (e.g.,`<XXX/utils.h>`). 

**Rationale::** Library developers must recognize that their software will be built as part of much larger packages, and the use of generic names in the global namespace increases the chance that the user of your library will run into build- and link-time errors that must be worked around.

***Ref:** Smart Libraries Practice 18 / Less restrictive than xSDK M9*

---

[![Generic badge](https://img.shields.io/badge/M.pac-3-blue.svg)]() **Use MPI in a way that is compatible with other products.**

**Details:** Each library that utilizes MPI must restrict its MPI operations to MPI communicators that are provided to it and not use directly `MPI_COMM_WORLD`. Products must use configure tests or version tests to detect MPI 2 or MPI 3 features that may not be available; it should not be assumed that a full MPI 2 or MPI 3 implementation is available. Products can change the MPI error-handling mode by default but should have an option to prevent them from changing the MPI error handling (which may have been set by another package or the application). The product should also behave appropriately regardless of the MPI error handling being used.

***Ref:** xSDK M3.*

---