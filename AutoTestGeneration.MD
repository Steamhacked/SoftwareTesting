Fuzz Testing (Fuzzing) - automated testing technique which is focused on providing unexpected//invalid inputs. It is used to find any possible exploits, the main drawback is that there is no
predicted outpud (which is a minor drawback, since most of the times, an actual output would be an error)

Mutation-Based: Modifying valid inputs to be invalid by various means
Feedback-Based: Optimization approach, generate test cases -> execute -> retrieve feedback -> fuzzer is expected to improve in effectiveness
Generation-Based: Generate test cases based on the given set of rules for valid input

Genetic Algorithm:
  1) Compute fitness score for each member of the current generation G_i
  2) Select a subset of G_i, such that members of that subset have greater fitness than the rest of G_i, by a certain threshold
  3) Use members of the subset ad "parents" to "breed" the next generation
  4) Set current generation to be G_i+1

Applied in Testing:
  1) Set of all possible inputs -> population, subsets of it -> generations
  2) Score fitness for each test input
  3) View each input as a sequence of bytes
  4) 2 Possible Ways:
    a) Choose random byte offsets common to 2 members of the subset, replace bytes of one member to bytes of another, based on the offsets
    b) Choose one input, replace byte at one random position

GA might take many iterations to reach optimal set

Symbolic Execution - executing code using symbolic, rather than concrete, variables, to generate set of constraints to execute each path of the code
It relies on solver's capabiltiies, therefore it might fail in cases of complex expressions
