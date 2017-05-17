May 17, 2017

This is a fork of King Wilder's dynamic linq project 
https://github.com/kahanu/System.Linq.Dynamic

You can copy the 'DynamicLinq.cs' and use it in your project, it is a single file that contains everything you need.

## Added methods

public static IQueryable<TResult> Select<TResult>(this IQueryable source, string selector, params object[] values)

Can be used to select dynamic types and cast them to a specific class.

public static class CustomLinq { }

Can be used to create your own user defined methods.

## Changed methods

The & and | operator are now bitwise operators if the left and right operand type is numeric.



## Future:

Next I will implement a method, that can handle static list creation. E.g.:


var resul = persons.Where("(new List<int>{22, 23, 31, 45}).Contains(Age)");

This is usefull if you want to create something like the where in clause in sql.
