# AIMS

# done in jupyter notebook.


import pandas as pd
df = pd.read_csv("carprices.csv")
df


# change kernel


dummy = pd.get_dummies(df.Car_Model)
dummy


# change kernel


merged = pd.concat([dummy, df],axis='columns')
merged


# change kernel


dropped = merged.drop('Car_Model', axis=1)
dropped


# change kernel


X = dropped.drop('Sell_Price',axis=1)
X


# change kernel


y = merged.Sell_Price
y


# change kernel


from sklearn.tree import DecisionTreeRegressor
model = DecisionTreeRegressor(random_state=1)
model.fit(X,y)


# change kernel


model.predict([[0,1,0,60000,5]])
