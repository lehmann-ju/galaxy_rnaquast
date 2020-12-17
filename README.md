# Implementation of rnaQUAST to Galaxy

Introduction
============

Galaxy is a webbased scientific workflow system that aims to make computational 
biology accessible to scientist without experience in computer programming or 
systems administration. They provide a graphical user interface for every tool where 
you can specifying what data to operate on and the steps and order to execute it. 
Galaxy supporting extension with additional tools (often wrappers for existing command
line tools) and datatypes. See http://www.galaxyproject.org/ and the publicserver at 
http://usegalaxy.org for an example.

The quality assessment tool rnaQUAST for de novo transcriptome assemblies 
evaluates the RNA-Sequence assemblies quality. Also it benchmarks transcriptome 
assemblers by using a reference genome and a gene database. Therefore it calculates 
various metrics that demonstrate the completness and correctness levels of the 
assembled transcripts. To get more informations about this tool see  
https://doi.org/10.1093/bioinformatics/btw218 and for the source code of rnaQUAST
https://github.com/ablab/rnaquast.

This repository is for the development of the main Galaxy toolintegration of rnaQUAST.

Also it is used as an pilot for software publication. If you are interessted in these 
steps see PUBLICATION.md.

Galaxy wrapper for rnaQUAST
===========================

The main focus of this work is the development of the rnaQuast wrapper for Galaxy, 
published on the Galaxy Tool Shed here:

* https://toolshed.g2.bx.psu.edu/view/iuc/rnaquast/33c060ec0ac9

Development test releases are on the Test Tool Shed here:

* https://testtoolshed.g2.bx.psu.edu/view/iuc/rnaquast/daebbd8ec767

The associated development is on GitHub at:

* https://github.com/lehmann-ju/galaxy_rnaquast/tree/main

There are already some open Galaxy servers which are running rnaQUAST:

* https://usegalaxy.eu/

* https://singlecell.usegalaxy.eu/

Folder Structure
================

Within the ``test-data`` folder is some sample data which is needed for testing of the 
tool. You also need this section for Planemo lint and Planemo test.

Planemo is a command line assist while developing Galaxy artifacts like tools, workflows 
and training materials. Withing planemo you can lint or test your tool. To reach a stable 
release of the toolintegration of rnaQUASt, a github workflow for linting and testing is 
added in the folder ``.github/workflows``. These workflow also add the tool to the toolshed, 
if the tests were successfull. To get to know planemo look at https://planemo.readthedocs.io/.


