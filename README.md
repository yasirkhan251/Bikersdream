# 🏍️ Bikers Dream — Bike Rental Management System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/Flask-Web%20Framework-000000?style=for-the-badge&logo=flask&logoColor=white">
  <img src="https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/SQLite-Alternative-003B57?style=for-the-badge&logo=sqlite&logoColor=white">
  <img src="https://img.shields.io/badge/Bootstrap-5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
</p>

<p align="center">
  <strong>A full-stack Flask-based bike rental platform for browsing bikes, managing users, creating rental bookings, processing payments, and administering the fleet.</strong>
</p>

---

## 🎯 What This Project Offers

**Bikers Dream** is a web-based motorcycle rental management system built with **Python Flask**.

The application provides separate workflows for:

- 👤 Customer registration and login
- 🏍️ Bike browsing and rental selection
- 📅 Rental duration and booking
- 💳 Payment and transaction recording
- 🧾 Printable rental invoices
- 🔐 Customer/admin authentication
- 🛠️ Fleet management
- 👥 User management
- 📋 Booking administration
- 🖼️ Bike image uploads
- 🗄️ MySQL and SQLite database implementations

The repository contains both the original **MySQL implementation** and SQLite-based versions for easier local development.

---

## ✨ Highlighted Features

<table>
<tr>
<td width="50%">

### 👤 User Features

- User registration
- Secure password hashing with `sha256_crypt`
- Login/logout flow
- User profile information
- Driving licence information
- Aadhaar information
- Session-based authentication

</td>
<td width="50%">

### 🏍️ Bike Rental

- Bike catalogue
- Bike images
- Bike specifications
- Bike type
- Fuel type
- Engine displacement
- Model/company details
- Rental rate
- Rental duration calculation

</td>
</tr>

<tr>
<td>

### 📅 Booking System

- Booking ID generation
- Start/end date and time
- Rental hours
- Price calculation
- Booking status
- Pending payment handling
- Booking confirmation

</td>
<td>

### 💳 Payment System

- Transaction ID storage
- Customer payment information
- Payment status
- Booking/payment association
- Transaction confirmation
- Printable invoice

</td>
</tr>

<tr>
<td>

### 🛠️ Admin Management

- Admin authentication
- Admin dashboard
- User information
- Booking management
- Bike management
- Add/delete bikes
- Fleet information

</td>
<td>

### 🖼️ Media Management

- Bike image uploads
- Static bike images
- Dynamic image storage
- Supported image extensions
- Image display in bike profiles and invoices

</td>
</tr>
</table>

---

## 🧠 How It Works

The application follows a relatively straightforward rental workflow:

```text
                 ┌───────────────────────┐
                 │      Bikers Dream      │
                 │      Landing Page      │
                 └───────────┬───────────┘
                             │
              ┌──────────────┴──────────────┐
              │                             │
        ┌─────▼─────┐                 ┌─────▼─────┐
        │   Login   │                 │  Sign Up  │
        └─────┬─────┘                 └─────┬─────┘
              │                             │
              └──────────────┬──────────────┘
                             │
                     ┌───────▼────────┐
                     │ Bike Dashboard │
                     └───────┬────────┘
                             │
                     Select a Bike
                             │
                     ┌───────▼────────┐
                     │ Booking Screen │
                     │ Date / Time    │
                     │ Duration       │
                     │ Rental Rate    │
                     └───────┬────────┘
                             │
                     ┌───────▼────────┐
                     │    Payment     │
                     │ Transaction    │
                     │     Status     │
                     └───────┬────────┘
                             │
                     ┌───────▼────────┐
                     │ Booking Done   │
                     └───────┬────────┘
                             │
                     ┌───────▼────────┐
                     │ Print Invoice  │
                     └────────────────┘
```

---

## 🛠️ Software & Technologies Used

