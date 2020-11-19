<template>
  <div class="container">
    <div class="navbar">
      <div class="logo">
        <img src="https://cdn5.vectorstock.com/i/thumb-large/76/79/your-logo-here-placeholder-symbol-vector-26077679.jpg" alt="">
        </div>
        <nav>
          <ul>
            <li><a href="#">About</a></li>
            <li><a href="#">Libray</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </nav>
        <div class="user">
          <p>Andre Robinson</p>
          <img src="http://wethesauce.com/wp-content/uploads/2016/07/Sauce-Logo-e1547434620690.jpeg" alt="">
        </div>
        <div class="sidebar">
          <img src="images/search.png" class="fa fa-search">
          <div class="social-links">
            <img src="images/fb.png" alt="">
            <img src="images/p.png" alt="">
            <img src="images/tw" alt="">
          </div>
        </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  components: {
    
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  font-family: sans-serif;
}
.container{
  width: 100%;
  height: 100vh;
  background: url('https://images.ctfassets.net/hrltx12pl8hq/5KiKmVEsCQPMNrbOE6w0Ot/94f8afc787d3f426baba3394d5271bb3/hero-img_copy.jpg?fit=fill&w=800&h=300') no-repeat center center fixed;
  background-size: cover;
  position: relative;
  padding-top: 30px;
  box-sizing: border-box;
}
.navbar{
  width: 100%;
  height: 60px;
  display: flex;
  align-items: center;
  background: rgba(29, 33, 61, 0.5);
  padding: 0 60px;
  box-sizing: border-box;
}
.logo{
  width: 155px;
}
.logo img{
  width: 30px;
  position: relative;
  z-index: 10px;
  cursor: pointer;
}
nav{
  flex: 1;
}
nav ul li{
  list-style: none;
  display: inline;
  margin-right: 60px;
}
nav ul li a{
  text-decoration: none;
  color: #fff;
  font-size: 14px;
}
.user{
  display: flex;
  align-items: center;
  color: #fff;

font-size: 14px;}
.user img{
  width: 30px;
  margin-left: 15px;
  cursor: pointer;

}
</style>
