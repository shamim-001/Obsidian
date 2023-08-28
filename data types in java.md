# Data types
https://youtu.be/BGTx91t8q50?t=2896

```java
class Main {
    public static void main(String a[]) {
        byte b = 127;        // 8-bit signed integer
        short sh = 345;      // 16-bit signed integer
        int num = 500;       // 32-bit signed integer
        long l = 533455333;  // 64-bit signed integer

        float f = 5.8f;      // 32-bit floating-point
        double d = 5.89;     // 64-bit floating-point

        char c = 'k';        // 16-bit Unicode character

        boolean bool = true; // Represents true or false
    }
}
```


![[Pasted image 20230828073721.png]]
In Java, the `short` and `byte` data types are used to represent smaller integer values with less memory compared to `int` and `long`. Here are the ranges for `short` and `byte`:

1. **byte:**
   The `byte` data type is an 8-bit signed integer type. It can hold values from -128 to 127.

   - Minimum value: -128
   - Maximum value: 127

   Example:
   ```java
   byte minValue = -128;
   byte maxValue = 127;
   ```

2. **short:**
   The `short` data type is a 16-bit signed integer type. It can hold values from -32,768 to 32,767.

   - Minimum value: -32,768
   - Maximum value: 32,767

   Example:
   ```java
   short minValue = -32768;
   short maxValue = 32767;
   ```

It's important to note that using `byte` and `short` data types can be useful for saving memory when you know that the values you're working with fall within these ranges. However, if you're dealing with larger values or computations that might exceed these ranges, you should consider using the `int` or `long` data types to prevent data loss or unexpected behavior.

## Int
The range of values for a 32-bit `int` in Java is from -2,147,483,648 to 2,147,483,647 (inclusive). This range is symmetric around zero, so half of the values are positive and half are negative.

Here's the range breakdown:

- Minimum value: -2,147,483,648
- Maximum value: 2,147,483,647

You can declare an `int` variable and assign values within this range like this:

```java
int minValue = -2147483648;
int maxValue = 2147483647;
```

Attempting to assign a value outside this range to an `int` variable will result in a compilation error or unexpected behavior.

```java
int outOfRange = 2147483648; // This will cause a compilation error
```

If you need to work with larger numbers, you might consider using the `long` data type, which has a larger range. The `long` data type is a 64-bit signed integer and can hold values from approximately -9.2 quintillion to 9.2 quintillion.


![[Pasted image 20230828074304.png]]

![[Pasted image 20230828074458.png]]

![[Pasted image 20230828074618.png]]

![[Pasted image 20230828074701.png]]

