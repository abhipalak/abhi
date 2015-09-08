
 // Example unit test function
     function divide( a, b ) {
        // To see the test pass, uncomment the following line
        //return a / b;
     }

     // Write a function that takes a single argument (a string) and returns the string reversed.
     function reverseString(str) {
        
		return str.split('').reverse().join('');
		
     }

     // Write a function that takes an array of numbers and returns the minimum value
     function findMinValue(values) {
        
		return Math.min.apply( Math, values );
		
     }

     // Write a function that takes an array and returns the distinct values only (i.e. removes duplicates)
     function findDistinctValues(values) {
         
		 return names.slice().sort(function(a,b){return a > b})
		 .reduce(function(a,b){if (a.slice(-1)[0] !== b) a.push(b);return a;},[]);
		 
     }

     // Write a function that logs the numbers from 1 to 100 to the console.
     // For multiples of three print "Fizz" instead of the number.
     // For multiples of five print "Buzz".
     // For numbers which are multiples of both three and five print "FizzBuzz".
     function doFizzBuzz() {
       
	   for (var x=1; x <= 100; x++){
    if( x % 3 && x % 5 ) {
        console.log("FizzBuzz");
    } else {
        if( x % 3 == 0 ) {
            console.log("Fizz");
        }
        if( x % 5 == 0 ) {
            console.log("Buzz");
        }
    }
  
}​
	   
	   
     }

     // You have a master array of strings, where each element is a fruit name.
     // You have a second array of fruit name strings, that is a list of fruits that should be removed from the fruits specified in the master array.
     // For the purpose of the exercise, we will call the master array fruits and the second array fruitsToRemove.
     // Write the function that will remove the values contained in fruitsToRemove from the array fruits.
     function removeFruits(fruits, fruitsToRemove) {
       
	   for(var i = fruits.length-1; i--){
	   
		 for (var j = 0; j < fruitsToRemove.length; j++) {
		 
				if (fruits[i] === fruitsToRemove[j]) fruits.splice(i, 1);
		 
		 }
	   
	   }
	   
	   
     }

     // Write a function to push either a simple value or an array of values onto a specified array.
     // For the purpose of the exercise, we will call the target array simply array and the stuff to push onto it (either a simple value or array) simply toPush.
     // If toPush is a simple value, it should be pushed onto array as an element.
     // If toPush is an array, all of its elements should be pushed onto array. Your solution should modify array (ie. not return a new array).
     function pushOntoArray(array, toPush) {
        
		  var s = typeof toPush;
		  
		    if (s === 'object') {
			
				if (toPush) {
				
					if (toPush instanceof Array) {
						
						array.concat(array);
						
					}
					
					else {
					
						array.push(toPush);
					
					}
			
			} 
			
			}
		
     }

     // Given a string, sourceStr, write some code that will split this string using comma as your delimiter, and producing an empty array if the string is empty.
     function splitListStrUsingComma(sourceStr) {
         
		 if(sourceStr.length==0) {
		 
		 return [];
		 
		 }
		 
		 else {
		 
		 var res = sourceStr.split(",");
		 
		 }
     }

     // Write a function that will take any number of arguments and return their sum
     function sum() {
        
		var sum = 0;
		
		  for(var i = 0; i < arguments.length; i++) {
		  
				sum += arguments[i];
		  
		  }
		  
		  return sum;
		
		
     }

     // Write a function that will return true if a specified string consists of only whitespace.
     function isOnlyWhitespace(sourceStr) {
        
		boolean containsSpace = false;
		
		if (/\s/.test(sourceStr)) {
		
		containsSpace = true;
		
		}
		
		return containsSpace;
		
     }

     // write an example of a javascript closure
	 
	 function showName (firstName, lastName) {
		
		​var nameIntro = "Your name is ";
		
		function makeFullName () {  
		​return nameIntro + firstName + " " + lastName;
	}
​
​		return makeFullName ();
	}
​
		showName ("Test", "User"); 
		
	 

     // define a json object that represents a collection of people.
     // each person should have the following properties
     // - first name
     // - last name
     // - city
     // - state
     // - zip
     // - a collection of phone numbers (home, work, mobile)
	 
	 
	 var rootbj = {};
var employees = []


rootbj.employees = employees;

var firstName = "John";
var lastName = "Smith";
var city = "NY";
var state = "NY";
var zip = "1111";
var homeNumber = "2222";
var workNumber = "2222";
var mobileNumber = "2222";

var phoneNumbers = {
    
    "homeNumber": homeNumber,
    "workNumber": workNumber,
    "mobileNumber":mobileNumber
    
    
}


var employee = {
    "firstName": firstName,
    "lastName": lastName,
    "city":city,
    "state":state,
    "zip":zip,
   
}

rootbj.employees.push(employee);


rootbj.employees[0].numbers = JSON.stringify(phoneNumbers);


