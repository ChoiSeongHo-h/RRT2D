# RRT_2D_with_CV
2D RRT Algorithm with OpenCV

The RRT algorithm finds a path in a grid-free space.

The sequence of the RRT algorithm is as follows.

1. Specify the starting point.
2. Assume a temporary point in space.
3. Compute the angle of the line connecting the temporary point and the starting point.
4. From the starting point, move "step"(constant) at that angle and draw point.
(assumed that there are no obstacles at 4.)
5. Assume a temporary point in space.
6. Find the point X closest to the temporary point.
7. Compute the angle of the line connecting the temporary point and the point X.
8. From the point X, move step at that angle and draw point. If there is an obstacle, the point is not specified.
9. It ends when it reaches the goal, otherwise it starts at 5.


Code explanations are in the comments.
