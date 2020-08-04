---
layout: single
permalink: /about/
title: About pandapipes
author_profile: false
toc: true
toc_sticky: true
toc_label: <a href="#site-nav">About pandapipes</a>
classes:
  - wide   
gallery:
  - url:        /images/about/validation/cross.png
    image_path: /images/about/validation/cross.png
    title:      "cross"
  - url:        /images/about/validation/delta.png
    image_path: /images/about/validation/delta.png
    title:      "delta"
  - url:        /images/about/validation/delta_2sinks.png
    image_path: /images/about/validation/delta_2sinks.png
    title:      "delta with 2 sinks"
  - url:        /images/about/validation/district.png
    image_path: /images/about/validation/district.png
    title:      "district"
  - url:        /images/about/validation/H-net.png
    image_path: /images/about/validation/H-net.png
    title:      "H-net"
  - url:        /images/about/validation/one_pipe.png
    image_path: /images/about/validation/one_pipe.png
    title:      "one pipe"
  - url:        /images/about/validation/heat_case_delta.png
    image_path: /images/about/validation/heat_case_delta.png
    title:      "heat case delta"
  - url:        /images/about/validation/heat_case_heights.png
    image_path: /images/about/validation/heat_case_heights.png
    title:      "heat case heights"
  - url:        /images/about/validation/heat_case_t_cross.png
    image_path: /images/about/validation/heat_case_t_cross.png
    title:      "heat case t-cross"
  - url:        /images/about/validation/heat_case_two_pipes.png
    image_path: /images/about/validation/heat_case_two_pipes.png
    title:      "heat case two pipes"
  - url:        /images/about/validation/heights.png
    image_path: /images/about/validation/heights.png
    title:      "heights"
  - url:        /images/about/validation/mixed_net.png
    image_path: /images/about/validation/mixed_net.png
    title:      "mixed net"
  - url:        /images/about/validation/one_source.png
    image_path: /images/about/validation/one_source.png
    title:      "one source"
  - url:        /images/about/validation/pump.png
    image_path: /images/about/validation/pump.png
    title:      "one pump"
  - url:        /images/about/validation/section_variation.png
    image_path: /images/about/validation/section_variation.png
    title:      "variation of pipe-sections"
  - url:        /images/about/validation/two_pumps.png
    image_path: /images/about/validation/two_pumps.png
    title:      "two pumps"
  - url:        /images/about/validation/valves.png
    image_path: /images/about/validation/valves.png
    title:      "valves"
  - url:        /images/about/validation/parallel.png
    image_path: /images/about/validation/parallel.png
    title:      "parallel"
  - url:        /images/about/validation/pumps.png
    image_path: /images/about/validation/pumps.png
    title:      "pumps"
  - url:        /images/about/validation/square.png
    image_path: /images/about/validation/square.png
    title:      "square"
  - url:        /images/about/validation/strand_net.png
    image_path: /images/about/validation/strand_net.png
    title:      "strand net"
  - url:        /images/about/validation/strand_net_stanet.png
    image_path: /images/about/validation/strand_net_stanet.png
    title:      "strand net of STANET"
  - url:        /images/about/validation/t-cross_1.png
    image_path: /images/about/validation/t-cross_1.png
    title:      "t-cross 1"
  - url:        /images/about/validation/t-cross_2.png
    image_path: /images/about/validation/t-cross_2.png
    title:      "t-cross 2"
  - url:        /images/about/validation/two_pipes.png
    image_path: /images/about/validation/two_pipes.png
    title:      "two pipes"
  - url:        /images/about/validation/two_pipes_two_ext_grid.png
    image_path: /images/about/validation/two_pipes_two_ext_grid.png
    title:      "two pipes with two external grids"
  - url:        /images/about/validation/two_valves.png
    image_path: /images/about/validation/two_valves.png
    title:      "two valves"
  - url:        /images/about/validation/versatility_gas.png
    image_path: /images/about/validation/versatility_gas.png
    title:      "versatility gas"
  - url:        /images/about/validation/versatility_water.png
    image_path: /images/about/validation/versatility_water.png
    title:      "versatility water"
---

pandapipes is an easy to use network calculation program aimed at automation of analysis of district heating
and gas systems. It utilizes the data analysis library pandas and is also closely related to
the power systems calculation program pandapower.

pandapipes and pandapower can be used in combination to analyze multi energy networks. An environment able to couple both
tools is pandapowerpro.

## Why another tool?

**Motivation**<br>

Multi-Energy networks and the utilization of synergies between energy sectors are an important research topic today. To
simulate these networks, it is crucial to not only include coupling points between the sectors in the analysis, but also to
know the network state of sectors of interest. pandapipes was developed to provide a tool capable of calculating
state variables of multi-energy networks. To do so, it can be used in combination with the open source software
pandapower. If only gas or district heating networks are of interest, pandapipes can also be used as a stand-alone 
application. 

