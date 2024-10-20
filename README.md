# AIMS
import pandas as pd
df = pd.read_csv("carprices.csv")
dummy = pd.get_dummies(df.Car_Model)
merged = pd.concat([dummy, df],axis='columns')
dropped = merged.drop('Car_Model', axis=1)
dropped
