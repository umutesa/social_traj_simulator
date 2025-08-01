

## Social Force Model Implementation

This tool implements the **Social Force Model** developed by **Dirk Helbing** at **ETH Zurich**, which simulates pedestrian dynamics by modeling individuals as particles influenced by various forces.

###  Forces Defined in the Model

#### 🚶‍♂ Driving Force
The **driving force** propels each pedestrian toward their intended destination. It is defined as:

$$
\vec{f}_i^{\,\text{drive}} = \frac{v_i^0 \vec{e}_i - \vec{v}_i}{\tau}
$$

- \( v_i^0 \): desired speed of pedestrian *i*  
- \( \vec{e}_i \): desired direction of movement  
- \( \vec{v}_i \): current velocity  
- \( \tau \): relaxation time (how quickly the pedestrian adjusts their velocity)

####  Repulsive Force
Pedestrians exert a **repulsive force** on each other that increases exponentially as they get closer:

$$
\vec{f}_{ij}^{\,\text{rep}} = A_i \exp\left(\frac{r_{ij} - d_{ij}}{B_i}\right) \vec{n}_{ij}
$$

- \( A_i \), \( B_i \): interaction strength and range  
- \( r_{ij} \): sum of radii of pedestrians *i* and *j*  
- \( d_{ij} \): actual distance between them  
- \( \vec{n}_{ij} \): normalized vector from *j* to *i*



### 📚 Reference

Helbing, D., & Molnár, P. (1995). *Social force model for pedestrian dynamics*. Physical Review E, 51(5), 4282.  
[Link to paper](https://doi.org/10.1103/PhysRevE.51.4282)

