# custom-css

## Stylish CSS 

Stylish CSS is a lightweight, responsive CSS framework designed for easy customization and modern web development. An easy and efortless way to keep you designs stylish.

Stylish.css includes:
- A CSS reset to ensure consistency across browsers.
- Base styles for typography, lists, buttons, forms, and layout.
- A responsive grid system.
- Utility classes for common styling needs.

## Installation

1. Download the `stylish.css` file and include it in your project.
2. Add the following line to your HTML file:
    <link rel="stylesheet" href="./css/stylish.css">

## CSS Reset

This framework includes a CSS reset (The new CSS reset - by Elad), to ensure consistency across different browsers. The reset removes default margins, paddings, and standardizes element styling to create a clean foundation for your designs. For you to start with a blank canvas.

    The new CSS reset - version 1.11.3 (last updated 25.08.2024)
    GitHub page: https://github.com/elad2412/the-new-css-reset

## Usage
Find below instructions and directions on how to use the Stylish CSS elements to improve your designs.
For further directions on how to use Stylish CSS you can refer to the index.html and the .scss files.

### Colors

Colors are set under 'variables.scss' in the theme map. Call the desired color by using their predefined classes:
`$theme: (
    "light":      #d0e2ff,
    "dark":       #e7c8f9,
    "primary":    #353165,
    "secondary":  #466cba,
    "info":       #7685f8,
    "success":    #119f5e,
    "warning":    #dfca12,
    "danger":     #ec2207,
    "white": #fff,
);

You can update the colors by altering the .scss file directly.

### Typography

There are two defined font families in Stylish CSS: "Indie Flower" and "Patric Hand".

- Change the default fonts in `variables.scss`:
  ```scss
  $heading-font: "Indie Flower", serif;
  $body-font: "Patrick Hand", serif;
  ```
- Modify font sizes and weights:
  ```scss
  $font-size-medium: 1.5rem;
  $font-weight-bold: 700;
  ```

### Utilities

For rounded borders, use the predefined classes. 

```scss
$rounded: (
    "sm": 6px,
    "md": 14px,
    "lg": 20px,
    "full": 50%,
);
```
```html
</div>
    <section>
        <h4>Utility classes - Rounded</h4>
        <p>use "rounded-sm", "rounded-md", "rounded-lg", "rounded-full", to customize your border radius.</p>
        <img class="rounded-sm" src="https://placehold.co/100?text=Hello+World&font=roboto" />
        <img class="rounded-md" src="https://placehold.co/100?text=Hello+World&font=poppins" />
        <img class="rounded-lg" src="https://placehold.co/100?text=Hello+World&font=playfair display" />
        <img class="rounded-full" src="https://placehold.co/100?text=Hello+World&font=montserrat" />
    </section>
<div>
```

You can update those values under the .scss files

#### Buttons & Links

This framework comprises two types of buttons and one type of link styles: 
**stylish-btn:** background color, no hover animation.
**stylish-outline-btn:** outline color, transparent background, hover animation with background color.
**stylish-link:** colored text, hover animation with background color.

Use the predefined button classes:
```html
<button class="btn btn-primary">Primary Button</button>
<button class="btn btn-secondary">Secondary Button</button>
```
Modify button styles using the `stylish-btn` mixin in `base.scss`:
```scss
@mixin stylish-btn($btn-bg-color: map-get(variables.$theme, "primary"), $btn-text-color: map-get(variables.$theme, "dark")) {
    background-color: $btn-bg-color;
    color: $btn-text-color;
    border-radius: variables.$border-radius;
}
```

#### Lists

Listed items on unordered list are represented by circles. 
Ordered lists use discs.

```scss
$list-ul: circle;
$list-ol: disc;
$border-radius: 6px;
```

#### Forms

Stylish CSS form's have outlined inputs and predefined layouts that can be altered in the .scss files.

```html
<form>
    <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email">
    </div>
    <button type="submit">Submit</button>
</form>
```

#### Cards

Cards have a coloured background with a drop shadow and colored text and a hover animation. Those can be used to display information that is meant to be highlited or call-to-action.

```scss
.card {
    background-color: map-get(variables.$theme, "light") ;
    border-radius: variables.$border-radius;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
    margin: 25px;
    display: flex;
    flex-wrap: wrap;
    transition: transform 0.3s ease;

    &:hover{
        transform: translateY(-5px);
    }
}
```
```html
<div class="card">
    <div class="card-header">Card Title</div>
    <div class="card-body">Card Content</div>
</div>
```

#### Navigation

Navigation links have hover animation and layout predefinitions.

```scss
.navbar {
    display: flex;
    justify-content: space-between;
    padding: 10px 20px;
    background: map-get(variables.$theme, "primary");
    color: white;

    .nav-links {
        display: flex;
        gap: 15px;
    }

    a {
        color: map-get(variables.$theme, "white");
        text-decoration: none;
        padding: 8px 12px;
        transition: background 0.3s ease;

        &:hover {
            background: map-get(variables.$theme, "secondary") ;
        }
    }
}
```
```html
<nav>
    <ul class="navbar">
        <li class="nav-links"><a href="#">Features</a></li>
        <li class="nav-links"><a href="#">Components</a></li>
    </ul>
</nav>
```

#### Footer

Footer section has a background color, like the navigation bar.

```scss
.footer{
    background: map-get(variables.$theme, "secondary");
    color:map-get(variables.$theme, "white");
    padding: 20px;
}
```
```html
<footer class="footer">
    &copy; 2025 Styish CSS
</footer>
```

## Customization

All elements covered by the Stylish CSS Framework can be altered and updated to your liking by altering the .scss files. There are no creative limitations and you can continue to use all predefined classes to bring your design to life.

## License

Stylish CSS is an open source Custom Framework 
MIT License - Free to use and modify!