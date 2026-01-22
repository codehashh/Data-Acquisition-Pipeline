Function main():

isLoggedIn = login() 

if (isLoggedIn):

accessDashboard() 
breed = inputBreed() 
age = inputAge() 
observedBehaviors = inputObservedBehaviors() 
isValidData = validateData(breed, age, observedBehaviors) 

if (isValidData): 

preProcessedData = preProcessData(breed, age, observedBehaviors) 
analyzedData = runAnalysis(preProcessedData) 

if (isIssueDetected(analyzedData)): 

generateForecast(analyzedData) 
recommendMeasures(analyzedData) 

else: 
displayNoIssues() 

else: 

displayValidationErrors() 
logActivity() 

else: 
displayAuthorizationFailure()