| Technology | Purpose |
|---|---|
| 🐍 Python | Backend application logic |
| 🌶️ Flask | Web framework |
| 🗄️ MySQL | Primary database implementation |
| 🪶 SQLite | Local database alternative |
| 🔐 Passlib | Password hashing |
| 🔑 Flask Sessions | Login/session state |
| 🖼️ HTML | Page structure |
| 🎨 CSS | UI styling |
| ⚡ JavaScript | Dynamic pricing, date/time logic and UI behavior |
| 🅱️ Bootstrap | Responsive UI components |
| 📁 Werkzeug | Secure filename handling |
| 📦 Node / npm | Bootstrap dependency management |

---

## 💻 System Requirements

### Minimum

| Component | Requirement |
|---|---|
| OS | Windows / Linux / macOS |
| Python | 3.x |
| RAM | 4 GB |
| Storage | ~500 MB+ |
| Browser | Chrome / Edge / Firefox |
| Database | MySQL or SQLite |

### Recommended

| Component | Recommendation |
|---|---|
| RAM | 8 GB+ |
| Python | Recent Python 3 release |
| Database | MySQL for multi-user deployment |
| Browser | Latest Chrome / Edge |
| Network | Internet connection for external CDN assets |

---

## 📦 Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yasirkhan251/Bikersdream.git
cd Bikersdream
```

---

### 2️⃣ Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

On Linux/macOS:

```bash
source venv/bin/activate
```

---

### 3️⃣ Install Python dependencies

The repository does not currently provide a root `requirements.txt`, so install the required packages manually:

```bash
pip install flask
pip install passlib
pip install mysql-connector-python
pip install flask-mysqldb
pip install werkzeug
```

Depending on which implementation you use, SQLite itself is provided through Python's standard library.

---

## 🗄️ Database Setup

Bikers Dream contains two database approaches.

### 🔵 MySQL Version

The main `app.py` implementation is configured for a local MySQL/XAMPP environment:

```python
app.config['MYSQL_HOST'] = 'localhost'
app.config['MYSQL_USER'] = 'root'
app.config['MYSQL_PASSWORD'] = ''
app.config['MYSQL_DB'] = 'motor'
```

Create the database first:

```sql
CREATE DATABASE motor;
```

Then configure your MySQL credentials in the application.

The application creates several tables during runtime, including structures for:

```text
user
booking
payment
admin
```

Bike-related tables are also accessed by the application.

---

### 🟢 SQLite Version

For easier local testing, the repository includes:

```text
app_sqlite_fixed.py
app_sqlite_converted.py
```

These versions use:

```text
sqlite3.db
```

and Python's built-in `sqlite3` module.

The SQLite application creates and manages tables using SQL statements compatible with SQLite.

---

## ⚙️ Configuration

### Upload Folder

Bike images are configured around:

```python
UPLOAD_FOLDER = 'dynamic/Bike Image'
```

The repository also contains:

```text
static/Bike Image/
static/uploads/
dynamic/Bike Image/
```

### Supported Image Types

The application allows:

```text
jpg
jpeg
png
gif
bmp
tiff
tif
svg
webp
ico
psd
ai
eps
```

---

## ▶️ How to Run

### MySQL Version

```bash
python app.py
```

Then open:

```text
http://127.0.0.1:5000/
```

### SQLite Version

For the SQLite implementation:

```bash
python app_sqlite_fixed.py
```

or:

```bash
python app_sqlite_converted.py
```

Then visit:

```text
http://127.0.0.1:5000/
```

---

## 🎮 How to Use

### 👤 Customer Flow

```text
Home
 ↓
Login / Sign Up
 ↓
Dashboard
 ↓
Browse Bikes
 ↓
Select Bike
 ↓
Choose Rental Period
 ↓
Calculate Rental Cost
 ↓
Create Booking
 ↓
Payment
 ↓
Booking Confirmation
 ↓
