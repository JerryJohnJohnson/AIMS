# AIMS

import pandas as pd

# change kernel


df=pd.read_csv("carprices.csv")
df

# change kernel

new = df.drop('Age(yrs)',axis=1)
new

# change kernel

Car_Model = ['Audi A5', 'Mercedez Benz C class','BMW X5']

# change kernel
from sklearn.preprocessing import OrdinalEncoder

# change kernel
enc = OrdinalEncoder(categories=[Car_Model])

# change kernel

new['Car_Model'] = enc.fit_transform(new[['Car_Model']])
new

# change kernel

X = new.drop('Sell_Price',axis=1)
X

# change kernel

y = new.Sell_Price
y

# change kernel

from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X,y)

# change kernel

model.predict([[2,50000]])
