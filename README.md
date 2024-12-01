# crossover-tournament


![Screenshot 2024-12-01 220756](https://github.com/user-attachments/assets/55a74936-4988-4b33-8a72-11e8d75b477e)


please call on +917038344755 to get the answer (in javascript)



Consider a string that consists of the characters < and > only. The string is balanced if each < always appears before (i.e., to the left of) a corresponding > character. They do not need to be adjacent. Moreover, each < and > acts as a unique pair of symbols and neither symbol can be considered as part of any other pair of symbols.

To balance a string, any > character can be replaced with <>. Givert an expression and a maximum number of replacements, determine whether the string can be balanced.

Example

expressions = ['<<>>', '<>', '<><>', '>>', '<<>', '><><']
maxReplacements = [0, 1, 2, 2, 2, 2]

Process a series of expressions and their corresponding maxReplacements. Each of the first three expressions is balanced already. The string expressions[3] = '>>'can be balanced in two moves by replacing each > with a <> to make <> <>. Neither of the last two strings can ever be balanced.

Function Description

Complete the function balancedOrNot in the editor below.

balancedOrNot has the following parameter(s): string expressions[n]: the strings to check int maxReplacements[n]: the maximum number of replacements available for each expressions[i]

Returns:

int[n]: each element[i] contains a 1 if expressions[i] is balanced or a 0 if it is not

Constraints

1) 1≤ n ≤ 10^2

2) 1 ≤ length of expressions[i] ≤ 10^5

3) 0 ≤ maxReplacements[i] ≤ 10^5

▼Input Formal for Custom Testing

Input from stdin will be processed as follows and passed to the function.

The first line contains an integer n, the size of the array expressions.

The next n lines each contain a string,expressions[i].

The next line contains an integer n, the size of the array maxReplacements.

The next n lines each contain an integer, maxReplacements[i].


▼ Sample Case 0

Sample input

STDIN         Function

-------       ----------------
2         →   expressions[] size n = 2

<>>>      →   expressions = ['<>>>', 
'<>>>>']
<>>>>

2         →   maxReplacements [] size n = 2

2         →   maxReplacements = [2,2]

2

Sample Output

1
0


Explanation

0. For the string <>>> with maxReplacements[0] = 2, it becomes balanced after two replacements: <>>>  → <><>> → <><><>. The string was converted in  ≤ maxReplacements[0] replacements. Store a 1 in index O of the return array.

1. For the string <>>>> with maxReplacements[1] = 2, it becomes balanced after three replacements: <>>>> → <><>>>  → <><><>> → <><><><>. There were not enough replacements available, so store a O in index 1 of the return array.

Return the array [1, 0] as the answer.

▼ Sample Case 1

Sample Input

STDIN        Function
-----        ---------

2       →    expressions[] size n = 2

<>      →    expressions = ['<>', '<>>

<']

<>><

2       →    maxReplacements[] size n = 2

1       →    maxReplacements = [1, 0]
0

Sample Output

1

0

Explanation

0. For the string <> with maxReplacements[0] = 1.
it is already balanced and needs no replacements. Store a 1 in index O of the return array.

1. For the string <>>< with maxReplacements[1] = 0, the string is not balanced. It is impossible to balance the string because it ends in < and because there are O replacements available. Store a O in index 1 of the return array.

Return the array [1, 0] as the answer.

▼ Sample Case 2

Sample Input

STDIN        Function
-------      ----------
1         →  expressions[] size n = 1

<<<><><>  →  expressions = ['<<<><><>']

1         →  maxReplacements[] size n = 1

2         →  maxReplacements = [2]

Sample Output

0

Explanation

0. For string <<<><><> with maxReplacements[0] = 2, the string is not
balanced. It is impossible to balance because there are more < than >. Store a O in index O of the return array.

Return the array [0] as the answer.





