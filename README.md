# v-hacd
Volumetric Hierarchical Approximate Convex Decomposition - written by K. Mamou

Automatically exported from code.google.com/p/v-hacd

As google code is closing down this is just a quick grab of the current source using 'export to github'. Anyone who comes across this should check the orriginal page (https://code.google.com/p/v-hacd/) or Mamou's blog (http://kmamou.blogspot.ca/) to see if the actual project has been updated or properly transitioned to another repository.

..
..

The V-HACD library decomposes a 3D surface into a set of "near" convex parts.

Why do we need approximate convex decomposition?
Collision detection is essential for realistic physical interactions in video games and computer animation. In order to ensure real-time interactivity with the player/user, video game and 3D modeling software developers usually approximate the 3D models composing the scene (e.g. animated characters, static objects...) by a set of simple convex shapes such as ellipsoids, capsules or convex-hulls. In practice, these simple shapes provide poor approximations for concave surfaces and generate false collision detection.


A second approach consists in computing an exact convex decomposition of a surface S, which consists in partitioning it into a minimal set of convex sub-surfaces. Exact convex decomposition algorithms are NP-hard and non-practical since they produce a high number of clusters. To overcome these limitations, the exact convexity constraint is relaxed and an approximate convex decomposition of S is instead computed. Here, the goal is to determine a partition of the mesh triangles with a minimal number of clusters, while ensuring that each cluster has a concavity lower than a user defined threshold.
