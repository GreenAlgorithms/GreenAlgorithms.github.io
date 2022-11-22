---
permalink: /GA4HPC/install

title: Installing GA4HPC


sidebar:
  nav: GA4HPC

toc: true
---

## How to install it?

_The script only needs to be installed once on a cluster, check first that someone else hasn't installed it yet!_

1. Clone the GitHub repository in a shared directory on your cluster:
    ```bash
    cd the_shared_directory
    git clone https://github.com/Llannelongue/GreenAlgorithms4HPC.git
    ```

2. Edit `myCarbonFootprint.sh` to load the module enabling `python3 ...` to load Python 3.7 or greater (the name of the module depends on your server).

3. Make the bash script executable:
    ```bash
    chmod +x the_shared_directory/GreenAlgorithms4HPC/myCarbonFootprint.sh
    ```

4. Edit `cluster_info.yaml` to plug in the values corresponding to the hardware specs of your cluster. You can find a lot of useful values on the [online calculator GitHub](https://github.com/GreenAlgorithms/green-algorithms-tool/tree/master/data).

5. Run the script a first time. It will check that the correct version of python is used
and will create the virtualenv with the required packages, based on `requirements.txt`:
```shell script
the_shared_directory/GreenAlgorithms4HPC/myCarbonFootprint.sh
```

## How to update the tool when a new version of the tool is released

_More elegant solutions welcome! [Discussion here](https://github.com/Llannelongue/GreenAlgorithms4HPC/issues/1)._

⚠️ Make sure you have saved your custom version of `cluster_info.yaml` and the module loading step of `GreenAlgorithms_global.py`.

- `git reset --hard` To remove local changes to files (hence the need for a backup!)
- `git pull`
- Update `cluster_info.yaml` and `GreenAlgorithms_global.py` with the details needed for your cluster.
- `chmod +x myCarbonFootprint.sh` to make it executable again
- Test `myCarbonFootprint.sh`
