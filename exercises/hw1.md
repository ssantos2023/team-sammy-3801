
1. What is meant by filtering a list? Give an example that uses a built-in filter function in the language of your choice.

Filtering means to "filter" out certain elements of a list, leaving you with a desired subset of the original list. 
```
nums = [1, 2, 3, -1, -2, -3]

def is_positive(n):
  return n > 0

filtered_nums = list(filter(is_positive, nums))

print(nums)
print(filtered_nums)
```
2. Give a compact Julia expression for the array just like the array called numbers except that every value is cubed. Use broadcasting.
```
numbers .^ 3
```
3. What is meant by the phrase “pragmatics of programming languages”?

"Pragmatics of programming languages" refers to the aspects of programming languages that impact the actual programmers in a real world context. For example, in spoken language, a pragmatic convention we use is implying an answer by giving context ("Are you hungry?" "I just ate"). In programming language, a pragmatic consideration might be a designer choosing to make their language resemble English as close as possible for beginners (Python) or focusing on  memory management for maximum efficiency ( C ).

4. Explain, in detail, this fragment of K: {+/x[&x!2]^2}

x!2 means x mod 2, and will return 0 if even, 1 if odd for every number in the list x

& returns the indices of a list where the element is true, which is in this case 1.

x[&x!2] then becomes the list x, but only the indices that were marked as true, which are all the odd elements.

^2 then squares every element.

Finally, +/ takes the sum of all elements.

So as an example:
[1, 2, 3] becomes [1, 0, 1] then [0, 2] then [1, 3] then [1, 9] then [10]

5. What does the term object-orientation mean today? What did it originally mean?

 Object orientation means a type of programming centered around features such as classes, objects, and inheritance. Originally, it was a system of autonomous, interacting objects that communicate via passing messages.

6. What characters comprise the following string: ᐊᐃᓐᖓᐃ? List the code point and name of each character that appears, in order. What is the meaning of the string, assuming its intended context?

U+140A CANADIAN SYLLABICS A 
U+1403 CANADIAN SYLLABICS I
U+14D0 CANADIAN SYLLABICS FINAL N
U+15D3 CANADIAN SYLLABICS NNGAA
U+1403 CANADIAN SYLLABICS I

Ainngai is a greeting similar to hello in Inuktitut, a Canadian Inuit language.

7. What is the difference between control flow and concurrency?

Control flow refers to the order in which blocks of code are executed in a program. For example, where the program go after checking an if statement or the condition of a for loop. Concurrency refers to a program being capable of dealing with multiple tasks simultaneously, meaning when multiple control flows are running at the same time.

8. How do machine and assembly languages differ? Give an example that is different from the one seen in class.

Machine language is the raw binary that a CPU executes directly, while Assembly language is an interpretation of machine language using a handful of mnemonics and words to replace some of the binary.

Example of a machine language function and corresponding assembly language
```
10110000 00000101    ; load 5 into register
10110001 00000110    ; load 6 into register
00000001 11000000    ; add registers
mov al, 5
mov bl, 6
add al, bl
```
9. We saw, in class, a function that computed either 3n+1 or 4n-3 depending on whether n is even or odd. Write this function in a programming language not seen in class.

C# version of the function
```
class Program
{
    static int transform(int n)
    {
        if (n % 2 == 0)
        {
            return 3 * n + 1;
        }
        else
        {
            return 4 * n - 3;
        }
    }
    static void Main()
    {
        int[] testValues = { 1, 2, 3, 4 };
        foreach (int n in testValues)
        {
            Console.WriteLine($"transform({n}) = {transform(n)}");
        }
    }
}
```
10. The language Verse is billed as a functional-logic programming languages. Write a short paragraph about Verse, including its creator, year of creation, why it was created, and what exactly “functional-logic” means.

Verse is a functional-logic programming language developed by Epic Games in 2023. The team includes Simon Peyton Jones, Tim Sweeney, Lennart Augustsson, Guy Steele, Olin Shivers, Ranjit Jhala, Koen Claessen, and Joachim Breitner. It was released to be the base for environments within the game of Fortnite. Verse allows users to write high level “functional-logic” code that combines functional and logical programming.