


## java

## variables

**//data type**

    var length=16; //Number
    
    var lastName="John" //String
    
    var x={firstName:"John",lastName:"Adams"};
    
    console.log(x.firstName+" "+x.lastName);



**//arithmetic operations**

   

     var x=5+6+7
        
        var x="John"+" "+"Adams"
        
        var x="5"+5+6
        
        var x="5"+(5+6)



**//redeclaring javascript variables**

    var carName ="Volvo";
    
    var carName


## web js

    //innerHTML
    document.getElementById("demo").innerHTML = 5 + 6;
    
    //document.write()
    document.write(5 + 6);
    //Using document.write()
    //after an HTML document is loaded, will delete all existing HTML
    
    window.alert()
    window.alert(5 + 6);
    
    console.log()
    console.log(5 + 6);

## array length

      var arr =  new  Array(  10,  20,  30  ); 
      document.write("arr.length is : "  + arr.length);

## comparison

## script

    < script>  < /script>
   
    < script src="myScript1.js">< /script>

## exit loop
**The Break Statement**

The  `break`  statement breaks the loop and continues executing the code after the loop (if any):

    for  (i =  0; i <  10; i++) {  
    if  (i ===  3) {  break; }  
    text +=  "The number is "  + i +  "<br>";  
    }

 **The Continue Statement**

The  `continue`  statement breaks one iteration (in the loop), if a specified condition occurs, and continues with the next iteration in the loop.



    for  (i =  0; i <  10; i++) {  
    if  (i ===  3) {  continue; }  
    text +=  "The number is "  + i +  "<br>";  
    }

**continue break label**


    var  cars = ["BMW",  "Volvo",  "Saab",  "Ford"];  
    list: {  
    text += cars[0] +  "<br>";  
    text += cars[1] +  "<br>";  
    break  list;  
    text += cars[2] +  "<br>";  
    text += cars[3] +  "<br>";  
    }

## string

var ch="ABCDEFGHIJKLMNOPQRSTUVWXYZ"

console.log(ch.length)


    var str = "Hello";
    var arr = str.split("");
    var text = "";
    var i;
    
    for (i = 0; i < arr.length; i++) {
    text += arr[i] + "<br>"
    }

## gerelementbyid

    document.getElementById('button').addEventListener('click',createH1);
    
    function createH1 (argument) {
    
    var container=document.getElementById('container');
    
    var h1=document.createElement("h1");
    
    var text=document.createTextNode("hello world !");
    
    h1.appendChild(text);
    
    container.appendChild(h1);
    
    }

## simple boolean expression

## average

    var arr=[12,66,4,8,7];
    var somme=0;
    var moyenne=0;
    
    for(var i=0;i<arr.length;i++)
    {
      somme+=arr[i];  
    }
    
    moyenne=somme/arr.length;
    
    print(moyenne);
     

## correction

## range sum

    var arr=[1,1,1,1];
    var x=rangeSum(arr,1,3);
    print(x);
    function rangeSum(arr,start,end)
    {
     if(start>end)
     {
         return 0;
     }else
     {
         return arr[start]+rangeSum(arr,start+1,end);
     }
        
    }

## combinaison option in tournement

    var x=count(4);
    print(x);
    
    function factoriel(n)
    {
        var res=1;
        
        for(var i=1;i<=n;i++)
        {
            res*=i;
        }
        
        return res;
    }
    
    
    function count(n)
    {
     return (factoriel(n)/(factoriel(n-2)*factoriel(2)));   
    }

## move towards zero


    var arr=[1,0,1,0,];
    moveTozero(arr);
    function moveTozero(arr)
    {
    var count=0;
             
      for(var i=0;i<arr.length;i++)
        {
           if(arr[i]!=0)
           {
               arr[count++]=arr[i];
           }
        }
             
        
        while(count<arr.length)
        {
            arr[count++]=0;
        }
      
       for(var i=0;i<arr.length;i++)
        {
         print(arr[i]);   
        }
    
    }

 

## twins