Invoice
```

Users provide information such as:

- Full name
- Username
- Password
- Driving licence
- Aadhaar number

The application hashes passwords using Passlib before storing them.

---

## 🏍️ Bike Selection

The bike booking pages expose information such as:

| Information | Example |
|---|---|
| Bike name | BMW G310 GS BS4 |
| Bike type | Sport / Cruiser / Touring / etc. |
| Fuel type | Stored in bike information |
| Displacement | CC |
| Model | Bike model |
| Company | Manufacturer |
| Rental rate | Hourly rate |
| Accessories | Helmet, batteries, gadgets, etc. |

The booking interface supports different rental periods such as:

```text
12 hours
1 day
2 days
3 days
4 days
5 days
6 days
1 week
2 weeks
3 weeks
1 month
```

---

## 💰 Rental Price Calculation

The frontend uses JavaScript to calculate the rental amount based on:

```text
Rental Hours × Rate per Hour
```

Example logic:

```javascript
var price = Math.floor(time * rate);
```

The calculated amount is then sent through the booking workflow.

---

## 📅 Booking System

A booking contains information such as:

```text
Booking ID
User ID
Bike Name
From Date
To Date
Rental Hours
Rate Per Hour
Total Price
Booking Status
Transaction ID
```

The application supports pending bookings and payment continuation through routes such as:

```text
/pendingpayment/<pending>
```

---

## 💳 Payment Workflow

The payment implementation records transaction-related fields including:

```text
Transaction ID
Cardholder
Card Number
Expiry
CVV
Bike
Price
Rental Hours
Status
```

The booking record is updated with the payment status and transaction information.

> ⚠️ The current implementation stores card-related fields directly in the database. This is not suitable for production payment processing and should be replaced with a PCI-compliant payment provider.

---

## ✅ Booking Confirmation

After successful processing, users are redirected to a confirmation page containing information such as:

```text
Bike
Price
Transaction ID
Booking ID
```

The confirmation page is rendered through:

```text
templates/done.html
```

---

## 🧾 Invoice System

Bikers Dream includes a printable invoice page.

The invoice displays:

- Invoice number
- Transaction ID
- Bike name
- Bike image
- Bike type
- Fuel type
- Engine displacement
- Model
- Company
- Accessories
- Start date
- End date
- Rental hours
- Total amount paid

The invoice can be printed directly using the browser's print dialog.

```javascript
window.print();
```

---

## 🛠️ Admin System

The project contains a separate administrator workflow.

Admin access begins at:

```text
/admin
```

The admin area provides access to:

```text
Admin Panel
User Information
Bookings
Bike Management
Bike Information
Logout
```

---

## 👥 User Management

The administrator can view registered customers and perform actions such as deleting users.

The corresponding interface is:

```text
templates/userdetails.html
```

User information includes:

```text
User ID
Name
Username
```

---

## 📋 Booking Management

Administrators can view rental bookings through:

```text
/adminuserbooking.html
```

The booking list includes information such as:

- Booking ID
- Bike name
- Rental hours
- Aadhaar
- Driving licence
- Price
- Status
- Delete action

---

## 🏍️ Fleet Management

The admin bike interface provides functionality for managing the rental fleet.

The bike management interface supports:

- Adding bike information
- Viewing bikes
- Bike images
- Bike ID
- Bike name
- Bike type
- Availability
- Rental rate
- Fuel type
- Engine CC
- Model
- Accessories
- Deleting bikes

The main interface is:

```text
templates/bikeform.html
```

---

## 🖼️ Bike Image Uploads

The project provides image handling through Flask/Werkzeug.

Uploaded filenames are processed using:

```python
secure_filename()
```

The application exposes uploaded bike images to customer-facing pages and invoices.

---

## 📸 Screenshots

The repository already contains real screenshots under:

```text
Website screenshots/
```

Current screenshots include:

<div align="center">

<img src="https://raw.githubusercontent.com/yasirkhan251/Bikersdream/main/Website%20screenshots/Screenshot%202026-10-03%20023819.png" width="90%" alt="Bikers Dream Screenshot 1">

<br><br>

<img src="https://raw.githubusercontent.com/yasirkhan251/Bikersdream/main/Website%20screenshots/Screenshot%202026-10-03%20024917.png" width="90%" alt="Bikers Dream Screenshot 2">

<br><br>

<img src="https://raw.githubusercontent.com/yasirkhan251/Bikersdream/main/Website%20screenshots/Screenshot%202026-10-03%20024923.png" width="90%" alt="Bikers Dream Screenshot 3">

<br><br>

<img src="https://raw.githubusercontent.com/yasirkhan251/Bikersdream/main/Website%20screenshots/Screenshot%202026-10-03%20024935.png" width="90%" alt="Bikers Dream Screenshot 4">

<br><br>

<img src="https://raw.githubusercontent.com/yasirkhan251/Bikersdream/main/Website%20screenshots/Screenshot%202026-10-03%20024946.png" width="90%" alt="Bikers Dream Screenshot 5">

</div>

---

## 🎞️ GIF Demonstrations

No dedicated GIF demonstration files were identified in the repository.

Recommended documentation location:

```text
docs/demo/
```

Example:

```markdown
![Booking Workflow](docs/demo/booking-workflow.gif)
```

Suggested GIF demonstrations:

```text
docs/demo/
├── user-registration.gif
├── bike-selection.gif
├── booking-flow.gif
├── payment-flow.gif
└── admin-management.gif
```

---

## 🎥 Video Demonstration

No dedicated project demonstration video was identified in the repository.

A future README section can use a YouTube thumbnail:

```html
<p align="center">
  <a href="YOUR_YOUTUBE_VIDEO_URL">
    <img src="https://img.youtube.com/vi/YOUR_VIDEO_ID/maxresdefault.jpg"
         alt="Bikers Dream Demo"
         width="85%">
  </a>
