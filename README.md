# Numcom-m.d.
import numpy as np
r1=10
r2=30
r3=10
r4=10
v1=303
v2=0
#Mesh1
i1_mesh1=r1
i2_mesh1=r1
v_mesh1=v1

#Mesh2
i1_mesh2=-r1
i2_mesh2=r1+r2
i3_mesh2=-r2
v_mesh2=v2

#Mesh3
i2_mesh3=-r2
i3_mesh3=r3+r2
i4_mesh3=-r3
v_mesh3=v2

#Mesh4
i3_mesh4=-r3
i4_mesh4=r3+r4
v_mesh4=v2
R = np.matrix([[i1_mesh1, i2_mesh1, 0, 0],[ i1_mesh2, i2_mesh2, i3_mesh2, 0], [0, i2_mesh3, i3_mesh3, i4_mesh3], [0, 0, i3_mesh4, i4_mesh4]])
V = np.matrix([[v_mesh1], [v_mesh2], [v_mesh3], [v_mesh4]])
I = np.linalg.inv(R) 
print(I)
