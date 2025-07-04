✅API Testing Summary Report

🔗 Base URL: https://reqres.in/


✅ Test Execution Overview:

### ⏱️ Execution Summary:

| Metric                | Value        |
|------------------------|--------------|
| Total Requests         | 10           |
| Total Assertions       | 37           |
| Failed Assertions      | 3            |
| Execution Time         | 3.9 seconds  |
| Avg Response Time      | 303ms        |
| Min/Max Response Time  | 55ms / 469ms |

📌 Request-wise Test Status:

| 🔢 # | Endpoint                              | Method | Status Code | Result     | Notes                                            |
|------|---------------------------------------|--------|-------------|------------|--------------------------------------------------|
| 1    | `/api/users/2`                        | GET    | 200         | ✅ Passed   | All assertions passed                            |
| 2    | `/api/users/1000`                     | GET    | 404         | ✅ Passed   | Status code 404 verified                         |
| 3    | `/api/users?page=2`                   | GET    | 200         | ✅ Passed   | Pagination + email/name checks done              |
| 4    | `/api/users/{{randomUserId}}`         | GET    | 200 / 404   | ✅ Passed   | Dynamic ID handled                               |
| 5    | `/api/users`                          | POST   | 201         | ✅ Passed   | User created successfully                        |
| 6    | `/api/users`                          | POST   | 201         | ❌ Failed   | Negative test – empty name, job undefined        |
| 7    | `/api/users`                          | POST   | 201         | ⚠️ Warning | Deprecated `data` usage, status undefined        |
| 8    | `/api/users/2`                        | PUT    | 200         | ✅ Passed   | Full update + validations                        |
| 9    | `/api/users/2`                        | PATCH  | 200         | ✅ Passed   | Partial update, response time < 1000ms           |
| 10   | `/api/users/2`                        | DELETE | 204         | ✅ Passed   | Empty body + response time check                 |



❌ Failed Assertions:

#
| ❌ Test Description              | Reason                                |
|----------------------------------|----------------------------------------|
| Should NOT accept empty name     | `''` was accepted                      |
| Job should not be undefined      | `job = undefined`                      |
| Status code is undefined         | Expected 201, found undefined          |


{These are expected failures for negative testing, validating how the API behaves with incorrect inputs.}