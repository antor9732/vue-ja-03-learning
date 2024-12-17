<template>
<footer class="footer">
  <div class="container">
    <div class="row">
      <!-- Footer Column 1 -->
      <div class="col-md-4 footer-item">
        <h3>CodeSolutionIT</h3>
        <p>Web Development Company</p>
      </div>
      <!-- Footer Column 2 -->
      <div class="col-md-4 footer-item">
        <h3>Our Services</h3>
        <ul>
          <li><a href="#">Web Design</a></li>
          <li><a href="#">Web Development</a></li>
          <li><a href="#">SEO Optimization</a></li>
        </ul>
      </div>
      <!-- Footer Column 3 -->
      <div class="col-md-4 footer-item">
        <h3>Contact Us</h3>
        <p>Email: info@codesolutionit.com</p>
        <p>Phone: +123 456 7890</p>
      </div>
    </div>
  </div>
  <!-- Footer Bottom -->
  <div class="footer-bottom text-center">
    <p>Copyright &copy; 2024 | <a href="#">CodeSolutionIT</a></p>
  </div>
</footer>


</template>

<style scoped>
.footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px;
  position: fixed;
  bottom: 0;
  width: 100%;
}
/* Footer Styles */

.footer h3 {
  font-size: 18px;
  margin-bottom: 15px;
  color: #f8f9fa;
}

.footer p {
  font-size: 14px;
  line-height: 1.6;
  color: #d1d1d1;
  margin: 5px 0;
}

.footer ul {
  list-style: none;
  padding: 0;
  
}

.footer ul li {
  margin: 5px 0;
  align-items: left;
}

.footer a {
  color: #00d9ff; /* Light blue links */
  text-decoration: none;
}

.footer a:hover {
  text-decoration: underline;
}

/* Footer Bottom Section */
.footer-bottom {
  margin-top: 20px;
  border-top: 1px solid #444;
  padding-top: 10px;
  font-size: 13px;
  color: #aaa;
}

.footer-bottom a {
  color: #00d9ff;
}

/* Flexbox Layout */
.row {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.col-md-4 {
  flex: 0 0 30%; /* Each column takes 30% width */
  margin-bottom: 20px;
}

.text-center {
  text-align: center;
}

/* Responsive Design */
@media (max-width: 768px) {
  .col-md-4 {
    flex: 0 0 50%; /* Full width on small screens */
    text-align: center;
  }
}

</style>
