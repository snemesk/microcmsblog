<template>
    <div class="no-pd" id="content">
      <div class="container">
            <div class="breadcrumb">
              <ul>
                <li><a href="index.html"> <i class="fas fa-home"></i>Home</a></li>
                <li class="active"><a href="#">Contact</a></li>
              </ul>
            </div>
<div class="center">
            <div class="contactform">
            <form name="contact" method="POST" data-netlify="true">
              <input type="hidden" name="form-name" value="contact" />
              <dl>
                <dt>お名前：</dt>
                <dd><input type="text" name="name" placeholder="名前" /></dd>
                <dt>メールアドレス：</dt>
                <dd><input type="email" name="email" placeholder="メールアドレス" /></dd>
                <dt>メッセージ：</dt>
                <dd><textarea name="message" placeholder="メッセージ" rows="4"></textarea></dd>
              </dl>
              <button type="submit">Send</button>
            </form>
            </div>
</div>
                <!-- /.p-contact__form -->
      </div>
    </div>
</template>

<style lang="scss" scoped>

form{
  background-color: #eaeaea;
  padding:30px 50px;
}

form dl dt{
  width: 165px;
  padding:10px 0;
  float:left;
  clear:both;
}

form dl dd{
  padding:10px 0;
}
input,textarea{
  background-color: #ffffff;
}
.contactform{
  width: 500px;
  margin: auto;
  padding: 5px 8px;
  border-radius: 6px;
  font-size: 16px;
}
</style>

