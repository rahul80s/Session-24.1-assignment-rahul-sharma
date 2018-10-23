# Session-24.1-assignment-rahul-sharma

Acagild session 24.1 assignment 

Problem Statement

1. Perform the below given activities:

a. Take a sample data set of your choice

b. Apply random forest, logistic regression using Spark R

c. Predict for new dataset


Ans ->

# Load training data

x <- read.x("libsvm_data.txt", source = "libsvm")

training <- x

test <- x

# For random forest classification model with spark.randomForest

abc <- spark.randomforest(training, label ~ features, "classification", numtrees = 20)

# Summary of model

summary(abc)

# Prediction for random forest

xyz <- predict(abc, test)

head(xyz)

# extracting training data

x <- read.x("libsvm_data.txt", source = "libsvm")

training <- x

test <- x

# For binomial logistic regression model with spark.logit

abc <- spark.logit(training, label ~ features, maxiter = 20, regparam = 0.5, elasticnetparam = 0.10)

# Summary of model

summary(abc)

# Prediction for logistic regression

xyz <- predict(abc, test)

head(xyz)

