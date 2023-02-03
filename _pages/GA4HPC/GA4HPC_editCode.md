---
permalink: /GA4HPC/edit
title: Editing the GA4HPC code

sidebar:
  nav: GA4HPC

toc: true
---

You may need to edit the tool, either to make it work with the specifities of your cluster, or just to add new features.
Eitherway, please consider submitting some pull requests to [the GitHub](https://github.com/GreenAlgorithms/GreenAlgorithms4HPC) to share these edits with other users!

There are some example of intermediary files [here](https://github.com/GreenAlgorithms/GreenAlgorithms4HPC/tree/main/example_files/).

## Custom workload manager

All the code related to the workload manager is stored in the `GreenAlgorithms_workloadManager.py` file. At the moment it is built for SLURM, but you can tailor it to different tools by editing this script.

You just need to make sure that you create a variable `WM.df_agg` (the output of `WM.clean_logs_df()`) similar to the example file [here](https://github.com/GreenAlgorithms/GreenAlgorithms4HPC/tree/main/example_files/example_output_workloadManager.tsv). Only the columns with a name ending with X are needed (the other ones are being used by the workload manager script). NB: the `pd.DataFrame` has been converted to a csv to be included here.

## Debugging

If SLURM seem to be returning data that are not expected, it may be an issue with SLURM version. The tool has been tested with SLURM `20.11.9`, the raw output of the `sacct` command (this is the command pulling all the logs) can be checked [here](https://github.com/GreenAlgorithms/GreenAlgorithms4HPC/tree/main/example_files/example_sacctOutput_raw.txt) ([here](https://github.com/GreenAlgorithms/GreenAlgorithms4HPC/tree/main/example_files/example_sacctOutput_raw_asDF.tsv) as a table); in the code, this is `WM.logs_raw`, the output of `WM.pull_logs()`.
