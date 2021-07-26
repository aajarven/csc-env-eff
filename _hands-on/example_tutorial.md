---
topic: Put here the topic name that is found in ohter tutorials in the same folder
title: Title that is shown in the rendered index.md
---

# Descriptive Headline

💬 This document contains general styleguide for handson tutorials and exercises. 

1. Use numbered list to describe actual steps that a student does
```bash
echo 'project_XXXX/YOURUSERNAME'   # Use commented code whenever clarification is necessary
```
## Get started

💬 This is the first phase of this tutorial eg. a preparation.  

💡 It is recommended to structurize the content with second level headlines.

2. A code block can contain multiple lines
```bash
export SCRATCH=/scratch/project_XXXX    # Use XXXX for projectnumber
mkdir YOURUSERNAME                      # Use YOURUSERNAME if student should use their own
echo $USER                              # Or use the environment variable
```
3. A step does not need to contain a code block, but instead make a point that student should notify
    - Further explanation can be provided with intended list element

### 1. Further structurizing
1. Feel free to add more headlines if it supports the understandability of the content 
2. The goal is to reduce the effort in following the material

## Usage of Emojis

💡 The emojis are meant to structure text and to improve its readability. 

1. Look for the symbols-option for your computer
    - Usually the emojis are there.
2. Copy the existing emojis if you don't find them anywhere else

| Emoji | Purpose |
|-------|:--------|
| 💬    | General instructions or description |
| 💭    | Provide extra information or insight |
| 🗯    | Emphasise the message a bit |
| 💡    | Valuable information, ideas or suggestions |
| ☝🏻    | Notice or a side-note |
| ‼️    | Very important notice. Failing to comply with this will result in error of some kind |

## Usage of images

1. Add images to the `/slides/img/`-folder
    - Or `/_hands-on/img/`-folder
2. Provide the path like this:
![terminal-icon](../../slides/img/terminal_icon1.png)

## Providing job-files

💬 [Job-files](https://docs.csc.fi/computing/running/creating-job-scripts-puhti/#a-basic-batch-job-script) are scripts for SLURM-queueing system used in CSC supercomputers.

1. Provide necessary job-files commented like this:
```bash
#!/bin/bash
#SBATCH --job-name=test           # Name of the job visible in the queue.
#SBATCH --account=project_xxxx    # Choose the billing project. Has to be defined!
#SBATCH --partition=test          # Job queues: test, interactive, small, large, longrun, hugemem, hugemem_longrun
#SBATCH --time=00:01:00           # Maximum duration of the job. Max: depends of the partition. 
#SBATCH --mem=1G                  # How much RAM is reserved for job per node.
#SBATCH --ntasks=1                # Number of tasks. Max: depends on partition.
#SBATCH --cpus-per-task=1         # How many processors work on one task. Max: Number of CPUs per node.

singularity exec tutorial.sif hello_world
```

💭 For more information on batch jobs, please see [CSC Docs pages](https://docs.csc.fi/computing/running/getting-started/).

## More information

💡 It is a good practice to provide more information on topic but it is not mandatory.

💬 This tutorial is meant as a brief introduction to get you started.

💭 When searching the internet for instruction, pay attention that the instructions are for the same version of Singularity that you are using. There has been some command syntax changes etc. between the versions, so older instructions may not work with copy-paste.

💡 Always a good idea to link [CSC documentation](https://docs.csc.fi/).