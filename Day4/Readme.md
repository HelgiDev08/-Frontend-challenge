# Building a Personal CV Webpage: HTML & CSS Tutorial

This tutorial will guide you through creating a personal CV webpage similar to the example provided. You'll learn how to structure your HTML content and style it with CSS to create a professional-looking online resume.

## Project Overview

In this project, we'll create a CV webpage with the following sections:
- Header with profile picture and title
- Skills section with collapsible list
- About me article
- Image gallery
- Embedded videos section
- Subscribe button
- Hobbies section with collapsible list
- Education section with a formatted table
- Inspirational quote
- Contact form
- Footer with social media links

## HTML Structure

Let's start by setting up the basic HTML structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <title>CV page</title>
</head>
<body>
    <!-- Content will go here -->
</body>
</html>
```

### 1. Creating the Header

The header contains a profile picture, name, and profession:

```html
<header class="header">
    <img src="assets/me.png" alt="profile picture" class="picture">
    <h1 class="header__title">Your Name | CV page</h1>
    <h3 class="header__subtitle">Your Profession</h3>
</header>
```

### 2. Main Content Section

Wrap all the main content in a `<main>` element:

```html
<main class="main">
    <!-- Main content sections will go here -->
</main>
```

### 3. Skills Section with Collapsible List

The `<details>` and `<summary>` elements create a collapsible section:

```html
<section class="skills">
    <h3>Skills</h3>
    <details>
        <summary>Skills list:</summary>
        <ol>
            <li>1. HTML</li>
            <li>2. CSS</li>
            <li>3. JavaScript</li>
            <!-- Add more skills as needed -->
        </ol>
    </details>
</section>
```

### 4. About Me Article

```html
<article>
    <h4 class="article">Short article about me</h4>
    <p>Write a brief description about yourself, your background, interests, and career goals.</p>
</article>
```

### 5. Image Gallery

```html
<section class="gallery">
    <h3>Gallery</h3>
    <img src="https://placehold.co/250x250" alt="gallery image 1">
    <img src="https://placehold.co/250x250" alt="gallery image 2">
    <img src="https://placehold.co/250x250" alt="gallery image 3">
</section>
```

### 6. Separator Line

```html
<hr class="separator">
```

### 7. Video Section

Embed YouTube videos using iframes:

```html
<section class="video">
    <h3>My videos</h3>
    <iframe width="337" height="599" src="https://www.youtube.com/embed/VIDEO_ID_1" title="Video Title 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    <!-- Add more video iframes as needed -->
</section>
```

### 8. Subscribe Button

Create a form that links to your YouTube channel:

```html
<form action="https://www.youtube.com/@YourChannel" method="get" target="_blank">
    <h3 class="form_text">SUBSCRIBE IT IS FREE!</h3>
    <button class="subscribe_button">SUBSCRIBE</button>
</form>
```

### 9. Hobbies Section

Another collapsible section using details and summary:

```html
<section class="hobbies">
    <h4>My hobbies</h4>
    <details>
        <summary>Hobbies</summary>
        <ul>
            <li>Hobby 1</li>
            <li>Hobby 2</li>
            <li>Hobby 3</li>
        </ul>
    </details>
</section>
```

### 10. Education Table

Create a structured table for education history:

```html
<hr class="ed">
<section class="Education">
    <table class="ed_table">
        <thead>
            <tr>
                <th>School/University</th>
                <th>Degree/Field</th>
                <th>Year</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Institution Name 1</td>
                <td>Degree/Field 1</td>
                <td>Year 1</td>
            </tr>
            <tr>
                <td>Institution Name 2</td>
                <td>Degree/Field 2</td>
                <td>Year 2</td>
            </tr>
        </tbody>
    </table>
</section>
```

### 11. Quote Section

```html
<section class="quote">
    <blockquote>
        "Your favorite inspirational quote." – Author Name
    </blockquote>
</section>
```

### 12. Contact Form

Create a form for visitors to contact you:

```html
<section class="interaction">
    <form action="mailto:your.email@example.com" method="post" target="_blank">
        <fieldset>
            <legend>Required fields:</legend>
            <label for="firstName-id">First Name:</label>
            <input type="text" name="firstName" id="firstName-id" required class="interaction_control" placeholder="your first name">
            
            <label for="lastName-id">Last Name:</label>
            <input type="text" name="lastName" id="lastName-id" required class="interaction_control" placeholder="your last name">
            
            <label for="email-id">Email:</label>
            <input type="email" name="email" id="email-id" required class="interaction_control" placeholder="your email">
        </fieldset>
        <br>
        <textarea name="message" cols="30" rows="7" class="interaction_control control_text" placeholder="your message"></textarea>
        <br>
        <button type="submit" class="interaction_button">Send me a message!</button>
    </form>
