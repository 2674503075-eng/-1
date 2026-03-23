# 局域网聊天（Python 后台）

## 目录结构

- `backend/app.py`: FastAPI + WebSocket 聊天后台
- `web/`: 前端页面（HTML/CSS/JS）

## 启动（Windows PowerShell）

在本项目根目录执行：

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn backend.app:app --host 0.0.0.0 --port 8000
```

浏览器打开：

- 本机访问：`http://127.0.0.1:8000`
- 局域网其他设备访问：`http://你的电脑局域网IP:8000`

## 获取局域网 IP

```powershell
ipconfig
```

找到你的网卡的 `IPv4 地址`（常见形如 `192.168.x.x` / `10.x.x.x`）。

## 防火墙提示

如果其他设备打不开，请在 Windows 防火墙中放行 `8000` 端口（或允许 Python/uvicorn 通过）。
