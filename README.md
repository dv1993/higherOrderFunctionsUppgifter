# higherOrderFunctionsUppgifter
Vi ska öva lite på funktioner i funktioner!
Jajjamensan va kul!

## foreach

signatur: foreach(arr, func)
funktion: funktionen ska iterera över alla element i arrayen och köra callback funktionen en gång.
Den inre funktionen ska kunna hantera tre input-parametrar, value, index, array. 
Value - värdet som just nu itereras (let element = arr[i])
Index - index som just nu itereras (i)
Array - arrayen som funktionen anropats med

## map
signatur: map(arr, func)
funktion: funktionen ska iterera över alla element i arrayen och köra callback funktionen för att ange nytt värde för dessa. Hur?
Funktionen ska skapa upp en ny array, iterera över alla element i den arrayen som funktionen anropats med, lägga in ett värdet av den inre funktion som funktionen anropats med samt, slutligen retunera den nyskapade arrayen.
Den inre funktionen ska kunna hantera tre input-parametrar, value, index, array. 
Value - värdet som just nu itereras (let element = arr[i])
Index - index som just nu itereras (i)
Array - arrayen som funktionen anropats med

## filter
signatur: filter(arr, func)
funktion: funktionen ska iterera över alla element i arrayen och köra callback funktionen för att avgöra huruvida det aktiva elementet ska finnas med i den nya lista eller inte. Hur? Funktionen ska skapa upp en ny array, iterera över alla element i den arrayen som funktionen anropats med, lägga in värdet av elementet i den nya arrayen givet att den uppnår det villkor som definierats i callback-funktionen (input-parameter "func" || inre funktionen). Callback-funktionen bör således returnera ett värde av bolesk typ.
Den inre funktionen ska kunna hantera tre input-parametrar, value, index, array. 
Value - värdet som just nu itereras (let element = arr[i])
Index - index som just nu itereras (i)
Array - arrayen som funktionen anropats med

## reduce

signatur: reduce(arr, func, initialValue = null) //initialValue ska vara frivilligt

funktion: funktionen ska iterera över alla element i arrayen och köra callbackfunktionen för att producera ett värde. Hur? Funktionen ska skapa upp en variabel som ska lagra det sammanlagda värdet av elementen när de körs i callbackfunktionen. Efter det att arrayen itererats retuneras det sammanlagda värdet. Callback-funktionen ska kunna ta emot fyra parametrar, totalValue, value, index och array

TotalValue - det just nu totala värde av alla element som körts i den inre funktionen
Value - värdet som just nu itereras (let element = arr[i])
Index - index som just nu itereras (i)
Array - arrayen som funktionen anropats med
