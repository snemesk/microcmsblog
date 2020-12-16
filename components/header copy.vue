<template>
     <div class="container">
        <div class="header-wrapper"><a class="header__logo" href="index.html"><img src="./assets/images/logo.png" alt="Logo"/></a>
          <nav>
            <ul>
              <li class="nav-item active"><a href="index.html">Home</a>
                <ul class="dropdown-menu">
                  <li><a href="index.html">HOMEPAGE1</a></li>
                  <li><a href="homepage2.html">HOMEPAGE2</a></li>
                  <li><a href="homepage3.html">HOMEPAGE3</a></li>
                  <li><a href="homepage4.html">HOMEPAGE4</a></li>
                  <li><a href="homepage5.html">HOMEPAGE5</a></li>
                  <li><a href="homepage6.html">HOMEPAGE6</a></li>
                  <li><a href="homepage7.html">HOMEPAGE7</a></li>
                  <li><a href="homepage8.html">HOMEPAGE8</a></li>
                  <li><a href="homepage9.html">HOMEPAGE9</a></li>
                </ul>
              </li>
              <li class="nav-item"><a>Blog</a>
                <ul class="dropdown-menu">
                  <li><a href="blog_category_grid.html">BLOG CATEGORY GRID</a></li>
                  <li><a href="blog_category_list.html">BLOG CATEGORY LIST</a></li>
                  <li><a href="post_standard.html">POST STANDARD</a></li>
                  <li><a href="post_standard_image_full.html">POST STANDARD IMAGE FULLWIDTH</a></li>
                  <li><a href="post_standard_sidebar.html">POST STANDARD SIDEBAR</a></li>
                  <li><a href="post_gallery.html">POST GALLERY</a></li>
                  <li><a href="post_video.html">POST VIDEO</a></li>
                  <li><a href="post_audio.html">POST AUDIO</a></li>
                  <li><a href="post_quote.html">POST QUOTE</a></li>
                </ul>
              </li>
              <li class="nav-item"><a href="#">Pages</a>
                <ul class="dropdown-menu">
                  <li><a href="author.html">AUTHOR</a></li>
                  <li><a href="about.html">ABOUT</a></li>
                  <li><a href="contact.html">CONTACT</a></li>
                  <li><a href="shop.html">SHOP</a></li>
                  <li><a href="product_detail.html">PRODUCT DETAIL</a></li>
                  <li><a href="cart.html">CART</a></li>
                  <li><a href="checkout.html">CHECKOUT</a></li>
                  <li><a href="error_404.html">ERROR</a></li>
                </ul>
              </li>
              <li class="nav-item"><a href="about.html">About</a></li>
              <li class="nav-item"><a href="contact.html">Contact</a></li>
            </ul>
          </nav>
          <div class="header__icon-group"><a href="#" id="search"><i class="fas fa-search"></i></a>
            <div class="social"><a href="#"><i class="fab fa-facebook-f"></i></a><a href="#"><i class="fab fa-twitter"></i></a><a href="#"><i class="fab fa-instagram"></i></a><a href="#"><i class="fab fa-dribbble"></i></a><a id="mobile-menu-controller" href="#"><i class="fas fa-bars"></i></a></div>
          </div>
        </div>
      </div>
<section>
  <div class="top">
    <header><h1>
          <NuxtLink to="/">
          <img src="/img/logo.png?w=100"
          alt
          />
          </NuxtLink>
          </h1>
        <HeaderNav />
    </header>
  </div>
</section>
</template>
