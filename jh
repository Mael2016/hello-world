<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Demineur</title>
<link rel="stylesheet " href ="CSS/monStyle.css"/>
</head>

<body>

<script>

/**************************************************************************
   Description du programme : Demineur
  
   Auteur: Mael Gador
   
   Date: 11/02/16
****************************************************************************/

var TabDemineur= new Array (19);
var TabScore= new Array (4);
var NbClique=0, PointManche=0, PointTot=0;

/*J'ai fais ce que j'ai pu*/

function btnJouer_onclick ()
{
    var PositionMine=0;
 
	for (var i=1; i<TabDemineur.length; i++)
	{
      	TabDemineur[i] =0 ;
	}  
    
    PositionMine= getRand(1,18);
    TabDemineur[PositionMine]= 1;
    TabScore[0]= 5;
    TabScore[1]= 10;
    TabScore[2]= 15;
    TabScore[3]= 25 ;

getEl("btnJouer").style.visibility="hidden";
}

function getRand (Min, Max)
{
	return Math.floor(Math.random()*(Max-Min+1)+Min);
}

function validerPosition (NoCase)
{
   if( TabDemineur[NoCase] == 0 ) //pas de mine
   {
   	getEl("imgC"+NoCase).src= "img/chance.jpg";

      if (NbClique<3)
      {
        PointManche+= TabScore[NbClique];
        NbClique++
      }
      else 
      {
        PointManche+= TabScore[3];
      }

        if (NbClique==1)
        {
   		    getEl("lblMessage").innerHTML="Et de une!";
        }
        else if(NbClique==2)
        {
   		    getEl("lblMessage").innerHTML="Tu es sur une lancée";
        }
        else if(NbClique==3)
        {
   		    getEl("lblMessage").innerHTML="Un peu de chance, c'est toujours bon";
        }
        else  
        {
   		    getEl("lblMessage").innerHTML="Ton nom est: Le démineur";
        }

    }     

   else
   {
    getEl("imgC"+NoCase).src= "img/mines.jpg";
    getEl("lblMessage").innerHTML="Préparation de la manche suivante ! ";
    calculerTot ();
   }

  
getEl("lblPtsManche").innerHTML=PointManche;

}

function calculerTot () 
{
    PointTot=PointManche;
    getEl("lblPtsTotal").innerHTML+=PointTot;
    document.getElementById("imgC"+NoCase).disabled = true;
}



function getEl( El )
{
	return document.getElementById( El );
}

</script>

<header>
<img id="logo" src="img\logo.png"> 
</header>


<section id=main>
<aside class=textColor>
Point manche <br> <label id="lblPtsManche"> 0 </label> <br>
Point total <br> <label id="lblPtsTotal"> 0 </label> <br>
Nombre de Mine(s) <br><input type="text" id="txtNbMine" name="txtNbMine"><br>
<img id="btnJouer" src="img\btnJouer.png" onclick="btnJouer_onclick()"> <br>
<label id="lblMessage">Message Ici</label><br>
<label id="lblMessageMine">Message Mine Ici</label>

</aside>
<section id="imgSection" >
	<img class="imgHolder" id="imgC1" name="imgC1" src="img\inactif.png" onclick="return validerPosition(1)">
	<img class="imgHolder" id="imgC2" name="imgC2" src="img\inactif.png" onclick="return validerPosition(2)">
	<img class="imgHolder" id="imgC3" name="imgC3" src="img\inactif.png" onclick="return validerPosition(3)">
	<img class="imgHolder"  id="imgC4" name="imgC4" src="img\inactif.png" onclick="return validerPosition(4)">
	<img class="imgHolder"  id="imgC5" name="imgC5" src="img\inactif.png" onclick="return validerPosition(5)">
	<img class="imgHolder"  id="imgC6" name="imgC6" src="img\inactif.png" onclick="return validerPosition(6)">
	</br>
	<img class="imgHolder" id="imgC7" name="imgC7" src="img\inactif.png" onclick="return validerPosition(7)">
	<img class="imgHolder" id="imgC8" name="imgC8" src="img\inactif.png" onclick="return validerPosition(8)">
	<img class="imgHolder" id="imgC9" name="imgC9" src="img\inactif.png" onclick="return validerPosition(9)">
	<img class="imgHolder" id="imgC10" name="imgC10" src="img\inactif.png" onclick="return validerPosition(10)">
	<img class="imgHolder" id="imgC11" name="imgC11" src="img\inactif.png" onclick="return validerPosition(11)">
	<img class="imgHolder" id="imgC12" name="imgC12" src="img\inactif.png" onclick="return validerPosition(12)">
	</br>
	<img class="imgHolder" id="imgC13" name="imgC13" src="img\inactif.png" onclick="return validerPosition(13)">
	<img class="imgHolder" id="imgC14" name="imgC14" src="img\inactif.png" onclick="return validerPosition(14)">
	<img class="imgHolder" id="imgC15" name="imgC15" src="img\inactif.png" onclick="return validerPosition(15)">
	<img class="imgHolder" id="imgC16" name="imgC16" src="img\inactif.png" onclick="return validerPosition(16)">
	<img class="imgHolder" id="imgC17" name="imgC17" src="img\inactif.png" onclick="return validerPosition(17)">
	<img class="imgHolder" id="imgC18" name="imgC18" src="img\inactif.png" onclick="return validerPosition(18)">
	</br>
</section>
	

</section>

<!-- Insert HTML here -->
 </body>
 </html>
