// List of icons to randomly choose between
var iconsList = ["icon://fa-heart", 
                 "icon://fa-music", 
                 "icon://fa-smile-o", 
                 "icon://fa-globe", 
                 "icon://fa-tree", 
                 "icon://fa-bolt", 
                 "icon://fa-moon-o",
                 "icon://fa-star"];

//change background color of home screen
setProperty("homeScreen", "background-color", rgb(randomNumber(0,255),randomNumber(0,255),randomNumber(0,255)));

//create random number to load up an icon image
var randNum = randomNumber(0, iconsList.length-1); 

//display icons randomly on screen to start
for (var i=0; i < 20; i++){
	//set random location (x & y)
  setProperty("icon"+i, "x", randomNumber(0,320));
  setProperty("icon"+i, "y", randomNumber(0,320));
	//set random size (width & height)
  setProperty("icon"+i, "width", randomNumber(0,320));
  setProperty("icon"+i, "height", randomNumber(0,320));
	//set random color
  setProperty("icon"+i, "icon-color", rgb(randomNumber(0,255),randomNumber(0,255),randomNumber(0,255)));
	//load up a random icon image  
	setProperty("icon"+i, "image", iconsList[randNum]);
}


//change colors
onEvent("colorsButton", "click", function( ) {
    setProperty("homeScreen", "background-color", rgb(randomNumber(0,255),randomNumber(0,255),randomNumber(0,255)));
	for (var i=0; i<20; i++){
    setProperty("icon"+i, "icon-color", rgb(randomNumber(0,255),randomNumber(0,255),randomNumber(0,255)));
  }
});

//change locations
onEvent("locationsButton", "click", function( ) {
  for (var i=0; i<20; i++){
    setProperty("icon"+i, "x", randomNumber(0,320));
    setProperty("icon"+i, "y", randomNumber(0,320));
  }
});

//change shapes
onEvent("shapesButton", "click", function( ) {
  var randNum2 = randomNumber(0, iconsList.length-1); 
  for (var i=0; i<20; i++){
    setProperty("icon"+i, "image", iconsList[randNum2]);
  }
});
