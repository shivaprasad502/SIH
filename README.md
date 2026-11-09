 weeek6
 
 @relation Iris

@attribute sepallength REAL
@attribute sepalwidth REAL
@attribute petallength REAL
@attribute petalwidth REAL

@attribute class {Iris-setosa,Iris-versicolor,Iris-virginica}

@data
5.1,3.5,1.4,0.2,Iris-setosa
4.9,3.0,1.4,0.2,Iris-setosa
4.7,3.2,1.3,0.2,Iris-setosa
4.6,3.1,1.5,0.2,Iris-setosa
5.0,3.6,1.4,0.2,Iris-setosa
5.4,3.9,1.7,0.4,Iris-setosa
4.6,3.4,1.4,0.3,Iris-setosa
5.0,3.4,1.5,0.2,Iris-setosa
4.4,2.9,1.4,0.2,Iris-setosa
4.9,3.1,1.5,0.1,Iris-setosa

Week1,week7 

@relation Student 
@attribute age { <30, 30-40, >40 } 
@attribute income { low, medium, high } 
@attribute student { yes, no } 
@attribute credit_rating { fair, excellent } 
@attribute marks numeric 
@attribute buysPC { yes, no } 
@data 
<30, high, no, fair, 80, no 
<30, high, no, excellent, 40, no 
30-40, high, no, fair, 65, yes 
>40, medium, no, fair, 90, yes 
>40, low, yes, excellent, 99, no 
>40, low, yes, fair, 60, yes 
30-40, low, yes, excellent, 70, yes 
<30, medium, no, fair, 75, no 
<30, low, yes, fair, 80, no 
>40, medium, yes, fair, 55, yes 
>40, medium, yes, excellent, 88, yes 
30-40, medium, no, excellent, 78, yes 
30-40, high, yes, fair, 45, yes 
>40, medium, no, excellent, 40, no


Week2,3 
@relation Contact_lenses 
@attribute age {young, pre-presbyopic, presbyopic} 
@attribute spectacle-prescrip {myope, hypermetrope} 
@attribute astigmatism {no, yes} 
@attribute tear-prod-rate {reduced, normal} 
@attribute contact-lenses {soft, hard, none} 
@data 
young, myope, no, reduced, none 
young, myope, no, normal, soft 
young, myope, yes, reduced, none 
young, myope, yes, normal, hard 
young, hypermetrope, no, reduced, none 
young, hypermetrope, no, normal, soft 
young, hypermetrope, yes, reduced, none 
young, hypermetrope, yes, normal, hard 
pre-presbyopic, myope, no, reduced, none 
pre-presbyopic, myope, no, normal, soft 
pre-presbyopic, myope, yes, reduced, none 
pre-presbyopic, myope, yes, normal, hard 
pre-presbyopic, hypermetrope, no, reduced, none 
pre-presbyopic, hypermetrope, no, normal, soft 
pre-presbyopic, hypermetrope, yes, reduced, none 
pre-presbyopic, hypermetrope, yes, normal, hard 
presbyopic, myope, no, reduced, none 
presbyopic, myope, no, normal, none 
presbyopic, myope, yes, reduced, none 
presbyopic, myope, yes, normal, hard 
presbyopic, hypermetrope, no, reduced, none 
presbyopic, hypermetrope, no, normal, soft 
presbyopic, hypermetrope, yes, reduced, none 
presbyopic, hypermetrope, yes, normal, none 



week4 
@relation Emp 
@attribute Age {20,30,40,50} 
@attribute Dept {cse,ece,csd,csm} 
@attribute Experience {3,4,5,6} 
@attribute Salary {50000,60000,70000,80000} 
@attribute Attendance {50,60,75,90} 
@attribute Performance {good,avg,poor} 
@data 
20,cse,3,50000,50,poor 
30,ece,4,60000,75,avg 
40,cse,5,70000,60,good 
50,csm,6,80000,90,good 
20,csd,4,50000,75,avg 
50,cse,6,80000,90,good 
20,csm,4,60000,75,avg 
50,ece,6,50000,60,avg 
40,cse,4,70000,75,good 
30,csm,3,50000,90,poor 



