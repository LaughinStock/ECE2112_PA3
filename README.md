# ECE2112_PA3
John Felipe M. Domingo

This is an introductory assignment to help students understand the basics of Python.
Done by an undergraduate student of Electronics Engineering at the University of Santo Tomas.
Section: 2ECE-A

This programming assingment (PA) deals with the used of Pandas, a software library written for Python that deals
with data manipulation and analysis. It offers data structures and operations for manipulating
numerical tables and time series (examining data).

To start with this assignment we must import the libraries numpy and pandas 

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

    ### A. Output of "carshead.iloc[:, 1::2]"
      ![image](https://github.com/user-attachments/assets/e4b9d53a-770d-4ba8-8d1c-9a72b3e785bd)

    ### B. Output of "carshead.loc[carshead['Model']=='Mazda RX4']"
      ![image](https://github.com/user-attachments/assets/821c69a1-47c9-4fc4-a57d-7f5a90511062)

    ### C. Output of "cars.loc[(cars['Model']) == 'Camaro Z28', ['cyl']]"
      ![image](https://github.com/user-attachments/assets/21370699-4a22-4f12-8ad5-a1641e42651a)

    ### D. Output of "cars.loc[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']), ['Model', 'cyl', 'gear']]"
      ![image](https://github.com/user-attachments/assets/594881e5-b961-4e31-9532-b75219338bc9)





