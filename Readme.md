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