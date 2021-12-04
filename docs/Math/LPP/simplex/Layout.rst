######
Layout
######

Layout
======
::
   ./simplex/
      algorithm.py
         SimplexAlgorithm
            frameAuxillary
               Frames auxillary components.
            frameInitialSimplexTable
               Frames initial simplex table.
            calculateDeltaJ
               Calculated deltaJ
            calculateKeys
               Calculates key components.
            calculateNewIterationTable
               Calculates new iteration table.
            frameOptimalSolution
               Frames optimal solution.
            calculateOptimalSolution
               Calculates optimal solution, automatically.
      
      customExceptions.py
         CustomExceptions
            PreProcessError
               Exception.
            FrameError
               Exception with ability to terminate SimplexProblem.
            CalculationError
               Exception with ability to terminate SimplexProblem.
            
            safe_execute
               Exception handler to safely execute a function.
      
      dataStructures.py
         Contains following data structures:
            Constraint
            AuxillaryConstraint
            Row
            IterationTable
            OptimalSolution
            SimplexProblem
      
      preprocessor.py
         PreProcessor
            processExpression
               Processes single expression.
            objectiveFunction
               Processes objective function and generates SimplexProblem.
            processConstraints
               Processes and attaches constraints to SimplexProblem.
            preProcess
               Pre-processes simplex problem, automatically.
