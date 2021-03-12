# Titanic-Survivor-AI

This program is designed to predict who would survive the titanic using a AI prediction algorithem. We use a dataset which contains the data that we use to predict.
The dataset contains the varialbes:


  PClass --  (Travle Class e.g 1 Class, 2 Class & 3 Class)
  Name
  Sex
  Age
  SibSp  --  (Siblings & Spouses)
  Parch  --  (Parent & Children)
  Ticket
  Fare
  Cabin
  Embarked -- (Where they got on the ship e.g S, Q & C)
  
For embarked S is Southampton, Q is Queenstown and C is Cherborg

With the data having empty fields we decided to use pre-processing to find corrolations between certain variables and from that determin what values should be there.
With pre-processing we were able to find the medain value of age using the mean age of each gender and which class they belonged to. When it came embarked we just 
filled the empty fields with S for Southhampton as there was a higher number of people traveling from southhampton. We did a similar thing with fare but we used the class they
belonged to, the number of parents and children the had and the number of sibling and spouses they had to find a median.
