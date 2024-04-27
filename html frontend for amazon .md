<html>
<head>
  <title>Amazon Clone</title>
  <style>
    body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  background-color: #131921;
  color: #fff;
  padding: 10px;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo a {
  color: #fff;
  text-decoration: none;
  font-size: 24px;
  font-weight: bold;
}

.search {
  display: flex;
}

.search input {
  padding: 8px;
  border: none;
  border-radius: 4px 0 0 4px;
}

.search button {
  background-color: #febd69;
  color: #131921;
  border: none;
  border-radius: 0 4px 4px 0;
  padding: 8px 12px;
  cursor: pointer;
}

.user-actions a {
  color: #fff;
  text-decoration: none;
  margin-left: 20px;
}

.cart {
  display: flex;
  align-items: center;
}

.cart i {
  margin-right: 5px;
}
  </style>
</head>
<body>
  <header>
    <nav>
      <div class="logo">
        <a href="#">Amazon Clone</a>
      </div>
      <div class="search">
        <input type="text" placeholder="Search">
        <button>Search</button>
      </div>
      <div class="user-actions">
        <a href="#">Sign In</a>
        <a href="#" class="cart">
          <i class="fas fa-shopping-cart"></i>
          Cart
        </a>
        <div class="theme-toggle">
          <button id="theme-toggle-btn">
            <i class="fas fa-moon"></i>
            Dark Mode
          </button>
        </div>
      </div>
    </nav>
  </header>

  <main>
  </main>

  <footer>
    <p>&copy; 2023 Amazon Clone. All rights reserved.</p>
  </footer>

  <script>
    const themeToggleBtn = document.getElementById('theme-toggle-btn');
const body = document.body;

// Check if dark mode is already set in localStorage
const isDarkMode = localStorage.getItem('darkMode') === 'true';
if (isDarkMode) {
  body.classList.add('dark-mode');
  updateThemeToggleButton();
}

themeToggleBtn.addEventListener('click', () => {
  body.classList.toggle('dark-mode');
  updateThemeToggleButton();
  localStorage.setItem('darkMode', body.classList.contains('dark-mode'));
});

function updateThemeToggleButton() {
  const themeToggleIcon = themeToggleBtn.querySelector('i');
  if (body.classList.contains('dark-mode')) {
    themeToggleIcon.classList.remove('fa-moon');
    themeToggleIcon.classList.add('fa-sun');
    themeToggleBtn.textContent = 'Light Mode';
  } else {
    themeToggleIcon.classList.remove('fa-sun');
    themeToggleIcon.classList.add('fa-moon');
    themeToggleBtn.textContent = 'Dark Mode';
  }
}
  </script>
</body>
</html>
