# ToMCAT
# Theory of Mind for Children Assembling Tangrams
## Dataset and Benchmarks


This repository contains the data for the Theory of Mind for Children Assembling Tangrams (ToMCAT) dataset and benchmarks.  The dataset consists of 436 examples of tangram puzzle arrangements.  All data is collected from child-robot interactions in which a Misty robot helped a child build either a CAT or RABBIT puzzle.

View paper: link coming soon

The CSV format of the dataset can be found under `/dataset`.

In creating this dataset, we created a new data point each time the state of the puzzle qualitatively changed.  This means that a new data point represents a change in the puzzle arrangement where the pieces were no longer being moved (at least momentarily). Since the dataset consists of examples of children assembling puzzles, each state of the puzzle often contains mistakes, and the final state of the puzzle occassionally is incomplete or has minor mistakes.  Additionally, the pink triangle is usually missing, as a result of the experimental design used in the original data collection.

Dataset is mostly ready for broad use, but there are a few updates to come:
- link to paper
- README needs a description of the columns in the CSV
- README needs a description of the symbolic representation
- In screenshots, s17 and s18 need to be updated to include the puzzle

## Dataset Description

The dataset includes three representations of the data.  The CSV file contains information on each puzzle arrangement, timing, and ground truth.  The symbolic files contain a complete symbolic representation of each puzzle arrangement.  Screenshots from the video are available, and there are reconstructed illustrations of each puzzle arrangement.

### CSV
The CSV format of the dataset can be found under `/dataset`. The file contains 436 rows, each depicting a state in the puzzle assembly process.

### Symbolic
Each puzzle arrangement has a file in the `/symbolic` folder.  Each file contains a complete description of the puzzle pieces and the arrangement of the pieces.  All descriptions are provided in predicate calculus.  Details of this representation are provided below.


### Screenshots
The `/screenshots` folder contains low-resolution screenshots of the video.  These screenshots are cropped from the original video and should include only the area of the image that has the puzzle.  No child faces are visible, though occassionally some hands and arms can be seen. 

A screenshot is available for each datapoint. If a screenshot includes the target illustration, we have blurred that portion of the image. This is done to avoid recognizing the puzzle by only looking at the illustration.

(s17 and s18 will be provided soon)

### Illustrations
The `/images` folder contains reconstructed illustrations for each datapoint.  Each illustration is hand-crafted to match the video and the logic representation.


## Symbolic Representation of Tangram Puzzles

The symbolic represenation of the data uses a novel representation to model spatial adjacency between 2D, non-overlapping, convex polygons.  The representation consists of 6 possible relationships between vertices and edges of a polygon.

add image depicting the possible relations

To describe each polygon in a tangram puzzle 