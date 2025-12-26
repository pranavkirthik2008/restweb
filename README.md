# Ex.06 Restaurant Website
## Date: 26.12.2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
//index.html:
{% load static %}
<!DOCTYPE html>
<html>
<head>
    <title>Tasty Bites</title>
    <link rel="stylesheet" href="{% static 'style.css' %}">
</head>
<body>

<header>
    <h1>Tasty Bites Restaurant</h1>
    <p>Delicious Food, Quality Service</p>
</header>

<nav>
    <a href="/">Home</a>
    <a href="/contact/">Contact</a>
</nav>

<section>
    <h2>Our Menu</h2>

    <div class="menu-item">
        <img src="{% static 'images/pizza.jpg' %}">
        <p>Pizza - ₹199</p>
    </div>

    <div class="menu-item">
        <img src="{% static 'images/burger.jpg' %}">
        <p>Burger - ₹149</p>
    </div>

    <div class="menu-item">
        <img src="{% static 'images/pasta.jpg' %}">
        <p>Pasta - ₹179</p>
    </div>

    <div class="menu-item">
        <img src="{% static 'images/salad.jpg' %}">
        <p>Salad - ₹99</p>
    </div>
</section>

<section>
    <h2>Our Services</h2>
    <ul>
        <li>Dine In</li>
        <li>Take Away</li>
        <li>Online Delivery</li>
        <li>Catering</li>
    </ul>
</section>

<footer>
    <p>📍 Chennai | ☎ 9876543210</p>
</footer>

</body>
</html>


//contact.html:
{% load static %}
<!DOCTYPE html>
<html>
<head>
    <title>Contact</title>
    <link rel="stylesheet" href="{% static 'style.css' %}">
</head>
<body>

<header>
    <h1>Contact Us</h1>
</header>

<nav>
    <a href="/">Home</a>
    <a href="/contact/">Contact</a>
</nav>

<section>
    <p>Email: tastybites@gmail.com</p>
    <p>Phone: 9876543210</p>
    <p>Address: Chennai, Tamil Nadu</p>
</section>

<footer>
    <p>Thank You!</p>
</footer>

</body>
</html>


//style.css:
body {
    font-family: Arial;
    margin: 0;
    background-color: #fff7ed;
}

header {
    background-color: #e67e22;
    color: white;
    text-align: center;
    padding: 20px;
}

nav {
    background-color: #333;
    text-align: center;
    padding: 10px;
}

nav a {
    color: white;
    margin: 15px;
    text-decoration: none;
}

section {
    padding: 20px;
}

.menu-item {
    display: inline-block;
    margin: 10px;
    text-align: center;
}

.menu-item img {
    width: 150px;
    height: 120px;
    border-radius: 10px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
}


//urls.py:
from django.contrib import admin
from django.urls import path
from restaurantapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.home, name='home'),
    path('contact/', views.contact, name='contact'),
]


//views.py:
from django.shortcuts import render

def home(request):
    return render(request, 'index.html')

def contact(request):
    return render(request, 'contact.html')

```
## OUTPUT:
![alt text](<Screenshot 2025-12-26 134534.png>)
![alt text](<Screenshot 2025-12-26 134553.png>)

## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
