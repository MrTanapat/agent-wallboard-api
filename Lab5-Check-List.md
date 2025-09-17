# Lab5: Testing & Integration

### **Test Case 1: System Health** <br>
**Request**
`GET http://localhost:3001/`

**Health Check**
`GET http://localhost:3001/api/health`

### **Test Case 2: Get All Agents** <br>
**Test filtering**
- `GET http://localhost:3001/api/agents?status=Available` <br>
- `GET http://localhost:3001/api/agents?department=Sales`

### **Test Case 3: Create Agent - Success** <br>
**Request**
- `POST http://localhost:3001/api/agents`
- `Content-Type: application/json`

### **Test Case 4: Validation Testing** <br>
**Request - Invalid data (ทดสอบ Joi validation)** <br>
- `POST http://localhost:3001/api/agents`
- `Content-Type: application/json`

## Status Management Testing
### **Test Status Update - Valid Transition** <br>
**Get agent ID first** <br>
`GET http://localhost:3001/api/agents` <br>

**Copy agent ID และทดสอบ status update**
- `PATCH http://localhost:3001/api/agents/[AGENT-ID]/status`
- `Content-Type: application/json`

**Try invalid transition** (Available -> Offline without proper flow)
- `PATCH http://localhost:3001/api/agents/[AGENT-ID]/status`
- `Content-Type: application/json`
