<template>
  <div>
    <head>
      <meta charset="UTF-8" />
      <meta http-equiv="X-UA-Compatible" content="IE=edge" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0" />
      <link rel="stylesheet" href="css/style.css" />
      <title>Move Bangladesh</title>
    </head>
    <body>
      <div class="main_menu">
        <ul>
          <li><a href="#">About</a></li>
          <li>
            <a href="#">Service</a>
            <ul>
              <li><a href="#">Event Management </a></li>
              <li><a href="#">Vlogers BD </a></li>
              <li><a href="#">Advertisment </a></li>
            </ul>
          </li>
          <li><a href="#">Contact</a></li>
          <li><a href="#">Parking BD</a></li>
          <li><a href="#">Home</a></li>
        </ul>
        <img src="../assets/logo.jpg" height="75px" alt="logo" />
      </div>

      <!-- <pre class="pregraph"> -->
      <!-- Lorem, ipsum dolor sit amet consectetur adipisicing elit. -->
      <!-- Officiis qui, minus id animi sequi sunt ad amet praesentium  -->
      <!-- omnis quis optio rem magni repellendus autem itaque maxime  -->
      <!-- tenetur quaerat magnam? -->
      <!-- </pre> -->

      <!-- <img src="images/banner.jpg" height="700px" width="350px" alt="banner"> -->

      <footer>
        <h3>
          Contact = arobiemon@gmail.com <br />
          Facebook = facebook.com/arobiemon47
        </h3>
        <h2>Mondol IT</h2>
      </footer>
    </body>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
});
</script>
<style scoped>
*{
    margin: 0;
    padding: 0;
}

ul
li{
    list-style:none;
}
a{
    text-decoration: none;
    display: inline-block;
}
.main_menu{
      background-image: url(../assets/banner.jpg);
      background-repeat: no-repeat;
      background-size: cover;
      background-position:center;
      height:600px;


}



.main_menu  ul li a{

    float: right;
    color: #000;
    line-height: 60px;
    padding: 0 40px;
    font-size: 20px;
    position: relative;

}
.main_menu ul li a:hover{
    color: coral;


}
.pregraph{
    /* float: right; */
    font-family: sans-serif;
    color: brown;
    font-size: 20px;
    float: right;
}
footer{
    /* background-color:cornflowerblue; */
    font-family: sans-serif;

}
 h2{
    /* background-color: cornflowerblue; */
    float: right;

}



.main_menu ul ul {
    display:none;
}
.main_menu ul li:hover > ul {
    display: block;

}

</style>
