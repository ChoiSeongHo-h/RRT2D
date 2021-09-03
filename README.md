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

Each point spreads out in the form of a tree in space.

When a child is added to the space, it points to its parent.

In addition to these tree-type data structures, lists exist. Whenever a new child is added, the children are added to the list.

Trees are used in the following situations:

1. To return a path when a goal is reached

Lists are used in the following situations:

1. When traversing the points to find the nearest point.
2. When freeing memory


![KakaoTalk_20210529_180357998](https://user-images.githubusercontent.com/72921481/132042933-de06d978-8955-4f46-87a3-3e9f71775405.png)
