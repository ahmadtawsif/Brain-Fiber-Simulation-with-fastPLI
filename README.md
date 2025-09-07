
# Brain-Fiber-Simulation-with-fastPLI
This seminar project was part of Medical Imaging specialization of the master's program Computer Simulation in Science
In this seminar project different fiber architecture were simulated using a class fastPLI. 

# fastPLI
A toolbox for generating Polarized Light Imaging (PLI) in computer-aided environment. 
Three purposes:
Sandbox - Designing Nerve Fiber Models
Solver - Generating Collision Free Model
Simulation - Simulation of 3D-Polarized Light
Imaging

# Necessary Software
Try installing the following software before our first meeting

Fiji: https://imagej.net/Fiji/Downloads
3D Viewer plugin: https://imagej.net/3D_Viewer
Python3 (>=3.6): https://www.python.org/
fastpli: https://github.com/3d-pli/fastpli
If you have trouble installing it, a docker service is available where you can use jupyter lab to work with the library https://github.com/3d-pli/fastpli/tree/Docker

# Task 
- Define a single
straight fiber as fiber object.

<img width="713" height="732" alt="image" src="https://github.com/user-attachments/assets/ef79eaed-c9ce-4017-8bc0-58d4bed1caf0" />


- Define a curved fiber as fiber object.
   -Fill this “fiber” with fibers with 1/10th of the original radius
   -Visualize the fiber bundle (e.g. with matplotlib)

<img width="467" height="525" alt="image" src="https://github.com/user-attachments/assets/2020b993-5bb9-4f14-a734-81d57301e74e" />


<img width="449" height="513" alt="image" src="https://github.com/user-attachments/assets/2d6eb826-87cd-4cba-b821-ccb2ecf77baa" />

- Design a 90° crossing fiber bundle

<img width="807" height="829" alt="image" src="https://github.com/user-attachments/assets/eb1221cf-88a6-4111-9bb3-70e640c3dc61" />

### What is observed at the solving process?
During the solving process, the solver algorithm attempts to find a non-colliding model of the fiber bundles by iteratively adjusting the position and orientation of the individual fibers. 
This process can take some time, depending on the complexity of the fiber bundles and the solver parameters.
### What is observed on the solved model?
Once the solver algorithm has found a non-colliding model, the solved model can be visualized to observe the position and orientation of the individual fibers. 
The solved model should show the fiber bundles crossing at a 90-degree angle, with the individual fibers in each bundle arranged in a non-overlapping configuration. 
It is also possible to compute and visualize additional properties of the fiber bundles, such as the average curvature or orientation of the individual fibers.

– Crossing Fibers Change parameters: 

<img width="442" height="455" alt="image" src="https://github.com/user-attachments/assets/349d07d3-e474-4f77-b3e1-687a642ea341" />

<img width="458" height="462" alt="image" src="https://github.com/user-attachments/assets/598be370-cbb7-4ee0-92ad-a6834a40be71" />

### What do you observe at the solving process? 
10X Computational Time Changing the fiber segment obj_mean_length parameter will affect the length of the segments used to discretize the fibers. 
Increasing this parameter will result in longer fiber segments, which may lead to a smoother model. 
Decreasing this parameter will result in shorter fiber segments, which may lead to a more detailed model with higher curvature(higher computational time).
Changing the fiber minimum bending radius obj_min_radius parameter will affect the degree of curvature allowed in the fibers. 
Increasing this parameter will limit the curvature of the fibers, resulting in a model with straighter fibers. 
Decreasing this parameter will allow for more curvature, resulting in a model with more curved fibers.

### How does it affect the result? 
Changes to these parameters may affect the convergence rate of the solver and the final quality of the model. 
It may also affect the computational time required to solve the model.

Now, simulation with the parameters: Use the following parameters:
final volume: 600µm x 600µm x 600µm
fiber bundle radius: 100µm
fiber radius: 2µm
fiber segment length: 4µm
fiber min radius: 4µm
the fiber bundles should lie in the xy-plane
add a random displacement to each fiber point (fiber[:,:2]) to add variability to the model.
What behavior do you observe between both models?

<img width="390" height="401" alt="image" src="https://github.com/user-attachments/assets/8439dfd1-9f64-46a7-be76-74bdc880ba81" />

<img width="390" height="396" alt="image" src="https://github.com/user-attachments/assets/31a2fdfd-60f4-4db7-b97c-8f206b44eeb9" />

<img width="413" height="398" alt="image" src="https://github.com/user-attachments/assets/6b3a26cc-b224-48fc-8f6c-43de05da453f" />






