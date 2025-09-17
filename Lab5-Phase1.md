# Lab5: Testing & Integration

### **Test Case 1: System Health** <br>
**Health Check**
`GET http://localhost:3001/api/health`
<br>
<img src="https://drive.google.com/uc?export=download&id=1B_g6EhuawPkqErlBVsSb6HzTMbTCFzHI" width="400" height="600">

### **Test Case 2: Get All Agents** <br>
**Test filtering**
- `GET http://localhost:3001/api/agents?status=Available` <br>
<img src="https://drive.google.com/uc?export=download&id=1334WNFv-38UX6BMBzRlAyVgHfvPtsAVw" width="400" height="600">

- `GET http://localhost:3001/api/agents?department=Sales`
<img src="https://drive.google.com/uc?export=download&id=1fvJVRv1n2wjJwthJr652kFeNh08UXS1r" width="400" height="600">

### **Test Case 3: Create Agent - Success** <br>
**Request**
- `POST http://localhost:3001/api/agents`
- `Content-Type: application/json`
<img src="https://drive.google.com/uc?export=download&id=1UNPUyc8Xvg26K3NBZgGCfIpksf1ILm3O" width="400" height="600">

### **Test Case 4: Validation Testing** <br>
**Request - Invalid data (ทดสอบ Joi validation)** <br>
- `POST http://localhost:3001/api/agents`
- `Content-Type: application/json` <br>
<img src="https://drive.google.com/uc?export=download&id=1dMVdZL6yasBabbOnfCsVaXIR9P-VdZMc" width="400" height="600">

## Status Management Testing
### **Test Status Update - Valid Transition** <br>
**Get agent ID first** <br>
`GET http://localhost:3001/api/agents` <br>

**Copy agent ID และทดสอบ status update**
- `PATCH http://localhost:3001/api/agents/[AGENT-ID]/status`
- `Content-Type: application/json`
<img src="https://drive.google.com/uc?export=download&id=1AyZDDYlNMtHEJvP5GwQ8i7kKgDlJDVxr" width="400" height="600">

**Try invalid transition** (Available -> Offline without proper flow)
- `PATCH http://localhost:3001/api/agents/[AGENT-ID]/status`
- `Content-Type: application/json`
<img src="https://drive.google.com/uc?export=download&id=1fzapEJc0D8sF75bw1ezFWb3gGhVuVPln" width="400" height="600">