In this sense, pandapipes closes two gaps: There are not many tools available which focus on multi-energy grid modeling.
In addition, most software for calculating fluid networks is only commercially available. The following table
summarizes some properties of commercial and open source tools, respectively.


|                                                      | Fluid Models                                                                                                                                | Automation                                                                                                               | Customization                                                                                           |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Commercial Tools (e.g. Stanet, Sincal, NEPLAN)       | <span style="color:green">Thoroughly validated and easy to parametrize models of pipes, pumps, valves etc. Typically, multi-energy networks are not considered.</span>            | <span style="color:red">Graphical User Interface (GUI) applications that are difficult to automate.</span>                     | <span style="color:red">Restricted possibilities for customization due to proprietary code base.</span> |
| Open Source Tools (e.g. Modelica, TransientEE)       | <span style="color:red">Models that require parametrization by the user with expert knowledge.</span>                                    | <span style="color:green">Console or GUI applications that might be automized.</span>                        | <span style="color:green">Open Source code base that can be freely modified and customized.</span>      |
| **pandapipes**                                       | <span style="color:green">**Thoroughly validated and easy to parametrize fluid models of pipes, pumps, valves etc. with the focus on multi-energy grids.**</span>        | <span style="color:green">**Console application that is designed for automated evaluations.**</span>                     | <span style="color:green">**Open source code base that can be freely modified and customized.**</span>  |

This is of course a very broad classification of tools that is only supposed to illustrate the focus of pandapipes without
considering the diverse landscape of existing tools. 


**Scope**<br>

pandapipes is aimed at **static** analysis of **balanced** fluid systems. This allows analysis of:
- **Static** or **quasi-static** analyses of pressure and velocity distributions in fluid networks using incompressible or compressible media. Gas composition is assumed fix.
-  **Static** or **quasi-static** analyses of temperature distributions in fluid networks. At present, this kind of analysis is only possible for incompressible media.


<h2 id="modeling">Fluid System Modeling</h2>

<h3 id="datastructure">Tabular Data Structure</h3>

pandapipes is based on a tabular data structure, where every element type is represented by a table that holds all parameters for a specific
element and a result table which contains the element specific results of the different analysis methods. The tabular data structure is
based on the Python library pandas. It allows storing variables of any data type, so that parameters can be stored
together with status variables and meta-data, such as names or descriptions. The tables can be easily expanded and customized by adding new
columns without influencing the pandapipes functionality. All inherent pandas methods can be used to efficiently read, write and
analyze the network and results data.

<h3 id="std_types">Standard Type Libraries</h3>

pandapipes includes a standard type library that allows the creation of pipes and pumps using predefined basic standard type parameters. The user can either define individual standard types or use the predefined pandapipes basic standard types for convenient definition of networks.

<h3 id="std_types">Fluid Property Library</h3>

pandapipes includes a fluid property library that allows the creation of fluid properties using predefined data. The user can either define individual properties or use the predefined data.
   
<h2 id="analysis">Fluid System Analysis</h2>

pandapipes supports the following fluid systems analysis functions:

