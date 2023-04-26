# Iris-Dataset
College Project on Sample dataset of R (iris)
data()
data("iris")
tab<-table(iris$Species)

#Barplot
barplot(tab, main="Barplot for Species", col=rainbow(3), xlab="Species",
        ylab="count")
<img width="677" alt="Screenshot 2023-04-27 at 2 45 58 AM" src="https://user-images.githubusercontent.com/97010579/234710015-1efa8927-3277-4540-9c62-bef4cd5cd68c.png">

#INSTALLING PACKAGES
install.packages("psych") #used to create a matrix scatter plots and histograms
                          #to visualize the pairwise relationships between variables in a dataset.
library(psych)
pairs.panels(iris[-5]) #-5 represents 
?pairs.panels
pairs.panels(iris[-5],cex.cor = 0.5)

#DAG
install.packages("DAAG")
library(DAAG)
data("rainforest")
str(rainforest)
summary(rainforest)

mean(rainforest$wood) #there's a missing value so there wont be mean, but use next command to get the mean anyway
mean(rainforest$wood, na.rm=TRUE) #remove/omit the missing value

data("science")
str(science)
summary(science)

science[!complete.cases(science),]#used to filter out the missing values
#                                 the GAP after , represents the whole column/row
dim(science)
new<-na.omit(science)
dim(new)

<img width="647" alt="Screenshot 2023-04-27 at 2 45 06 AM" src="https://user-images.githubusercontent.com/97010579/234709825-9b4bd1e3-8a99-4cec-9d54-13bf1599c058.png">


