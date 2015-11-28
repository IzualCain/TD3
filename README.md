# TD3

```HTML
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
        <style type="text/css">
        	html{
        		background-color: #D3D3D3;
        	}

        	#global{
        		background-color: white;
        		height: 100%;
        		width: 60%;
        		margin-left: 20%;
        		margin-right: 20%;
        		border-radius: 0px 0px 10px 10px;
        		border-style: solid;
        		border-color: grey;
        		border-width: 1px;
        	}

        	body{
        		margin-top: -1px;
        	}

        	header{
        		float: center;
        		margin-left: 5px;
        		margin-top: 15px;
        		height: 120px;
        	}

        	#logo{
        		width: 200px;
        		float: left;
        	}

        	#contacter{
        		float: right;
        		color: lightgrey;
        		text-align: right;
        		margin-right: 10px;
        	}

        	#barremenu{
        		width: 100%;
        		display: inline-block;
        		margin-top: -20px;
        		margin-bottom: 15px;
        	}

        	
			#menu{
				padding-left: 0px;
				display: inline-block;
				width: 99.8%;
				border-style: solid;
				border-color: lightgrey;
			    border-width: 1px;
			}



			#menu li:hover{
				background-color: #00FF00;
			}
			 
			#menu li{
				margin-top: -1px;
				margin-left: -1px;
				margin-bottom: -1px;
				float : left;
			    display: inline-block;
			    border-style: solid;
			    border-color: lightgrey;
			    border-width: 1px;
			    border-spacing: 13px;
			    padding: 10px;
			}

			#menu li a{
				text-decoration: none;
				color: black;
				text-transform: uppercase;
				font-weight: bold;
			}

			section{
				margin-top: 20px;
				margin-left: 5px;
				height: 500px;
			}

			#photos{
				margin: 5px;
				width: auto;
				height: auto;
				max-width: 98%;
				max-height: 98%;
			}

			/*article{
				float: left;
				width: 68%;
				height: 475px;
				border-style: solid;
				border-width: 1px;
				border-color: lightgrey;
			}*/

			aside{
				width: 24%;
				border-style: solid;
				border-width: 1px;
				border-color: lightgrey;
				float: right;
				margin-right: 20px;
			}

			footer{
				background-color: #373737;
				text-align: center;
				margin-bottom: -16px;
        		border-radius: 0px 0px 10px 10px;
        		height: 80px;
			}

			#listeCommandes{
				color: lightgrey;
			}

			#droits{
				color: white;
			}

        </style>
		
		
		<title>Folio</title>
	</head>
	<div id="global">
		<header>
			<div id="banniere">
				<p id="contacter">
					Pour nous contacter,<br>
					Tél : <b>04.93.xx.xx.xx</b><br>
					Email : <b>contact@folio.com</b>
				</p>
			</div>
			<!-- <img id="logo" src="img/logo.png" alt="Logo DAM" /> -->
			<div id="barremenu">
	            <ul id="menu">
	                <li><a href="#" id="menu_accueil">Accueil</a></li>
	                <li><a href="#" id="menu_blog">Panier</a></li>
	                <li><a href="#" id="menu_contact">Contact</a></li>
	            </ul>
	        </div>
		</header>
		<body>
			<section>
				<article>
					<!-- <img id="photos" src="Photos/photo_1.jpg" alt="Photo a vendre" /> -->

					<label for="Ville">Ville :</label>
					<input id="ville" type="text" name="Ville" />
					<br/><br/>
					<input type="button" onclick="ReloadVille()" value="Valider" />
					<br/><br/>
					<IFRAME id="meteoVille" src="" width=150 height=150> </IFRAME>
					<script>
						
						function  ReloadVille() {
							var villeif;
							villeif = document.getElementById('ville').value;
							/*setInterval(function(){
								document.getElementById('meteoVille').contentWindow.reload();
							}, 1000);*/
							document.getElementById('meteoVille').src = "http://api.openweathermap.org/data/2.5/weather?q="+villeif+"&mode=html&appid=2de143494c0b295cca9337e1e96b00e0";
						}
						
			
		
					</script>
				</article>
				<aside>
				</aside>
			</section>
		</body>
		<footer>
			<a href="#" id="listeCommandes">Accéder à la liste des commandes</a>
			<p id="droits">(c) LP DAM - 2013</p>
		</footer>
	</div>
</html>
```
