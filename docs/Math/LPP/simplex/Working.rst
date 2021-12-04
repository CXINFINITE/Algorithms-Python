#######
Working
#######

Description
===========
This illustrates the basic working of simplex algorithm.

Mathematical steps
==================
Pre-processor
-------------
1. Convert the objective function / simplex problem into maximization type.
2. Convert constraint equations into standard form.

Simplex algorithm
-----------------
1. Select initial basis to form initial basic feasible solution.
2. Calculate initial simplex table.
3. Compute deltaJ = Zj - Cj for all j,
   where Zj = vectorsum(Zij), Zij = CBi * aij.
4. If deltaJ <= 0 for any j, goto 5, else goto 11.
5. Select key column as column whose deltaJ is most negative, i.e. far from
   0 toward left side of number line.
6. Select key row as row whose minimum ratio is least positive, but not
   infinity.
   If all ratios are negative or infinity, solution is unbounded and hence
   the calculation can't proceed further.
   Stop.
7. Calculate new iteration table.
8. For key row, key element = 1 and rest elements = oldvalue / key element
   value.
9. For non-key rows, key column = 0 and rest elements = old value - 
   ((corresponding key row value * corresponding key column value) /
   key element value).
10.Goto 4.
11.Solution is optimal, last iteration table gives the solution.
12.Optimal value can be derived by XB's x by corresponding b in objective
   function with other x's as 0 and calculating the sum.