</section>
```

### 13. Footer with Social Links

```html
<footer class="footer">
    <a href="https://github.com/YourUsername" target="_blank">
        <i class="fab fa-github"></i> GitHub
    </a>
    <!-- Add more social links as needed -->
</footer>
```

## CSS Styling

Now let's style our CV page with CSS. Create a file named `styles.css`:

```css
body {
    background-color: rgb(137, 181, 220);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Header Styles */
.header {
    text-align: center;
}

.picture {
    width: 300px;
    height: 300px;
}

.header__title {
    font-size: 25px;
}

.header__subtitle {
    color: rgb(255, 255, 255);
}

/* Main Content Styles */
.main {
    border: 1px solid darkcyan;
    text-align: center;
}

/* Skills Section */
.skills ol {
    list-style: none;
}

/* Separator */
.separator {
    width: 50%;
    height: 3px;
    background-color: darkcyan;
}

/* Subscribe Button */
.form_text {
    color: rgba(255, 0, 0, 0.337);
}

.subscribe_button {
    color: white;
    background-color: red;
    border-radius: 3px;
}

/* Education Table */
.ed_table {
    border-collapse: collapse;
}

.ed_table th,
.ed_table td {
    border: 1px solid black;
    padding: 10px;
}

/* Quote Section */
.quote {
    font-size: 32px;
}

/* Contact Form */
.interaction {
    width: 600px;
    margin: 0 auto;
}

.interaction_control {
    width: 100%;
}

.control_text {
    width: 50%;
}

.interaction_button {
    display: block;
    margin: 0 auto;
}

/* Footer */
.footer {
    text-align: center;
    background-color: rgb(113, 178, 198);
}
```

## Key HTML Elements and Concepts Used

1. **Semantic HTML Elements**
   - `<header>`, `<main>`, `<footer>`: Define the structure of the page
   - `<section>`, `<article>`: Group related content
   - `<h1>` through `<h4>`: Create a hierarchy of headings
   - `<blockquote>`: Format a quoted text

2. **Lists**
   - `<ol>` (ordered list) for skills
   - `<ul>` (unordered list) for hobbies

3. **Interactive Elements**
   - `<details>` and `<summary>`: Create collapsible sections
   - `<form>` with various input types
   - `<button>`: For interactive actions

4. **Tables**
   - `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`: Structure tabular data

5. **Media Elements**
   - `<img>`: Display images
   - `<iframe>`: Embed YouTube videos

6. **Form Elements**
   - `<fieldset>` and `<legend>`: Group form controls
   - `<input>`: Various types for user input
   - `<textarea>`: Multi-line text input
   - `<label>`: Associate text with form controls

7. **External Resources**
   - Font Awesome icons via CDN
   - Link to external stylesheet

## Key CSS Concepts Used

1. **Selectors**
   - Class selectors (`.header`, `.skills`, etc.)
   - Element selectors (`body`, `h1`, etc.)
   - Descendant selectors (`.skills ol`, `.ed_table th`)

2. **Text Styling**
   - `font-family`: Set the typeface
   - `font-size`: Control text size
   - `color`: Set text color
   - `text-align`: Center text content

3. **Box Model Properties**
   - `width` and `height`: Size elements
   - `border`: Add borders to elements
   - `padding`: Create space inside elements
   - `margin`: Create space around elements

4. **Colors**
   - RGB notation: `rgb(137, 181, 220)`
   - RGBA with transparency: `rgba(255, 0, 0, 0.337)`
   - Named colors: `white`, `red`, `black`

5. **Layout**
   - `margin: 0 auto`: Center elements horizontally
   - `display: block`: Change element display type

6. **Table Styling**
   - `border-collapse`: Control how borders are handled

## Customization Tips

1. **Colors and Theme**
   - Change the background color and accent colors to match your personal brand
   - Consider a light/dark mode toggle for better accessibility

2. **Fonts**
   - Import Google Fonts or other web fonts for a unique look
   - Ensure font sizes are readable on all devices

3. **Images**
   - Replace placeholder images with real photos of your work or yourself
   - Optimize images for web to improve loading times

4. **Responsive Design**
   - Add media queries to make the page look good on mobile devices
   - Consider a flexible grid layout for the gallery

5. **Additional Sections**
   - Portfolio section showcasing your work
   - Testimonials from clients or colleagues
   - Certifications and achievements

## Conclusion

This tutorial has guided you through creating a personal CV webpage using HTML and CSS. By understanding the structure and styling techniques used, you can now customize this template to create your own professional online presence.

Remember to keep your content concise, highlight your strengths, and maintain a clean, organized layout. Regular updates to your CV page will ensure it remains current with your latest skills and accomplishments.

Happy coding!