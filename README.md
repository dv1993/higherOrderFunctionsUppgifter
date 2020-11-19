# higherOrderFunctionsUppgifter
Vi ska öva lite på funktioner i funktioner!
Jajjamensan va kul!

## foreach

signatur: foreach(arr, func)<br/>
funktion: funktionen ska iterera över alla element i arrayen och köra callback funktionen en gång.<br/>
Den inre funktionen ska kunna hantera tre input-parametrar, value, index, array. <br/>
Value - värdet som just nu itereras (let element = arr[i])<br/>
Index - index som just nu itereras (i)<br/>
Array - arrayen som funktionen anropats med<br/>

```javascript

//Funktionen som ska användas som callback
let input =[1,23,546,878,23];
foreach(input, write) //Denna rad ska leda till att elementen i arrayen ovan skrivs ut i konsollen
function write(val){
  console.log(val)
}

function foreach(arr, callback){
  //Kod här
}
```

## map
signatur: map(arr, func)<br/>
funktion: funktionen ska iterera över alla element i arrayen och köra callback funktionen för att ange nytt värde för dessa. Hur?<br/>
Funktionen ska skapa upp en ny array, iterera över alla element i den arrayen som funktionen anropats med, lägga in ett värdet av den inre funktion som funktionen anropats med <br/>samt, slutligen retunera den nyskapade arrayen.<br/>
Den inre funktionen ska kunna hantera tre input-parametrar, value, index, array. <br/>
Value - värdet som just nu itereras (let element = arr[i])<br/>
Index - index som just nu itereras (i)<br/>
Array - arrayen som funktionen anropats med

```javascript

let arr = [
  
		{
      "age":17,
			"name": {
				"title": "Mr",
				"first": "Naël",
				"last": "Henry"
			},
			"email": "Nael.Henry@example.com",
			"nat": "FR"
		},
		{
      "age":18,
			"name": {
				"title": "Miss",
				"first": "Sara",
				"last": "Faure"
			},
			"email": "Sara.Faure@example.com",
			"nat": "FR"
		},
		{
      "age":27,
			"name": {
				"title": "Mademoiselle",
				"first": "Christel",
				"last": "Legrand"
			},
			"email": "Christel.Legrand@example.com",
			"nat": "CH"
		},
];
//resultatet från att anropa map med ovanstående data som input plus getFirstName som callback är denna array: ["Henry", "Sara", "Christel"]

//Funktionen som ska användas som callback
function getFirstName(person){
  return person.name.first;
}

function map(arr, callback){
  //Kod här
}
```



## filter
signatur: filter(arr, func)<br/>
funktion: funktionen ska iterera över alla element i arrayen och köra callback funktionen för att avgöra huruvida det aktiva elementet ska finnas med i den nya lista eller inte.<br/> Hur? Funktionen ska skapa upp en ny array, iterera över alla element i den arrayen som funktionen anropats med, lägga in värdet av elementet i den nya arrayen givet att<br/> den uppnår det villkor som definierats i callback-funktionen (input-parameter "func" || inre funktionen). Callback-funktionen bör således returnera ett värde av bolesk typ.<br/>
Den inre funktionen ska kunna hantera tre input-parametrar, value, index, array. <br/>
Value - värdet som just nu itereras (let element = arr[i])<br/>
Index - index som just nu itereras (i)<br/>
Array - arrayen som funktionen anropats med<br/>

```javascript

let arr = [
  
		{
      "age":17,
			"name": {
				"title": "Mr",
				"first": "Naël",
				"last": "Henry"
			},
			"email": "Nael.Henry@example.com",
			"nat": "FR"
		},
		{
      "age":18,
			"name": {
				"title": "Miss",
				"first": "Sara",
				"last": "Faure"
			},
			"email": "Sara.Faure@example.com",
			"nat": "FR"
		},
		{
      "age":27,
			"name": {
				"title": "Mademoiselle",
				"first": "Christel",
				"last": "Legrand"
			},
			"email": "Christel.Legrand@example.com",
			"nat": "CH"
		},
];
//resultatet från att anropa filter med ovanstående data som input plus isUnderage som callback är en ny array med det endast 
//det näst sista och sista objektet från arrayen ovan.

//Funktionen som ska användas som callback
function isOverEighteen(person){
  return person.age>=18;
}

function filter(arr, callback){
  //Kod här
}
```

## reduce

signatur: reduce(arr, func, initialValue = null) //initialValue ska vara frivilligt

funktion: funktionen ska iterera över alla element i arrayen och köra callbackfunktionen för att producera ett värde. Hur? Funktionen ska skapa upp en variabel som ska lagra det sammanlagda värdet av elementen när de körs i callbackfunktionen. Efter det att arrayen itererats retuneras det sammanlagda värdet. Callback-funktionen ska kunna ta emot fyra parametrar, totalValue, value, index och array

TotalValue - det just nu totala värde av alla element som körts i den inre funktionen
Value - värdet som just nu itereras (let element = arr[i])
Index - index som just nu itereras (i)
Array - arrayen som funktionen anropats med

```javascript

let arr = [
  
		{
      "age":17,
			"name": {
				"title": "Mr",
				"first": "Naël",
				"last": "Henry"
			},
			"email": "Nael.Henry@example.com",
			"nat": "FR"
		},
		{
      "age":18,
			"name": {
				"title": "Miss",
				"first": "Sara",
				"last": "Faure"
			},
			"email": "Sara.Faure@example.com",
			"nat": "FR"
		},
		{
      "age":27,
			"name": {
				"title": "Mademoiselle",
				"first": "Christel",
				"last": "Legrand"
			},
			"email": "Christel.Legrand@example.com",
			"nat": "CH"
		},
];
//resultatet från att anropa reduce med ovanstående data som input plus sumAges som callback är värdet 62

//Funktionen som ska användas som callback
function sumAges(currentSum, person){
  return currentSum + person.age;
}

function reduce(arr, func, initialValue = null){
  //Kod här
}
```