Week5 
@relation Employee 
@attribute Age {Young, Middle, Senior} 
@attribute Department {IT, HR, Finance, Sales} 
@attribute Experience {Low, Medium, High} 
@attribute Salary {Low, Medium, High} 
@attribute Attendance {Poor, Average, Good} 
@attribute Performance {Poor, Average, Good} 
@data 
Young, IT, Low, Low, Poor, Poor 
Middle, HR, Medium, Medium, Average, Average 
Senior, Finance, High, High, Good, Good 
Young, Sales, Medium, High, Good, Average 
Senior, HR, High, High, Average, Good 
Middle, Finance, Low, Medium, Poor, Average 
Young, HR, Low, Low, Poor, Poor 
Middle, Sales, Medium, High, Poor, Good 
Senior, IT, High, High, Average, Good 
Young, Sales, Medium, Low, Poor, Average


Week 11 
1. Normal Distribution –
2. dnorm() 
x <- seq(-10, 10, by = 0.1) 
y <- dnorm(x, mean = 2.0, sd = 1.5) 
plot(x, y, main = "Density Normal Distribution", 
xlab = "x", ylab = "Density", type = "l") 
model <- lm(y ~ x) 
abline(model, col = "red", lwd = 2)
 
4. Normal Distribution – pnorm() 
x <- seq(-10, 10, by = 0.1) 
y <- pnorm(x, mean = 2.0, sd = 0.5) 
plot(x, y, main = "Cumulative Normal Distribution", 
xlab = "x", ylab = "Cumulative Probability", type = "l") 
model <- lm(y ~ x) 
abline(model, col = "red", lwd = 2)

6. Normal Distribution – qnorm() 
x <- seq(0, 1, by = 0.02) 
y <- qnorm(x, mean = 2, sd = 1) 
plot(x, y, main = "Quantile Normal Distribution", 
xlab = "Probability", ylab = "Quantile", type = "l") 
model <- lm(y ~ x) 
abline(model, col = "red", lwd = 2)

8. Normal Distribution – rnorm() 
y <- rnorm(50) 
hist(y, main = "rnorm", xlab = "Values", col = "blue")

10. Binomial Distribution – dbinom() 
x <- seq(0, 50, by = 1) 
y <- dbinom(x, size = 50, prob = 0.5) 
plot(x, y, main = "Binomial Distribution", 
xlab = "Number of Successes", ylab = "Probability", 
type = "h")

12. Binomial Distribution – pbinom() 
x <- 0:51 
y <- pbinom(x, size = 51, prob = 0.5) 
plot(x, y, main = "Cumulative Binomial Distribution", 
xlab = "Number of Successes", ylab = "Cumulative Probability", 
type = "s")

14. Binomial Distribution – qbinom() 
x <- qbinom(8, size = 150, prob = 0.4) 
print(x) 
plot(x)

rbinom:
x <- qbinom(0.25, size = 51, prob = 0.5) 
print(x) 
plot(x, main = "Binomial Quantile")

week8 
# Mean 
x <- c(10, 20, 30, 40, 50) 
result <- mean(x) 
print(result) 
# Median 
x <- c(10, 20, 30, 40, 50) 
result <- median(x) 
print(result) 
# Mode (user-defined function) 
getmode <- function(a) { 
uniq_a <- unique(a) 
uniq_a[which.max(tabulate(match(a, uniq_a)))] 
} 
a <- c(10, 20, 10, 30, 20, 10, 40) 
result <- getmode(a) 
print(result) 
# Covariance 
x <- c(10, 20, 30, 40) 
y <- c(50, 60, 70, 80) 
result <- cov(x, y) 
print(result) 
boxplot(x, y, names = c("x", "y"), main = "Boxplot of x and y") 
# Linear regression 
x <- c(10, 20, 30, 40) 
y <- c(50, 60, 70, 80) 
result <- lm(y ~ x) 
print(result) 
plot(x, y, main = "Linear Regression", xlab = "x", ylab = "y", pch = 20) 
abline(result, col = "red", lwd = 2) 


week 9 
2. Linear Regression 
stdhrs <- c(1, 2, 3, 4, 5) 
marks <- c(30, 40, 50, 60, 70) 
student <- data.frame(stdhrs, marks) 
print(student) 
model <- lm(marks ~ stdhrs, data = student) 
print(summary(model)) 
plot(stdhrs, marks, 
main = "Linear Regression", 
xlab = "Study Hours", ylab = "Marks", 
pch = 20, col = "blue") 
abline(model, col = "red", lwd = 2) 
# Predict marks for the given study hours 
new_student <- data.frame(stdhrs = c(6, 7)) 
print(predict(model, newdata = new_student)) 

