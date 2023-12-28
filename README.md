Problem Description: Metro System Path Finder

The provided C++ code implements a Metro System Path Finder, designed to find the optimal path and associated fare between two metro stops in a given metro system. The metro system is represented using object-oriented programming principles with classes for MetroStop, MetroLine, AVLNode, AVLTree, Trip, Exploration, and Path.

Classes and Components:

1. MetroStop:
   - Represents a metro station with attributes such as stopName, nextStop, prevStop, metro line, and fare.
   - Linked list structure to connect stops within a metro line.

2. MetroLine:
   - Represents a metro line with a name and a linked list of MetroStop nodes.
   - Provides methods to print the line and get the total number of stops.

3. AVLNode:
   - Represents a node in an AVL tree containing a stopName and a vector of associated MetroStop objects.
   - AVL nodes are used to efficiently search for metro stops in the system.

4. AVLTree:
   - Represents an AVL tree containing AVLNodes.
   - Supports methods for insertion, balancing, searching, and populating the tree with metro stops.

5. Trip:
   - Represents a trip between metro stops, forming a linked list structure.
   - Used during the exploration phase to discover possible paths.

6. Exploration:
   - A queue structure for managing Trip objects during the exploration phase.

7. Path:
   - Represents a path between two metro stops, containing a vector of stops and the total fare.

8. PathFinder:
   - Main class orchestrating the path-finding process.
   - Uses an AVLTree to search for metro stops efficiently.
   - Employs exploration through the Exploration queue and backtracking to find the optimal path.
   - Calculates the fare for the identified path.

Main Functions:

- createAVLTree:
  - Initializes and populates an AVL tree with metro stops from different metro lines.

- findPath:
  - Takes origin and destination stop names as input.
  - Utilizes exploration and backtracking to find the optimal path.
  - Returns a Path object containing the sequence of stops and the total fare.

- getJunctionVector:
  - Helper function to identify alternative metro stops at a junction.
