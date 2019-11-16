# CMS
Homework 1 for course Computational Methods of Science

import numpy as np
import matplotlib.pyplot as pit
def velocity(v0, t_step):
    g = 9.81
    c = 12.5
    m = 68.1
    t = 0
    n = 1
    all_v = []
    all_v.append(0)
    while n <= 12:
        v = v0 + (g - (c/m)*v0)*(t_step)
        n += t_step
        all_v.append(v)
        v0 = v
    return all_v

a = velocity(0, 4)
b = velocity(0, 2)
c = velocity(0, 1)
d = velocity(0, 0.5)

ta = np.array([0, 4, 8, 12])
tb = np.array([0, 2, 4, 6, 8, 10, 12])
tc = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12])
td = np.array([0, 0.5, 1, 1.5, 2, 2.5, 3, 3.5, 4, 4.5, 5, 5.5, 6, 6.5, 7, 7.5, 8, 8.5, 9, 9.5, 10, 10.5, 11, 11.5])

pit.plot(ta, a)
pit.plot(tb, b)
pit.plot(tc, c)
pit.plot(td, d)
