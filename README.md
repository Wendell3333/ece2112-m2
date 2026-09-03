# ece2112-m2

I. Intended Learning Outcomes

At the end of this laboratory activity, the student should be able to:
  1. create and reshape NumPy arrays using appropriate NumPy functions;
  2. perform vectorized numerical operations on an ndarray;
  3. compute array statistics and use Boolean conditions to select elements; and
  4. save computed NumPy arrays as .npy files.

II. Instructions

Write Python code in a Jupyter Notebook to solve each problem. Import NumPy as np. Place each problem in a separate, clearly labeled section of the notebook.
  • Use NumPy array operations. Do not use Python loops or list comprehensions to perform the required numerical calculations or filtering.
  • Donothard-code a computed result. Construct every result from the array specified in the problem.
  • Use the exact variable and output filenames stated below.
  • Display the requested checks in the notebook before saving each result.
  • Do not use libraries other than NumPy

III. Programming Problem

A. REPRODUCIBLE NORMALIZATION PROBLEM

      np.random.seed(2112)
      
This line of code creates a seed for random numbers, ensuring the experiment can be reproduced exactly the same way each time.

    X = np.random.randint(10, 101, size=(5, 5))

This creates a 5x5 array X with numbers ranging from 10 to 101.

    X_normalized = (X - X.mean())/X.std()

This is the formula for computing the normalized values of each number, with X.mean() returning the array's mean and X.std() its standard deviation. and then saving the result of the equation in and X_normanlized array.

    np.save("X_normalized.npy", X_normalized)

This saves the X_normalized array into "X_normalized.npy".

B. CUBES DIVISIBLE BY 4 PROBLEM

    C = np.arange(1,101,1)

Creates an array of the first 100 positive integers, the first argument being the start of the array, the second argument being the threshold, and the third argument being the increment. Then, save these values into the array C.

    C = C.reshape(10,10)

Reshapes C into a 10x10 array.

    C = pow(C, 3)

Cube each of the elements inside the array C.

    div_by_4 = C[C % 4 == 0]

Then, find any number inside the array C that is divisible, and then save it into the div_by_4 array.

C. ABOVE-MEAN SQUARES PROBLEM

    above_mean = S[S > S_mean]

Grabs any number greater than S_mean from the S array.

This problem combines many ideas and techniques from the other two problems, leaving no unique codes to explain. 
