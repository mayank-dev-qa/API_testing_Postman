📊 API Testing Summary Report

## 🧪 Project: Reqres API Testing using Postman
- 🔧 Tool: Postman (with JavaScript assertions)
- 📅 Date: June 2025
- 🌐 Base URL: https://reqres.in

---

## ✅ APIs Covered

| Method | Endpoint             | Description                  |
|--------|----------------------|------------------------------|
| GET    | /api/users/2         | Get single user              |
| GET    | /api/users?page=2    | Get paginated users          |
| POST   | /api/users           | Create new user              |
| POST   | /api/login           | Login with credentials       |
| PUT    | /api/users/2         | Full update                  |
| PATCH  | /api/users/2         | Partial update               |
| DELETE | /api/users/2         | Delete user                  |

---

## 🧪 Test Case Summary

| API                | Test Cases | Passed | Failed | Status |
|--------------------|------------|--------|--------|--------|
| GET /users/2       | 3          | 3      | 0      | ✅     |
| GET /users?page=2  | 2          | 2      | 0      | ✅     |
| POST /users        | 3          | 3      | 0      | ✅     |
| POST /login        | 3          | 3      | 0      | ✅     |
| PUT /users/2       | 2          | 2      | 0      | ✅     |
| PATCH /users/2     | 2          | 2      | 0      | ✅     |
| DELETE /users/2    | 2          | 2      | 0      | ✅     |

---

## 📌 Sample Test Case

| TC ID | Endpoint         | Input                          | Expected Output         | Result |
|-------|------------------|--------------------------------|--------------------------|--------|
| TC001 | GET /users/2     | ID = 2                         | Status 200 + user info  | ✅     |
| TC002 | POST /users      | name: \"Mayank\", job: \"QA\" | Status 201 + user id    | ✅     |
| TC003 | POST /login      | missing password               | Status 400 + error      | ✅     |

---

## 📘 Notes

- ✔️ Positive & negative test cases included
- ✔️ Assertions using `pm.expect()`
- ✔️ Response time under 1000ms
- ✔️ All tests passed in latest run
- 📸 Refer to `screenshots/` for visuals

---

**Author**: Mayank Agrawal  
**GitHub**: [mayank--dev-qa](https://github.com/mayank--dev-qa)