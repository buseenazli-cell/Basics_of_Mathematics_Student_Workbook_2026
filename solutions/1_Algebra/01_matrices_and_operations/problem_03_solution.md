import numpy as np

M = {"A": np.ones((2, 3)), "B": np.ones((3, 4)),
     "C": np.ones((4, 2)), "D": np.ones((2, 2))}

for p in ["AB", "BA", "BC", "CB", "AC", "CA", "AD", "DA"]:
    try:
        print(p, "->", (M[p[0]] @ M[p[1]]).shape)
    except ValueError:
        print(p, "-> not defined")
