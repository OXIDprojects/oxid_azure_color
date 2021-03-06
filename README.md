Custom Colors in Oxid eShops Azure Theme made easy
==================================================

Add as stand-alone theme (with azure as parent)
-----------------------------------------------
Clone this repository into your shops 'out' directory.

```
cd out
git clone git://github.com/1st8/oxid_azure_color.git
```

and select the 'Oxid Azure Custom Color' Theme in the Admin Area

Add to your already modified azure theme
----------------------------------------
Get the contents of the ```src``` directory and copy it to your theme.
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

Production
----------
I recommend compiling the less File once and adding the resulting css to your page instead of the client side compilation

Demo (with ugly colors)
-----------------------
http://oxid.polar.christophgeschwind.de/

Contribution
------------
Feel free to fork this and implement additional features.
Please Report places where I've missed a default color.

TODO
----
- Find unobtrusive way to include the needed files (without shadowing base.tpl)
- Implement more Color Variables
- Replace Gradients with mixin
- Allow non Gradient Backgrounds