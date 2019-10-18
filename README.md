Cambridge Digital Communications Assessment Model (cdcam)
=========================================================

[![Documentation Status](https://img.shields.io/badge/docs-latest-brightgreen.svg)](http://ccam.readthedocs.io/en/latest/?badge=latest)
[![Build Status](https://travis-ci.org/nismod/digital_comms.svg?branch=master)](https://travis-ci.org/nismod/digital_comms)
[![Coverage Status](https://coveralls.io/repos/github/nismod/digital_comms/badge.svg?branch=master)](https://coveralls.io/github/nismod/digital_comms?branch=master)

Description
===========

The **Cambridge Digital Communications Assessment Model** is a decision support tool to
quantify the performance of national digital infrastructure strategies for mobile broadband,
focussing on 4G and 5G technologies.

Citations
---------

```
Oughton, E.J. and Frias, Z. (2017) The Cost, Coverage and Rollout Implications of 5G Infrastructure
in Britain. Telecommunications Policy. https://doi.org/10.1016/j.telpol.2017.07.009.

Oughton, E.J., Z. Frias, T. Russell, D. Sicker, and D.D. Cleevely. 2018. Towards 5G: Scenario-Based
Assessment of the Future Supply and Demand for Mobile Telecommunications Infrastructure. Technological
Forecasting and Social Change, 133 (August): 141–55. https://doi.org/10.1016/j.techfore.2018.03.016.

Oughton, E.J., Frias, Z., van der Gaast, S. and van der Berg, R. (2019) Assessing the Capacity,
Coverage and Cost of 5G Infrastructure Strategies: Analysis of The Netherlands. Telematics and
Informatics (January). https://doi.org/10.1016/j.tele.2019.01.003.
```

Setup and configuration
=======================

All code for **The Cambridge Communications Assessment Model** is written in Python
(Python>=3.5) and has a number of dependencies. See `requirements.txt` for a full list.

Using conda
-----------

The recommended installation method is to use [conda](http://conda.pydata.org/miniconda.html),
which handles packages and virtual environments, along with the `conda-forge` channel which has
a host of pre-built libraries and packages.

Create a conda environment called `cdcam`:

    conda create --name cdcam python=3.5

Activate it (run this each time you switch projects):

    conda activate cdcam

First, install required packages:

    conda install fiona shapely rtree pyproj

For development purposes, run this command once per machine:

    python setup.py develop

Install test/dev requirements:

    conda install pytest pytest-cov

The run the tests:

    pytest --cov-report=term --cov=cdcam tests/


Quick start
===========

If you want to quickly generate results run:

    python scripts/mobile_run.py

And then to visualize, install `pandas`, `matplotlib` and `seaborn`:

    conda install pandas matplotlib seaborn

Followed by running:

    python vis/vis.py


Background and funding
======================

The **Cambridge Digital Communications Assessment Model** has been collaboratively developed
between the [Environmental Change Institute](http://www.eci.ox.ac.uk/) at the [University of
Oxford](https://www.ox.ac.uk/), the [Networks and Operating Systems Group
(NetOS)](http://www.cl.cam.ac.uk/research/srg/netos) at the [Cambridge Computer
Laboratory](http://www.cl.cam.ac.uk),  and the UK's [Digital
Catapult](http://www.digtalcatapult.org.uk). Research activity between 2017-2018 also took
place at the [Cambridge Judge Business School](http://www.jbs.cam.ac.uk/home/) at the
[University of Cambridge](http://www.cam.ac.uk/).

Development has been funded by the EPSRC via (i) the [Infrastructure Transitions Research
Consortium](http://www.itrc.org.uk/) (EP/N017064/1) and (ii) the UK's [Digital
Catapult](http://www.digicatapult.org.uk) Researcher in Residence programme.

Contributors
============
- Edward J. Oughton (University of Oxford)
- Tom Russell (University of Oxford)
