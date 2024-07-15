2 Main Approaches: Decomposition & Call-Graph

Decomposition testing follows modular structure of the system

There are 2 ways to do decomposition testing:

  1) Top-Down:
    Begin by testing main program with mocked subcomponents, repeat with 1 left child of components tree being replaced with an actual code.
    Repeat with next child components until the entire system is tested
  
  2) Bottom-Up:
    Start with leaf functions and repeat with parent functions until top is reached, mocking of components is not required, unit-testing utilized/reused

  Limitations:
    Tested by the structure of components tree, the app itself is not neccessarily executed in the same sequence

Call-Graph testing: Rather than using tree structure of components, call-graph is defined, to follow proper sequence. From there on - same decomposition testing is used

If there is a cycle within the graph, strong-connected components are tested as a unit, to prevent recursion

Pair-wise Testing is an alternative to Top-Down // Bottom-Up. Each edge of the graph is tested, converting unit test for each component for every pair. Provides higher fault isolation

System Testing - less formal that Unit/Integration testing, test cases are defined by use case docs, sequence diagrams and state machine diagrams

Life-Cycle-based Testing:

  Wterfall Testing, Iterative Life-Cycle Testing & Agile Testing -> Check Diagrams in Notes
