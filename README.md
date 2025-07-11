# ToMCAT
# Theory of Mind for Children Assembling Tangrams
## Dataset and Benchmarks


This repository contains the data for the Theory of Mind for Children Assembling Tangrams (ToMCAT) dataset and benchmarks.  The dataset consists of 436 examples of tangram puzzle arrangements.  All data is collected from child-robot interactions in which a Misty robot helped a child build either a CAT or RABBIT puzzle.

View paper: link coming soon

The CSV format of the dataset can be found under `/dataset`.

Each example 
incomplete
mistakes
a missing piece

## Dataset Description

The dataset includes three representations of the data.  The CSV file contains information on each puzzle arrangement, timing, and ground truth.  The symbolic files contain a complete symbolic representation of each puzzle arrangement.  Screenshots from the video are available, and there are reconstructed illustrations of each puzzle arrangement.

### CSV
The CSV file contains 436 datapoints depicting the sequence of puzzle arrangements

### Symbolic
Each puzzle arrangement has a file in the `/symbolic` folder.  Each file contains a complete description of the puzzle pieces and the arrangement of the pieces.  

predicate calculus
representation of adjacency (see below)


### Screenshots
The `\screenshots` folder contains low-resolution screenshots of the video.  A screenshot is available for each datapoint. If a screenshot includes the target illustration, we have blurred that portion of the image. This is done to avoid recognizing the puzzle by only looking at the illustration.

### Illustrations
The images folder contains reconstructed illustrations for each datapoint.  Each illustration is hand-crafted to match the video and the logic representation.


## Symbolic Representation of Tangram Puzzles