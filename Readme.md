# MUY FÁCIL

## 1  

[Flip the Boolean](https://edabit.com/challenge/seB6cQjuSqgudatyF)

### Instructions
Create a function that reverses a boolean value.

Examples
Reverse(true) ➞ false
Reverse(false) ➞ true

Notes
Don't forget to return the result.

### Test suit  
```
using System;
using NUnit.Framework;

[TestFixture]
public class Tests
{
	[Test]
	[TestCase(false, Result=true)]
	[TestCase(true, Result=false)]
	public static bool FixedTest(bool boolean)
	{
		Console.WriteLine($"Input: {boolean}");
		return Program.Reverse(boolean);
	}
}
```
### Solution Code  

```
public class Program {
	public static int Reverse(bool boolean) {
		return !boolean;
	}
}
```

### Estimación
5 minutos

### Duración Real
1 minuto

## 2  

[Circuit Power Calculator](https://edabit.com/challenge/L2fwjYi9YixY8kJfK)

### Instructions
Create a function that takes voltage and current and returns the calculated power.

Examples

CircuitPower(230, 10) ➞ 2300
CircuitPower(110, 3) ➞ 330
CircuitPower(480, 20) ➞ 9600

Notes
power = voltage * current

### Test suit  

```
using System;
using NUnit.Framework;

[TestFixture]
public class Tests {

	[Test]
	[TestCase(110, 3, Result=330)]
	[TestCase(230, 10, Result=2300)]
	[TestCase(480, 20, Result=9600)]
	public static int CircuitPower(int voltage, int current)
	{
		Console.WriteLine($"Input: {voltage} {current}");
		return Program.CircuitPower(voltage, current);
	}
}
```

### Solution Code  

```
public class Program {
	public static int CircuitPower(int voltage, int current)
	{
		return voltage * current;
	}
}
```

### Estimación
5 minutos

### Duración Real
32 segundos

## 3  

[Convert Minutes into Seconds](https://edabit.com/challenge/bizjGL4wyd8PwR4Ke)

### Instructions
Write a function that takes an integer minutes and converts it to seconds.

Examples
convert(5) ➞ 300
convert(3) ➞ 180
convert(2) ➞ 120

Notes
Don't forget to return the result.

### Test suit  

```
using System;
using NUnit.Framework;

[TestFixture]
public class Tests {

	[Test]
	[TestCase(6, Result=360)]
	[TestCase(4, Result=240)]
	[TestCase(8, Result=480)]
	[TestCase(60, Result=3600)]
	public static int FixedTest(int a) {
		Console.WriteLine($"Input: {a}");
		return Program.convert(a);
	}
}
```

### Solution Code  

```
public class Program {
	public static int convert(int minutes) {
		return minutes * 60;
	}
}
```

### Estimación
5 minutos

### Duración Real
23 segundos

# FÁCIL

## 1 

[Find the Smallest and Biggest Numbers](https://edabit.com/challenge/kMWmiNJM4szSv7dLd)

### Instructions

Create a function that takes an array of numbers and return both the minimum and maximum numbers, in that order.

Examples
FindMinMax([1, 2, 3, 4, 5]) ➞ [1, 5]
FindMinMax([2334454, 5]) ➞ [5, 2334454]
FindMinMax([1]) ➞ [1, 1]

Notes
All test arrays will have at least one element and are valid.

### Test suit  

```
using NUnit.Framework;
using System;

[TestFixture]
public class Tests
{
	[Test]
	public static void MaxText()
	{
		Assert.AreEqual(new double[]{1,54},Program.FindMinMax(new double[]{14,35,6,1,34,54}));
		Assert.AreEqual(new double[]{1.346, 1.8734},Program.FindMinMax(new double[]{1.346, 1.6532, 1.8734, 1.8723}));
		Assert.AreEqual(new double[]{0.2345, 0.984},Program.FindMinMax(new double[]{0.432, 0.874, 0.523, 0.984, 0.327, 0.2345}));
		Assert.AreEqual(new double[]{13, 98},Program.FindMinMax(new double[]{13, 72, 98, 43, 24, 65, 31}));
		Assert.AreEqual(new double[]{-54, -21},Program.FindMinMax(new double[]{-54, -23, -54, -21}));
		Assert.AreEqual(new double[]{-0.6834, 0.5632},Program.FindMinMax(new double[]{-0.473, -0.6834, -0.1287, 0.5632}));
		Assert.AreEqual(new double[]{0, 0},Program.FindMinMax(new double[]{0, 0, 0, 0}));
	}
}
```

### Solution Code  

```
using System;
using System.Linq;

public class Program
{
	public static double[] FindMinMax(double[] values)
	{
			double[] result = new double[2];
			result[0] = values.Min();
			result[1] = values.Max();
			return result;
	}
}
```

### Estimación
10 minutos

### Duración Real
10 minutos

## 2

[Hamming Distance](https://edabit.com/challenge/K49LXsoMmS6tXxP7R)

### Instructions
Hamming distance is the number of characters that differ between two strings.

To illustrate:
String1: "abcbba"
String2: "abcbda"

Hamming Distance: 1 - "b" vs. "d" is the only difference.
Create a function that computes the hamming distance between two strings.

Examples
HammingDistance("abcde", "bcdef") ➞ 5
HammingDistance("abcde", "abcde") ➞ 0
HammingDistance("strong", "strung") ➞ 1

Notes
Both strings will have the same length.

### Test suit  

```
using NUnit.Framework;

[TestFixture]
public class Tests
{
	[Test]
	[TestCase("abcde", "bcdef", Result=5)]
	[TestCase("abcde", "abcde", Result=0)]
	[TestCase("strong", "strung", Result=1)]
	public static int FixedTest(string str1, string str2)
	{
		return Program.HammingDistance(str1, str2);
	}
}
```

### Solution Code  

```
public class Program
{
	public static int HammingDistance(string str1, string str2)
	{
		int differences = 0;
		for(int i = 0; i < str1.Length ; i++){
			if(str1[i] != str2[i]){
				++differences;
			}
		}
		return differences;
	}
}
```

### Estimación
10 minutos

### Duración Real
5 minutos

## 3

[How many Vowels](https://edabit.com/challenge/5ytLyHsZHfyDhBgXr)

### Instructions
Create a function that takes a string and returns the number (count) of vowels contained within it.

Examples
CountVowels("Celebration") ➞ 5
CountVowels("Palm") ➞ 1
CountVowels("Prediction") ➞ 4

Notes
-   a, e, i, o, u are considered vowels (not y).
-   All test cases are one word and only contain letters.

### Test suit  

```
using NUnit.Framework;

[TestFixture]
public class Tests
{
	[Test]
	[TestCase("Celebration", Result=5)]
	[TestCase("Palm", Result=1)]
	[TestCase("Prediction", Result=4)]
	[TestCase("Suite", Result=3)]
	[TestCase("Quote", Result=3)]
	[TestCase("Portrait", Result=3)]
	[TestCase("Steam", Result=2)]
	[TestCase("Tape", Result=2)]
	[TestCase("Nightmare", Result=3)]
	[TestCase("Convention", Result=4)]
	public static int FixedTest(string str)
	{
		return Program.CountVowels(str);
	}
}
```

### Solution Code  

```
public class Program
{
	public static int CountVowels(string str)
	{
		int count = 0;
		for (int i = 0; i < str.Length; i++){
			if(str[i] == 'a' ||
				str[i] == 'e' ||
				str[i] == 'i' || 
				str[i] == 'o' || 
				str[i] == 'u'){
				cont++;
			}
		}
		return count;
	}
}
```

### Estimación
10 minutos

### Duración Real
5 minutos

# Medio

## 1 

[Find the nth Tetrahedral Number](https://edabit.com/challenge/j34NRDnwRC2YgGPXN)

### Instructions
A tetrahedron is a pyramid with a triangular base and three sides. A tetrahedral number is a number of items within a tetrahedron.
Create a function that takes an integer n and returns the nth tetrahedral number.

Examples
Tetra(2) ➞ 4
Tetra(5) ➞ 35
Tetra(6) ➞ 56

Notes
There is a formula for the nth tetrahedral number.

### Test suit  

```
using System;
using NUnit.Framework;

[TestFixture]
public class Tests
{
    [Test]
    [TestCase(1, Result=1)]
    [TestCase(2, Result=4)]
  	[TestCase(3, Result=10)]
	[TestCase(4, Result=20)]
	[TestCase(5, Result=35)]
	[TestCase(9, Result=165)]
    public static int FixedTest(int n)
    {
		Console.WriteLine($"Input: {n}");
        return Program.Tetra(n);
    }
}
```

### Solution Code  

```
public class Program {
	public static int Tetra(int n) {
		return (n * (n + 1) * (n + 2)) / 6;
	}
}
```

### Estimación
10 minutos

### Duración Real
7 minutos

## 2 

[Return the Index of All Capital Letter](https://edabit.com/challenge/6qFnpAhd3kdmYcNG2)

### Instructions
Create a function that takes a single string as argument and returns an ordered array containing the indices of all capital letters in the string.

Examples
IndexOfCapitals("eDaBiT") ➞ [1, 3, 5]
IndexOfCapitals("eQuINoX") ➞ [1, 3, 4, 6]
IndexOfCapitals("determine") ➞ []
IndexOfCapitals("STRIKE") ➞ [0, 1, 2, 3, 4, 5]
IndexOfCapitals("sUn") ➞ [1]

Notes
Return an empty array if no uppercase letters are found in the string.
Special characters ($#@%) and numbers will be included in some test cases.
Assume all words do not have duplicate letters.

### Test suit  

```
using NUnit.Framework;
using System;
[TestFixture]
public class Tests
{
  	[Test]
  	[TestCase("eDaBiT", Result=new int[]{1, 3, 5})]
  	[TestCase("eQuINoX", Result=new int[]{1, 3, 4, 6})]
  	[TestCase("determine", Result=new int[]{})]
  	[TestCase("STRIKE", Result=new int[]{0, 1, 2, 3, 4, 5})]
  	[TestCase("sUn", Result=new int[]{1})]
  	[TestCase("SpiDer", Result=new int[]{0, 3})]
  	[TestCase("accOmpAnY", Result=new int[]{3, 6, 8})]
  	[TestCase("@xCE#8S#i*$en", Result=new int[]{2, 3, 6})]
  	[TestCase("1854036297", Result=new int[]{})]
  	[TestCase("Fo?.arg~{86tUx=|OqZ!", Result=new int[]{0, 12, 16, 18})]
  	public static int[] IndexTests(string str)
    {    
    	return Program.IndexOfCapitals(str);
    }
}
```

### Solution Code  

```
using System;
using System.Linq;
using System.Collections.Generic;
public class Program 
{
    public static int[] IndexOfCapitals(string str) 
    {
		List<int> res = new List<int>();
		for(int i = 0; i < str.Length; i++){
			if(Char.IsUpper(str[i])){
				res.Add(i);
			}
		}
		return res.ToArray();
    }
}
```

### Estimación
10 minutos

### Duración Real
11 minutos

## 3

[Positive Count / Negative Sum](https://edabit.com/challenge/SXeEZPxDM9Y5HzLvw)

### Instructions
Create a function that takes an array of positive and negative numbers.
Return an array where the first element is the count of positive numbers and the second element is the sum of negative numbers.

Examples
CountPosSumNeg([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15]) ➞ [10, -65]
// There are a total of 10 positive numbers.
// The sum of all negative numbers equals -65.
CountPosSumNeg([92, 6, 73, -77, 81, -90, 99, 8, -85, 34]) ➞ [7, -252]
CountPosSumNeg([91, -4, 80, -73, -28]) ➞ [2, -105]
CountPosSumNeg([]) ➞ []

Notes
If given an empty array, return an empty array: []
Cast sum to int, don't mind the remaining decimal places.
0 is not positive.


### Test suit  

```
using NUnit.Framework;

[TestFixture]
public class FindNeedleTest
{
    [Test]
    public void GenericTests()
    {
        double[] haystack_1 = new double[] { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, -11, -12, -13, -14, -15 };
        double[] haystack_2 = new double[] { 92, 6, 73, -77, 81, -90, 99, 8, -85, 34 };
        double[] haystack_3 = new double[] { 91, -4, 80, -73, -28 };
        double[] haystack_4 = new double[] { };
        double[] haystack_5 = new double[] { 69, 100, 28, 47, 53, -61, -24 };
        double[] haystack_6 = new double[] { 5, 7, 9, -3, -7, 61, -24 };
        double[] haystack_7 = new double[] { 0 };
        double[] haystack_8 = new double[] { 98, 51, -19, -97 };
        double[] haystack_9 = new double[] { -42, 3, -51, -64, 69, 77, -20, -5, 68, -76 };
		double[] haystack_10 = new double[] { 0, 0, 0 };
        Assert.AreEqual(new int[] { 10, -65 }, Program.CountPosSumNeg(haystack_1));
        Assert.AreEqual(new int[] { 7, -252 }, Program.CountPosSumNeg(haystack_2));
        Assert.AreEqual(new int[] { 2, -105 }, Program.CountPosSumNeg(haystack_3));
        Assert.AreEqual(new int[] {  }, Program.CountPosSumNeg(haystack_4));
        Assert.AreEqual(new int[] { 5, -85 }, Program.CountPosSumNeg(haystack_5));
        Assert.AreEqual(new int[] { 4, -34 }, Program.CountPosSumNeg(haystack_6));
        Assert.AreEqual(new int[] { 0, 0 }, Program.CountPosSumNeg(haystack_7));
        Assert.AreEqual(new int[] { 2, -116 }, Program.CountPosSumNeg(haystack_8));
        Assert.AreEqual(new int[] { 4, -258 }, Program.CountPosSumNeg(haystack_9));
        Assert.AreEqual(new int[] { 0, 0 }, Program.CountPosSumNeg(haystack_10));
    }
}
```

### Solution Code  

```
public class Program 
{
    public static int[] CountPosSumNeg(double[] arr) 
    {
		if (arr == null || arr.Length == 0) return new int[0]{};
		
      	int[] result = new int[2];
		result[0] = 0;
		result[1] = 0;
		
		for (int i = 0; i < arr.Length; i++)
		{
			if (arr[i] > 0)
			{
				result[0]++;
			} else {
				result[1] += (int)arr[i];
			}
		}
		
		return result;
    }
}
```

### Estimación
7 minutos

### Duración Real
10 minutos

# Dificil

## 1

[Do All Bigrams Exist?](https://edabit.com/challenge/p39Q6JFuran7t5LpS)

### Instructions
You are given an input array of bigrams, and an array of words.
Write a function that returns true if every single bigram from this array can be found at least once in an the list of words.

Examples
CanFind(new string[] { "at", "be", "th", au" }, new string[] { "beautiful", "the", "hat" }) ➞ true
CanFind(new string[] { "ay", "be", "ta", cu" }, new string[] { "maybe", "beta", "abet", "course" }) ➞ false
// "cu" does not exist in any of the words.
CanFind(new string[] { "th", "fo", "ma", or" }, new string[] { "the", "many", "for", "forest" }) ➞ true
CanFind(new string[] { "oo", "mi", "ki", la" }, new string[] { "milk", "chocolate", "cooks" }) ➞ false

Notes
A bigram is string of two consecutive characters in the same word.
If the array of words is empty, return false.

### Test suit

```
using NUnit.Framework;
using System;

[TestFixture]
public class Tests
{
	[TestCase(new string[] { "at", "be", "th", "au" }, new string[] { "beautiful, the, hat" }, Result=true)]
	[TestCase(new string[] { "bo", "ta", "el", "st", "ca" }, new string[] { "books, table, cap, hostel" }, Result=true)]
	[TestCase(new string[] { "la", "te" }, new string[] { "latte" }, Result=true)]
	[TestCase(new string[] { "th", "fo", "ma", "or" }, new string[] { "the, many, for, forest" }, Result=true)]
	[TestCase(new string[] { "ay", "be", "ta", "cu" }, new string[] { "maybe, beta, abet, course" }, Result=false)]
	[TestCase(new string[] { "oo", "mi", "ki", "la" }, new string[] { "milk, chocolate, cooks" }, Result=false)]
	[TestCase(new string[] { "la" }, new string[] { }, Result=false)]
	[TestCase(new string[] { "la", "at", "te", "ea" }, new string[] { "latte" }, Result=false)]
	public static bool TestSolution(string[] bigrams, string[] words)
    {
        return Program.CanFind(bigrams, words);
    }
}
```

### Solution Code

```
using System;

public class Program
{
    public static bool CanFind(string[] bigrams, string[] words) {
		if(words == null || words.Length == 0){
			return false;
		}

		string joinedWords = String.Join(" ", words);

		for(int i = 0; i < bigrams.Length; i++){
			if(!joinedWords.Contains(bigrams[i])){
				return false;
			}
		}

		return true;
	}
}

```

### Estimación
15 minutos

### Duración Real
42 minutos

## 2

[Track the Robot (Part 1)](https://edabit.com/challenge/g88PKZrCY6sWPBva7)

### Instructions
A robot has been given a list of movement instructions.
Each instruction is either left, right, up or down, followed by a distance to move. The robot starts at [0, 0].
You want to calculate where the robot will end up and return its final position as an array.

To illustrate, if the robot is given the following instructions:

new string[] { "right 10", "up 50", "left 30", "down 10" }
It will end up 20 left and 40 up from where it started, so we return int[] { -20, 40 }.

Examples
TrackRobot(new string[] { "right 10", "up 50", "left 30", "down 10" }) ➞ int[] { -20, 40 }

TrackRobot(new string[] { }) ➞ int[] { 0, 0 } // If there are no instructions, the robot doesn't move.

TrackRobot(new string[] { "right 100", "right 100", "up 500", "up 10000" }) ➞ new int[] { 200, 10500 }
Notes
The only instructions given will be left, right, up or down.
The distance after the instruction is always a positive whole number.


### Test suit

```
using NUnit.Framework;
using System;

[TestFixture]
public class Tests
{
	[Test]
    public static void TestSolution()
    {
		var inst1 = new string[] { "right 10", "up 50", "left 30", "down 10" };
		var inst2 = new string[] {  };
		var inst3 = new string[] { "left 10", "left 100", "left 1000", "left 10000" };
		var inst4 = new string[] { "right 100", "right 100", "up 500", "up 10000" }; 
		var inst5 = new string[] { "left 10", "right 10", "down 10", "up 10" };

        Assert.AreEqual(new int[] { -20, 40 }, Program.TrackRobot(inst1));
        Assert.AreEqual(new int[] { 0, 0 }, Program.TrackRobot(inst2));
        Assert.AreEqual(new int[] { -11110, 0 }, Program.TrackRobot(inst3));
        Assert.AreEqual(new int[] { 200, 10500 }, Program.TrackRobot(inst4));
        Assert.AreEqual(new int[] { 0, 0 }, Program.TrackRobot(inst5));
    }
}
```

### Solution Code

```
using System;

public class Program
{
    public static int[] TrackRobot(string[] instructions) {
		int[] result = new int[2]{0,0};
		string[] splitedInstruction;
		int steps;
		string direction;

		for (int i = 0; i < instructions.Length; i++)
		{
			splitedInstruction = instructions[i].Split(' ');
			direction = splitedInstruction[0];
			steps = Int32.Parse(splitedInstruction[1]);

			switch(direction)
			{
				case "left":
					result[0] -= steps;
					break;
				case "right":
					result[0] += steps;
					break;
				case "up":
					result[1] += steps;
					break;
				case "down":
					result[1] -= steps;
					break;
				}
			}

			return result;
	}
}
```

### Estimación
20 minutos

### Duración Real
13 minutos

## 3

[Consecutive numbers](https://edabit.com/challenge/TAZywz6R2hu9tDQWc)

### Instructions
Create a function that determines whether elements in an array can be re-arranged to form a consecutive list of numbers where each number appears exactly once.

Examples
Cons([5, 1, 4, 3, 2]) ➞ true // Can be re-arranged to form [1, 2, 3, 4, 5]
Cons([5, 1, 4, 3, 2, 8]) ➞ false
Cons([5, 6, 7, 8, 9, 9]) ➞ false // 9 appears twice

Notes
N/A

### Test suit

```
using NUnit.Framework;

[TestFixture]
public class Tests
{
	[Test]
	[TestCase(new int[]{5, 1, 4, 3, 2}, Result=true)]
	[TestCase(new int[]{55, 59, 58, 56, 57}, Result=true)]
	[TestCase(new int[]{-3, -2, -1, 1, 0}, Result=true)]
	[TestCase(new int[]{5, 1, 4, 3, 2, 8}, Result=false)]
	[TestCase(new int[]{5, 6, 7, 8, 9, 9}, Result=false)]
	[TestCase(new int[]{5, 3}, Result=false)]
	public static bool FixedTest(int[] arr) =>
		Program.Cons(arr);

}
```

### Solution Code

```
using System;
using System.Linq;

public class Program
{
	public static bool Cons(int[] arr)
	{
		if(arr.GroupBy(t => t).Any(t => t.Count() > 1)) return false;
		int minimo = arr.Min();
		int maximo = arr.Max();
		for(int i = minimo + 1; i < maximo; i++){
			if(!arr.Contains(i)){
				return false;
			}
		}
		return true;
	}
}
```

### Alternative Solution Code

```
using System;
using System.Linq;

public class Program
{
	public static bool Cons(int[] arr)
	{
		if(arr.GroupBy(t => t).Any(t => t.Count() > 1)) return false;
		int minimo = arr.Min();
		int maximo = arr.Max();

		return maximo - minimo == arr.Length - 1;
	}
}
```

### Estimación
30 minutos

### Duración Real
30 minutos

