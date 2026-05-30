# SwadesiKart 🛒

SwadesiKart is a fully-functional, feature-rich e-commerce web application built using Django. It provides a complete shopping experience, from browsing products and managing a shopping cart to secure checkout, order tracking, and user profile management.

## 🌟 Key Features

### User Experience
*   **Custom User Authentication**: Uses email as the primary login identifier instead of a standard username.
*   **Account Verification & Security**: Includes email-based account activation and a secure password reset flow.
*   **User Dashboard**: Dedicated dashboard for users to view their order history, update their profile picture, manage shipping addresses, and change passwords.
*   **Review & Rating System**: Customers can leave reviews and rate products they have purchased.

### Store & Shopping
*   **Product Catalog**: Browse products by category with dynamic rendering.
*   **Product Variations**: Support for different product variations (e.g., sizes, colors).
*   **Smart Cart Management**: Context-aware shopping cart that merges guest carts with the user's account upon logging in.
*   **Order & Payment Processing**: Complete checkout flow generating order numbers, calculating subtotals, and managing order items.

### Administration & Security
*   **Custom Admin Panel**: Enhanced Django admin interface with inline product galleries using `django-admin-thumbnails`.
*   **Security Measures**: Implements `django-admin-honeypot` to intercept unauthorized login attempts on the default `/admin/` URL, moving the real admin portal to a secure path.
*   **Session Management**: Enforces session timeouts using `django-session-timeout` for better security.

---

## 🛠️ Tech Stack

*   **Backend**: Python, Django 3.2
*   **Database**: SQLite3 (Development)
*   **Frontend**: HTML5, CSS3, JavaScript, Bootstrap 4, FontAwesome
*   **Image Processing**: Pillow
*   **Environment Management**: python-decouple

---

## 🚀 Local Setup & Installation

Follow these steps to set up the project on your local machine.

### 1. Clone the repository
```bash
git clone https://github.com/Sam-Verma/swadesikart-django.git
cd swadesikart-django
```

### 2. Create and activate a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables
Create a `.env` file in the root directory based on the `.env-sample` file:
```env
SECRET_KEY=your_secret_key_here
DEBUG=True
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=your_email@gmail.com
EMAIL_HOST_PASSWORD=your_email_password
EMAIL_USE_TLS=True

# To print emails to the terminal during local development:
EMAIL_BACKEND=django.core.mail.backends.console.EmailBackend
```

### 5. Apply Database Migrations
```bash
python manage.py migrate
```

### 6. Create a Superuser (Optional)
Because of the custom user model, create an admin account using:
```bash
python manage.py createsuperuser
```
*(Note: Use your email address as the username when logging in)*

### 7. Run the Development Server
```bash
python manage.py runserver
```
Visit `http://127.0.0.1:8000/` in your browser.

> **Admin Access:** The default `/admin/` path is a honeypot. To access the real Django admin panel, go to `/admin-sam/`.

---

## 📸 Screenshots
*(You can add screenshots of your home page, product details, cart, and dashboard here to showcase the UI)*

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Sam-Verma/swadesikart-django/issues).
