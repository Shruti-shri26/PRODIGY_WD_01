<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Navigation Menu</title>
<style>
  body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    color: #333;
  }
  .navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background-color: #333;
    padding: 15px 0;
    z-index: 1000;
    transition: background-color 0.3s ease;
  }
  .navbar a {
    color: white;
    text-decoration: none;
    padding: 15px;
    transition: color 0.3s ease;
  }
  .navbar a:hover {
    color: #ff6600;
  }
  .content {
    padding-top: 70px; /* Adjust based on navbar height */
    text-align: center;
  }
  .home-page {
    background-color: #f9c2ff;
  }
  .about-page {
    background-color: #aaffc3;
  }
  .services-page {
    background-color: #c3aaff;
  }
  .contact-page {
    background-color: #ffd966;
  }
</style>
</head>
<body>

<div class="navbar" id="navbar">
  <a href="#" onclick="changePage('home')">Home</a>
  <a href="#" onclick="changePage('about')">About</a>
  <a href="#" onclick="changePage('services')">Services</a>
  <a href="#" onclick="changePage('contact')">Contact</a>
</div>

<div class="content" id="page-content">
    <h2>XYZ IT Solution</h2>
  <h1>Welcome to the Home Page!</h1>
  <p>This is the home page. It contains information about our company.</p>
</div>

<script>
  window.onscroll = function() {scrollFunction()};

  function scrollFunction() {
    if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
      document.getElementById("navbar").style.backgroundColor = "#555";
    } else {
      document.getElementById("navbar").style.backgroundColor = "#333";
    }
  }

  function changePage(page) {
    var content = document.getElementById("page-content");
    if (page === 'home') {
      content.innerHTML = `
        <h1>Welcome to the Home Page!</h1>
      `;
      content.className = "content home-page";
    } else if (page === 'about') {
      content.innerHTML = `
        <h1>About Us</h1>
      `;
      content.className = "content about-page";
    } else if (page === 'services') {
      content.innerHTML = `
        <h1>Our Services</h1>
      `;
      content.className = "content services-page";
    } else if (page === 'contact') {
      content.innerHTML = `
        <h1>Contact Us</h1>
        <p>Get in touch with us for any inquiries or feedback.</p>
      `;
      content.className = "content";
    }
  }
</script>

</body>
</html>


![Screenshot (1709)](https://github.com/Shruti-shri26/PRODIGY_WD_01/assets/123724798/472f9464-6946-49bc-9916-19f67b00e56f)




