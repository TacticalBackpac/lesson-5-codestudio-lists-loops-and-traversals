// get data as lists from the dataset and store in variables
var dogNames = getColumn("Dogs", "Name");
var dogHeight = getColumn("Dogs", "Maximum Height");
var dogImages = getColumn("Dogs", "Image");

// set up blank lists to store the filtered lists
var filteredDogNames = [];
var filteredDogImages = [];

// filter the lists and sets up the screen
listSetup();

// when the dropdown is changed, filter the lists and set up the screen
onEvent("sizeDropdown", "change", function(){
  listSetup();
});

// filters the lists, based on the value in the dropdown
// if the dog height is under a certain amount and the dropdown matches a value
// the corresponding name and image will be stored in the filtered lists. 
function filter(){
  // clears the filtered lists
  filteredDogNames = [];
  filteredDogImages = [];
  
  // gets the size from the dropdown
  var dogSize = getText("sizeDropdown");
  
  // traverses the dogHeight List
  // if dogHeight and dogSize meet certain conditions
  // the corresponding names and images are stored in the filtered lists
  for(var i=0; i<dogHeight.length; i++){
    if(dogHeight[i] < 16 && dogSize == "Small"){
      appendItem(filteredDogNames, dogNames[i]);
      appendItem(filteredDogImages, dogImages[i]);
    } else if(dogHeight[i] >= 16 && dogHeight[i] < 24 && dogSize == "Medium"){
      appendItem(filteredDogNames, dogNames[i]);
      appendItem(filteredDogImages, dogImages[i]);
    } else if(dogHeight[i] >= 24 && dogSize == "Large") {
      appendItem(filteredDogNames, dogNames[i]);
      appendItem(filteredDogImages, dogImages[i]);
    } 
  }
  
  // prints the list of dog names that match the value in the dropdown
  console.log(dogSize + " Dogs:\n" + filteredDogNames);
}

// sets up the screen elements
function updateScreen(){
  var randomIndex = randomNumber(0, filteredDogNames.length-1);
  setText("nameOutput", filteredDogNames[randomIndex]);
  setImageURL("picture", filteredDogImages[randomIndex]);
}

// sets up the lists and the screen
function listSetup(){
  filter();
  updateScreen();
}
