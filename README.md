# Final-Project-Topology-Optimization
This final project was conducted to understand topology optimization through the use of a tutorial on the top88 function, created by Erik Andreassen, Anders Clausen, Mattias Schevenels, Boyan S. Lazarov, and Ole Sigmund. Topology optimization is used in many stress simulations in order to avoid expenses. There are numerous modeling softwares that do this, namely ANSYS. Having an intimate understanding of how these simulations are conducted can make for designs that are less computationally complex, which usually results in a more efficient use of material.
	While a more in-depth explanation of the top88 function can be found at https://www.topopt.mek.dtu.dk/apps-and-software/efficient-topology-optimization-in-matlab, a brief overview will be given here. Essentially, top88 utilizes the stiffness method of finite element analysis, which accounts for all forces and moments acting across the system. This can then be used with matrix mathematics to solve for the displacement at specific points at once. This info is then used to find the minimum material necessary to support a given load.

![image](https://user-images.githubusercontent.com/67770226/206836424-3d8ff9bb-6fcc-4723-b56c-fdc9e5719298.png)


	 In our tutorial, we were given a beam whose left side was fixed in the x direction, the bottom right point was fixed in the y direction, and a force of -1N was applied on the top left node. This beam had 45 nodes, which were where forces were applied. Using these conditions, top88 gave this result:

![image](https://user-images.githubusercontent.com/67770226/206836427-37d7093e-30a7-4bc7-b17e-83ec00903d2e.png)


The darker colored squares have more reactions acting on them than lighter colored squares. This output is only made more useful by increasing the resolution. This can be done easily, by increasing the number of elements. Here is the same optimization with an 80 x 40 element beam:

![image](https://user-images.githubusercontent.com/67770226/206836430-db7cdde5-c72e-4388-8025-8f9720756fac.png)


After 61 iterations, the model had less than 1% error and outputted the graph shown above. The darker elements show the optimal placement of material to support this load, a truss formation. Different loading conditions produce different trusses; In figure [] below, the same constraints were used, but the force was moved to be applied on the top node, halfway between both ends. When half of the supports were removed from the left side, figure [] was produced.

![image](https://user-images.githubusercontent.com/67770226/206836440-a2984ba2-a277-450f-8e78-ddbf20707795.png)

![image](https://user-images.githubusercontent.com/67770226/206836443-0376dd54-159b-4484-babb-f07a958fb2be.png)


