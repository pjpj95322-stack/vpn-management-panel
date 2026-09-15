# VPN Management Panel 🔐

یک پنل مدیریت VPN جامع که از پروتکل‌های مختلف پشتیبانی می‌کند.

## پروتکل‌های پشتیبانی شده
- **OpenVPN** - VPN کلاسیک و امن
- **WireGuard** - VPN سریع و modern
- **Trojan** - پروتکل سرعت بالا
- **ShadowSocks** - پروتکل lightweight

## ویژگی‌ها
✅ مدیریت سرورها
✅ مدیریت کاربران
✅ درخواست‌های بندی width محدود
✅ نظارت بر ترافیک
✅ تولید کنفیگ‌های متنوع
✅ Dashboard تحت وب

## نیازمندی‌ها
- Python 3.8+
- Docker & Docker Compose
- Node.js 14+

## نصب و راه‌اندازی

### 1️⃣ Clone کردن
```bash
git clone https://github.com/pjpj95322-stack/vpn-management-panel.git
cd vpn-management-panel
```

### 2️⃣ نصب وابستگی‌ها
```bash
# Backend
cd backend
pip install -r requirements.txt

# Frontend
cd ../frontend
npm install
```

### 3️⃣ اجرا با Docker
```bash
docker-compose up -d
```

### 4️⃣ دسترسی
- Dashboard: http://localhost:3000
- API: http://localhost:8000
- Username: admin
- Password: admin123

## ساختار پروژه
```
vpn-management-panel/
├── backend/          # Flask API
├── frontend/         # React Dashboard
├── docker/           # Docker files
├── configs/          # VPN configs
└── docs/             # مستندات
```

## استفاده

### ایجاد سرور
```bash
python cli.py create-server --protocol wireguard --name my-server
```

### ایجاد کاربر
```bash
python cli.py create-user --server my-server --username john
```

### دریافت کنفیگ
```bash
python cli.py get-config --user john --protocol openvpn
```

## مستندات کامل
- [Backend](./backend/README.md)
- [Frontend](./frontend/README.md)
- [API Documentation](./docs/API.md)
- [پروتکل‌ها](./docs/PROTOCOLS.md)
