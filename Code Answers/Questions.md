# Database Challenges

## Question 1

I would remove the attributes of ``` Cellphone``` down to ```Cellphone Contract End``` and create a new Entity named ```CellphoneContract```.
I would then include ```EmployeeGUID``` as a foreign key in order to have a link between Employee and CellphoneContract
```Cellphone Number``` would then be the primary key of the new entity as it should be a unique value attribute.

## Question 2

An analyst has asked you to run a query to see the number of movie tickets per genre that was sold in December last year. The data he needs is spread across two tables.
```sql

SELECT Movies.#Genre, COUNT(Tickets.TicketID) AS NumberOfTickets FROM Tickets
JOIN Movies ON Tickets.#MovieID = Movies.#MovieID
GROUP BY #Genre
```

# Back-end Code Challenges
* Only send back the code required for your the challenges

## Question 1

```csharp
	public static void PrintWordMultiple(string word)
	{
		int wordLength = word.Length;
		string output = "";
		
		if (wordLength % 2 == 0)
			output += "Stack ";
		if (wordLength % 4 == 0)
			output += "Overflow ";
		Console.WriteLine(output);
	}
```

## Question 2

Code Refactoring

```csharp
    public class Animal 
	{
		public string Eat()
		{
			return "Yummy";
		}
		
		public virtual string MakeNoise()
		{
			return "Durrr";
		}
	}
	
	public class Horse: Animal
	{
		public override string MakeNoise()
		{
			return "Neigh";
		}
	}
	
	public class Sheep: Animal 
	{
		public override string MakeNoise()
		{
			return "Baaah";
		}
	}

```
# Front-end Code Challenges

## Question 1
Given the below code snippet, solve the problems that follow:

```html
<div id="firstDiv" class="red-card">
<div id="secondDiv" class="red-card">

<style>
    #secondDiv {
        background: orange;
    }

    div {
        height: 150px;
        width: 150px;
        background: green;
    }

    .red-card {
        background: red;
    }

    .yellow-card {
        background: yellow;
    }
</style>
```

1) What will the colour of both div elements be?

```#firstDiv``` is red, ```secondDiv``` is orange

2)How would you dynamically target firstDiv and make it's colour pink? (provide the code snippet)

```javascript
	document.getElementById("firstDiv").style.background = "pink";
```
3) How would you dynamically target secondDiv and add the yellow-card class to its class list? (provide the code snippet)
```javascript
	document.getElementById("secondDiv").classList.add('yellow-card');
```

## Question 2
Consider the function below:

```javascript
function legal(x) {
    console.log(x);
    var x;
}
```

1. Why will the function be parsed correctly? 
	```Since javascript is not a statically typed language, it will not check the data type of the parameter. Using the **var** keyword also does not stop the declaration of already declared variables.```

2. How could you introduce a stricter syntax to variable/function declaration and avoid this behaviour?
 Why will the function be parsed correctly? 
	```Using the **let** keyword ensures that once a variable is declared, it cannot be declared again. If the issue was about parameter types in function declaration, It would be best to use TypeScript.```
