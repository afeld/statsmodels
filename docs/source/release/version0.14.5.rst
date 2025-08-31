:orphan:

==============
Release 0.14.5
==============

Release summary
===============

statsmodels is using github to store the updated documentation. Two version are available:

- `Stable <https://www.statsmodels.org/>`_, the latest release
- `Development <https://www.statsmodels.org/devel/>`_, the latest build of the main branch

**Warning**

API stability is not guaranteed for new features, although even in
this case changes will be made in a backwards compatible way if
possible. The stability of a new feature depends on how much time it
was already in statsmodels main and how much usage it has already
seen.  If there are specific known problems or limitations, then they
are mentioned in the docstrings.

Stats
-----
**Issues Closed**: 1

**Pull Requests Merged**: 2


The Highlights
==============
This patch release fixes an issue with recent SciPy releases (1.16+) that prevented 
statsmodels from importing. It also addresses some small changes that improve future 
compatibility.

The main fix removes the use of the private ``scipy._lib._util._lazywhere`` function
that was removed in SciPy 1.16.0, replacing it with equivalent functionality.


What's new - an overview
========================

There are no new features in release 0.14.5.


Major Bugs Fixed
================

**SciPy 1.16+ Compatibility**

- Fixed ``ImportError: cannot import name '_lazywhere'`` that occurred when trying to 
  import statsmodels with SciPy 1.16.0 or later. The fix removes dependency on the 
  private SciPy function and implements equivalent functionality directly.


Development summary and credits
===============================

Besides receiving contributions for new and improved features and for bugfixes,
important contributions to general maintenance for this release came from

- Kevin Sheppard

and the general maintainer and code reviewer

- Josef Perktold

Additionally, many users contributed by participation in github issues and
providing feedback.


Merged Pull Requests
--------------------

The following Pull Requests were merged since the last release:

- :pr:`9586`: MAINT: Remove lazywhere
- :pr:`9591`: Rls 0 14 5 notes