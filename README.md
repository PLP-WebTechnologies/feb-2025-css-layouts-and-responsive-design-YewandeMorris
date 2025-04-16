# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Flexbox Layout</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <nav class="navbar">
    <div class="logo">MySite</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <main class="content">
    <section class="box">Content Box 1</section>
    <section class="box">Content Box 2</section>
    <section class="box">Content Box 3</section>
  </main>
</body>
</html>


* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  padding: 1rem;
  color: white;
}

.nav-links {
  display: flex;
  gap: 1rem;
  list-style: none;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

.content {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  padding: 1rem;
  justify-content: center;
}

.box {
  background-color: #f2f2f2;
  padding: 2rem;
  flex: 1 1 300px;
  text-align: center;
}

/* Media Queries */
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-links {
    flex-direction: column;
    width: 100%;
  }

  .nav-links li {
    padding: 0.5rem 0;
  }

  .content {
    flex-direction: column;
    align-items: center;
  }
}
