# demo-api-test
Demo API test script using postman and newman


# Instruction to generate report using Newman and Htmlextra

1. Install Node JS - https://nodejs.org/en/
2. Install Newman npm install -g newman
3. Install HTML report npm install -g newman-reporter-htmlextra
4. Go to the working directory and Run the following command

    newman run ./collection-file/api_test_postman_collection.json -e ./environment-file/api_test_postman_environment.json -r cli,htmlextra --reporter-htmlextra-export ./results/API_Test_Report_%DATE:~-4%-%DATE:~4,2%-%DATE:~7,2%_%TIME:~0,2%.%TIME:~3,2%.%TIME:~6,2%.html --insecure