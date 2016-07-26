<template>
  <div id="app">
    <menu></menu>
    <my-header></my-header>
    <slider-header></slider-header>
    <my-footer></my-footer>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Menu from './components/Menu'
import MyHeader from './components/Header'
import MyFooter from './components/Footer'
import SliderHeader from './components/SliderHeader'

export default {
  components: {
    Hello,
    Menu,
    MyHeader,
    MyFooter,
    SliderHeader
  }
}
</script>

<style>
@import './assets/css/colors/color-default.css';
/* Fancy Title */
.fancy-title{ text-transform:uppercase; margin-bottom:40px; }
.fancy-title:after{content: ""; background:#ececec; display: block; height: 1px; margin: 0;  position: relative; width: 100%;}
.fancy-title span:after {content: ""; display: block; height: 5px; margin: 20px 0 -3px;  position: relative; width: 10%; z-index:2;}
.text-center.fancy-title:after{content: ""; background:#ececec; display: block; height: 1px; margin: 0 auto;  position: relative; width: 30%;}
.text-center.fancy-title span:after {content: ""; display: block; height: 5px; margin: 20px auto -3px;  position: relative; width: 10%;}
.text-right.fancy-title:after{content: ""; background:#ececec; display: block; height: 1px; margin: 0 auto;  position: relative; width: 100%;}
.text-right.fancy-title span:after {content: ""; display: block; height: 5px; margin: 20px 0 -3px 90%;  position: relative; width: 10%;}
h5.fancy-title span:after, h6.fancy-title span:after { margin-top:10px !important;}
h5.fancy-title , h6.fancy-title { margin-bottom:20px !important;}
@media (min-width:350px) and (max-width: 400px)  {
 #Myh2 {margin-left: -12px;}
}
@media only screen and (max-width: 350px) {
 #Myh2 {font-size:40px;}
}

/*typography*/
p{font-family: 'Raleway', sans-serif;}
h1, h2, h3 { color:#32313b; font-family: 'Raleway', sans-serif;  font-style: normal; font-weight: 300; text-rendering: optimizelegibility;}
h4, h5, h6 { color:#32313b; font-family: 'Raleway', sans-serif;  font-style: normal; font-weight: 600; text-rendering: optimizelegibility;}
h1 {font-size: 58px; margin-top: 0;}
h2 {font-size: 48px; margin-top: 0;}
h3 {font-size: 36px; margin-top: 0;}
h4 {font-size: 22px; margin-top: 0;}
h5 {font-size: 16px; margin-top: 0;}
h6 { margin-top: 0;}
h1 small, h2 small, h3 small, h4 small, h5 small, h6 small, .h1 small, .h2 small, .h3 small, .h4 small, .h5 small, .h6 small, h1 .small, h2 .small, h3 .small, h4 .small, h5 .small, h6 .small, .h1 .small, .h2 .small, .h3 .small, .h4 .small, .h5 .small, .h6 .small { color: #778899; font-weight:300;}
p {font-size:14px; font-weight: 300; line-height:1.8;  margin-bottom: 20px; text-rendering: optimizelegibility;}
/* global style*/
body {background-color: #fff; color: #778899;font-family: 'Raleway', sans-serif; text-rendering: optimizelegibility; }

a { -webkit-transition: all 0.3s ease-in-out;  -moz-transition: all 0.3s ease-in-out;  -o-transition: all 0.3s ease-in-out; -ms-transition: all 0.3s ease-in-out; transition: all 0.3s ease-in-out;}
a:hover, a:focus { text-decoration:none;}
a:focus, a:active, button::-moz-focus-inner, input[type="reset"]::-moz-focus-inner, input[type="button"]::-moz-focus-inner, input[type="submit"]::-moz-focus-inner,
select::-moz-focus-inner, input[type="file"] > input[type="button"]::-moz-focus-inner {border: 0;outline : none !important;}
.btn {  -webkit-transition: all 0.3s ease-in-out;
    -moz-transition: all 0.3s ease-in-out;
    -o-transition: all 0.3s ease-in-out;
  -ms-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
  -webkit-transform: translate3d(0,0,0);}

/*========== Main Wrapper Header ==========*/
.main-wrapper-header { padding:50px 0; background:#f8f8f8; border-bottom:1px solid #ececec;}
.main-wrapper-header .page-title {}
.main-wrapper-header .page-title h1, .page-title h2, .page-title h3 { margin:0; font-size:28px;line-height:2;}

.main-wrapper-header .breadcrumbs-wrapper { text-align:right;}
.main-wrapper-header .breadcrumbs-wrapper .breadcrumb { margin:0; line-height:2.8; background:none; padding: 8px 0;}
.main-wrapper-header .breadcrumbs-wrapper .breadcrumb li { float:none; width:auto;}
.main-wrapper-header .breadcrumbs-wrapper .breadcrumb > li + li:before {content: "\f138";font-family: 'FontAwesome'; padding: 0 8px;}
.main-wrapper-header .breadcrumbs-wrapper .breadcrumb > .active {color: #32313b;}


/* Fancy Header*/
.fancy-header {}
.fancy-header .page-title h1,.fancy-header .page-title h2, .fancy-header .page-title h3 { font-size:48px; line-height:1.2; text-align:center;}
.fancy-header .breadcrumbs-wrapper { text-align:center;}

/* Dark Header */
.dark-header .page-title h1,.dark-header .page-title h2, .dark-header .page-title h3{ color:#ffffff;}
.dark-header .breadcrumbs-wrapper .breadcrumb > li + li:before { color:#ffffff !important;}
.dark-header .breadcrumbs-wrapper .breadcrumb > li a { color:#ffffff;}
.dark-header .breadcrumbs-wrapper .breadcrumb > li a:hover { border-bottom:1px solid #ffffff;}
.dark-header .breadcrumbs-wrapper .breadcrumb > .active { color:#ffffff;}

/* Background Overlay*/

.parallax{ background-position:50% 50%; background-repeat: no-repeat; position:relative; 
    -webkit-background-size: cover !important; /* For WebKit*/
    -moz-background-size: cover !important;    /* Mozilla*/
    -o-background-size: cover !important;      /* Opera*/
    background-size: cover !important;         /* Generic*/  }
  
@media only screen and (max-width: 768px) {
.parallax{ background-position:50% 50% !important; background-attachment: scroll; }
} 
.bg-overlay{display: block;height: 100%; position: absolute; top:0; width: 100%; z-index:0;-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=60)"; /* Safari 1.x */ -khtml-opacity: 0.6; /* Modern browsers */opacity: 0.6;}
.bg-overlay-solid{-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=100)"; /* Safari 1.x */ -khtml-opacity: 1; /* Modern browsers */opacity: 1;}
.bg-overlay.bg-overlay-light{background:#f4f4f4;}
.bg-overlay.bg-overlay-glight{
background: -moz-radial-gradient(center, ellipse cover,  rgba(255,255,255,0.3) 0%, rgba(255,255,255,0.6) 50%, rgba(255,255,255,1) 100%); /* FF3.6+ */
background: -webkit-gradient(radial, center center, 0px, center center, 100%, color-stop(0%,rgba(255,255,255,0.3)), color-stop(50%,rgba(255,255,255,0.6)), color-stop(100%,rgba(255,255,255,1))); /* Chrome,Safari4+ */
background: -webkit-radial-gradient(center, ellipse cover,  rgba(255,255,255,0.3) 0%,rgba(255,255,255,0.6) 50%,rgba(255,255,255,1) 100%); /* Chrome10+,Safari5.1+ */
background: -o-radial-gradient(center, ellipse cover,  rgba(255,255,255,0.3) 0%,rgba(255,255,255,0.6) 50%,rgba(255,255,255,1) 100%); /* Opera 12+ */
background: -ms-radial-gradient(center, ellipse cover,  rgba(255,255,255,0.3) 0%,rgba(255,255,255,0.6) 50%,rgba(255,255,255,1) 100%); /* IE10+ */
background: radial-gradient(ellipse at center,  rgba(255,255,255,0.3) 0%,rgba(255,255,255,0.6) 50%,rgba(255,255,255,1) 100%); /* W3C */
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#4dffffff', endColorstr='#ffffff',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */

-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=100)"; /* Safari 1.x */ -khtml-opacity: 1; /* Modern browsers */opacity: 1;
}
.bg-overlay.bg-overlay-dark{background:#000;}
.bg-overlay.bg-overlay-gdark{
background: -moz-radial-gradient(center, ellipse cover,  rgba(37,36,44,0.5) 0%, rgba(37,36,44,0.75) 50%, rgba(0,0,0,1) 100%); /* FF3.6+ */
background: -webkit-gradient(radial, center center, 0px, center center, 100%, color-stop(0%,rgba(37,36,44,0.5)), color-stop(50%,rgba(37,36,44,0.75)), color-stop(100%,rgba(0,0,0,1))); /* Chrome,Safari4+ */
background: -webkit-radial-gradient(center, ellipse cover,  rgba(37,36,44,0.5) 0%,rgba(37,36,44,0.75) 50%,rgba(0,0,0,1) 100%); /* Chrome10+,Safari5.1+ */
background: -o-radial-gradient(center, ellipse cover,  rgba(37,36,44,0.5) 0%,rgba(37,36,44,0.75) 50%,rgba(0,0,0,1) 100%); /* Opera 12+ */
background: -ms-radial-gradient(center, ellipse cover,  rgba(37,36,44,0.5) 0%,rgba(37,36,44,0.75) 50%,rgba(0,0,0,1) 100%); /* IE10+ */
background: radial-gradient(ellipse at center,  rgba(37,36,44,0.5) 0%,rgba(37,36,44,0.75) 50%,rgba(0,0,0,1) 100%); /* W3C */
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#8025242c', endColorstr='#000000',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */
-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=100)"; /* Safari 1.x */ -khtml-opacity: 1; /* Modern browsers */opacity: 1;
}
</style>
