# 🧪 Technical Test – Budget Realization Monitoring (4 Hours)

## ⏱️ Time Limit
You have **4 hours** to complete this test.

Focus on **core functionality and code quality**, not completeness.

---

## 🎯 Objective
Build a simple API (or minimal UI) to monitor **budget and realization per activity**, including **basic authentication**.

---

## 🔐 1. Authentication (Required)

Implement:

- Login endpoint
- Hardcoded user is allowed (no need for registration)

Example:
- Admin user:
  - email: admin@test.com
  - password: password

### Requirements:
- Use JWT or session
- Password must be hashed
- No need for full user management

---

## 📂 2. Activity

### Entity: Activity

Fields:
- `id`
- `activity_name`
- `budget_amount`
- `year`

### Features:
- Create activity
- Get list of activities

---

## 💰 3. Realization

### Entity: Realization

Fields:
- `id`
- `activity_id`
- `amount`
- `date`

### Features:
- Add realization to activity
- Get realizations per activity

---

## 📊 4. Monitoring (Important)

For each activity, return:

- budget_amount
- total_realization
- remaining_budget
- percentage

### Rules:
- total_realization = sum of all realizations
- remaining_budget = budget - total_realization
- percentage = total_realization / budget × 100%
- total realization must NOT exceed budget

---

## 🔌 Required Endpoints

- `POST /login`
- `GET /activities`
- `POST /activities`
- `GET /activities/:id`
- `POST /activities/:id/realizations`

---

## ⚖️ Constraints

- Only authenticated users can access endpoints
- No role system required (everything = admin)

---

## 🛠️ Tech Stack

Free to choose:
- Backend: Node.js / Laravel / Django / etc.
- Database: any (or even in-memory for simplicity)

---

## 📦 Deliverables

- Source code
- README with:
  - how to run
  - assumptions
  - what you would improve with more time

---

## ⭐ Bonus (Optional)

- Input validation
- Error handling
- Clean project structure
- Simple UI or Postman collection
