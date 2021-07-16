## Demonstration of reproducibility and deployability of the computational workflow of the article "Profiling the baseline performance and limits of machine learning models for adaptive immune receptor repertoire classification"

### Purpose of this repository
> The main purpose of this repository is to demonstrate the ease of re-usability of a well-functioning containzerized computational environment of the analysis workflow of the article https://doi.org/10.1101/2021.05.23.445346. In the original article, the findings were based on reading in ~ 2 TB of data and writing ~ 10 TB of data to disk. To serve the main purpose of demonstrating ease of re-usability and deployability, we feed a very small toy dataset to each category of experiments tested in the original manuscript and reduced the number of cross-validation loops, iterations to reduce the running time for this demonstration. **Thus, the findings in this document will not make any sense - but should reflect the fact that the containerized computational workflow of the manuscript is well-functioning and hence re-usable, deployable across computational environments.**

### Code and data availability from original manuscript

- Code from the original manuscript with permanent DOI: https://doi.org/10.11582/2021.00038
- Containerized computational environment (Docker image on DockerHub): `kanduric/immuneml-v1:latest`
- Input data (~ 2.1 TB) with permanent DOI: https://doi.org/10.11582/2021.00064

> **Note:** To reproduce the findings of the manuscript, the code, input data, and the docker image provided above have to be used in a similar fashion as demonstrated in the **demo_reproducibility jupyter notebook** in this repository. The analysis scripts in this github repository are modified versions of the code used in the original manuscript (fed with a small dataset and reduced iterations in ML training only for the sake of demonstration) and cannot be used for replication of findings.

### Organization of the analyses in this repository for the demonstration of re-usability, reproducibility, and deployability

- In the original manuscript (https://doi.org/10.1101/2021.05.23.445346), the findings were organized into 10 heatmaps. In each heatmap, one particular variable property of AIRR-ML model training setup was explored (y-axis of heatmaps) at different witness rates (x-axis). These analyses were specified using a configurable YAML specification files, where for each experiment only the properties that are of interest are varied while other parameters remained the same. **Therefore, it would be sufficient to test the re-usability, reproducibility and deployability of the computational environment by re-running and producing output from one cell of each heatmap.** In the original manuscript, to gauge uncertainty, we repeated each analysis 3 times on separate datasets, whereas here we re-run each cell only on one dataset.

- In the **demo_reproducibility jupyter notebook**, under each sub-heading (matching the descriptions of the manuscript), we re-run one cell of each heatmap on toy data (the output of which will make no sense as explained above). **To check the reproducibility on your machine**, clone this github repository and make sure that the **analyses** directory is empty before re-running the code snippets in a terminal or from the supplied jupyter notebook. Note that jupyter notebook uses "!" symbol for running command-line commands. If you instead run these commands directly in a terminal, the "!" symbol has to be removed from the code snippets below.

- The stdout and stderr of each analysis snippet are printed below each snippet whereas the output of each excution is redirected to respective analysis directories as indicated under each snippet. 
