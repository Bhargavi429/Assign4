# Assign4
Frequency <-c(0.6, 0.3, 0.4, 0.4, 0.2, 0.6, 0.3, 0.4, 0.9, 0.2)
BloodPressure <-c(103, 87, 32, 42, 59, 109, 78, 205, 135, 176)
FirstAssessment <-c(1, 1, 1, 1, 0, 0, 0, 0, NA, 1)
SecondAssessment <-c(0, 0, 1, 1, 0, 0, 1, 1, 1, 1)
FinalDecision <-c(0, 1, 0, 1, 0, 1, 0, 1, 1, 1)

# Create a data frame
df <-data.frame(Frequency, BloodPressure, FirstAssessment, SecondAssessment, FinalDecision)

# Side-by-side boxplot
par(mfrow = c(1, 2))  
boxplot(BloodPressure ~ FirstAssessment, data = df, main = "Boxplot of Blood Pressure by First Assessment", xlab = "First Assessment", ylab = "Blood Pressure")

boxplot(BloodPressure ~ SecondAssessment, data = df, main = "Boxplot of Blood Pressure by Second Assessment", xlab = "Second Assessment", ylab = "Blood Pressure")

# Histogram
hist(BloodPressure, main = "Histogram of Blood Pressure", xlab = "Blood Pressure", col = "skyblue", border = "black")

