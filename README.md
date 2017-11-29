# CyVerse Discovery Environment (DE) High Throughput (HT) File Creation for SimPrily
## Overview for the CyVerse Discovery Environment SimPrily Workflow
A SimPrily (https://github.com/agladstein/SimPrily) workflow has been established on the CyVerse Discovery Environment to provide a graphical user interface (GUI) for users. This workflow can run several hundred or thousand simulation (with a current maximum of 5000 in a single submission). There are three major steps in the DE SimPrily workflow:
1. Creating the necessary HT files for submitting a user-defined number of jobs. Users will submit these HT files as input for the second step.
2. Running the SimPrily DE app generate simulations based on the parameter, model, array HT file. The genetic map input file is optional. Note: The DE SimPrily app can be submitted and run by itself to create a single simulation as a test. There are three examples provided for users to test the app: a human hapmap simulation (), a Brassica simulation (derived from Qi et al. 2017 DOI: 10.1111/mec.14131), and a small test example.  
3. Collection of all the summary statistics from each simulation into a single file. The final file output will have a single simulation on each row, and the columns will be every summary statistic calculated for that simulation. 

## This SimPrily DE App
This app is the first app designed for the Simprily workflow on the DE. It will setup a high-throughput (HT) files to run the SimPrily workflow for a user-defined number of simulations (e.g. 1000 SimPrily simulations). Up to four files will be created including the path to each SimPrily input file type (i.e. parameter file, model file, genetic map, and array). The output HT files will have a green icon ![HT file icon on the DE](https://github.com/bjoyce3/SimPrily_DE_HTfile_Setup_App/blob/master/images/HTfile_icon.png).

## Related Links
* [Main SimPrily GitHub Repository](https://github.com/agladstein/SimPrily)
  * [SimPrily Wiki](https://github.com/agladstein/SimPrily/wiki)
  * [SimPrily ]()
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
* [SimPrily Pegasus Workflow]()