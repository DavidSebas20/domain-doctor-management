# 🩺 **Doctor Management Domain**

## 📖 Description
The **Doctor Management** domain handles all information related to doctors within the hospital system. Each CRUD operation is implemented as an independent microservice to ensure **modularity, scalability, and maintainability**.

---

## 🔹 Microservices

### ✅ **1. Register Doctor**
- **📌 Description:** Adds a new doctor to the system.
- **🔹 Method:** `POST`
- **🔗 Dependencies:** Security & Authorization Domain (for password encryption) 🔐
- **📥 Inputs:** Doctor's data (full name, specialty, phone, email, username, password*)
- **📤 Outputs:** Registration confirmation ✅

### 🔍 **2. Get Doctor Details**
- **📌 Description:** Retrieves information about a specific doctor.
- **🔹 Method:** `GET`
- **🔗 Dependencies:** Doctor database 🗂️
- **📥 Inputs:** `Doctor ID, username`
- **📤 Outputs:** Doctor profile 📄

### ✏️ **3. Update Doctor Information**
- **📌 Description:** Modifies a doctor's profile details.
- **🔹 Method:** `PUT`
- **🔗 Dependencies:** Doctor database 🗄️, Security & Authorization Domain (for password updates) 🔐
- **📥 Inputs:** `Doctor ID` and updated data
- **📤 Outputs:** Update confirmation 🔄

### ❌ **4. Remove Doctor**
- **📌 Description:** Deletes a doctor's profile from the system.
- **🔹 Method:** `DELETE`
- **🔗 Dependencies:** Doctor database 🗄️
- **📥 Inputs:** `Doctor ID`
- **📤 Outputs:** Deletion confirmation 🗑️

---

## 🛠️ **Technologies Used**
- **⚙️ Backend:** Java, Spring Boot 💻
- **🗄️ Database:** MySQL 🐬
- **🔐 Security:** JWT authentication, password encryption

---

## 🔗 **Integrations**
- **🩺 Medical Care Domain:** Doctors must be registered to schedule appointments and manage patients.
- **🩹 Clinical History Domain:** Only authorized doctors can update patient records and medical histories.

