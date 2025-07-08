# 📦 BV_API_EDI – Postman API Test Collection

This repository contains a Postman collection and environment configuration used for automated API testing of the **BV EDI System**.

## 📁 Files Included

| File                             | Description                                      |
|----------------------------------|--------------------------------------------------|
| `EDI.postman_collection.json`    | Postman collection with API test cases           |
| `BVDEV.postman_environment.json` | Postman environment for BV development server    |
| `result.xml`                     | JUnit test result output from Newman run         |

---

## 🚀 How to Run Tests Locally

Make sure you have [Postman](https://www.postman.com/) and [Newman](https://www.npmjs.com/package/newman) installed:

```bash
npm install -g newman
Run the Collection with Environment
newman run EDI.postman_collection.json -e BVDEV.postman_environment.json --reporters cli,junit --reporter-junit-export result.xml
🧪 Sample CI/CD Integration (Newman + Allure)
You can integrate this collection into CI/CD pipelines using:

GitHub Actions

Jenkins with Newman + Allure

Docker containers

Example:
newman run EDI.postman_collection.json \
  -e BVDEV.postman_environment.json \
  --reporters cli,junit,allure \
  --reporter-junit-export reports/result.xml \
  --reporter-allure-export reports/allure-results
👤 Author
GitHub: @hangho89

Maintainer: thuyhang89