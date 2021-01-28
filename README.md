# Mathematical Calculations using JavaScript
## AIM:
To design a website to calculate the area of a triangle and volume of a cylinder using JavaScript.

## DESIGN STEPS:
### Step 1: 
Requirement collection.
### Step 2:
Creating the layout using HTML and CSS.
### Step 3:
Write JavaScript to perform calculations.
### Step 4:
Choose the appropriate style and color scheme.
### Step 5:
Validate the layout in various browsers.
### Step 6:
Validate the HTML code.
### Step 6:
Publish the website in the given URL.


## PROGRAM:

## mathadd.html
~~~
{% load static %}
<!DOCTYPE html>
<html>

<head>
    <title>VOLUME OF THE CYLINDER</title>
    <link rel="stylesheet" href="{% static 'css/calculation.css' %}">
</head>

<body>
    <div class="container">
        <div class="formview">
            <div class="banner">
                VOLUME OF THE CYLINDER
            </div>
            <div class="content">
                <form action="" method="GET">
                    {% csrf_token %}
                    <div class="forminput">
                        <label for="value_a">BASE=</label>
                        <input type="text" name="value_a" id="value_a">
                    </div>
                    <div  class="forminput">
                        <label for="value_b">HEIGHT=</label>
                        <input type="text" name="value_b" id="value_b">
                    </div>                    
                    <div class="forminput">
                        <button type="button" name="button_add" id="button_add">CALCULATE</button>
                    </div>
                    <div  class="forminput">
                        <label for="value_c">RESULT=</label>
                        <input type="text" name="value_c" id="value_c" readonly>
                    </div>                   
                </form>
            </div>
        </div>
    </div>
    <script src="/static/js/mathscript.js"></script>
</body>

</html>
~~~
## trianglearea.html
~~~
{% load static %}
<!DOCTYPE html>
<html>

<head>
    <title>AREA OF TRIANGLE</title>
    <link rel="stylesheet" href="{% static 'css/calculation.css' %}">
</head>

<body>
    <div class="container">
        <div class="formview">
            <div class="banner">
                AREA OF TRIANGLE
            </div>
            <div class="content">
                <form action="" method="GET">
                    {% csrf_token %}
                    <div class="forminput">
                        <label for="value_d">BASE=</label>
                        <input type="text" name="value_d" id="value_d">
                    </div>
                    <div  class="forminput">
                        <label for="value_e">HEIGHT=</label>
                        <input type="text" name="value_e" id="value_e">
                    </div>                    
                    <div class="forminput">
                        <button type="button" name="button_area" id="button_area">CALCULATE</button>
                    </div>
                    <div  class="forminput">
                        <label for="value_f">AREA=</label>
                        <input type="text" name="value_f" id="value_f" readonly>
                    </div>                   
                </form>
            </div>
        </div>
    </div>
    <script src="/static/js/2.js"></script>
</body>

</html>
~~~
## mathscript.js
~
result_button = document.querySelector('#button_add');

result_button.addEventListener('click', function(e){
    txta = document.querySelector('#value_a');
    txtb = document.querySelector('#value_b');
    txtc = document.querySelector('#value_c');
    
    let c;

    c = 22/7 * parseFloat(txta.value**2) * parseFloat(txtb.value);

    txtc.value = c;

});
~
## 2.js
~
result_button = document.querySelector('#button_area');

result_button.addEventListener('click', function(e){
    txtd = document.querySelector('#value_d');
    txte = document.querySelector('#value_e');
    txtf = document.querySelector('#value_f');
    
    let f;

    f =  parseFloat(txtd.value)/2 * parseFloat(txte.value);

    txtf.value = f;

});
~
## calculations.css
~
*{
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
      color: #DDE3FD;
}

body, html{
    margin-top: 0px;
    margin-right: 0px;
    margin-bottom: 0px;
    margin-left: 0px;
    padding-top: 0px;
    padding-right: 0px;
    padding-bottom: 0px;
    padding-left: 0px;
    background-color: #798EF6;
}

.container{
    width: 750px;
    margin-left: auto;
    margin-right: auto;
    box-shadow: 15px 15px 8px black;
}

.formview{
    justify-content: center;
    margin-top: 100px; 
}

.forminput{
    height: 50px;
    padding-top: 20px;
    font-size: larger;
}

.banner{
    display: block;
    width: 100%;
    background-color: #0A2299;
    padding-top: 20px;
    text-align: center;
    height: 60px;
}

.content{
    display: block;
    width: 100%;
    background-color:#183BF0;  
    text-align: center;
}

input{
    color: #0A2299;
}
button{
    color: #091034;
}

## OUTPUT:

![output](./static/img/o2.png)

![output](./static/img/o1.png)

## RESULT:
Thus a website is designed for the area of triangle and volume of cylinder using javascript and is hosted in the URL 
http://prasanna.student.saveetha.in:8000/mathadd/
http://prasanna.student.saveetha.in:8000/trianglearea/