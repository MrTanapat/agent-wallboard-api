# Lab5: Testing & Integration

### **1. Database Connection Test** <br>
```
# Start MongoDB (if local)
mongod

# Start the server
npm run dev
```

### **2. API Endpoints Test** <br>
**Create agent**
- `curl http://localhost:3001/api/health` <br>
<img src="https://drive.google.com/uc?export=download&id=1DBwmwJG5Fo6a-B-JH3mHGKIRWsOcdWye" width="400" height="600">

### **3. CRUD Operations Test (MongoDB)** <br>
**Health check**
```
  curl -X POST http://localhost:3001/api/agents \
  -H "Content-Type: application/json" \
  -d '{
    "agentCode": "A101",
    "name": "MongoDB Test Agent",
    "email": "test@mongo.com",
    "department": "Technical"
  }'` <br>
```
<img src="https://drive.google.com/uc?export=download&id=1DBwmwJG5Fo6a-B-JH3mHGKIRWsOcdWye" width="400" height="600">
