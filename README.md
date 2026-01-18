# Scalable Order Processing System (Amazon SDE I Level)

A scalable e-commerce order processing backend built with **Python**, **FastAPI**, **SQLite**, and an **async in-memory order queue**.  
This project demonstrates **multi-tier backend design, distributed system concepts, inventory management, rate limiting, and fault-tolerant processing** — fully aligned with **Amazon SDE I University Hiring requirements**.

---

##  Tech Stack
- **Language:** Python 3
- **Framework:** FastAPI
- **Database:** SQLite (replaceable with PostgreSQL/DynamoDB)
- **Async Queue:** Python Queue + Worker Thread (simulates distributed async processing)
- **Other Concepts:** Rate limiting, fault tolerance, inventory management, modular architecture

---

##  Features
- Place orders asynchronously via API  
- Track order status in real-time  
- Inventory management with stock validation  
- Rate limiting per client to prevent abuse  
- Fault-tolerant processing for failed orders  
- Persistent storage for orders and inventory  
- Modular and scalable architecture  

---

##  Architecture Overview
- POST `/orders/` → places order in queue  
- Worker validates stock, simulates payment, updates order status  
- GET `/orders/{order_id}` → checks order status  
- Rate limiting protects APIs  

---

## 🔧 How to Run (Locally / Colab)
1. Install dependencies:
```bash
pip install fastapi pydantic sqlalchemy


