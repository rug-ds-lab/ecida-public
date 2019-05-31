+++
title = "ECiDA"
tagline = "Evolutionary Changes in Data Analysis"
+++
In the past years, the collection of data has increased significantly. Large scale data analysis requires a distributed server cluster where the data is divided among the available machines such that it can be processed in parallel, speeding up the analysis substantially. 

Distributed data processing platforms such as Spark have become a de-facto standard in the world of large-scale data processing. The data processing pipelines for such platforms are composed during design time and then submitted to the central “master” component who then distributes the code among several worker nodes. However, in many situations, the application is not static and evolve over time: the developers add new processing steps, data scientists adjust parameters of their algorithm and quality assurance discovers new bugs. Currently, an update of the pipeline looks as follows: the developers patch their code, re-submit the updated version, and finally restart the entire pipeline. 

However, restarting the processing pipeline safely is difficult: the intermediate state is lost and needs to be re-computed; some data needs to be reprocessed and, finally, the cost of restarting may not be trivial - especially for real-time streaming components that require 24x7 availability. In this project we investigate the possibility to support evolving data-intensive applications without the need for restarting them when the requirements change (e.g., new data sources or algorithms are available).
