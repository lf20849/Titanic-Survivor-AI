# Titanic-Survivor-AI

This program is designed to predict who would survive the titanic using a Machine learning prediction algorithem. We use a dataset which contains the data that we use to predict.
The dataset contains the varialbes:


    PClass --  (Travle Class e.g 1 Class, 2 Class & 3 Class)
    Name  -- (Name of Person)
    Sex  -- (Gender of Person)
    Age  -- (Age of Person)
    SibSp  --  (Siblings & Spouses)
    Parch  --  (Parent & Children)
    Ticket --  (Ticket Number)
    Fare  --  (Price of Ticket)
    Cabin  -- (Cabin/Room Number)
    Embarked -- (Where they got on the ship e.g S, Q & C)
    
  
-- For embarked S is Southampton, Q is Queenstown and C is Cherborg


First what we did is we found corrolations between the catagories in the dataset. With that we can use the corrolations and display then graphically which will help us see what catagories affect which. Analysing this we can see that all catagories are important to the machine learing prediction model. With the corrolations it help use design our first version of the Explaitory Data Analysis(EDA) model. When developing the first EDA we dropped some catagories with too many null values and then filled in the rest of the catagories null values with simple data, this made the perdiction  model less accurate and so we decidec to use pre-processing instead.


With the data having empty fields we decided to use pre-processing from that we determin what values should be entered into the null fields, which would help improve the prediction modle.With pre-processing we were able to find the medain value of age using the mean age of each gender and which class they belonged to. When it came embarked we just filled the empty fields with S for Southhampton as there was a higher number of people traveling from southhampton. We did a similar thing with fare but we used the passenger class they belonged to, the number of parents and children they had and the number of sibling and spouses they had to find a median. 



With all that done then what we did is put the cabins into decks as we had the ships layout and we found:

        Cabins A, B, C are all first class
        Cabin D is mostly first class(87%) and partly second class(13%)
        Cabin E is mostly first class(83%) and partly second class(10%) and a small amout is third class(7%)
        Cabin F is mostly second class(62%) and partly thrid class(38%)
        Cabin G is all thrid class
        Cabin T has only one person and they are in first class


-- With cabin T is it most like cabin A and therefore we put then togeter.

After this we found ther survival rare of each cabin and displayed it graphically, with this information we can see that each cabin had different survival rate and this shows us that each passenger class had different survival rate. From this we see that first class has the highest and third class has the lowest.


The cabins are grouped as such:

        A, B & C
        D, E
        F, G
        
Now that all the missing values are filled in we then displayed more corrolations of the new catagories as to see what the missing data effect was on the corrolations. These new corrolations were displayed graphically. As ther is a vast range of ages we decidec to put them into bins which allowed for us to set ranges of people ages and find a the survival rate of different age groups. Once that is compleated we also decided replace some titles of the passengers to more common ones so it make it easier for the prediction model to see if someone was married or not which will help us see if family survival rate was different dependent on wether they were married or not. We also grouped the different tickets together and the frequency of how many time that ticket was bought. Family sizes was also important and we grouped them together too. 


With all of the data now clean and grouped together we were able to use non-numerical & hot-one encoding to convert some of the string data into integers to make it easier for the prediction model to understand the data. Combining the two datasets into one big dataset. After that we find the standard deviation of the dataset and fill in any missing values with either 1 or 0.


Now we use the machine learing model Random Forest to determin the accuracy of each fold of the dataset and display the mean feature importance between the folds graphical as well as a curve graph of the folds. This allowed us to analyes the folds and determin how accurate the machine learning prediction model was per fold. We do one last check to see if there are any missing values using a heatmap before storing the prediction data into a csv file. Once that is done then the program cleans the new prediction dataset as the survival column has 1.0 or 0.0 as a result and therefor it need to converted to an intger not a float which the program does.

The final prediction dat is stored in a csv file and then is displayed.
        
