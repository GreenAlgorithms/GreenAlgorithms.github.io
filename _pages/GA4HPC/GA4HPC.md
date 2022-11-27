---
permalink: /GA4HPC/

title: "Green Algorithms 4 HPC"

excerpt: "[![Generic badge](https://img.shields.io/badge/Version-v0.2.2-blue.svg)](https://shields.io/) [![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity) [![Open Source? Yes!](https://badgen.net/badge/Open%20Source%20%3F/Yes%21/purple?icon=github)](https://github.com/Naereen/badges/)"

header:
  overlay_image: assets/images/stripes_banner_1.png
  overlay_filter: linear-gradient(rgba(255, 255,255, 0), 20%, rgba(255, 255, 255, 1))
  text_color: rgb(80, 80, 80)
  actions:
  - label: "GitHub"
    url: https://github.com/GreenAlgorithms/GreenAlgorithms4HPC

sidebar:
  nav: GA4HPC

toc: true
toc_sticky: true
---

In some situations, using an online calculator such as the [Green Algorithms one](http://calculator.green-algorithms.org) isn't very practical, e.g. when many different jobs are run. In an ideal world, there would be a tool that collects automatically all the details of the algorithms ran and estimate the corresponding energy usage and carbon footprint.
__GA4HPC__ is a first step in this direction.

High Performance Computing (HPC) clusters tend to log information on all jobs ran on them, for accounting purposes, and this information can be pulled.

## Who is it for?

At this stage, the script works on any HPC server using [SLURM](https://slurm.schedmd.com/documentation.html) as a workload manager. It can be adapted to other workload managers, see [here](/GA4HPC/edit) on how to add one.

## How to install it

It doesn't require any particular permissions, you just need to copy the GitHub repository on your HPC drive, enter some information about your data centre, and you're good to go! [Tutorial here](/GA4HPC/install)

## How to use it

Anyone with access to `the_shared_directory` where the script is located can run the calculator,
by running the same command, with various options available:

```
usage: GreenAlgorithms_global.py [-h] [-S STARTDAY] [-E ENDDAY] [--filterCWD]
                                 [--filterJobIDs FILTERJOBIDS]
                                 [--filterAccount FILTERACCOUNT] [--reportBug]
                                 [--reportBugHere]
                                 [--useCustomLogs USECUSTOMLOGS]

Calculate your carbon footprint on CSD3.

optional arguments:
  -h, --help            show this help message and exit
  -S STARTDAY, --startDay STARTDAY
                        The first day to take into account, as YYYY-MM-DD
                        (default: 2022-01-01)
  -E ENDDAY, --endDay ENDDAY
                        The last day to take into account, as YYYY-MM-DD
                        (default: today)
  --filterCWD           Only report on jobs launched from the current
                        location.
  --filterJobIDs FILTERJOBIDS
                        Comma seperated list of Job IDs you want to filter on.
  --filterAccount FILTERACCOUNT
                        Only consider jobs charged under this account
  --reportBug           In case of a bug, this flag logs jobs informations so
                        that we can fix it. Note that this will write out some
                        basic information about your jobs, such as runtime,
                        number of cores and memory usage.
  --reportBugHere       Similar to --reportBug, but exports the output to your
                        home folder
  --useCustomLogs USECUSTOMLOGS
                        This bypasses the workload manager, and enables you to
                        input a custom log file of your jobs. This is mostly
                        meant for debugging, but can be useful in some
                        situations. An example of the expected file can be
                        found at `example_files/example_sacctOutput_raw.tsv`.
```

### Limitations to keep in mind

 - The workload manager doesn't alway log the exact CPU usage time, and when this information is missing, we assume that all cores are used at 100%.
 - For now, we assume that GPU jobs only use 1 GPU and the GPU is used at 100% (as the information needed for more accurate measurement is not available)
 (both of these may lead to slightly overestimated carbon footprints, although the order of magnitude is likely to be correct)
 - Conversely, the wasted energy due to memory overallocation may be largely underestimated, as the information needed is not always logged.

## Report bugs

If you spot any bugs, or would like new features, just [open a new issue on GitHub](https://github.com/GreenAlgorithms/GreenAlgorithms4HPC/issues).

## How to modify the script for my cluster?

See the ["Edit code and contribute"](/GA4HPC/edit) page on how to modify the code and share your improvements with other users.

## Licence

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-shield]][cc-by]

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
