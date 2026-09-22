# VeyForge-3D-Assets-and-Sim-to-Real
TsingtaoAI · From physical objects to simulation, and from simulation back to the real world Core conclusion: Generation can be initiated with just 2 to 4 multi-view photos; a single asset is completed in about 30 seconds; it supports outputs such as GLB, PLY, USD/USDA, and connects to Isaac Sim, robot training, and real-machine validation.
access the site through the link：https://veyforge.tsingtaoai.com/

1. What is VeyForge? An AI 3D Asset Factory for Embodied Intelligence
VeyForge is independently developed by TsingtaoAI, built for robotics developers, simulation engineers, and intelligent manufacturing teams. It is not just about generating a good-looking model; it is an end-to-end asset engine that connects input, generation, rendering, physics, simulation, and real-world validation.

The official website summarizes it as an AI-driven 3D asset factory from physical objects to simulation: users can take multi-view photos of real objects with a smartphone or input natural language descriptions. The platform automatically completes 3D reconstruction and exports assets into standard formats suitable for different R&D stages. These are then applied to the Isaac Sim platform to achieve one-click digital twins (Real-to-Sim) from real objects to simulation scenes. The reconstructed 3D assets are converted into USD format and automatically bound with physical properties (mass, inertia, collision bodies) and interactive Articulation structures, allowing them to be directly loaded into robot simulation scenes as objects to be grasped or manipulated. On this basis, the platform closes the Sim-to-Real loop: users can complete robot motion planning, grasping strategy training, reinforcement learning, and visual data synthesis in Isaac Sim, then replay validated strategies and trajectories onto real robots. This enables a complete digital twin R&D pipeline: "Real object photo/description → 3D reconstruction → Standard format assets → Isaac Sim simulation validation → Real robot deployment," significantly shortening the R&D cycle from physical objects to simulation and then to real-world deployment.

Figure: From multi-view image input, to AI-generated 3D assets, to Isaac Sim simulation applications, and deployment to real machines.

The value of this pipeline lies in the fact that model generation is no longer the end of the R&D process, but the starting point for robot training, scene testing, and real-world deployment.

2. Three Input Methods: Turning Both the Real World and the Imagined World into Assets
2.1. Multi-view Images to 3D: Reconstructing Real Objects with 2 to 4 Photos
Users simply take photos of the same object from different angles using a smartphone, and VeyForge can reconstruct the object's spatial structure, appearance, materials, and textures based on the multi-view information. Compared to a single image, multi-view input reduces occlusion and information loss, making it more suitable for robot simulation and digital twin projects that require higher geometric fidelity.

2.2. Single Image to 3D: Quickly Bringing Existing Image Assets into the Digital World
For product photos, historical images, commercial materials, and on-site captured images, the platform supports generating 3D assets from a single image. This is suitable for rapid validation, concept display, and large-scale asset pre-screening.

2.3. Text to 3D: Turning a Sentence into a Visual Prototype
Input a natural language description, such as "a red apple with smooth surface," to generate the corresponding 3D asset. Robot props, game scenes, industrial parts, and creative prototypes can all be quickly formed through text first, then enter subsequent screening and simulation processes.

From images to text, VeyForge lowers the barrier to 3D content production and allows algorithm engineers and scene designers to participate more directly in asset creation.

3. From Input to Output: A Fully Automated Asset Production Pipeline
Step 1: Material Input. Supports multi-view images, single images, and text descriptions; basic collection can be done with a smartphone.
Step 2: AI Generation. The platform automatically performs background processing, sparse skeleton generation, and structured latent variable generation—first determining the overall spatial structure, then adding geometric and texture details.
Step 3: Real-time Preview. Users can view Gaussian rendering, normal rendering, and interactive 3D models to identify structural, texture, and perspective issues in advance.
Step 4: Format Export. Depending on the use case, output GLB mesh models, PLY Gaussian point clouds, and USD/USDA physical assets for simulation.
Step 5: Enter Simulation and Training. Assets can be used for grasping, navigation, collision, stacking, conveyor belt loading/unloading, and closed-loop testing in Isaac Sim.

