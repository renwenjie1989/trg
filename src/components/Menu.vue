<template>
	<div class="container">
		<div class="main-navigation">
        	<div class="row">
                <div class="col-md-12 columns">
					<nav class="navbar navbar-default gfx-mega nav-left" role="navigation">
						<div class="navbar-header">
							<a class="navbar-toggle" data-toggle="collapse" data-target="#gfx-collapse"></a>
            				<div class="logo" id="logo">
           	    				<a href="index.html">
           	    					<!-- <img v-attr="src: logoUrl"> -->
           	    					<img src="../assets/trg.png">
           	    				</a>
                			</div>
						</div>

						<div class="collapse navbar-collapse" id="gfx-collapse">
							<ul class="nav navbar-nav gfx-nav">
								<li><a href="index.html">Home</a></li>
								<li class="dropdown" v-bind:class="{'open': isDropdown}"><a v-on:click="drop" href="#" data-toggle="dropdown" class="dropdown-toggle">Services <b class="caret"></b></a>
									<ul class="dropdown-menu">
										<li><a href="web-development.html">Web Development</a></li>
										<li><a href="fraud-prevention.html">Fraud Prevention</a></li>
										<li><a href="it-solutions.html">IT Solutions</a></li>
										<li><a href="mobile-apps.html">Mobile Apps</a></li>
										<li><a href="hardware.html">Hardware</a></li>
										<li><a href="xyz.html">XyZ </a></li>
									</ul>
								</li>
								<li><a href="blog.html">Blog</a></li>
								<li><a href="about-us.html">About</a></li>
								<li><a href="faq.html">FAQ</a></li>
								<li><a href="careers.html">Careers</a></li>
								<li><a href="contact.php">Contact</a></li>
							</ul>
						</div><!-- /.navbar-collapse -->
					</nav>
                </div>
            </div>              
		</div>
	</div>
</template>

<script>
export default {
	data () {
		return {
			isDropdown: false,
			logoUrl: "trg.png"
		}
	},
	methods: {
		drop: function (){
			alert("haha");
			isDropdown = true;
		}
	}
}
</script>

<style scoped>

.navbar-header{float:none;}
.nav-right .navbar-header{float:right;}
.nav-left .navbar-header{float:left;}
.nav-left .gfx-nav{float:right;}
.nav-centered .navbar-header{float:none; text-align:center;}
.nav-centered .nav > li { display:inline-block;}
.nav-centered .navbar-nav > li { float:none;}
.nav-centered .gfx-nav{ width:100%; text-align:center;}

@media (min-width: 768px) and (max-width: 991px) {
.nav > li > a { padding-left:9px; padding-right:9px;}
.navbar-nav > li > a {line-height: 76px;}
}
@media screen and (max-width: 767px) {
.nav-right .navbar-header{float:none; width:100%; text-align:right;}
.nav-left .navbar-header{float:none; width:100%; text-align:left;}
.nav-right .navbar-toggle { left:0;}
.nav-left .navbar-toggle { right:0;}
.nav-left .gfx-nav{float:none;}

}

