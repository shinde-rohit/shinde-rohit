<!DOCTYPE html>
<html >
<head>
  <meta charset="UTF-8">
  <title>sideToggle</title>
  <link href='https://fonts.googleapis.com/css?family=PT+Sans:400,700italic,700,400italic|PT+Serif:400,700,400italic,700italic|Vollkorn|Rokkitt:400,700' rel='stylesheet' type='text/css'>


  <link rel='stylesheet prefetch' href='http://cadice.b1.jcink.com/uploads/cadice/Style_My_Tooltips/style_my_tooltips.css'>
<link rel='stylesheet prefetch' href='https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.5.0/css/font-awesome.min.css'>
<script src='http://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.2/jquery.min.js'></script>
<script src='https://cdnjs.cloudflare.com/ajax/libs/velocity/1.2.3/velocity.min.js'></script>
<script src='http://cadice.b1.jcink.com/uploads/cadice/slideToggleExtended_min.js'></script>

<style>
    * {box-sizing: border-box;}
body {
  background: #fcfcfc;
  font: 12px 'PT Sans', Helvetica, Arial, sans-serif;
}
a {
  color: #f06060;
  text-decoration: none;
  -moz-transition: 0.1s all ease-in-out;
  -o-transition: 0.1s all ease-in-out;
  -webkit-transition: 0.1s all ease-in-out;
  transition: 0.1s all ease-in-out;
}
a:hover {
  color: #fcfcfc;
}
.colorchange {
  color: #f35626;
    background-image: -webkit-linear-gradient(92deg,#f35626,#feab3a);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    -webkit-animation: hue 60s infinite linear;
}
@-webkit-keyframes hue {
  from {
    -webkit-filter: hue-rotate(0deg);
  }

  to {
    -webkit-filter: hue-rotate(-360deg);
  }
}

nav {
  background: #202020;
  box-shadow: 0px 1px 5px #5c4b51;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 56px;
  font: 14px Rokkitt;
  padding: 20px;
  position: fixed;
  top: 0;
  left: 0;
  text-transform: uppercase;
  width: 100%;
}
#userPLink {
  position: relative;
}
nav a, #sideMenu {
  margin: 0 10px 0 0;
  text-shadow: 1px 1px 2px #212121;
} 
#userMenuToggle {
  position: absolute;
  right: 0;
}
ul#userMenu {
  background: #202020;
  list-style: none;
  position: absolute;
  top: 40px;
  left: 0;
  padding: 0;
}
#userMenu li {
  display: block;
  padding: 5px 10px;
  text-align: left;
  width: 150px;
}
ul#userMenu li a::after {
  content: attr(title);
}
#userMenu li a:hover, #sideMenuContainer > a:hover {
  padding-left: 3px
}

#scrollingNews {
  color: #fcfcfc;
}

#sideMenu {
  color: #f06060;
  float: right;
  z-index: 5;
}
#sideMenuContainer {
  background: #202020;
  height: 100%;
  padding: 10px;
  position: fixed;
  top: 56px;
  right: -200px;
  width: 200px;
  z-index: 4;
}
#sideMenuContainer h2 {
  color: #fcfcfc;
  font: 16px 'PT Sans', Helvetica, Arial, sans-serif;
  letter-spacing: 2px;
  text-transform: uppercase;
}
#sideMenuContainer > a {
  display: block;
  padding: 5px 10px;
}
#sideMenuContainer > a::after {
  content: attr(title);
  font: 12px 'PT Sans', Helvetica, Arial, sans-serif;
  padding-left: 10px;
  text-transform: uppercase;
}

#logo {
  display: block;
  font: 700 48px Helvetica, Arial, sans-serif;
  letter-spacing: 10px;
  margin: 0 auto;
  text-align: center;
  text-transform: uppercase;
  position: relative;
  top: 100px;
  left: 0;
}
#logo span {
  display: block;
  font-size: 12px;
  letter-spacing: 7.5px;
}

#sourceCode {
  position: absolute;
  top: 50%;
  margin: 0 auto;
}
</style>


</head>

<body>
  <nav>
  <a href="#" id="userPLink">
    <span class="fa fa-user"></span>
    username 
  </a>
  <div id="sideMenu">
    <span class="fa fa-navicon" id="sideMenuClosed"></span>
  </div>
</nav>

<div id="sideMenuContainer">
  <h2>heading</h2>
  <a href="#" title="new user guide"><span class="fa fa-bolt"></span></a>
  <a href="#" title="rules"><span class="fa fa-exclamation-circle"></span></a>
  <a href="#" title="setting"><span class="fa fa-map"></span></a>
  <a href="#" title="usergroups"><span class="fa fa-info-circle"></span></a>
  <a href="#" title="directory"><span class="fa fa-users"></span></a>
  <a href="#" title="claims"><span class="fa fa-camera"></span></a>
  <a href="#" title="summaries"><span class="fa fa-commenting"></span></a>
  <a href="#" title="requests"><span class="fa fa-heart"></span></a>
  <a href="#" title="unanswered"><span class="fa fa-flag"></span></a>
  <a href="#" title="faq / suggestions"><span class="fa fa-question-circle"></span></a>
  <a href="#" title="chat"><span class="fa fa-glass"></span></a>
</div>

<div id="logo" class='colorchange'>
  toggling
  <span>things is oddly satisfying</span>
</div>

<pre><code id='sourceCode'><script type="text/javascript">
$(document).ready(function(){
  $('#sideMenu').sideToggle({
    moving: '#sideMenuContainer',
    direction: 'right'
  });
});
  </script></code></pre>


    <script src="js/index.js"></script>

</body>
</html>
