# Flexbox Layout Documentation

## Introduction
This guide provides a step-by-step explanation of how to recreate two different website layouts using **CSS Flexbox**. These examples demonstrate how Flexbox can be used to build **responsive** and **dynamic** web designs.

## Prerequisites
To follow along, you should have basic knowledge of:
- HTML and CSS
- CSS Flexbox properties
- Media queries for responsive design

## Example 1: Two-Column Layout with Navbar

### 1. Structure (HTML)
This layout consists of:
- A **navigation bar** at the top
- A **main content** section
- A **sidebar**

```html
<div class="container">
    <nav class="navbar">Navigation Bar</nav>
    <div class="content">
        <aside class="sidebar">Sidebar</aside>
        <main class="main">Main Content</main>
    </div>
</div>
```

### 2. Styling (CSS)
To structure this layout with Flexbox:

```css
.container {
    display: flex;
    flex-direction: column;
}

.navbar {
    background: #333;
    color: white;
    padding: 10px;
    text-align: center;
}

.content {
    display: flex;
    flex: 1;
}

.sidebar {
    width: 25%;
    background: #f4f4f4;
    padding: 20px;
}

.main {
    width: 75%;
    padding: 20px;
}
```

### 3. Responsiveness
To make the layout responsive, we use media queries:

```css
@media (max-width: 800px) {
    .content {
        flex-direction: column;
    }
    .sidebar, .main {
        width: 100%;
    }
}
```

---

## Example 2: Responsive Grid Layout

### 1. Structure (HTML)
This layout consists of **multiple content blocks** that dynamically adjust based on screen size.

```html
<div class="grid-container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
    <div class="box">Box 4</div>
</div>
```

### 2. Styling (CSS)
We use Flexbox to create a dynamic grid layout:

```css
.grid-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
}

.box {
    background: #007bff;
    color: white;
    padding: 20px;
    flex: 1 1 200px;
    text-align: center;
}
```

### 3. Responsive Adjustments
Breakpoints adjust the number of columns:

```css
@media (max-width: 800px) {
    .grid-container {
        flex-wrap: wrap;
    }
    .box {
        flex: 1 1 45%; /* Two columns */
    }
}

@media (max-width: 600px) {
    .box {
        flex: 1 1 100%; /* One column */
    }
}
```

## Conclusion
By following this guide, you can recreate both layouts and understand how **Flexbox** simplifies web design. Experiment with different flex properties to enhance your skills. For further learning, check out W3Schools Flexbox tutorials and interactive games like **Flexbox Froggy**!

