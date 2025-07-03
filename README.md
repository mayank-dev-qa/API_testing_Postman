✅API Testing Project using Postman


{{This project showcases REST API testing using Postman, covering all major HTTP methods with both positive and negative test cases. The dummy API used is from reqres.in.}}

@@@@🔍 Overview

Tested APIs: GET, POST, PUT, PATCH, DELETE

Manual test cases written and executed using Postman GUI

Test validations using JavaScript (Chai assertions) in Postman's Tests tab

Included response validation, status code checks, key presence, and response time

@@@@🧰 Tools Used

!Postman

!JavaScript (Chai assertions)

!Reqres.in (dummy REST API)

!GitHub (for version control)

@@@@📂 Folder Structure

API-Testing-Postman/
├── README.md
├── postman_collection/
│   └── API_Testing_Collection.json
├── screenshots/
│   ├── get_user_passed.png
│   ├── post_user_created.png
│   └── ...
├── reports/
│   └── API_Testing_Summary_Report.md

@@@@✅ What's Covered?

#HTTP Method

#Description

#GET

{Fetch user(s), handle invalid IDs}

#POST

{Create user, login with/without credentials}

#PUT

{Full update of user data}

#PATCH

{Partial update}

#DELETE

{Delete user by ID}

@@@@2🧵 Key Highlights

✅ Functional testing of all endpoints

✅ Test scripts using pm.test() in Postman

✅ Response time validation (< 1000ms)

✅ Assertion of response body and keys

✅ Negative scenarios tested (invalid login, missing data)

@@@@🔄 How to Run

1. Open Postman

2. Import API_Testing_Collection.json from postman_collection/

3. Click on each request or use Collection Runner

4. Check Tests tab and Response for results

@@@@📸 Screenshots::

Screenshots of all passed tests and responses are available in screenshots/ folder.

  !!!!🌐 Author !!!!!!

  {{{{Mayank Agrawal}}}}

✅GitHub: mayank--dev-qa

"Testing is not just about finding bugs, it's about ensuring quality."