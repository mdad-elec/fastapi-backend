# FastAPI Secure Address API 🚀

## 📌 Overview  
This is a **production-ready** FastAPI backend that exposes a secure **GET** endpoint (`/address`).  
- Supports **environment variables** (postcode from `.env`)  
- Includes **API key authentication** for security  
- Implements **rate limiting** to prevent abuse  
- Uses **logging** for monitoring  
- Supports **CORS** for frontend integration  

---

## ⚙️ Setup & Installation  

### **1️⃣ Clone the Repository**  
```sh
git clone https://github.com/mdad-elec/fastapi-backend.git
cd fastapi-backend
pip install -r requirements.txt

create .env file and add:
POSTCODE=12345
API_KEY=supersecureapikey123

run fastapi app:
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload

fetch an address:
curl -X GET "http://127.0.0.1:8000/address" -H "X-API-KEY: supersecureapikey123"

🔒 Production Features
API Key Authentication: Requests must include a valid X-API-KEY.
Rate Limiting: Limits 5 requests per minute per user.
CORS Protection: Restricts access to approved domains.
Logging: All requests are logged for debugging and security.

🛠️ Future Enhancements
🔹 JWT Authentication for better security
🔹 Database Support (PostgreSQL, MongoDB)
🔹 Advanced Monitoring (Prometheus, Grafana)`