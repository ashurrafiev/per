# per
Performance-Energy-Reliability (PER) Interplay exploration tool

## About

Modelling the interplay between Performance, Energy and Reliability (PER) in multi- and many-core systems has been one of the main objectives within the PRiME project (http://www.prime-project.org). This has led to the development of the idea to represent PER interplay as a region of reliable operation in the throughput-voltage space. This region is defined by platform-specific constraints (minimum and maximum voltage, dynamic voltage-frequency scaling points), and also design requirements, such as maximum power consumption or minimum throughput.

The concepts behind this approach can now be explored using our tool, PER. Using the tool is done in three straightforward steps:

1. Select the platform. The tool contains a set of example pre-defined power and performance profiles. The teams at Imperial College London, University of Southampton, and Newcastle University have produced characterizations on a number of contemporary platforms running certain standard benchmarks. In addition to these built-in profiles, the tool also accepts custom data input in CSV format. The method of presenting profile data in the right CSV format can be found by studying the existing profiles in the tool's source code.

2. Specify the constraints. Further restrictions on the region of reliable operation can be set by the user. These are driven by the power or throughput requirements, as well as the application-specific mode of concurrency. The tool supports the following many-core performance scaling models: Amdahl's Law, Gustafson's model, and Sun and Ni's model.

3. Read the solution. The tool will plot the PER diagram and suggest the best operating point: the number of active cores and the operating voltage and frequency for these cores. For given power requirements, the tool maximizes the combined throughput. For given throughput requirements, the tool minimizes the power consumption.


## Information for contributors

The master branch of the tool must follow these requirements:
- All functionality and resources must be contained in a single html file.
- The tool must be functional in offline mode: no links to libraries like JQuery, no server-side processing.
- It must work in the latest versions of all major browsers.
Any commits to the master branch that do not comply to these requirements will be rejected. Fork if in disagreement.