console.log(JSON.stringify(rootbj));

	 
	 


     // Create a javascript object (DataTable) with the following:
     // A private columns property (string array)
     // A private rows property (string array)
     // A public method addRows that adds an item to the rows array
     // A public method addColumns that adds an item to the columns array
     // A public method getData that returns the a json object representation of the DataTable
     // Note: the row object should be a hash of the column name and row item value
     // Example:
     // .addColumns('column1', 'column2', 'column3');
     // .addRow('value1A', 'value1B', 'value1C');
     // .addRow('value2A', 'value2B', 'value2C');
	 
	 
	function DataTable (columns, rows) {
		this.columns = columns;
		this.rows = rows;
	}
 
	DataTable.prototype.addRows = function(rowValue) {
		this.rows.push(rowValue);

	};
	 
	 
	DataTable.prototype.addColumns = function(colValue) {
		this.columns.push(colValue);

	}
	
	DataTable.prototype.getData = function() {
	
		var json = [];
	
		for (i=0;i<this.rows.length;i++){
			
			json.push({"row":this.columns[i]+"#"+this.rows[i]});
			
	}
	
		return json;
	};
	 
	 

     // within div1, programatically create a
     // SELECT element (with multiple items) and a button.
     // when the button is clicked write out the name and value of the selected item to the console.
	 
	var div1 = document.getElementById("div1");
	 
	var select = document.createElement("select");
	 select.name = "Items";
	 select.id = "Items";
	 
	var option = document.createElement("option");
		option.text = "First";
		option.value = "First";
		
	select.appendChild(option);

	option = document.createElement("option");
		option.text = "Second";
		option.value = "Second";

	select.appendChild(option);
	div1.appendChild(select);

	
	var newButton = document.createElement("input");
		newButton.type = "button";
		newButton.value = "Select";
		newButton.id = "Select";
    
	document.getElementById("div1").appendChild(newButton);	

	var element1 = document.getElementById("Select");
	
	element1.addEventListener("click", SelectValue);
	
	
	function SelectValue() {
	
	var e = document.getElementById("Items");
	var itemName = e.options[e.selectedIndex].name;
	var itemValue = e.options[e.selectedIndex].value;
	
	console.log(" Name "+itemName+" Value "+itemValue);
	
	}
	
	
	
     // Write 5 different jQuery selectors to retrieve the
     // sample anchor in the markup below.
	 
	 
	 $( "#linkId" );
	 $( ".linkClass" );
	 $( "#parentOfATag a" );
	 $( "a.havingThisClass:first" );
	 $( "a:gt(2)" );
	 
	 

     // Programatically create an array with 5 items.  Create a list item for each item in the array
     // and add the list items to the unordered list with an id of "list1".
	 
		var arr = [];
		
		for(var i=1; i<=5; i++) {
			arr.push("Element "+i);
	
		}
	 
		var list = document.getElementById('list1');
		
		
		for (i=0;i<arr.length;i++) {
		
		var entry = document.createElement('li');
		entry.appendChild(document.createTextNode(arr[i]));
		
		list.appendChild(entry);
		
		}
		
	 

     // Use javascript to add a list of checkboxes and 2 links
     // to the div with an id of "foobar"
     // When the first link is clicked, all the checkboxes should be checked (i.e. check all)
     // When the second link is clicked, all the checkboxes should be unchecked (i.e. uncheck all)

	  var newCheckbox = document.createElement("input");
    checkbox.type = "checkbox";
    checkbox.value = "One";
    document.getElementById("foobar").appendChild(newCheckbox);
	
	 newCheckbox = document.createElement("input");
    checkbox.type = "checkbox";
    checkbox.value = "Two";
    document.getElementById("foobar").appendChild(newCheckbox);
	
	var aTag = document.createElement('a');
	aTag.setAttribute('href',"#");
	aTag.id = "Check";
	aTag.innerHTML = "Check All";
	document.getElementById("foobar").appendChild(aTag);
	
	
	aTag = document.createElement('a');
	aTag.setAttribute('href',"#");
	aTag.id = "UnCheck";
	aTag.innerHTML = "UnCheck All";
	document.getElementById("foobar").appendChild(aTag);
	
	var element1 = document.getElementById("Check");
	
	element1.addEventListener("click", CheckAll);
	
	var element2 = document.getElementById("UnCheck");
	
	element2.addEventListener("click", UnCheckAll)
	
	function CheckAll() {
	
	  var checkboxes = document.getElementsByTagName('input');
	  
	   for (var i = 0; i < checkboxes.length; i++) {
             if (checkboxes[i].type == 'checkbox') {
                 checkboxes[i].checked = true;
             }
         }
	
	}
	
	function UnCheckAll() {
	
	var checkboxes = document.getElementsByTagName('input');
	  
	   for (var i = 0; i < checkboxes.length; i++) {
             if (checkboxes[i].type == 'checkbox') {
                 checkboxes[i].checked = false;
             }
         }
	
	
	
	
	}
	
	


	 
	 
	 
