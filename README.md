# Mealmate-Online Food Ordering System

Mealmate is a Django-based web application that allows users to register as restaurant owners or customers.
It is a user-friendly and efficient online food ordering system designed to connect customers with their favorite restaurants seamlessly. 
It offers a convenient platform for users to browse menus, place orders, and get food delivered to their doorstep with just a few clicks.

---

## 🚀 Features


### 🔐 Authentication

- User can register and login as both customer and vendor.
- Secured authentication has build using built-in Django's auth system.


### 🏪 Restaurant Management

- Vendor can add, update, delete restaurants.
- Owner dashboard to manage listings.


### 📋 Menu & Orders

- Customers can browse restaurant menus.
- Add food items to the shopping cart.
- Place and manage orders.


### 💳 Payment Integration

- Razorpay integrated for secure online payments.

---

## 🛠 Installation & Setup


### 1. Clone the Repository

```bash
git clone https://github.com/your-username/mealmate.git
cd mealmate
```


### 2. Set Up a Virtual Environment

```bash
pip install virtualenv
virtualenv myenv
myenv\Scripts\activate
```


### 3. Install Dependencies

```bash
pip install -r requirements.txt
```


### 4. Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```


### 5. Create a Superuser

```bash
python manage.py createsuperuser
```


### 6. Run the Development Server

```bash
python manage.py runserver
```

Now, open your browser and navigate to:
http://127.0.0.1:8000/

---

## 📁 Directory Structure

```
mealmate/
│── delivery/
│   ├── migrations/
│   ├── static/
│   ├── templates/delivery/
│   │   ├── add_res.html
│   │   ├── base.html
│   │   ├── checkout.html
│   │   ├── cusmenu.html
│   │   ├── customer_home.html
│   │   ├── display_res.html
│   │   ├── failed.html
│   │   ├── index.html
│   │   ├── menu.html
│   │   ├── orders.html
│   │   ├── show_cart.html
│   │   ├── sign_in.html
│   │   ├── sign_up.html
│   │   ├── success.html
│   │   ├── userdata.html
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── tests.py
│   ├── views.py
├── manage.py
├── requirements.txt
```

---

## 📡 API Endpoints (If Using Django REST Framework)

| Method | Endpoint                         | Description                 |
|--------|----------------------------------|-----------------------------|
| GET    | `/restaurants/`                  | List all restaurants        |
| POST   | `/restaurants/add/`              | Add a new restaurant        |
| PUT    | `/restaurants/update/<id>/`      | Update restaurant details   |
| DELETE | `/restaurants/delete/<id>/`      | Delete a restaurant         |
| GET    | `/menu/`                         | Get menu items              |
| POST   | `/order/`                        | Place an order              |

---

## 💸 Razorpay Payment Integration

### Steps:

1. **Sign up at [Razorpay](https://razorpay.com)**
   
2. **Get your Key ID and Key Secret from the Razorpay Dashboard**
   
3. **Add them to your Django `settings.py`**:

   Open the `settings.py` file in your Django project and add the following:
```python
RAZORPAY_KEY_ID = "your_key_id"
RAZORPAY_KEY_SECRET = "your_key_secret"
```