</p>
```

---

## 📁 Project Structure

```text
Bikersdream/
│
├── app.py
├── app_sqlite_fixed.py
├── app_sqlite_converted.py
│
├── package.json
├── package-lock.json
├── sqlite3.db
│
├── templates/
│   ├── index.html
│   ├── Login.html
│   ├── Signup.html
│   ├── dashboard.html
│   ├── dashboard1.html
│   ├── bikelanding.html
│   ├── bikeform.html
│   ├── bikeprofile.html
│   ├── booking.html
│   ├── payments.html
│   ├── done.html
│   ├── invoice.html
│   ├── adminlogin.html
│   ├── adminmain.html
│   ├── adminuserbooking.html
│   ├── userdetails.html
│   └── ...
│
├── static/
│   ├── Bike Image/
│   ├── uploads/
│   ├── bg/
│   ├── css/
│   ├── fonts/
│   ├── images/
│   ├── js/
│   └── login.png
│
├── dynamic/
│   └── Bike Image/
│
├── Website screenshots/
│
├── Sources/
├── Backup/
└── __pycache__/
```

---

## 🧩 Application Architecture

The project can be viewed as four major layers:

```text
┌─────────────────────────────────────┐
│             Frontend                │
│ HTML + CSS + JavaScript + Bootstrap │
└──────────────────┬──────────────────┘
                   │
                   ▼
┌─────────────────────────────────────┐
│              Flask                  │
│ Routes + Sessions + Business Logic  │
└──────────────────┬──────────────────┘
                   │
          ┌────────┴────────┐
          ▼                 ▼
┌─────────────────┐  ┌─────────────────┐
│     MySQL       │  │     SQLite      │
│ Main DB Variant │  │ Local Variant   │
└─────────────────┘  └─────────────────┘
          │
          ▼
