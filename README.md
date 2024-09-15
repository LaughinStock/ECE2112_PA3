# ECE2112_PA3
John Felipe M. Domingo

This is an introductory assignment to help students understand the basics of Python.
Done by an undergraduate student of Electronics Engineering at the University of Santo Tomas.
Section: 2ECE-A

This programming assingment (PA) deals with the used of Pandas, a software library written for Python that deals
with data manipulation and analysis. It offers data structures and operations for manipulating
numerical tables and time series (examining data).

To start with this assignment we must import the numpy and pandas libraries and the cars.csv file into the Jupyter Notebook.
Download first the cars.csv file into your computer and then move it into your Jupyter Notebook folder.
To import the csv file into the notebook, we are going to use the "pd.read_csv('cars.csv').

![image](https://github.com/user-attachments/assets/de60329c-ccdc-451b-ae8e-c4e443bb8838)

# Problems

## **3.1**, Displaying the first and last five rows of the file, "cars.csv".
  The first two problems are simple to solve, after importing and using pandas, we are going to utilize
    the functions *".head()"*, and *'.tail()*' in order to display the first (head) and last (tail) five
    rows of cars (cars.csv). 

  ### A. Output of ".head()"
   ![image](https://github.com/user-attachments/assets/98e13691-7208-4367-a5ee-0c7b6369d5f0)

  ### B. Output of ".tail()"
   ![image](https://github.com/user-attachments/assets/56393846-621f-4c0e-b649-4e52b1170805)

  In order to save these functions, we are going to convert the functions 'carshead' and 'carstail' into arrays
    using *".to_numpy"*. And then continue to save the arrays using the *"np.save()"* function of numpy.

   ![image](https://github.com/user-attachments/assets/e9347b25-374c-4ecd-a23b-400b87e664ec)

## **3.2**, Extracting information using slicing, subsetting, and indexing.
  Compared to the first problem, this one is going to use the different extracting methods such as slicing, subsetting,
    and indexing. The second problem is divided into four parts. 
    
   **A.** Display the first five rows with odd-numbered columns (1, 3, 5, 7, ...).
   **B.** Display the row that contains the 'Model' of 'Mazda RX4'.
   **C.** How many cylinders ('cyl') does the car model 'Camaro Z28' have?
   **D.** Determine how many cylinders ('cyl') and what gear type ('gear') do the car models 'Mazda RX4 Wag',  
          'Ford Pantera L', and 'Honda Civic' have.
  
  For majority of the parts, we are going to utilize the *".loc[]"* and *".iloc[]"* functions of pandas
  in order to find the exact data that we are going to find. 
 
  ### A. Output of "carshead.iloc[:, 1::2]"
   ![image](https://github.com/user-attachments/assets/e4b9d53a-770d-4ba8-8d1c-9a72b3e785bd)
  
  For part A, we are going to use *".iloc"* because we are focused on selecting columns by their position 
  and not by their name. The syntax '[:, 1::2]' is explained as '[select all rows, index 1 and then every second column]'

  In part B, we are finding the data in "carshead" which contains the car 'Model' of 'Mazda RX4'.
  ### B. Output of "carshead.loc[carshead['Model']=='Mazda RX4']"
   ![image](https://github.com/user-attachments/assets/821c69a1-47c9-4fc4-a57d-7f5a90511062)
  
  For part B and others, we are going to use *".loc[]"* because we are now focusing on selecting columns
  because of their specific categories and names.

  ### C. Output of "cars.loc[(cars['Model']) == 'Camaro Z28', ['cyl']]"
   ![image](https://github.com/user-attachments/assets/21370699-4a22-4f12-8ad5-a1641e42651a)
  
  In part C, we are still using the same function but instead of the dataFrame "carshead", we are going to use the 
  whole "cars" dataFrame because the model we are looking for is not available in the carshead dataFrame. 
  Plus the code for this part specifies that only the 'cyl' column should be returned.

  ### D. Output of "cars.loc[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']), ['Model', 'cyl', 'gear']]"
   ![image](https://github.com/user-attachments/assets/594881e5-b961-4e31-9532-b75219338bc9)
  
  In part D, we are going to continue to use the whole "cars" spreadsheet because we are now looking for multiple
  data entries with corresponding datas. Since this problem requires us to find the datas corresponding to multiple 
  values, we are going to use the 'isin()' function to filter rows based on multiple values. And then specify which 
  values/data is returned when that specific 'Model' is matched.
 
  ### E. Code for creating and saving the dictionary into .npy
   ![image](https://github.com/user-attachments/assets/4b7efd09-08ee-4992-b4d5-9e1b72fc6edd)
  
  Now in order to save the created dataframes into "DomingoJF_Pandas_P2, we are going to first convert the variables 
  into arrays using the *".to_numpy"* function of numpy and then store the arrays into a dictionary (*dict = {*) in order
  for the arrays to be saved into a .npy file.




  