## give back change

     var euros=[50,20,10,5];
                                          
     function rendreMonnaie(montant)
    {
    var rendu=new Array(euros.length);
       for (var i=0;i<euros.length;i++)
       {
       rendu[i]=montant/euros[i];
        montant %= euros[i];
       }
       return rendu;                                   
    }
                                          
    var rendu=rendreMonnaie(55);
                                          
    for(var j=0;j<rendu.length;j++)
    {
      if(rendu[j]>=1)
     {
      print(Math.round(rendu[j])+"pieces de "+euros[j]+"euro");
                                          
     }
    }
     

## type conversion
```
function passVar(object1, object2, number1) {

        object1.key1= "laptop";
        object2 = {
            key2: "computer"
        };
        number1 = number1 + 1;
    }

    var object1 = {
        key1: "car"
    };
    var object2 = {
        key2: "bike"
    };
    var number1 = 10;

    passVar(object1, object2, number1);
    console.log(object1.key1);
    console.log(object2.key2);
    console.log(number1);

Output: -
    laptop
    bike
    10
```
 

## thread

 

## event

    < button onclick="document.getElementById('demo').innerHTML = Date()">The time is?< /button>
    
    < button onclick="displayDate()">The time is?< /button>
    
    //onchange An HTML element has been changed
    
    //onclick The user clicks an HTML element
    
    //onmouseover The user moves the mouse over an HTML element
    
    //onmouseout The user moves the mouse away from an HTML element

 
## title

## use of exception

 

## objects

 



## arrays

    var cars = ["Saab", "Volvo", "BMW"];
    
    var cars = new Array("Saab", "Volvo", "BMW");
    
    var name = cars[0];
    
    var x = cars.length; // The length property returns the number of elements
    
    var y = cars.sort(); // The sort() method sorts arrays
    
    var fruits, text, fLen, i;
    
    fruits = ["Banana", "Orange", "Apple", "Mango"];
    
    fLen = fruits.length; text = "<ul>";
    
    for (i = 0; i < fLen; i++) {
    
    text += "<li>" + fruits[i] + "</li>";
    
    }
    
    text += "</ul>";
     

## concat
var str1 = "Hello ";  
var str2 = "world!";  
var res = str1.concat(str2);
var res = str1 + str2
## jquery selector

    **$("*")**
    
    All elements
    
    
    **$("#lastname")**
    
    The element with id="lastname"
    
    
    **$(".intro")**
    
    All elements with class="intro"
    
    
    **$(".intro,.demo")**
    
    All elements with the class "intro" or "demo"
    
    
    **$("p")**
    
    All < p> elements
    
    **$("h1,div,p")**
    
    All < h1>, < div> and < p> elements

## loop step

## console errors
    var myObj = { firstname : "John", lastname : "Doe" };  
    console.error(myObj);
## array index



 

## singleton

 

## dates

    Date var d = new Date();
    
    var d = new Date(2018, 11, 24, 10, 33, 30);
    
    var d = new Date("October 13, 2014 11:13:00");
    
    var d = new Date(0); var d = new Date(86400000);
    
    d = new Date(); var d = new Date("2015-03");
    
    var d = new Date("2015-03-25");
    
    Date.now() //Get the time. ECMAScript 5.

## object properties

    //JavaScript Objects
    
    var person = {
    
    firstName:"John",
    
    lastName:"Doe",
    
    age:50,
    
    eyeColor:"blue"
    
    };
    
    var person = {
    
    firstName: "John",
    
    lastName : "Doe",
    
    id : 5566,
    
    fullName : function() {
    
    return this.firstName + " " + this.lastName;
    
    }
    
    };
    
    name = person.fullName();

## string split
**Tip:** If an empty string ("") is used as the separator, the string is split between each character.
## custom sort

## ascii art

## approximation of pi

    var c=0;
    
    function Calculate()
    
    {
    
    var c=prompt("Enter number of cycles:","0");
    
    if (c>0)
    
    {
    
    var Pi=0;
    
    var n=1;
    
    for (i=0;i<=c;i++)
    
    {
    
    Pi=Pi+(4/n)-(4/(n+2))
    
    n=n+4
    
    }
    
    alert(Pi);
    
    }
    
    else
    
    {
    
    alert("Canceled or Error in input: Input must be positive.");
    
    }
    
    }

