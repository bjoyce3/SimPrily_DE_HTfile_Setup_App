# CyVerse Discovery Environment (DE) High Throughput (HT) File Creation for SimPrily
## Overview for the CyVerse Discovery Environment SimPrily Workflow
A [SimPrily](https://github.com/agladstein/SimPrily) workflow has been established on the CyVerse Discovery Environment to provide a graphical user interface (GUI) for users. This workflow can run several hundred or thousand simulation (with a current maximum of 5000 in a single submission). There are three major steps in the DE SimPrily workflow:
1. Creating the necessary HT files for submitting a user-defined number of jobs. Users will submit these HT files as input for the second step.
2. Running the SimPrily DE app generate simulations based on the parameter, model, array HT file. The genetic map input file is optional. Note: The DE SimPrily app can be submitted and run by itself to create a single simulation as a test. There are three examples provided for users to test the app: a human hapmap simulation (), a Brassica simulation (derived from Qi et al. 2017 DOI: 10.1111/mec.14131), and a small test example.  
3. Collection of all the summary statistics from each simulation into a single file. The final file output will have a single simulation on each row, and the columns will be every summary statistic calculated for that simulation. 

## This SimPrily DE App
This app is the first app designed for the Simprily workflow on the DE. It will setup a high-throughput (HT) files to run the SimPrily workflow for a user-defined number of simulations (e.g. 1000 SimPrily simulations). Up to four files will be created including the path to each SimPrily input file type (i.e. parameter file, model file, genetic map, and array). The output HT files will have a green icon ![HT file icon on the DE](https://github.com/bjoyce3/SimPrily_DE_HTfile_Setup_App/blob/master/images/HTfile_icon.png). 

## Code Description for SimPrily HT File Setup
### Arguments
```-r Number of runs/simulations the user would like to have (integer)
-p Path to Parameter file
-m Path to Model file
-g Path to Genetic Map file
-a Path to Array file
-z Path to where the Parameter HT file will be saved 
-y Path to where the Model HT file will be saved
-w Path to where the Genetic Map HT file will be saved
-x Path to where the Array HT file will be saved```

### Example Command Line Input
```SimPrily_HTfile_setup -y model_htfile -p  -m  -g  -a  -z parameter_htfile -w geneticmap_htfile -x array_htfile -r 10```

## Related Links
* [Main SimPrily GitHub Repository](https://agladstein.github.io/SimPrily/)
  * [SimPrily Wiki](https://github.com/agladstein/SimPrily/wiki)
  * [SimPrily Code](https://github.com/agladstein/SimPrily)
* [CyVerse Discovery Environment SimPrily Workflow]()
  1. SimPrily HT File Setup App
    * [App in the DE]()
    * [GitHub Repo for App]()
    * [DockerHub Repo for App]()
  2. DE SimPrily App
    * [App in the DE]()
    * [GitHub Repo for App]()
    * [DockerHub Repo for App]()
  3. DE SimPrily Concatenation App
    * [App in the DE]()
    * [GitHub Repo for App]()
    * [DockerHub Repo for App]()
  4. [DE SimPrily Example Data](https://de.cyverse.org/de/?type=data&folder=/iplant/home/shared/iplantcollaborative/example_data)
    * [Randomly Generated Data for App Testing](https://de.cyverse.org/de/?type=data&folder=/iplant/home/shared/iplantcollaborative/example_data/SimPrily_version1)
    * [Homo sapiens HapMap Data from 1000 genomes Project](https://de.cyverse.org/de/?type=data&folder=/iplant/home/shared/iplantcollaborative/example_data/SimPrily_version1)
    * [Brassica sp. populations from Qi 2017](https://de.cyverse.org/de/?type=data&folder=/iplant/home/shared/iplantcollaborative/example_data/SimPrily_version1)
    * [SimPrily Benchmarking Data](https://de.cyverse.org/de/?type=data&folder=/iplant/home/shared/iplantcollaborative/example_data/SimPrily_version1)
* SimPrily Pegasus Documentation
  1. [SimPrily Pegasus Workflow Quick Start](https://agladstein.github.io/SimPrily/#open-science-grid)
  2. [Detailed Pegasus Workflow Documentation](https://github.com/agladstein/SimPrily/wiki#pegasus-workflow-on-the-open-science-grid)


# References
1. 1000 Genomes Project Consortium, A global reference for human genetic variation. Nature. 526, 68–74 (2015).
2. X. Qi et al., Genomic inferences of domestication events are corroborated by written records in Brassica rapa. Molecular Ecology (2017).
