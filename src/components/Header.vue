<template>
    <div class="main-wrapper-header fancy-header dark-header parallax parallax-about" data-stellar-background-ratio="0.4">
        <div class="bg-overlay bg-overlay-gdark"></div>
			<div class="container">
			<div class="row">
            	<div class="col-sm-12 columns">
            		<div class="page-title">
                		<h2>About Us</h2>                    
                	</div>
                	<div class="breadcrumbs-wrapper">               
						<ol class="breadcrumb">
								<li><a href="#">Home</a></li>
							<li class="active">About Us</li>
						</ol>
            		</div>
				</div>
			</div>
		</div>
    </div>       
</template>

<script>
	
</script>

<style scoped>

/*========== Header Wrapper ==========*/	

.header-wrapper{position: relative;}

/*header top*/
.header-top{ background:#fff; border-bottom:1px solid #ececec; color: #555566; font-size:12px; position:relative; z-index:1150; }
.header-top ul, .header-top ol, .header-top dl{font-weight:500; font-size:12px; margin-bottom:0;}
.header-top ul .fa{ margin-right: 10px;}
.header-top p{margin:0;}
.header-top-left{ float:left; width:100%;}
.header-top-right{ float:right; width:100%;}

/*header top navigation */
.top-menu {list-style:none; padding-left:0; float:right;}
.top-menu li:first-child { border-left:1px solid #ececec;}
.top-menu li { border-right:1px solid #ececec; display:inline-block;}
.top-menu li a{ color:inherit; padding:10px 12px; display:block;}
.header-top .dropdown:hover .dropdown-menu {display: block;}
.header-top .dropdown-menu{ border:1px solid #ececec; margin-top:0px; margin-left:-4px;}
.header-top .dropdown-menu > li{ display:block; border:none;}


/* social top */
.social-top{ list-style:none; padding-left:0; float:left;}
.social-top li:first-child { border-left:1px solid #ececec;}
.social-top li { border-right:1px solid #ececec; display:inline-block;}
.social-top li a{ color:inherit; padding:8px 12px; display:block; font-size:14px;}
.social-top a:hover, .social-top a:focus { text-decoration:none;}
.social-top .fa{ margin-right:0 !important;}

.top-menu a{ color: inherit;}
.top-menu a:hover, .top-menu a:focus {text-decoration:none;}
/*header main*/
.header-main{width:100%; position:relative; z-index:1100; background:#FFF; -webkit-box-shadow: 0px 3px 0px 0px rgba(214, 224, 230, 0.6); -moz-box-shadow: 0px 3px 0px 0px rgba(214, 224, 230, 0.6); box-shadow:  0px 3px 0px 0px rgba(214, 224, 230, 0.6); -webkit-transform: translateZ(0);}
.main-navigation{ position:relative;}
.logo{ line-height:100px;-webkit-transition: all 0.3s ease-in-out; -moz-transition: all 0.3s ease-in-out; -o-transition: all 0.3s ease-in-out; transition: all 0.3s ease-in-out;}
.logo img{-webkit-transition: all 0.3s ease-in-out;-moz-transition: all 0.3s ease-in-out;-o-transition: all 0.3s ease-in-out;transition: all 0.3s ease-in-out;}
.header-main.shrink .logo{ line-height:60px; -webkit-transition: all 1s ease-in-out; -moz-transition: all 0.3s ease-in-out; -o-transition: all 0.3s ease-in-out; transition: all 0.3s ease-in-out;}
.header-main.shrink .logo img{-webkit-transform:scale(0.8); -moz-transform:scale(0.8); -o-transform: scale(0.8); -ms-transform: scale(0.8); transform: scale(0.8);}

@media (max-width: 767px) {
	
.header-top-left{padding:0px;}
.social-top{ text-align:center; float:none;}
.top-menu{ float:none; text-align:center;}
.top-menu li { border-top:1px solid #ececec;}

.logo {line-height: 105px !important;}
.gfx-nav { float:none;}
.header-main.shrink .gfx-nav a { line-height:1.4;}
.header-main {
    position: relative !important;
}

.main-wrapper-header .breadcrumbs-wrapper { text-align:left;}
.fancy-header .breadcrumbs-wrapper { text-align:center;}

ul.gallery {margin-left: 0;}
ul.gallery li {width: 50% !important; /* this value + 2% should = 50% */}
}



.parallax-about { background-image:url(../assets/images/parallax-about.jpg);}


</style>