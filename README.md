# backTalk-AI
`postman`, `api-testing`, `newman`, `SQA`, `automation`
# 🧪 BackTalkAI – Postman API Testing Collection

This repository demonstrates automated API testing for the **BackTalkAI** project using **Postman** and **Newman**. It includes robust test scripts, environment variable usage, negative test cases, and detailed HTML test reports.

---

## 📦 Project Contents

| File Name                            | Description                                                              |
|-------------------------------------|--------------------------------------------------------------------------|
| `BackTalkAI.postman_collection.json`| Postman collection with API tests (Signup, Signin, Forgot Password, Chat)|
| `BackTalkAI.postman_environment.json`| Postman environment file (with base URL and collection variables)        |
| `BackTalkAI_API_report.html`        | Newman HTML report (22 assertions, 0 failures)                           |
| `BackTalkAi_API_report_4time_run.html`| Extended Newman report (4 iterations, all passed)                      |
| `screenshots/report-summary.png`    | Optional screenshot from the test report                                |

---

## 🧰 Tools & Technologies

- [Postman](https://www.postman.com/)
- [Newman](https://www.npmjs.com/package/newman)
- [htmlextra Reporter](https://github.com/DannyDainton/newman-reporter-htmlextra)

---

## 🚀 How to Run the Tests

### 1. Install Newman and HTML Reporter globally

```bash
npm install -g newman newman-reporter-htmlextra
```
### 2. Run the Collection
```bash
newman run BackTalkAI.postman_collection.json -e BackTalkAI.postman_environment.json -r htmlextra --reporter-htmlextra-export BackTalkAI_API_report.html
```
### 3. TO Run the test 4 time 
```bash
newman run BackTalkAI.postman_collection.json -e BackTalkAI.postman_environment.json -r htmlextra --iteration-count 4 --reporter-htmlextra-export BackTalkAi_API_report_4time_run.html
```

