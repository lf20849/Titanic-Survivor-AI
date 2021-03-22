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
        Cabin T has only one person and is in first class


-- With cabin T is it most like cabin a and therefore we put then togeter.
        
