<!DOCTYPE html>
<html lang="en">
<head>
	
  <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1.0"/>
  <link rel="icon" href="favicon.ico" type="image/x-icon" />  
	<link rel="apple-touch-icon" href="imgs/hello-icon-152.png">   
	<meta name="theme-color" content="white"/>  
	<meta name="apple-mobile-web-app-capable" content="yes">  
	<meta name="apple-mobile-web-app-status-bar-style" content="black"> 
	<meta name="apple-mobile-web-app-title" content="NAMIS DEF"> 
	<meta name="msapplication-TileImage" content="imgs/hello-icon-144.png">  
	<meta name="msapplication-TileColor" content="#FFFFFF">
  <title>NAMIS - CROP DATA COLLECTION FORM</title>

  <link rel="manifest" href="/namispwa.github.io/pwa.webmanifest">
  <!-- CSS  -->
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <link href="css/materialize.css" type="text/css" rel="stylesheet" media="screen,projection"/>
  <link href="css/style.css" type="text/css" rel="stylesheet" media="screen,projection"/>
</head>
<body>

<!--
	<div class="navbar-fixed">
	  <nav class="light-green lighten-1" role="navigation">
		<div class="nav-wrapper container"><a id="logo-container" href="#" class="brand-logo"><img src="imgs/hello-icon-152.png"></a>
		  <ul class="right hide-on-med-and-down">
			<li><a href="#data-entry">Form<i class="material-icons right">assignment</i></a></li>
			<li><a href="#log">Log<i class="material-icons right">view_list</i></a></li>
			
		  </ul>

		  <ul id="nav-mobile" class="sidenav">
			<li><a href="#data-entry">Form<i class="material-icons right">assignment</i></a></li>
			<li><a href="#log">Log<i class="material-icons right">view_list</i></a></li>
		  </ul>
		  <a href="#" data-target="nav-mobile" class="sidenav-trigger"><i class="material-icons">menu</i></a>
		</div>
	  </nav>
	</div>
	
-->

	
		<div class="fixed-action-btn toolbar">
		  <a class="btn-floating btn-large teal lighten-1">
			<i class="large material-icons">menu</i>
		  </a>
		  <ul>
			<li><a href="#data-entry"><i class="material-icons">assignment</i></a></li>
			<li><a href="#log"><i class="material-icons">view_list</i></a></li>
	
		  </ul>
		</div>
			  


<div class="container">
<main role="main" class="app">

  	<div id="log" class="section">
		<div class="row">
			<div class="col s12">
				<a id="showLog" class="btn waves-effect waves-light">Generate Log<i class="material-icons right">list</i>
				</a>
				<a id="prepareLog" class="btn waves-effect waves-light disabled">Process Log<i class="material-icons right">dynamic_feed</i>
				</a>
				 <a id="export" class="btn waves-effect waves-light ">Export<i class="material-icons right">save_alt</i>
				</a>
			 </div>
			<div class="col s12">
				<div id="LogList">

				</div>
			</div>
		</div>
	</div>
   
   
   <div id="data-entry" class="section">

   <div class="row">
    <form id="entry-form" class="col s12">
		<div class="row">
			
		<input class="tooltipped teal lighten-1" data-position="right" data-tooltip="Clear / Start New Entry" type="reset" value="Reset">
		</div>

	
	  <div class="row">
		<div class="input-field col s12">
          <input id="farmer_ID" type="text" class="validate">
          <label for="farmer_ID">Farmer's ID</label>
        </div>
	  
		<div class="input-field col s12">
          <input id="full_name" type="text" class="validate">
          <label for="full_name">Name</label>
        </div>
		<div class="input-field col s12">
			<select id="gender">
			  <option value="" disabled selected>Please Select Gender</option>
			  <option value="M">Male</option>
			  <option value="F">Female</option>
			</select>
		 </div>
	  </div>

      <div class="row">		
		<div class="input-field col s12">
           <input id="farm_visit" type="text" class="datepicker">
		<label for="farm_visit">Date Visited</label>
        </div>
        <div class="input-field col s12">
          <input id="Farmer_Address" type="text" class="validate">
          <label for="Farmer_Address">Farmer Address</label>
        </div>
		<div class="input-field col s12">
          <input id="Farm_location" type="text" class="validate">
          <label for="Farm_location">Farm location</label>
        </div>

      </div>
      <div class="row">
	  		<div class="input-field col s12">
			<select id="cropID">
			  <option value="" disabled selected>Please Select Crop</option>
			  <option value="101">Arrowroot</option>
			  <option value="102">Beans(string)</option>
			  <option value="103">Beets</option>
			  <option value="104">Cabbage</option>
			  <option value="105">Carrot</option>
			  <option value="106">Cassava</option>
			  <option value="107">Cauliflower</option>
			  <option value="108">Chive/Thyme</option>
			  <option value="109">Christophine(chocho)</option>
			  <option value="110">Corn</option>
			  <option value="111">Cucumber</option>
			  <option value="112">Dasheen</option>
			  <option value="125">Sweet Potato</option>
			</select>
		 </div>
        <div class="input-field col s12">
          <input id="Acreage" type="text" class="validate">
          <label for="Acreage">Acreage</label>
        </div>
		<div class="input-field col s12">
          <input id="Exp_Yield" type="text" class="validate">
          <label for="Exp_Yield">Expected Yield</label>
        </div>

      </div>
	  <div class="row">
		<div class="input-field col s12">
           <input id="Date_Planted" type="text" class="datepicker">
		<label for="Date_Planted">Date Planted</label>
        </div>
		<div class="input-field col s12">
           <input id="Exp_Harvest_Date" type="text" class="datepicker">
		<label for="Exp_Harvest_Date">Expected </label>
		</div>
	 </div>
	 
	 
    <div class="row">
      <div id="add-update" class="col s4 offset-s9">
		<button id="addLogButton" class="btn waves-effect waves-light">Submit
			<i class="material-icons right">send</i>
		</button>
	  </div>
    </div>
         
		</form>
  </div>
      </div>
	  
	  
	<div id="the-default-view" class="section no-pad-bot">
		<div class="row center">
		    <div class="container">
			  <br><br>
			  <h1 class="header center orange-text">Welcome</h1>
			  <div class="row center">
				<h5 class="header col s12 light">National Marketing Information System (NAMIS)</br>Farm Data Collection Entry Form</h5>
						<br><br><br><br>
				 <p>Simply enter your full name below to begin.</br></p>

			  </div>

			  <br><br>

			</div>
		
		<form>
			<div class="col s6 offset-s3">
				<div class="input-field col s12">
					 <input id="datacollector" type="text" class="validate">
					 <label for="datacollector">Name</label>
				</div>
			</div>
			<div class="col s6 offset-s3">
				<button id="login" class="btn waves-effect waves-light">Submit
					<i class="material-icons right">send</i>
				</button>
			</div>
		</form>
		</div>
	</div>
	  
</main>
    </div>
	

	
    </br></br>





  <footer>

  </footer>


  <!--  Scripts-->
  <script src="https://code.jquery.com/jquery-2.1.1.min.js"></script>
  <script src="js/materialize.js"></script>
  <script src="js/init.js"></script>
  <script src="js/crops.js"></script>
  
  
  </body>
</html>
