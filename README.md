# Magnetorotational Instability （MRI) 
The magnetorotational instability (MRI) is a very important instability in astrophysics. It is a fluid instability that causes an accretion disk orbiting a massive central object to become trubulent.  
  
The MRI happens when a group of plasma rotating around a central object with big mass (like black hole) and will destroy the structure of the plasma.We are going to use Python 3 to simulate the MRI phenomenon in two dimension. We mainly refer to the paper written by Riquelme[1].  
  
We use Particle-In-Cell (PIC) method which divide the box into many grids(cells) and put several particles in each grid. We will only record the position of the particles. For other variables like velocity, currency, electric field, and magnetic field, we assume that they are not attached the particles but the grids. 
  
First we will set the initial values, then calculate the grid-related variables and the postion of the particles. We will check if the particles move from one grid to another and redistribute them if they do. After that, the code will move forward to next loop.  
  
The main class we write is Particle_in_cell_2D(Lx, Lz, Nx, Nz, t_max, dt, dt_out, alpha, D), where Lx, Lz are the size of the box, Nx, Nz are the number of grid in x and z direction, t_max, dt are the running time and the length of time step, alpha is the smooting factor and D is the diffusion factor.  
  
To get the final result, use Particle_in_cell_2D.solve(), which will give (x,z, pos_x, pos_z, Ux, Uy, Uz, Bx, By, Bz, Ex, Ey, Ez) respectively.  
  
Packages we use:  
&bull; numpy  
&bull; matplotlib  
&bull; scipy  
&bull; jupyter