- [Pipe Flow](#pf)


<h3 id="pf">Pipe Flow</h3>

The pandapipes pipe flow solver is based on the Newton-Raphson method.
<br><small>[Learn more](https://pandapipes.readthedocs.io/en/latest/pipeflow.html)</small>
<br>
To initialize the solution vector for the pipe flow calculation pandapipes offers two different methods:
 <ul>
 <small>
  <li>flat start</li>
  <li>solution vector of a previous calculation</li>
  </small>
 </ul>

<h2 id="tests">Tests and Validation</h2>

So far pandapipes has been successfully tested with [pytest](https://docs.pytest.org/en/latest/).
To ensure the correctness of the functionalities in pandapipes, various test networks were created,
in which different factors were varied:

 <ul>
 <small>
  <li>medium: gas and water</li>
  <li>topology</li>
  <li>pressure at external grids</li>
  <li>number of external grids</li>
  <li>friction model</li>
  <li>length, diameter and roughness of a pipe</li>
  <li>volume flow</li>
  <li>number and height values of nodes</li>
  <li>direction of pipe link between nodes, for checking the correct flow velocity calculation</li>
  <li>combinations of sources, sinks, pumps, valves and external grids</li>
  <li>heat network calculation (only with OpenModelica)</li>
  </small>
 </ul>

<br>
The test networks were created in [STANET](http://www.stafu.de/de/home.html) and
[OpenModelica](https://www.openmodelica.org/) and transformed into a
pandapipes network using the respective converter to perform the tests
in [PyCharm](https://www.jetbrains.com/pycharm/). A total of 83 tests were created
using both programs. 22 water and 21 gas networks with STANET and 32 water and 8 heating
networks with OpenModelica. How to call up the individual example networks is described in
the [Networks](https://pandapipes.readthedocs.io/en/latest/networks.html) chapter of the documentation.
The structures of all test networks are listed below:

{% include gallery caption="The pandapipes test networks." %}

<img src="{{"/images/about/validation/legend.png" | relative_url }}" alt=""/>
<figcaption>Legend of the network components.</figcaption>


<h3 id="tests_stanet">STANET Tests</h3>

The STANET test nets were saved in CSV format so that a conversion
into a json file can take place. A test is considered passed, if certain error tolerances are met.
The relative error <math><mi>p<sub>diff</sub></mi></math> during the calculation of the pressures
mostly has a value less than 0.002. In two cases the limit has to be increased, once to 0.01
and the second time to 0.03.

<math>
    <mrow>
        <mi>p<sub>diff</sub></mi>
        <mo>=</mo>
        <mo>|</mo>
            <mo>(</mo>
                <mi>p<sub>stanet</sub></mi>
                <mo>-</mo>
                <mi>p<sub>pandapipes</sub></mi>
            <mo>)</mo>
            <mo>/</mo>
            <mi>p<sub>stanet</sub></mi>
        <mo>|</mo>
    </mrow>
</math>
<br>
Furthermore, the absolute error in the calculation of the flow velocities <math><mi>v<sub>diff,abs</sub></mi></math>
is always less than 0.03.

<math>
    <mrow>
        <mi>v<sub>diff,abs</sub></mi>
        <mo>=</mo>
        <mo>|</mo>
        <mi>v<sub>stanet</sub></mi>
        <mo>-</mo>
        <mi>v<sub>pandapipes</sub></mi>
        <mo>|</mo>
    </mrow>
</math>


<h3 id="tests_om">OpenModelica Tests</h3>

Using the mo- and a mat-file containing the simulation results, the OpenModelica
net will be converted into a pandapipes network.
OpenModelica uses the [Navier-Stokes equations](https://www.maplesoft.com/documentation_center/online_manuals/modelica/Modelica_Fluid_UsersGuide_ComponentDefinition.html#Modelica.Fluid.UsersGuide.ComponentDefinition.BalanceEquations)
to calculate pressure loss and flow velocities. Whereas pandapipes uses an approach similar to STANET.
Consequently, the tolerances for errors for passing a test should be increased.
For the relative error <math><mi>p<sub>diff</sub></mi></math> with respect to pressure, a limit of 0.01
is usually sufficient. In 3 cases the limit should be increased to 0.02 and
in 2 cases to 0.06 and 0.4 respectively.
Presumably, the deviations are caused by the complexity of the networks, in which pumps and
valves are usually found. However, it is not generally due to the use of pumps and valves,
since test networks with pumps and valves that maintain a fault tolerance of 0.01 also exist.
In addition, the limit for the relative pressure deviation for heating networks lies in a
range between 0.01 and 0.05.

<math>
    <mrow>
        <mi>p<sub>diff</sub></mi>
        <mo>=</mo>
        <mo>|</mo>
            <mo>(</mo>
                <mi>p<sub>modelica</sub></mi>
                <mo>-</mo>
                <mi>p<sub>pandapipes</sub></mi>
            <mo>)</mo>
            <mo>/</mo>
            <mi>p<sub>modelica</sub></mi>
        <mo>|</mo>
    </mrow>
</math>
<br>
Furthermore, the absolute error for the flow velocities <math><mi>v<sub>diff,abs</sub></mi></math>
is always below 0.05.

<math>
    <mrow>
        <mi>v<sub>diff,abs</sub></mi>
        <mo>=</mo>
        <mo>|</mo>
        <mi>v<sub>modelica</sub></mi>
        <mo>-</mo>
        <mi>v<sub>pandapipes</sub></mi>
        <mo>|</mo>
    </mrow>
</math>
<br>
For the thermal network calculation, the upper tolerance value for the relative error of
the mean temperatures <math><mi>T<sub>diff,mean</sub></mi></math> is in a range from 0.004 to 0.04.

<math>
    <mrow>
        <mi>T<sub>diff,mean</sub></mi>
        <mo>=</mo>
        <mo>|</mo>
            <mo>(</mo>
                <mi>T<sub>mean,modelica</sub></mi>
                <mo>-</mo>
                <mi>T<sub>mean,pandapipes</sub></mi>
            <mo>)</mo>
            <mo>/</mo>
            <mi>T<sub>mean,modelica</sub></mi>
        <mo>|</mo>
    </mrow>
</math>
<br>
In the following, the deviations of pressures and flow velocities from the OpenModelica and pandapipes
calculations are graphically displayed for three different networks. The first net is the
[Delta net](https://pandapipes.readthedocs.io/en/latest/networks/meshed/meshed_networks.html#delta)
calculated with Prandtl-Colebrook where <math><mi>p<sub>diff</sub></mi></math> is less than 0.01:

| <img src="{{"/images/about/validation/delta_pressure_deviations.png" | relative_url }}" alt=""/> | <img src="{{"/images/about/validation/delta_velocity_deviations.png" | relative_url }}" alt=""/> |

For the [Pumps net](https://pandapipes.readthedocs.io/en/latest/networks/meshed/meshed_networks.html#pumps)
using Swamee-Jain for calculation, <math><mi>p<sub>diff</sub></mi></math> is below 0.02 and
has the below deviations in the junctions and the pipes:

| <img src="{{"/images/about/validation/pumps_pressure_deviations.png" | relative_url }}" alt=""/> | <img src="{{"/images/about/validation/pumps_velocity_deviations.png" | relative_url }}" alt=""/> |

At last the deviations for a network with valves are shown. Here, a limit of 0.4 must be set for the
relative error with respect to pressure to pass the test. The [Valves network](https://pandapipes.readthedocs.io/en/latest/networks/t_cross/t_cross_networks.html#valves)
was calculated with Prandtl-Colebrook:

| <img src="{{"/images/about/validation/valves_pressure_deviations.png" | relative_url }}" alt=""/> | <img src="{{"/images/about/validation/valves_velocity_deviations.png" | relative_url }}" alt=""/> |

<br>
In order to create your own nets in OpenModelica and to perform a comparison with pandapipes,
the elements that serve as equivalents for the components in pandapipes are listed hereafter:

<img src="{{"/images/about/validation/component_definition.png" | relative_url }}" alt=""/>

<br>
In the case of heat network calculation, the DynamicPipe must be used instead of the StaticPipe:

<img src="{{"/images/about/validation/DynamicPipe.png" | relative_url }}" alt=""/>

<h3 id="tests_example"><i>Example</i></h3>

In the following section an example is presented in which all the above mentioned components
except the DynamicPipe appear. The components have the below parameters:
<br>

| Component                 | Parameter                                                                          |
|---------------------------|------------------------------------------------------------------------------------|
| External Grid (ext_grid1) | p = 5 bar                                                                          |
| Sink (sink1)              | m_flow = -1 kg/s                                                                   |
| Source (source1)          | m_flow = 3 kg/s                                                                    |
| Junction (junction1)      | m_flow = 0 kg/s                                                                    |
| Pipe (pipe1)              | length = 1km <br> diameter = 0.075 m <br> roughness = 2 mm <br> height_ab = -400 m |
| Valve (valve1)            | A ~= 0,031416 m^2                                                                  |
| Constant (const_v1)       | k = 1 (valve opened)                                                               |
| Pump (pump1)              | pump characteristic curve P1 in pandapipes                                         |

<br>
The medium is water with a temperature of 293.15 K, where the ambient temperature has the same value.
The fluid properties can be called using special methods in OpenModelica,
for this purpose the source code must be considered.

<center><img src="{{"/images/about/validation/example_graph.png" | relative_url }}" alt="" /></center>

<img src="{{"/images/about/validation/example_code.png" | relative_url }}" alt=""/>

<br>
The results of the calculations are shown in the following. The results for junction1
and sink1 are highlighted in color. Also the deviations of the comparison are listed further down.

<img src="{{"/images/about/validation/example_result_OM.png" | relative_url }}" alt=""/>
<figcaption>Results of OpenModelica calculations with Prandtl-Colebrook.</figcaption>

<br>

<img src="{{"/images/about/validation/example_result_pp.png" | relative_url }}" alt=""/>
<figcaption>Results of the pandapipes calculations with Prandtl-Colebrook and the results of the comparison with the OpenModelica simulation.</figcaption>

<h2 id="citing">Citing pandpipes</h2>

If you use pandapipes in your work, we kindly ask you to cite the [pandapipes reference paper](/references/#citing)

<h2 id="license">License</h2>

pandapipes is published under the following 3-clause BSD license: 

> Copyright (c) 2020 by Fraunhofer Institute for Energy Economics
and Energy System Technology (IEE) Kassel and individual contributors (see AUTHORS file for details).
All rights reserved.
>   Redistribution and use in source and binary forms, with or without modification, are permitted 
    provided that the following conditions are met:   


> 1. Redistributions of source code must retain the above copyright notice, this list of conditions
    and the following disclaimer.

> 2. Redistributions in binary form must reproduce the above copyright notice, this list of
    conditions and the following disclaimer in the documentation and/or other materials provided
    with the distribution.

> 3. Neither the name of the copyright holder nor the names of its contributors may be used to 
    endorse or promote products derived from this software without specific prior written permission.

    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR 
    IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND 
    FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR 
    CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
    DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, 
    DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
    WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY
    WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
    
    
