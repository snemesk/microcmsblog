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
          <input type="hidden" name="form-name" value="contact" />
          <div class="contactform">
          <label>お名前：<input type="text" name="name" placeholder="名前" /></label>
          <label>メールアドレス：<input type="email" name="email" placeholder="メールアドレス" /></label>
          <label>メッセージ：<textarea name="message" placeholder="メッセージ" rows="3"></textarea></label>
          </div>
          <button type="submit">Send</button>
      </form>
          <!-- /.p-contact__form -->
        </div>
      </div>
</template>

<style lang="scss" scoped>
.contactform{
  margin:12px 0;

}
</style>

