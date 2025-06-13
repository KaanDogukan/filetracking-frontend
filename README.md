
# 📁 FileTracking – File Validity Tracking System

**FileTracking** is a full-stack file tracking system built with .NET 8 (Web API) and React.  
Users can upload files, get alerts based on expiry dates, and be managed by an admin.

---

## 🚀 Features

### 🔐 Authentication & Role Management
- Identity-based user authentication
- Admin and User roles
- JWT-based authorization

### 📤 File Upload and Management
- Upload files (.pdf, .docx, .jpg, etc.)
- Set expiration dates
- List files nearing expiration

### ⚠️ Alert System
- Separate listing of soon-to-expire files
- Actions:
  - ✅ Extend validity
  - 🕓 Snooze for 5 days
  - 🔕 Suppress alert
  - ❌ Delete file

### 🛠 Admin Panel
- View and delete all user files
- Assign roles to users
- Delete users

---

## 🧱 Project Structure

```
📦 FileTracking
├── FileTracking.API              # .NET Web API
│   ├── Controllers               # Auth and File controllers
│   └── Program.cs / Startup     # Service configurations
├── FileTracking.Application      # CQRS + MediatR logic
│   └── Commands / Queries
├── FileTracking.Infrastructure  # Identity + EF + Services
├── FileTracking.Domain           # Entities and interfaces
├── filetracking-frontend         # React frontend
│   ├── LoginPage.js
│   ├── UploadFile.js
│   ├── ExpiringFilesPage.js
│   ├── AdminPanelPage.js
│   └── UserPanelPage.js
```

---

## ⚙️ Installation

### 🔧 Backend (.NET 8 API)

```bash
cd FileTracking.API
dotnet run
```

- Swagger: `https://localhost:7187/swagger`
- API: `https://localhost:7187` or `http://localhost:5268`

### 💻 Frontend (React)

```bash
cd filetracking-frontend
npm install
npm start
```

- React App: `http://localhost:3000`

---

## 🔑 Default Admin Login

```
Email: admin@mail.com
Password: Admin123!
```

- After login, use `assign-role` to grant Admin privileges to other users.

---

## ✅ Technologies Used

| Technology       | Description                    |
|------------------|--------------------------------|
| ASP.NET Core 8   | Web API backend                |
| MediatR          | CQRS pattern implementation    |
| Identity         | User and role management       |
| EntityFramework  | In-Memory DB (or SQL support)  |
| React            | Frontend UI                    |
| JWT              | Token-based authorization      |
| MailKit          | (Optional) Email notifications |

---
