PageRank Algorithm Implementations


This repository contains multiple implementations of the PageRank algorithm, a link analysis algorithm used by Google Search to rank web pages in their search engine results. This project demonstrates different approaches to solving the same problem, from a foundational, "from scratch" implementation to more efficient versions utilizing popular data science libraries.

Project Highlights
The project is structured to showcase different methods of implementing the PageRank algorithm. Each implementation tackles the problem with a different philosophy, highlighting a range of skills:

page_rank_from_scratch.py: This file contains a pure Python implementation of the PageRank algorithm. It is built without using external libraries like NumPy or Pandas, providing a clear and fundamental understanding of the algorithm's core mathematical logic.

page_rank_numpy.py: This version leverages the NumPy library for matrix operations. By representing the web graph as a matrix, this implementation is significantly more performant and computationally efficient than the "from scratch" version.

page_rank_pandas.py: This implementation uses the Pandas library to handle and manipulate the data representing the web graph. It demonstrates proficiency in using Pandas DataFrames for data processing and analysis within a computational context.

How It Works
The PageRank algorithm operates on a web graph, where each web page is a node and each hyperlink is a directed edge. The core idea is that a page is more important if it receives links from other important pages.

The algorithm iteratively calculates a PageRank score for each page based on the following principles:

A link from page A to page B is considered a "vote" for page B.

The weight of this vote is determined by the PageRank score of page A.

A "damping factor" is introduced to prevent the score from being monopolized by circular links, simulating a user who might randomly jump to a new page instead of following a link.

Technologies Used
Python 3.x

NumPy

Pandas

Usage
To run the different implementations, you'll need to have the required libraries installed.

Bash

pip install numpy pandas
To run the from-scratch version:

Bash

python page_rank_from_scratch.py
To run the NumPy version:

Bash

python page_rank_numpy.py
To run the Pandas version:

Bash

python page_rank_pandas.py
Each script should output the PageRank score for each node in the graph, as shown in the example below.

Example Output
Assuming a simple graph is hardcoded into the scripts, the output would look similar to this:

PageRank scores:
A: 0.183
B: 0.223
C: 0.354
D: 0.240
(Note: Actual output will vary based on the specific graph and damping factor used in the code.)

Future Work
Integrate a command-line interface (CLI) to allow users to specify input graphs.

Add a visualization component to display the graph and the PageRank scores.

Implement a method for handling larger, more complex datasets.

Refactor the page_rank_from_scratch.py implementation for better performance.