3. Multiple Linear Regression 
experience <- c(1, 2, 3, 4, 5) 
qualification <- factor(c("SSC", "BTech", "MTech", "PhD", "MPhil")) 
salary <- c(1, 2, 3, 4, 5) 
employee <- data.frame(experience, qualification, salary) 
print(employee) 
model <- lm(salary ~ experience + qualification, data = employee) 
print(summary(model)) 
plot(employee$experience, employee$salary, 
main = "Experience vs Salary", 
xlab = "Experience (years)", ylab = "Salary", 
pch = 20, col = "purple") 
abline(lm(salary ~ experience, data = employee), col = "red", lwd = 2) 

4. Logistic Regression 
students <- data.frame( 
studyhours = c(1, 2, 3, 4, 5, 6, 7, 8), 
pass = c(0, 0, 0, 1, 1, 1, 1, 1) 
) 
model <- glm(pass ~ studyhours, data = students, family = binomial()) 
print(summary(model)) 
students$probability <- predict(model, type = "response") 
students$prediction <- ifelse(students$probability >= 0.5, 1, 0) 
print(students) 
plot(students$studyhours, students$probability, 
main = "Logistic Regression", 
xlab = "Study Hours", ylab = "Probability of Passing", 
pch = 19) 
lines(students$studyhours, students$probability, lwd = 2) 

5. Poisson Regression
   
hrs <- c(1, 2, 3, 4, 5, 6, 7, 8) 
ques <- c(2, 3, 4, 6, 8, 10, 13, 16) 
data <- data.frame(hrs, ques) 
print(data) 
model <- glm(ques ~ hrs, family = poisson(), data = data) 
print(summary(model)) 
predicted <- predict(model, type = "response") 
print(predicted) 
plot(data$hrs, data$ques, 
pch = 19, xlab = "Study Hours", 
ylab = "Questions Answered", 
main = "Poisson Regression") 
lines(data$hrs, predicted, lwd = 2) 


week10 

Time Series Analysis 

sales <- c(100, 200, 300, 400, 500, 600, 700, 800, 900, 1000) 
sales_ts <- ts(sales, frequency = 12) 
print(sales_ts) 
plot(sales_ts, type = "o", 
main = "Time Series Analysis", 
xlab = "Months", ylab = "Sales", lwd = 2) 

7. Nonlinear Least-Squares Regression 
year <- c(1, 2, 3, 4, 5, 6) 
population <- c(100, 110, 125, 140, 160, 185) 
model <- nls(population ~ a * exp(b * year), 
start = list(a = 90, b = 0.1)) 
print(summary(model)) 
predicted <- predict(model) 
print(predicted) 
plot(year, population, pch = 19, 
main = "Population Growth (Nonlinear Regression)", 
xlab = "Year", ylab = "Population (thousands)") 
lines(year, predicted, lwd = 2) 
new_year <- data.frame(year = 8) 
predicted_8 <- predict(model, newdata = new_year) 
print(predicted_8) 

8. Decision Tree Modeling (Regression Tree) 
if(!require(rpart) install.packages("rpart")
if(!require(rpart.plot) install.packages("rpart.plot")
library(rpart) 
library(rpart.plot) 
data(mtcars) 
reg_tree <- rpart(mpg ~ hp + wt, 
method = "anova", 
data = mtcars) 
rpart.plot(reg_tree, type = 2, digits = 3, 
fallen.leaves = TRUE, 
main = "Regression Decision Tree (Predicting MPG)")


week12\

Chi-Square Test:
library(MASS)
data(Cars93)
str(Cars93)
car = data.frame(Cars93$AirBags, Cars93$Type)
car = table(Cars93$AirBags, Cars93$Type)
print(car)
mosaicplot(car, main="AirBags vs Car Type",
           col=rainbow(3))
print(chisq.test(car))

T-TEST:
x = c(0.593, 0.142, 0.329, 0.691, 0.231, 0.793, 0.392, 0.418)
result = t.test(x, alternative="greater", mu=0.3)
print(result)
hist(x, probability=TRUE,
     main="One-Sample t-Test",
     xlab="Sample Values",
     ylab="Density",
     col="lightblue",
     border="green")

F-TEST
x = c(66, 67, 75, 76, 82, 84, 88, 90, 92)
y = c(64, 66, 74, 78, 82, 85, 87, 92, 93, 95, 97)
result = var.test(x, y)
print(result)
boxplot(x, y, names=c("Group X", "Group Y"),
        main="Comparison of Variances",
        xlab="Groups",
        ylab="Values",
        col=c("lightblue", "lightgreen"))


