# internmatch
# 🚀 Internship Discovery Platform

A full-stack web application that helps students discover relevant internship opportunities based on their **skills, course, location, and interests**.

The platform provides personalized internship recommendations, internship search and filtering, application tracking, and role-based features for students and companies/admins.

---

## 🎯 Problem Statement

Students often struggle to find internships that match their actual skills, academic background, interests, and preferred location.

The **Internship Discovery Platform** addresses this problem by providing a centralized platform where students can:

* Create their professional profile
* Add skills and interests
* Search for internships
* Filter opportunities
* Receive personalized recommendations
* View internship details
* Apply for internships
* Track application status

---

## 💡 Key Features

### 👨‍🎓 Student Features

* 🔐 Student registration and login
* 👤 Student profile management
* 🎓 Course selection
* 🛠️ Skills management
* 📍 Location preferences
* ❤️ Interest selection
* 🔎 Internship search
* 🎯 Advanced internship filters
* ⭐ Personalized internship recommendations
* 📊 Internship match percentage
* 📝 Internship applications
* 📋 Application tracking
* 📱 Responsive design

### 🏢 Company/Admin Features

* 🔐 Secure authentication
* ➕ Create internship opportunities
* ✏️ Edit internships
* 🗑️ Delete internships
* 📋 Manage posted internships
* 👥 View student applications
* 🔄 Update application status
* 📊 View basic platform statistics

---

## 🎯 Personalized Matching

The platform calculates how well an internship matches a student's profile.

The recommendation system considers:

| Factor    | Weight |
| --------- | -----: |
| Skills    |    50% |
| Course    |    20% |
| Location  |    15% |
| Interests |    15% |

### Example

A student has:

```text
Skills:
Python
React
SQL

Course:
Computer Science Engineering

Location:
Hyderabad

Interests:
AI
Web Development
```

An internship matching several of these criteria could receive:

```text
87% Match
```

The platform can also explain the recommendation:

```text
✓ 2 matching skills
✓ Same course
✓ Same location
✓ Matching interest
```

---

## 🏗️ System Architecture

```text
                    ┌──────────────────┐
                    │     Student      │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │   React Frontend │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Supabase Auth    │
                    │ & PostgreSQL     │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Matching Engine  │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Recommendations  │
                    └──────────────────┘
```

---

## 🛠️ Tech Stack

### Frontend

* React
* Vite
* JavaScript
* React Router
* Axios
* CSS
* Lucide Icons

### Backend / Database

* Supabase
* PostgreSQL
* Supabase Authentication
* Row Level Security

### Development

* Git
* GitHub
* Replit
* VS Code

---

## 📂 Project Structure

```text
internship-discovery-platform/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── context/
│   │   ├── hooks/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   └── package.json
│
├── backend/
│   └── ...
│
├── .env.example
├── .gitignore
├── README.md
└── package.json
```

---

## 📱 Main Pages

### Student

```text
/login
/register
/dashboard
/profile
/internships
/internships/:id
/applications
```

### Admin / Company

```text
/admin/dashboard
/admin/internships
/admin/internships/create
/admin/applications
```

---

## 🔐 Authentication

The platform uses Supabase Authentication for:

* Registration
* Login
* Logout
* Session management
* Protected routes

User roles include:

```text
Student
Company
Admin
```

Access to different features is controlled based on the user's role.

---

## 🗄️ Database

The application uses Supabase PostgreSQL.

Main entities include:

```text
Users / Profiles
      │
      ├── Skills
      ├── Course
      ├── Location
      └── Interests

Internships
      │
      ├── Skills
      ├── Courses
      ├── Location
      ├── Interests
      └── Company

Applications
      │
      ├── Student
      ├── Internship
      └── Status
```

---

## 🔎 Internship Search

Students can search for opportunities using:

* Internship title
* Company
* Skills
* Location

They can also filter opportunities by:

* Course
* Location
* Skills
* Work mode
* Interests
* Stipend

---

## 📝 Application Tracking

Students can track their applications through different stages:

```text
Applied
   ↓
Under Review
   ↓
Shortlisted
   ↓
Selected
```

Applications can also be marked as:

```text
Rejected
```

---

## 🔒 Security

The application follows basic security practices:

* Passwords handled by Supabase Auth
* Protected routes
* Role-based access
* Row Level Security
* Environment variables
* No database credentials in source code
* `.env` excluded from Git
* Duplicate applications prevented

---

## ⚙️ Environment Variables

Create a `.env` file locally.

Example:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_PUBLISHABLE_KEY=your_supabase_publishable_key
```

Never commit the actual `.env` file to GitHub.

Use `.env.example` for sharing the required variable names.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Enter the project

```bash
cd internship-discovery-platform
```

### 3. Install dependencies

```bash
npm install
```

If frontend and backend have separate package files:

```bash
cd frontend
npm install
```

and:

```bash
cd ../backend
npm install
```

### 4. Configure Supabase

Create your `.env` file and add your Supabase environment variables.

### 5. Start the application

```bash
npm run dev
```

---

## 🧪 Testing

The following functionality should be tested:

* [ ] User registration
* [ ] User login
* [ ] Logout
* [ ] Profile creation
* [ ] Profile editing
* [ ] Internship listing
* [ ] Internship search
* [ ] Internship filtering
* [ ] Internship details
* [ ] Recommendation system
* [ ] Match percentage
* [ ] Internship application
* [ ] Duplicate application prevention
* [ ] Application tracking
* [ ] Admin/company dashboard
* [ ] Internship creation
* [ ] Internship editing
* [ ] Internship deletion
* [ ] Application status updates
* [ ] Mobile responsiveness

---

## 🌟 Future Improvements

Possible future enhancements include:

* 🤖 AI-powered resume skill extraction
* 🧠 Semantic internship matching
* 📄 Resume analysis
* 📊 Skill-gap analysis
* 🎯 Personalized learning recommendations
* 🔔 Internship deadline notifications
* 📧 Email notifications
* 💬 Company-student communication
* 📈 Advanced analytics dashboard
* 🔍 Natural-language internship search

---

## 🎯 Project Vision

The goal is to make internship discovery more **personalized, efficient, and relevant** for students.

Instead of students searching through hundreds of unrelated opportunities, the platform helps surface internships that better match their:

```text
Skills
   +
Course
   +
Location
   +
Interests
   ↓
Relevant Internship Opportunities
```

---

## 👩‍💻 Author

**Deepthika Bopparaju**

B.Tech — Computer Science Engineering (AI/ML)

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

---

## 📄 License

This project is created for educational, project development, and hackathon purposes.
