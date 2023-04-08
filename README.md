# logistic_Regression_exercise
# I save my left column """df[df.left==1]""" as "left" and retained """df[df.left==0]""" as retained
# Then i visualize my data of "salary" and "left" """pd.crosstab(df.salary,df.left).plot(kind='bar')""" using "crosstab"
# And next "department",  "left"  "salary" """pd.crosstab(df.Department, df.left).plot(kind='bar')"""
# I take four columns """df[['satisfaction_level','average_montly_hours','promotion_last_5years','salary']]""" and save as "subdf"
# I need to change "salary" into numerical values using dummies """salary_dummies = pd.get_dummies(subdf.salary, prefix="salary")"""
# Now i have my "df_with_dummies" saved """pd.concat([subdf,salary_dummies],axis='columns')"""
# And i can drop colum "salary" """df_with_dummies.drop('salary',axis='columns',inplace=True)""" 
# I save my "df_with_dummies" on "X" and "df.left" on "y". So I can make "train_test_plit" method on my "X" and "y"
# Then i get "LogisticRegression" model and train my data """model.fit(X_train,y_train)"""
# Finally I can make predictions """model.predict(X_test)""" and get score """model.score(X_test, y_test)"""
