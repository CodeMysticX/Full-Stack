## CSS Positioning Example

This HTML code demonstrates the use of CSS positioning to create a simple layout with a rectangle and a circle. It's designed to showcase various positioning techniques in CSS.

## CSS Positioning Methods

Using different type of css positioning methods:
1. Static
2. Relative
3. Absolute
4. Fixed
5. Sticky

## HTML Code

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Rectangle</title>
    <style>
        /* Define styles for the rectangle */
        .rect {
            border: 1px solid black;
            width: 50%;
            height: 700px;
        }

        /* Define styles for the colored rectangle */
        .rectangle {
            background-image: linear-gradient(rgb(109, 128, 0), rgb(196, 255, 192));
            border: 1px solid black;
            left: 35%;
            height: 250px;
            width: 300px;
            margin: 0 auto;
            position: sticky;
            top: 0px;
            bottom: 0px;
        }

        /* Define styles for the circle */
        .circle {
            position: absolute;
            border: 1px solid black;
            background-image: linear-gradient(rgb(140, 0, 255), rgb(0, 255, 195));
            width: 50%;
            height: 50%;
            top: 25%;
            left: 25%;
            border-radius: 50%;
        }
    </style>
</head>

<body>
    <!-- Create the first rectangle -->
    <div class="rect"></div>

    <!-- Create the colored rectangle with the circle inside -->
    <div class="rectangle">
        <div class="circle"></div>
    </div>

    <!-- Create the second rectangle -->
    <div class="rect"></div>
</body>

</html>