┌─────────────────────────────────────┐
│       Rental / Booking Data         │
│ Users • Bikes • Bookings • Payment  │
└─────────────────────────────────────┘
```

---

## ⚠️ Limitations

This repository is best considered a **development/academic project** rather than a production-ready payment platform.

Important limitations include:

- No root `requirements.txt`
- Multiple duplicated/experimental application files
- MySQL configuration is hard-coded
- Flask secret key is hard-coded
- Database credentials are embedded in source
- Payment card fields are stored directly
- Database schema creation occurs inside application routes
- Some functionality relies on local Windows paths
- Some templates contain hard-coded example bike information
- Some routes and business logic could be consolidated
- Production-grade validation is limited
- CSRF protection is not implemented across the forms
- Authentication/authorization should be strengthened
- `node_modules/` is committed to the repository
- `__pycache__/` is committed to the repository

---

## 🔐 Security Recommendations

Before using the project publicly, the following should be addressed.

### 1. Move secrets to environment variables

Instead of:

```python
app.secret_key = 'many random bytes'
```

use:

```python
app.secret_key = os.environ.get("FLASK_SECRET_KEY")
```

---

### 2. Never store raw payment card data

The current application stores:

```text
cardholder
cardnumber
expiry
cvv
```

A production version should use a payment gateway such as:

```text
Razorpay
Stripe
PayPal
PhonePe
Cashfree
```

and store only the gateway's transaction/reference information.

---

### 3. Add CSRF protection

Flask-WTF or another CSRF mechanism should protect POST requests.

---

### 4. Separate configuration from application code

Use:

```text
.env
config.py
environment variables
```

for:

```text
Database credentials
Secret keys
Upload paths
Payment credentials
Production settings
```

---

### 5. Remove generated files

Add a `.gitignore` containing at least:

```gitignore
__pycache__/
*.py[cod]
venv/
.env
node_modules/
*.db
```

A production repository should not normally commit local runtime databases or generated dependency directories.

---

## 🔮 Future Improvements / Roadmap

### 🚀 Phase 1 — Codebase Cleanup

- Create `requirements.txt`
- Add `.gitignore`
- Remove duplicated application versions
- Separate routes into Flask Blueprints
- Centralize configuration
- Remove hard-coded paths
- Add proper error handling

### 💳 Phase 2 — Production Payments

- Integrate Razorpay/Stripe/PhonePe
- Remove card-number/CVV storage
- Add payment verification callbacks
- Add refund support
- Add payment history

### 🏍️ Phase 3 — Rental Management

- Real-time bike availability
- Automatic booking conflict detection
- Rental extension
- Cancellation workflow
- Damage reporting
- Maintenance tracking
- Bike service history

### 👨‍💼 Phase 4 — Admin Improvements

- Modern admin dashboard
- Booking analytics
- Revenue charts
- Fleet utilization
- Customer statistics
- Search/filter/sort
- Role-based admin permissions

### 📍 Phase 5 — Location & Delivery

- Pickup/drop-off locations
- Google Maps integration
- GPS tracking
- Route information
- Location-based fleet discovery

### 📱 Phase 6 — Modern Platform

- Responsive mobile-first redesign
- REST API
- React frontend
- JWT authentication
- Mobile application
- Notifications
- Email/SMS/WhatsApp booking alerts

### 🗄️ Phase 7 — Production Infrastructure

- PostgreSQL
- Gunicorn
- Nginx
- Docker
- Cloud object storage
- CI/CD
- Logging and monitoring

---

## 👨‍💻 Author

<p align="center">
  <strong>Yasir Khan</strong><br>
  Website Developer • Python Developer • Django/Flask Developer • AI/ML Enthusiast
</p>

<p align="center">
  <a href="https://github.com/yasirkhan251">
    <img src="https://img.shields.io/badge/GitHub-yasirkhan251-181717?style=for-the-badge&logo=github">
  </a>
</p>

---

## 📄 License

No explicit license file was identified in the repository.

Until a license is added, the code should be treated as **all rights reserved** by the repository owner.

---

<p align="center">
  🏍️ <strong>Bikers Dream</strong> — Ride. Book. Explore.
</p>