# Open Science Software

## Rational/About
The purpose of this repository is to document and refine thoughts on open science software in the context of data centers.  We need to think about this because of directives from the US Federal Government and from NASA, as well as from other funding agencies.  We also need to think about this because open science is a good thing for science.

## What is software?
I am going to use a very broad definition of software as a set of instructions that is executed by a computer.  This includes programs written in low-level languages such as C, Fortran, etc; scripts written in Python, Julia, Perl, Matlab and IDL; executable notebooks used to explain processes, educate users and document workflows.  _Also include here makefiles, yaml files etc._

## Types of software
It is important to distinguish the different types of software.  Software is written for missions; to control spacecraft, manage on-board data collection, and the produce data products from Level-0 to Level-3.  Software is also wriiten to generate derived research datasets.  There are also software tools.  In the python ecosystem these are packages that can be imported and used by other scripts.  In C and Fortran these are libraries.  

- Mission software
- Software/Workflows to produce mission data products
- Software to produce research datasets
- Software to analyse these datasets and produce tables and figures for publications/reports
- Executable notebooks that describe how to work with data
- Executable notebooks used for education; e.g. how sea ice thickness is calculated.
- Executable notebooks that describe workflows
- Executable notebooks written as interactive papers _also include other forms of executable publications_
- Software packges _maybe specific to a dataset/domain or generic e.g `numpy`
- Software libraries

Within the context of data center it is likely that they will be mostly responsible for making available software used to produce data products (mission and research), and software to demontrate how to use and work with the data.  There may also be some tools.

## What is required to make software open?
- Clean code
- Use standard libraries/packages
- Good documentation
- Tests
- Containerized workflows
- Well documented dependancies
- A way to access the data.

## Maintaining Software
Who maintains research software?  
Who can contribute?  
Level of support.  
Open Source does not have to mean actively seeking input to projects.  Mission and research data product software will not be run by users.  No one (only a few maybe one person) is going to want to run the Sea Ice Index code locally.  Only the data will be used.  However, making the software/code public helps to document workflows and algorithms.  The code will be static and require little maintainance.  
Nadia Eghbal's Working in Public is a good a good intro the modern open source software and collaborative environments. Project structure are classified into Federations, Stadiums, Clubs and Toys based on User Growth and Contributor Growth.

|         | High User Growth | Low User Growth |
|---------|------------------|-----------------|
| **High Conributor Growth** | Federations (e.g. Rust) | Clubs (e.g. Astropy) |
| **Low Contributor Growth** | Stadiums (e.g. Babel) | Toys (e.g. ssh-chat) |

This table could be rewritten to reflect scientific software.  Federations are rare, active large contributor and large user community projects.  I think of clubs as hobby groups working on small but possibly impactful projects within a domain.  `icepyx` might be one example of a _Club_.  I don't like the term Toys, in this context, but code for publications and individual science projects might fit into the low user growth, low contributor growth quadrant.  Stadiums have few contributors but many users.  This might be a processing tool we host.

We can control the "Level of Service" and engagement based on software type and purpose.  In many cases we don't have to actively maintain code, as long as it runs without errors.  How easy it is to maintain depends on the code itself and the level of documentation.  If NSIDC is to maintain code, we need to ensure the code can be maintained without too much effort on our part.  Alternatively, we need to seek funding to refactor code to make it easily maintainable.

## Versioning and citation
Code needs to be versioned and each version associated with a dataset needs to have a unique identifier for citation.  
Github is a collaborative tool not an archive for code.  

## References
[USGS code types](https://github.com/emartinez-usgs/best-practices/blob/b44ccae73a3915eb644036ed37f004f8702fe71f/software/types.md)

Eghbal, N. (2020). Working in public: the making and maintenance of open source software (First Edition). San Francisco: Stripe Press.

