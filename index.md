# Assignment 6.3 — Overflow & Layout Fixing

## File 1: `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Overflow & Layout Fixing</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1>CSS Overflow Examples</h1>

    <section>
        <h2>Overflow: Visible</h2>
        <div class="container visible">
            This is a sample paragraph with extra content to demonstrate how overflow visible works. The content extends outside the fixed-height container and remains visible. This text is intentionally long to show the overflow behavior.
        </div>
    </section>

    <section>
        <h2>Overflow: Hidden</h2>
        <div class="container hidden">
            This is a sample paragraph with extra content to demonstrate how overflow hidden works. The content that extends outside the fixed-height container is clipped and cannot be seen.
        </div>
    </section>

    <section>
        <h2>Overflow: Auto</h2>
        <div class="container auto">
            This is a sample paragraph with extra content to demonstrate how overflow auto works. When the content exceeds the container height, a scrollbar appears so users can read the remaining text. This extra sentence makes the content overflow.
        </div>
    </section>

    <section>
        <h2>Overflow: Scroll</h2>
        <div class="container scroll">
            This is a sample paragraph with extra content to demonstrate how overflow scroll works. A scrollbar is provided so users can scroll through the content inside the fixed-height container.
        </div>
    </section>

    <section>
        <h2>Fixed Layout Using Overflow Auto</h2>
        <div class="fixed-container">
            <p>This container has a fixed height and uses overflow auto.</p>
            <p>When more content is added, it stays inside the container and can be read by scrolling.</p>
            <p>Using overflow auto helps prevent content from spilling over and disturbing the page layout.</p>
            <p>This is additional content to demonstrate scrolling in the fixed container.</p>
        </div>
    </section>

</body>
</html>
```

## File 2: `style.css`

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #1e293b;
    margin: 20px;
}

h1 {
    color: #1d4ed8;
    text-align: center;
}

section {
    margin-bottom: 30px;
}

.container {
    height: 100px;
    width: 350px;
    border: 2px solid #2563eb;
    padding: 10px;
    background-color: white;
}

.visible {
    overflow: visible;
}

.hidden {
    overflow: hidden;
}

.auto {
    overflow: auto;
}

.scroll {
    overflow: scroll;
}

.fixed-container {
    height: 120px;
    width: 350px;
    padding: 10px;
    border: 2px solid green;
    background-color: white;
    overflow: auto;
}
```

## Explanation

1. `overflow: visible` allows content to extend outside the container.
2. `overflow: hidden` clips content that exceeds the container.
3. `overflow: auto` adds scrollbars when the content needs them.
4. `overflow: scroll` provides scrollbars even when they are not needed.
5. The fixed layout uses `overflow: auto` to keep extra content inside the container and allow scrolling.

## Layout Fix

The overflow issue is fixed by applying `overflow: auto` to the fixed-height container. This keeps excess content inside the container and makes it accessible through scrolling.