# DummyRestAPI

### Prerequisites:
Install Postman (I don't think it's necessary tbh, but if you have trouble with newman later on please tick this step too)

Install nodejs

Run in cmd: npm install -g newman

### For basic execution
Either import the collection in Postman and run it from there

OR

Run in cmd: newman run [COLLECTION-LOCATION]\DummyRest.postman_collection.json

* make sure to replace [COLLECTION-LOCATION] to the path where the collection is (e.g. C:\Users\ADMIN\Desktop\DummyRest)

### For reporting in HTML file
Run in cmd: npm install -g newman-reporter-htmlextra

Run in cmd: newman run [COLLECTION-LOCATION]\DummyRest.postman_collection.json -r htmlextra --reporter-htmlextra-export [COLLECTION-LOCATION]\TestResults.html

### Known issues:
- 429 "Too many requests error" will likely occur when running the tests. The target website tries to protect itself against abuse by limiting how many requests you can make.
- No data persistence from the target API