Figure: Preview of generated Gaussian and normal rendering, supporting model quality inspection before export.

4. More Than Just Generating Models: VeyForge Gives Assets Physical Properties
What robots need is not a beautiful texture, but a digital object capable of physical interaction. VeyForge can further calculate mass, volume, center of mass, and inertia tensor based on the generated GLB mesh, and configure corresponding physical parameters.

Configurable physical properties include:

Mass and Density: Used to establish the object's weight and force relationships.

Collision Body Types: Supports options such as none, convexHull, convexDecomposition, boundingCube, and boundingSphere.

Static and Dynamic Friction: Used to simulate friction behavior during object contact, sliding, and grasping.

Restitution Coefficient: Used to control the bounce effect after collision.

These parameters can ultimately be written into USDA assets and checked in the physical visualization interface for visual meshes and collision meshes, providing a foundation closer to the real world for robot grasping and interaction training.


Figure: Physical property visualization interface, allowing simultaneous viewing of visual mesh, collision mesh, center of mass, density, inertia, and mass information.

5. Sim-to-Real: Letting Robots Learn in Simulation and Work in Reality
For embodied intelligence, the endpoint of 3D asset generation is not "looking similar in simulation," but whether the robot can transfer capabilities learned in simulation to the real world. This process is commonly referred to as Sim-to-Real, i.e., capability transfer from Simulation to Reality.

VeyForge's value lies in filling in the most easily underestimated asset and scene gaps before Sim-to-Real: making the shape, material, scale, collision relationships, and physical properties of objects in simulation closer to real objects, so that training data no longer stays at the level of idealized models.

5.1. Real to Sim: Bringing Real Objects into Simulation
Take multi-view photos of real objects, generate textured 3D models, then add physical properties such as collision bodies, mass, friction, and inertia, and finally import them into Isaac Sim. In this way, target objects in robot training scenes are no longer just geometric approximations, but interactive assets with both visual and physical information.

5.2. Sim: Low-cost, High-density Training in the Digital World
In simulation environments, it is possible to rapidly change the shape, size, material, placement, lighting conditions, and background environment of target objects, and batch-generate data for different tasks, perspectives, and difficulty levels. For tasks such as grasping, stacking, navigation, obstacle avoidance, and loading/unloading, simulation can handle a large amount of repetitive training and dangerous scenario testing.

5.3. Domain Randomization: Letting Models See More Variations
The real world always has lighting changes, occlusions, reflections, background interference, and object differences. The multi-category, multi-texture, and multi-shape assets generated by VeyForge can serve as a foundation for data generalization, helping training systems encounter more variations during the simulation phase and reducing the risk of models adapting to only a single scenario.

5.4. Sim to Real: Transferring Simulation Strategies to Real Machines
After the robot completes strategy training in the simulation environment, control strategies, perception results, and action flows can be transferred to real robots. The real2sim2real process showcased on the official website further emphasizes that actions and states on the virtual and real sides can be synchronized, and tasks such as grasping and palletizing can be validated and compared between simulation and real machines.

5. Real to Sim: Letting Real Failures Feed Back into the Next Training Round
Failure cases during real machine operation, such as grasping offset, object slipping, collision misjudgment, and navigation deviation, can be brought back into the simulation environment and transformed into new asset parameters, scene conditions, or training samples. Thus, the process is no longer a one-time simulation-to-real transfer, but a continuous closed loop of real collection—simulation training—real machine validation—data feedback—retraining.

The key to Sim-to-Real is not just importing a model into a simulator, but enabling assets, scenes, physics, data, and strategies to form an iterable closed loop. VeyForge is turning the asset preparation at the front end of this loop into scalable engineering capability.

