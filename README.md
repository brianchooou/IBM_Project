# Task Management API

這是一個使用Node.js、Express和MongoDB構建的RESTful API服務，用於管理任務。該服務使用Podman進行容器化部署。

## 功能特點

- RESTful API endpoints支援任務的CRUD操作
- Swagger/OpenAPI文檔
- 容器化部署（Podman/Docker）
- 日誌記錄（Winston）
- 環境變數配置

## 技術棧

- Node.js
- Express.js
- MongoDB
- Swagger/OpenAPI
- Winston (日誌記錄)
- Podman/Docker

## API端點

- GET /api/tasks - 獲取所有任務
- GET /api/tasks/:id - 獲取特定任務
- POST /api/tasks - 創建新任務
- PUT /api/tasks/:id - 更新任務
- DELETE /api/tasks/:id - 刪除任務

## 部署指南

### 前置條件

- 安裝Podman
- 安裝Podman Compose

### 使用Podman Compose部署

1. 克隆倉庫：
   ```bash
   git clone <repository-url>
   cd api-demo
   ```

2. 創建並啟動容器：
   ```bash
   podman-compose up -d
   ```

3. 驗證服務運行狀態：
   ```bash
   podman-compose ps
   ```

### 環境變數

- PORT: API服務端口（默認：3000）
- MONGODB_URI: MongoDB連接字符串
- NODE_ENV: 運行環境（development/production）

## API文檔

API文檔可在服務運行後通過以下地址訪問：
http://localhost:3000/api-docs

## 監控和可觀察性

服務包含以下監控功能：

- 請求日誌記錄
- 錯誤日誌記錄
- HTTP請求追踪

日誌文件位於 `logs` 目錄：
- error.log: 錯誤日誌
- combined.log: 所有日誌

## 測試API

可以使用Postman或curl測試API：

```bash
# 獲取所有任務
curl http://localhost:3000/api/tasks

# 創建新任務
curl -X POST http://localhost:3000/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title":"測試任務","description":"這是一個測試任務"}'
```

## 故障排除

1. 如果無法連接到MongoDB：
   - 確認MongoDB容器是否運行
   - 檢查網絡配置
   - 驗證連接字符串

2. 如果API服務無響應：
   - 檢查服務日誌
   - 確認端口映射
   - 驗證服務狀態

## 維護

- 定期檢查日誌文件
- 監控數據庫大小
- 更新依賴包 