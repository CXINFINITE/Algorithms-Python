############
Data Formats
############

Formats
=======
Constraint::
   
   lhs
      list [(float, str,),] - [(coefficient, 'variable',),].
   equalityType
      str - '<|>|<=|>=|='.
   rhs
      float - constant.

AuxillaryConstraint::
   
   lhs
      list [(float, str,),] - [(coefficient, 'variable',),].
   equalityType
      str - '<|>|<=|>=|='.
   rhs
      float - constant.
   slackVariable
      NoneType or str - None or 'd1|d2|e1|e2|...'

Row::
   
   i
      int - 1, 2, ...
   CB
      float - 0.0, 1.0, ...
   B
      str - 'a1|a2|...'.
   XB
      str - 'x1|x2|...'.
   b
      float - -inf, -1.0, 0.0, 1.0, inf, ...
   aj
      dict {str: float} - {'a1': 0.1,}.
   zij
      dict {str: float} - {'a1': 10.0,}.
   isKeyRow
      bool - True|False.
   minRatio
      float - 2.0.

IterationTable::
   
   iteration
      int - 1, 2, ...
   Cj
      dict {str: float} - {'a1': 0.0,}.
   aj
      list [str,]- ['a1', 'a2',].
   keyRow
      NoneType or Row - None or Row().
   keyColumn
      NoneType or str - None or 'a1'.
   keyElement
      NoneTyep or float - None or 0.0.
   rowi
      list [Row,] - [Row(),].
   zj
      dict {str, float} - {'a1': 10.0,}.
   deltaJ
      dict {str, float} - {'a1': 0.0,}.

OptimalSolution::
   
   iterationTable
      IterationTable - IterationTable().
   Xj
      dict {str: float,} - {'a1': 2.0,}.
   optimalValue
      float - 5.0.

SimplexProblem::
   
   problemType
      str - 'min' or 'max'.
   objectiveFunction
      list [(float, str,),] - [(coefficient, 'variable',),].
   auxillaryObjectiveFunction
      list [(float, str,),] - [(coefficient, 'variable',),].
   constraints
      list [Constraint,] - [Constraint(),]
   auxillaryConstraints
      list [Constraint,] - [Constraint(),]
   slackLetter
      str - 'd1|d2|...'.
   slacks
      int - 1, 2, ...
   netVariables
      tuple - ('x1',).
   AXBMaps
      dict {str: str,} - {'a1': 'x1',}.
   XABMaps
      dict {str: str,} - {'x1': 'a1',}.
   iterationTables
      list [IterationTable,] - [IterationTable(),]
   terminated
      NoneType or bool - None or True|False.
   terminationReason
      str - 'Some reason'.
   optimalSolution
      OptimalSolution - OptimalSolution()
