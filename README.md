# Ex.05 Book Front Cover Page Design
# Date:14-12-2025
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
```
book.html

{% load static %}
<html>
<head>
    <title>Preview</title>
    <link rel="stylesheet" href="{% static 'book.css' %}">
</head>
<body>

<div id="cover">

    <h1>The Alchemist</h1>
    <hr>

    <div id="author">
        <p class="tagline">
            This timeless tale was crafted by,<br>
            <strong>Paulo Coelho</strong>
        </p>

        <img src="{% static 'auth.jpg' %}" >
    </div>

    <p id="designer">Book Cover by Varoodhini</p>

</div>

</body>
</html>
```
css
```

body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
}

#cover {
    height: 650px;
    width: 450px;
    border: 2px solid brown;
    background: radial-gradient(circle, #ffeb3b, #ff9800);

    display: flex;
    flex-direction: column;
    align-items: center;
}

h1 {
    margin-top: 30px;
    font-family: serif;
}

hr {
    width: 120px;
    border: 1px solid brown;
    margin-bottom: 30px;
}


#author {
    margin-top: 40px;
    text-align: center;
}

#tagline {
    color: brown;
    font-family: monospace;
    margin-bottom: 10px;
}


#author img {
    height: 90px;
    width: 90px;
    border-radius: 5%;
    border: 2px solid brown;
    padding: 8px;
    background-color: white;
}


#designer {
    margin-top: auto;
    margin-bottom: 10px;
    font-size: 12px;
    font-family: monospace;
}
```
views.py
```

from django.shortcuts import render
def bc(request):
    return render(request,'book.html')


```
urls.py
```

from django.contrib import admin
from django.urls import path
from myapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.bc),
]
```
# OUTPUT:
![Book Cover](book/myapp/static/op.png)


# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
