# Al Bayan - Candidate Assessment Platform

## Overview
Al Bayan is a comprehensive candidate assessment platform designed to streamline the hiring process by allowing HR professionals to create, manage, and evaluate assessments. Inspired by platforms like TestGorilla, Al Bayan provides a variety of question types, full security features during assessments, and a powerful dashboard for administrators.

## Features
### **For HR Professionals**
- Create assessments by combining multiple tests.
- Define various question types, including:
  - True/False
  - Multiple Choice
  - Coding
  - Ranking
  - Dropdown
  - Qualifier
  - Date
  - Number
  - Rating
  - Matching
  - Fill in the Blank
  - Video, Audio, File Upload
  - Slides, Spreadsheet, Document
  - Open-ended, Short Answer, Long Answer
- Send assessments to candidates via Excel sheets.
- View assessment results with detailed grades and insights.

### **For Candidates**
- Take assessments with full security, including:
  - Tab-switch prevention.
  - Camera monitoring for observation.
- Submit tests with a seamless and user-friendly interface.

### **For Super Admins**
- Access a dashboard with real-time statistics on HR and assessments.
- Manage users and platform settings.

## Technologies Used
- **Backend:** Node.js with Express.js
- **Database:** MongoDB (Mongoose ODM)
- **Authentication:** JSON Web Token (JWT), bcrypt for password hashing
- **File Storage:** Cloudinary, Azure Blob Storage
- **Internationalization:** i18next for multi-language support
- **PDF Generation:** Puppeteer (to generate candidate results as PDFs)
- **Email Service:** Nodemailer, Resend (for sending notifications)
- **Data Handling:** XLSX (for importing/exporting candidate data via Excel)
- **Security:** Helmet, CORS, Rate Limiting

## Project Structure
```
al-bayan_backend/
├── app.js
├── controllers
│   ├── adminControllers.js
│   ├── assesController.js
│   ├── assessResultControllers.js
│   ├── assessSubmitControllers.js
│   ├── authControllers.js
│   ├── candidateControllers.js
│   ├── checkRoleController.js
│   ├── contactControllers.js
│   ├── dashboardControllers.js
│   ├── errorControllers.js
│   ├── hrControllers.js
│   ├── questionController.js
│   └── testController.js
├── dbConnect.js
├── models
│   ├── Admin.js
│   ├── Assessment.js
│   ├── AssessmentResult.js
│   ├── Candidate.js
│   ├── ContactRequest.js
│   ├── Question.js
│   └── Test.js
├── package.json
├── package-lock.json
├── routes
│   ├── adminRoutes.js
│   ├── assessmentResultRoutes.js
│   ├── assessmentRoutes.js
│   ├── assessmentSubmitRoutes.js
│   ├── authRoutes.js
│   ├── candidateRoutes.js
│   ├── checkRoleRoutes.js
│   ├── contactRoutes.js
│   ├── dashboardRoutes.js
│   ├── hrRoutes.js
│   ├── questionRoutes.js
│   └── testRoutes.js
├── server.js
├── uploads/
├── utils
│   ├── apiFeatures.js
│   ├── appError.js
│   ├── azureStorage.js
│   ├── catchAsync.js
│   ├── email.js
│   ├── evaluateCodingQuestion.js
│   ├── evaluateQuestion.js
│   ├── helpers/
│   ├── mailer.js
│   ├── puppeteer.js
│   ├── sendCandidate.js
│   ├── sendHr.js
```

## API Endpoints
### **Authentication**
- `POST /api/auth/signup` - Register a new HR user.
- `POST /api/auth/login` - Login HR user.
- `POST /api/auth/forgot-password` - Send password reset link.
- `POST /api/auth/reset-password` - Reset user password.

### **HR Management**
- `GET /api/hr` - Get all HR users.
- `POST /api/hr` - Create a new HR user.
- `DELETE /api/hr/:id` - Delete HR user.

### **Assessments & Tests**
- `POST /api/assessment` - Create a new assessment.
- `GET /api/assessment/:id` - Get assessment details.
- `POST /api/assessment/:id/submit` - Submit an assessment.

### **Candidates**
- `POST /api/candidates` - Add candidates via Excel sheet.
- `GET /api/candidates` - Get all candidates.

### **Results & Reporting**
- `GET /api/assessment-result/:id` - Get assessment results.
- `GET /api/assessment-result/:id/pdf` - Download candidate result as PDF.

### **Super Admin Dashboard**
- `GET /api/dashboard` - Get platform statistics.

## Special Thanks
A special thanks to **Youssef Megahed** and **Ziad Ahmed** for their valuable contributions to this project.

---

## License
This project is licensed under the ISC License.

## Contact
For any inquiries, reach out to `youssef22772002salah@gmail.com`.

---

This `README.md` provides a complete guide for developers, HR users, and administrators working with the Al Bayan platform.