## reshape string

    var str="sqfsdfgsdgfdghdghdfhgd";
    var x= reshape(str,4);
    print(x);
    function reshape(str,n)
    {
        var res="";
        for(var i=0;i<str.length;i++)
        {
            if(i%n==0 && i!=0)
            {
                res+="\n"+str.charAt(i);
            }else
            {
                res+=str.charAt(i);
            }
        }
        
        return res;
    }

## random number

      var min=4; 
        var max=5;  
        var random = 
        Math.floor(Math.random() * (+max - +min)) + +min; 
        document.write("Random Number Generated : " + random );

## string comparison
```
string_a.localeCompare(string_b);

/* Expected Returns:

 0:  exact match

-1:  string_a < string_b

 1:  string_a > string_b

 */
```
    x=5
    
    **equal to**
     
    x == 8 false
    
    
    x == 5  true
    
    
    x == "5" true
    
    
    
    ===
    
    
    x === 5 true
    
    
    x === "5" false
    
    
    !=
    
    x != 8 true
    
    
    !==
    
    x !== 5 false
    
    
    x !== "5" true
    
    
    x !== 8 true
    
    
    >
    
    x > 8 false
    
    
    <
    
    x < 8 true
    
    
     > =
    x >= 8 false
    
    <=
    x <= 8 true

## type comparison
Given that  `x = 6`  and  `y = 3`, the table below explains the logical operators:


    **&&**
    
    (x < 10 && y > 1) is true
    
    
    **||**
    
    (x == 5 || y == 5) is false
    
    **!**
    
    !(x == y) is true
    
    2 < 12 true
    2 < "12" true
    2 < "John" false
    2 > "John" false
    2 == "John" false
    "2" < "12" false
    "2" > "12" true
    "2" == "12" false
     

## prototypes

 The JavaScript  `prototype`  property allows you to add new properties to object constructors:

### Example

    function  Person(first, last, age, eyecolor) {  
    this.firstName  = first;  
    this.lastName  = last;  
    this.age  = age;  
    this.eyeColor  = eyecolor;  
    }  
      
    Person.prototype.nationality  =  "English";

The JavaScript  `prototype`  property also allows you to add new methods to objects constructors:

### Example

    function  Person(first, last, age, eyecolor) {  
    this.firstName  = first;  
    this.lastName  = last;  
    this.age  = age;  
    this.eyeColor  = eyecolor;  
    }  
      
    Person.prototype.name  =  function() {  
    return  this.firstName  +  " "  +  this.lastName;  
    };

## parametres
 Arguments are Passed by Value
 Objects are Passed by Reference
 

## type conversion


**ToString**
String conversion happens when we need the string form of a value.

    let value = true;
    value = String(value); // now value is a string "true"


**ToNumber**

     let str = "123";
    let num = Number(str); // becomes a number 123
     let age = Number("an arbitrary string instead of a number");
    
     alert( Number("   123   ") ); // 123
    alert( Number("123z") );      // NaN (error reading a number at "z")
    alert( Number(true) );        // 1
    alert( Number(false) );       // 0

**ToBoolean**

     alert( Boolean(1) ); // true
    alert( Boolean(0) ); // false
    alert( Boolean("hello") ); // true
    alert( Boolean("") ); // false

## remove duplication

    var arr=[1,1,3,3,4,4]
    var arrr=new Array();
    var temp= removeDuplicates( arr,  6);
    function removeDuplicates( arr,  n) 
        { 
           
            if (n==0 || n==1) 
                return n; 
           
            var temp = new Array(n); 
            var j = 0; 
            
            
            for (var i=0; i<n-1; i++) 
            {
                
                if (arr[i] != arr[i+1]) 
                {
                    temp[j++] = arr[i];
                }
            } 
              
           
            temp[j++] = arr[n-1];    
              
             
            for (var i=0; i<j; i++) 
            {
                arr[i] = temp[i];
                print(arr[i]);
            } 
                 
            
        } 

## sum based on factors

    var x=sumFactor(15)
    print(x);
    function sumFactor(n)
    {
        var res=0;
        for(var i=2;i<=Math.sqrt(n);i++)
        {
         
            if(n%i==0)
            {
                if(i==n/i){
                    res+=i;
                }else
                {
                    res+=(i+n/i)
                }
            }
            
        }
        
        return 1+n+res;
    }
