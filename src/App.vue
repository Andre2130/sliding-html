<template>
  <div class="container">
    <div class="navbar">
      <div class="logo">
        <img src="./images/logo.png" alt="">
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
          <img src="./images/search.png" class="search-icon">
          <div class="social-links">
            <img src="./images/fb.png">
            
            <img src="./images/tw.png">
            <img src="./images/pt.png">
          </div>
          <img src="./images/info.png" class="info-icon">
        </div>

        <div class="msg-container">
          <div id="slider" ref="slider">
            <div class="msg-col">
              <h1>WeTheSauce</h1>
              <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Provident ipsam necessitatibus consectetur, 
                distinctio illum culpa maxime sed, a fugit optio eum natus ipsa dolorem? Nemo non aliquam eos debitis dicta?</p>
                <a href="#">Learn More</a>
            </div>
            <div class="msg-col">
              <h1>Trap Sauce</h1>
              <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Provident ipsam necessitatibus consectetur, 
                distinctio illum culpa maxime sed, a fugit optio eum natus ipsa dolorem? Nemo non aliquam eos debitis dicta?</p>
                <a href="#">Learn More</a>
            </div>
            <div class="msg-col">
              <h1>Sweet Baby Sauce</h1>
              <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Provident ipsam necessitatibus consectetur, 
                distinctio illum culpa maxime sed, a fugit optio eum natus ipsa dolorem? Nemo non aliquam eos debitis dicta?</p>
                <a href="#">Learn More</a>
            </div>
            <div class="msg-col">
              <h1>HOT Sauce</h1>
              <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Provident ipsam necessitatibus consectetur, 
                distinctio illum culpa maxime sed, a fugit optio eum natus ipsa dolorem? Nemo non aliquam eos debitis dicta?</p>
                <a href="#">Learn More</a>
            </div>
          </div>
        </div>

        <div class="controller">
          <div @click="line1()" id="line1"></div>
          <div @click="line2()" id="line2"></div>
          <div @click="line3()" id="line3"></div>
          <div @click="line4()" id="line4"></div>
          <div id="active" ref="active"></div>
        </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  components: {
    
  },
  methods:{
    
   line1: function(){
  this.$refs.slider.style.transform = 'translateX(0)';
  this.$refs.active.style.top = '0px';
},
line2:function(){
  this.$refs.slider.style.transform = 'translateX(-25%)';
  this.$refs.active.style.top = '80px';
},
line3:function(){
  this.$refs.slider.style.transform = 'translateX(-50%)';
  this.$refs.active.style.top = '160px';
},
line4:function(){
  this.$refs.slider.style.transform = 'translateX(-75%)';
  this.$refs.active.style.top = '240px';
}
  },
  computed:{
    


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
  font-size: 14px;
  }
.user img{
  width: 30px;
  margin-left: 15px;
  cursor: pointer;
}
.sidebar{
  width: 155px;
  height: 100vh;
  background: rgba(29,31,58,0.5);
  position: absolute;
  top: 0;
  left: 0;
}
.search-icon{
  width: 20px;
  display: block;
  margin: 120px auto 0;;
}
.social-links{
  width:20px;
  display: block;
  margin: 220px auto 0;
  text-align: center;
}
.social-links img{
  height: 15px;
  margin-bottom: 30px;
}
.info-icon{
  width: 20px;
  position: absolute;
  left: 50%;
  bottom: 30px;
  transform: translate(-50%);
}
.msg-container{
  width: 600px;
  height: 280px;
  position: absolute;
  left:34%;
  top:37%;
  transform: translate(-50%);
  overflow: hidden;
}
#slider{
  display: inline-flex;
  transition: 0.5s;
}
.msg-col{
  width: 600px;
  height: 280px;
}
.msg-col h1{
  color: #fff;
  font-size: 80px;
  font-weight: 100;
  margin: 10px 0;
}
.msg-col p{
  color: #ddd;
  font-size:15px;
  line-height: 25px;
}
.msg-col a{
  display: inline-block;
  text-decoration: none;
  color:#555;
  background: #fff;
  font-size:15px;
  padding:10px 35px;
  border-radius: 30px;
  margin-top:25px;
}
.controller{
  width: 1px;
  height: 320px;
  display: block;
  background: #c0c0c0;
  position: absolute;
  top: 55%;
  right: 50px;
  transform: translate(-50%);
}
#line1,#line2,#line3,#line4{
  height: 80px;
  width: 10px;
  cursor: pointer;
  transform: translate(-50%);
}
#active{
  width: 5px;
  height: 80px;
  border-radius: 10px;
  background: #fff;
  position: absolute;
  top: 0;
  transform: translate(-50%);

}
</style>
