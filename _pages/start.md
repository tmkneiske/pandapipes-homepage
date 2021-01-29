---
layout: single
title: Getting Started
permalink: /start/
author_profile: false
toc: true
toc_sticky: true
toc_label: <a href="#site-nav">Getting Started</a>
classes:
   - wide
---


## Installing pandapower

For the installation of pandapipes it is necessary to install pandapower first. For the installation please follow the detailed instructions which can be found on the [pandapower website](http://www.pandapower.org/start/). 



<h2 id="install">Installing pandapipes</h2>
        
<h3 id="pip">Through pip</h3>

The easiest way to install pandapipes is through pip:

1. Open a command prompt (e.g. start --> cmd on windows systems)

2. Install pandapipes by running:

        pip install pandapipes

<h3 id="nopip">Without pip</h3>

If you don't have internet access on your system or don't want to use pip for some other reason, pandapipes can also be installed without using pip:

1.  Download and unzip the current pandapipes distribution from [PyPi](https://pypi.org/project/pandapower/) under "Download files".
2.  Open a command prompt (e.g. start --> cmd on windows systems) and navigate to the folder that contains the setup.py file with the command cd
    \<folder\> :

        cd %path_to_pandapipes%\pandapipes-x.x.x\

3.  Install pandapipes by running :

        python setup.py install

<h3 id="develop">Development Version</h3>

To install the latest development version of pandapipes from [github](https://github.com/e2nIEE/pandapipes), simply follow these steps:

1. Download and install [git](https://git-scm.com). 

2. Open a git shell and navigate to the directory where you want to keep your pandapipes files.

3. Run the following git command:

        git clone https://github.com/e2nIEE/pandapipes.git

4. Navigate inside the repository and check out the develop branch:

        cd pandapipes
        git checkout develop
       
5. Open a command prompt (cmd or anaconda command prompt) and navigate to the folder where the pandapipes files are located. Run:

        pip install -e .
        
   This registers your local pandapipes installation with pip.
        
## Test your installation <a name="test"></a>

A first basic way to test your installation is to import all pandapower submodules to see if all dependencies are available:

    import pandapipes
    import pandapipes.plotting
    import pandapipes.timeseries
    import pandapipes.networks
    import pandapipes.io
    import pandapipes.control
    import pandapipes.component_models
    
   
If you want to be really sure that everything works fine, run the pandapower test suite:

1.  Install pytest if it is not yet installed on your system:

        pip install pytest

2. Run the pandapower test suite:

        import pandapipes.test
        pandapipes.test.run_tests()

If everything is installed correctly, all tests should pass or xfail (expected to fail).


## A short introduction <a name="intro"></a>

A network in pandapipes is represented in a pandapipesNet object, which
is a collection of pandas Dataframes. Each dataframe in a pandapipesNet
contains the information about one pandapipes element, such as pipe,
junction, sink, etc.

We consider the following simple example network as a minimal
example:

<center><img src="{{"/images/getting_started/simple_network.png" | relative_url }}" alt="" /></center>

### Creating a network

The above network can be created in pandapipes as follows:

    import pandapipes as pp
    #create empty net
    net = pp.create_empty_network(fluid="lgas")

    #create junctions
    j1 = pp.create_junction(net, pn_bar=1.05, tfluid_k=293.15, name="Junction 1")
    j2 = pp.create_junction(net, pn_bar=1.05, tfluid_k=293.15, name="Junction 2")
    j3 = pp.create_junction(net, pn_bar=1.05, tfluid_k=293.15, name="Junction 3")

    #create junction elements
    ext_grid = pp.create_ext_grid(net, junction=j1, p_bar=1.1, t_k=293.15, name="Grid Connection")
    sink = pp.create_sink(net, junction=j3, mdot_kg_per_s=0.045, name="Sink")

    #create branch elements
    pipe = pp.create_pipe_from_parameters(net, from_junction=j1, to_junction=j2, length_km=0.1, diameter_m=0.05, name="Pipe")
    valve = pp.create_valve(net, from_junction=j2, to_junction=j3, diameter_m=0.05, opened=True, name="Valve")



The pandapipes representation now looks like this:

<img src="{{"/images/getting_started/pandapipes_results.png" | relative_url }}" alt="" />


### Running a Pipe Flow

A pipeflow can be carried out with the [pipeflow function](https://pandapipes.readthedocs.io/en/latest/pipeflow/run.html):

    pp.pipeflow(net)

When a pipeflow is run, pandapipes combines the information of all
element tables and calculates the current state of the network. Afterwards, results are written into the
result tables.


This minimal example is also available as a [jupyter notebook].

  [jupyter notebook]: https://github.com/e2nIEE/pandapipes/blob/master/tutorials/Minimal%20Example.ipynb


  
## Interactive Tutorials <a name="tutorials"></a>

There are jupyter notebook tutorials on different functionalities of pandapipes. They can be viewed as static
tutorials on GitHub or as interactive tutorials via Binder. Interactive tutorials take a moment to load.

Pandapipes provides different calculation modes and, depending on the task you want to apply pandapipes to, you
will not have to do all tutorials. Read the following descriptions in order to determine the tutorials which
are important for you.

<b>Static hydraulic calculations:</b>

The tutorials linked in this section describe how pandapipes can be used to calculate the pressure and
velocity distribution in a network in case of static boundary conditions. Examples are given for compressible and incompressible 
media. Because every other calculation includes the calculation of network hydraulics, this section is a good
place to begin:

   -  Minimal example hydraulic calculation ([static](https://github.com/e2nIEE/pandapipes/blob/master/tutorials/minimal_example.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/minimal_example.ipynb))
   -  Creating a simple gas or water network ([static](https://github.com/e2nIEE/pandapipes/blob/master/tutorials/creating_a_simple_network.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/creating_a_simple_network.ipynb))
   -  Working with height differences ([static](https://github.com/e2nIEE/pandapipes/blob/develop/tutorials/height_difference_example.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/height_difference_example.ipynb))
   
Some tutorials on the calculation of network hydraulics are also available in German:

 -  Einfache Netzwerke in pandapipes modellieren ([static](https://github.com/e2nIEE/pandapipes/blob/master/tutorials/ein_einfaches_netz_erstellen.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/ein_einfaches_netz_erstellen.ipynb.ipynb))
 -  Modellieren mit Höhendifferenzen ([static](https://github.com/e2nIEE/pandapipes/blob/master/tutorials/höhendifferenzen.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/höhendifferenzen.ipynb.ipynb))

<b>Static thermal calculations:</b>

If not only network hydraulics are of interest, but also temperature values along the pipes and nodes have to be known,
you can have a look at the following tutorial:

   -  How to calculate pipe temperature ([static](https://github.com/e2nIEE/pandapipes/blob/master/tutorials/temperature_calculation.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/temperature_calculation.ipynb))
   
In the special case of a district heating grid, the fluid flows in a closed loop. Heat is extracted by the consumers
of the district heating network, which can be modeled in pandapipes with heat exchangers. To model flow in a closed
loop, pandapipes provides a special kind of pump, which is introduced in this tutorial:

   -  Circular flow in a district heating grid ([static](https://github.com/e2nIEE/pandapipes/blob/develop/tutorials/Circular%20flow%20in%20a%20district%20heating%20grid.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=%2Ftutorials%2FCircular%20flow%20in%20a%20district%20heating%20grid.ipynb))

<b>Quasistatic timeseries calculations:</b>

With pandapipes, quasistatic processes can be modeled. For example, a timeseries describing values of an extracted
mass flow over several time steps can be read. For each time step value, a pandapipes calculation is done automatically.
A tutorial describing the basic setup of these calculations can be found here:

   -  Simple timeseries example: ([static](https://github.com/e2nIEE/pandapipes/blob/develop/tutorials/simple_time_series_example.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/simple_time_series_example.ipynb))

<b>Coupled pandapower-pandapipes simulations:</b>

This tutorial shows how to use pandapipes in combination with pandapower to solve a time-dependent
sector coupling application. Also, a German version is available:

   -  Introduction to coupled simulation of power and gas networks (multinet) ([static](https://github.com/e2nIEE/pandapipes/blob/develop/tutorials/coupled_nets_h2_p2g2p.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/coupled_nets_h2_p2g2p.ipynb))
   -  German version of tutorial for coupled simulations ([static](https://github.com/e2nIEE/pandapipes/blob/develop/tutorials/multienergienetze.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/multienergienetze.ipynb))
   
<b>Miscellaneous:</b>   
   
In this last section, you can find tutorials on auxiliary functions which are useful for all pandapipes users:
   -  Introduction to Plotting ([static](https://github.com/e2nIEE/pandapipes/blob/master/tutorials/simple_plot.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=tutorials/simple_plot.ipynb))
   -  Standard type and fluid library ([static](https://github.com/e2nIEE/pandapipes/blob/develop/tutorials/standard_libraries.ipynb) / [interactive](https://mybinder.org/v2/gh/e2nIEE/pandapipes/master?filepath=%2Ftutorials%2Fstandard_libraries.ipynb))
   





