Custom Colors in Oxid eShops Azure Theme made easy
==================================================

Add as stand-alone theme (with azure as parent)
-----------------------------------------------
Copy the contents of this repository into your oxid basedir 
and select the 'Oxid Azure Custom Color' Theme in the Admin Area

Add to your already modified azure theme
----------------------------------------
Get the contents of the 'src' directory and copy it to your theme.
Add the two lines in your ```<head>``` section after the stylesheets (!)

```html
    <link rel="stylesheet/less" type="text/css" href="/out/oxid_azure_color/src/less/main.less">
    <script type="text/javascript" src="/out/oxid_azure_color/src/js/less-1.2.1.min.js"></script>
```

Change the colors
-----------------
edit the 'main.less' file and change the color values assigned to the variables.

Development
-----------
You might want to add 

```html
    <script type="text/javascript">
      less = {env: 'development'}
    </script>
```
before including less.js during development. It gives you nice error and status reports.

Demo (with ugly colors)
-----------------------
http://oxid.polar.christophgeschwind.de/

Contribution
------------
Feel free to fork this and implement additional features.
Please Report places where I've missed a default color.