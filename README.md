# 🏥 Clinic Slot Booking System

> **Smart appointment booking with bulletproof concurrency control** - Never overbook again, even under extreme load.

[![CI](https://github.com/yourusername/clinic-slot-booking/actions/workflows/ci.yml/badge.svg)](https://github.com/yourusername/clinic-slot-booking/actions/workflows/ci.yml)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue.svg)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-blue.svg)](https://www.postgresql.org/)
[![React](https://img.shields.io/badge/React-18-blue.svg)](https://reactjs.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

![Project Screenshot](docs/screenshots/demo.png)
*Screenshot: Admin Dashboard and Slot Booking Interface*

---

## 🎯 What Problem Does This Solve?

When multiple users try to book the same appointment slot simultaneously, traditional systems fail - resulting in overbooking. This system uses **PostgreSQL row-level locking** to guarantee **zero overbooking**, even with 100+ concurrent requests.

**Try it live:** [Frontend](https://clinic-booking-frontend.vercel.app) | [Backend API](https://clinic-booking-backend.onrender.com)

---

## ✨ Key Features

- 🔒 **Concurrency-Safe**: Database-level locking prevents overbooking
- ⚡ **Real-Time Updates**: Automatic polling keeps availability current
- 🎨 **Modern UI**: Responsive design with Tailwind CSS
- 🧪 **Fully Tested**: Unit, integration, and E2E tests
- 🚀 **Production Ready**: Deployed and monitored
- 📊 **Admin Dashboard**: Manage doctors and slots easily

---

## 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/yourusername/clinic-slot-booking.git
cd clinic-slot-booking

# Backend setup
cd backend
npm install
cp .env.example .env  # Configure database
npm run migrate:dev
npm run dev

# Frontend setup (new terminal)
cd frontend
npm install
cp .env.example .env  # Set VITE_API_BASE_URL
npm run dev
```

Visit `http://localhost:5173` to see it in action!

---

## 📚 Documentation

- 📖 [System Design](docs/system-design.md) - Architecture and design decisions
- 🚀 [Deployment Guide](docs/deployment.md) - Step-by-step deployment
- 🔒 [Concurrency Tests](docs/concurrency-test.md) - Validation report
- 🎥 [Video Demo Script](docs/video-script.md) - Walkthrough guide
- 📋 [Submission Checklist](submission.md) - Assignment deliverables

---

## 🛠️ Tech Stack

**Backend:** Node.js, Express, TypeScript, PostgreSQL  
**Frontend:** React, TypeScript, Vite, Tailwind CSS  
**Testing:** Jest, Playwright, Vitest  
**Deployment:** Render, Vercel  
**CI/CD:** GitHub Actions

---

## 🧪 Testing

```bash
# Backend tests
cd backend && npm test

# Frontend tests
cd frontend && npm test

# E2E tests
cd e2e && npm test

# Concurrency verification
node scripts/verify-concurrency.js
```

---

## 📖 API Documentation

**Base URL:** `https://clinic-booking-backend.onrender.com`

- `GET /health` - Health check
- `GET /slots` - List available slots
- `POST /bookings` - Create booking
- `GET /admin/slots` - Admin: List all slots
- `POST /admin/doctors` - Admin: Create doctor

[Full API Docs](backend/docs/api.json) | [Postman Collection](backend/docs/postman-collection.json)

---

## 🏗️ Architecture

```
Frontend (Vercel) → Backend API (Render) → PostgreSQL
                    ↓
              Row-Level Locking
         (SELECT FOR UPDATE SKIP LOCKED)
```

The system uses **PostgreSQL row-level locking** to ensure atomic booking operations. When multiple users book simultaneously, only one succeeds - the others receive clear error messages.

[Read the full architecture](docs/system-design.md)

---

## 📊 Project Status

✅ **Phase 1:** Project Planning  
✅ **Phase 2:** System Design  
✅ **Phase 3:** Backend Implementation  
✅ **Phase 4:** Frontend Implementation  
✅ **Phase 5:** Integration & E2E Tests  
✅ **Phase 6:** Deployment & CI  
✅ **Phase 7:** Documentation  
✅ **Phase 8:** Final Polish

**Status:** 🚀 Production Ready

---

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📝 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) for details.

---

## 👤 Author

**Your Name**  
- Email: your.email@example.com
- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your Profile](https://linkedin.com/in/yourprofile)

---

## 🙏 Acknowledgments

- PostgreSQL for robust concurrency control
- Render and Vercel for free hosting tiers
- The open-source community

---

**⭐ Star this repo if you find it helpful!**
