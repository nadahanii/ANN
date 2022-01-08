# ANN
This code represents two programs. 
The first one implements the back propagation algorithm and the second one implements the feed forward.


Input is read (x vector) and the output (y vector) from a file. Below is the structure of the input file:
  1) First line: M, L, N where M is number of Input Nodes, L is number of Hidden Nodes and N is number of Output Nodes
  2) Second line: K, the number of training examples, each line has length M+N values, first M values are X vector and last N values are output values.
  3) K lines follow as described
  An example of input file (just for clarification not to be used):
  3 2 2
  3
  1 1 1.5 2 2
  -1 2.25 0.5 -0.5 1.2
  1 1 1 1 2
  Above is a file that describes:
  1) Network with 3 input nodes, 2 hidden and 2 output
  2) Training is 3 examples
  3) Second example has training example X [1 1 1.5] and output vector [2 2]


Deliverables of the first program:
   • After reading the input file, normalization step on the input features is performed.
   • Normalization is done by computing, for each numeric x-data column value v, v' = (v - mean) / std dev. This technique is sometimes called Gaussian normalization.
    For example, the mean of the first column = (30 + 36 + 52 + 42) / 4 = 160 / 4 = 40.0. 
    The standard deviation of the first column = sqrt((30-40)^2 + (36-40)^2 + (52-40)^2 + (42-40)^2) / 4) = sqrt((100 + 16 + 144 + 4) / 4) = sqrt(66.0) = 8.12.
    So the normalized value for an input of value 30 = (30 - 40.0) / 8.12 = -1.23.
  • Back propagation algorithm is performed. (The algorithm stops after running for a number of iterations, let’s say 500 iterations.)
  • After finishing the 500 iterations,  MSE is printed on the screen and final weights are saved to a file.
Deliverables of the second program:
  • After reading the input file,  feed forward algorithm is performed on the input data using the best weights calculated in the first program. 
