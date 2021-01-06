<template>
    <div class="no-pd" id="content">
      <div class="container">
            <div class="breadcrumb">
              <ul>
                <li><a href="index.html"> <i class="fas fa-home"></i>Home</a></li>
                <li class="active"><a href="#">Contact</a></li>
              </ul>
            </div>

<form name="contact" method="POST" data-netlify="true">
  <p>
<input type="hidden" name="form-name" value="contact" />
    <label>Your Name: <input type="text" name="name" /></label>
  </p>
  <p>
    <label>Your Email: <input type="email" name="email" /></label>
  </p>
  <p>
    <label>Message: <textarea name="message"></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>
    <!-- /.p-contact__form -->
  </div>
</div>
    </div>
</template>