.navbar, .navbar-nav{ margin:0; min-height:inherit;}
.navbar-collapse{ max-height:inherit; padding:0;}
.navbar-default{ background:none; border:none;}
.navbar-default .navbar-nav > li > a {color: #32313b; border-top:3px solid transparent; font-family: 'Raleway', sans-serif; font-size: 12px; font-weight: 500; text-transform:uppercase; text-decoration: none; letter-spacing:1px;}
.navbar-default .navbar-nav > .active > a, .navbar-default .navbar-nav > .active > a:hover, .navbar-default .navbar-nav > .active > a:focus { background:none;}
.nav .open > a, .nav .open > a:hover, .nav .open > a:focus {background-color: transparent;}
.navbar-default .navbar-nav > .active > a, .navbar-default .navbar-nav > .active > a:hover, .navbar-default .navbar-nav > .active > a:focus{ border-top:3px solid;}
.navbar-default .navbar-nav > li > a:hover, .navbar-default .navbar-nav > li > a:focus{text-decoration: none; background-color: none; }
.navbar-default .navbar-nav > .open > a, .navbar-default .navbar-nav > .open > a:hover, .navbar-default .navbar-nav > .open > a:focus { background: none; color: #32313b;}

.navbar-toggle {position: absolute; cursor:pointer; top:30px; width:48px; height:48px; font-size:18px; float: none; text-align:center; right:0;  margin: 0;  padding: 9px 10px; background-color: #32313b; color:#fff;  border: none; border-radius: 0;}
.navbar-toggle:focus {outline: none;}
.navbar-toggle:after {content:'\f0c9'; font-family:FontAwesome;}



@media (min-width: 992px) {
  .navbar-nav > li > a {padding: 9px 16px 12px; line-height:76px; }  
  .header-main.shrink .navbar-nav > li > a { line-height:41px;  -webkit-transition: all 0.3s ease-in-out; -moz-transition: all 0.3s ease-in-out; -o-transition: all 0.3s ease-in-out; transition: all 0.3s ease-in-out;}
  .navbar-nav > li > a:hover,.navbar-nav > li > a:focus {}
  .navbar-nav > li > a.current::before, .navbar-nav > li > a.current::after, .navbar-nav > li > a:hover::before, .navbar-nav > li > a:focus::before, .navbar-nav > li > a:hover::after, .navbar-nav > li > a:focus::after, .navbar-nav > li > a.highlighted:before, .navbar-nav > li > a.highlighted:after{opacity: 1; -webkit-transform: translateY(0px);
 -moz-transform: translateY(0px); transform: translateY(0px);}
}

/* Mega Menu */
.gfx-mega .nav,
.gfx-mega .collapse,
.gfx-mega .dropup,
.gfx-mega .dropdown {
  position: static;
}
.gfx-mega .container {position: relative;}
.gfx-mega .dropdown-menu {left: auto;}
.gfx-mega .nav.navbar-right .dropdown-menu {left: auto; right: 0;}
.gfx-mega .gfx-mega-content { padding:0px 15px;}
.gfx-mega .dropdown.gfx-mega-fw .dropdown-menu {left: 0; right: 0;}

/* Mega Menu Elements styling*/
/* lists */
.mega-menu-list{ list-style: none; margin:0; padding:0;}
.mega-menu-list > li {font-size: 11px; font-weight: 600;  text-transform: uppercase;}
.mega-menu-list > li > a {color: #32313b; display:block;padding: 10px;}
.mega-menu-list > li.active > a {color:#ffffff !important;}
.mega-menu-list > li > a:hover, .mega-menu-list > li > a:focus{background:#f2f2f2;}
.mega-menu-list .title-header{ color:#778899; font-size:13px; margin-bottom:10px; display:block;}
.gfx-nav h1, .gfx-nav h2, .gfx-nav h3, .gfx-nav h4, .gfx-nav h5, .gfx-nav h6{color:#778899; padding:10px 0;}


/* dropdowns */
.dropdown-menu { background:#ffffff; padding:15px 0; border:none; -webkit-box-shadow: 0px 3px 0px 0px rgba(214, 224, 230, 0.6); -moz-box-shadow:  0px 3px 0px 0px rgba(214, 224, 230, 0.6); box-shadow:  0px 3px 0px 0px rgba(214, 224, 230, 0.6);}
.dropdown-menu > li > a {color: #333; font-size: 11px; font-weight: 600; text-transform: uppercase;padding:10px 20px;}
.dropdown-menu .divider{ background:#ececec;}
.dropdown-menu > .active > a, .dropdown-menu > .active > a:hover, .dropdown-menu > .active > a:focus {}
.dropdown-menu > li > a:hover, .dropdown-menu > li > a:focus { background-color: #f2f2f2;}

/* logo */
.logo{ line-height:100px;-webkit-transition: all 0.3s ease-in-out; -moz-transition: all 0.3s ease-in-out; -o-transition: all 0.3s ease-in-out; transition: all 0.3s ease-in-out;}
.logo img{-webkit-transition: all 0.3s ease-in-out;-moz-transition: all 0.3s ease-in-out;-o-transition: all 0.3s ease-in-out;transition: all 0.3s ease-in-out;}
</style>