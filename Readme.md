**1281.Given an integer number n, return the difference between the product of its digits and the sum of its digits.**
**Решение:**
```cpp
class Solution {
public:
    int subtractProductAndSum(int n) {
        int product = 1;
        int sum = 0;
        while (n > 0) {
            int digit = n % 10;
            product *= digit;
            sum += digit;
            n /= 10;
        }
        return product - sum;
    }
};
```
**Задача:**
**1678.Given the string command, return the Goal Parser's interpretation of command.**
**Решение:**
```cpp
class Solution {
public:
    string interpret(string command) {
       string result = "";
for (int i = 0; i < command.size(); i++) {
if (command[i] == 'G') {
result += 'G';
} else if (command[i] == '(' && command[i+1] == ')') {
result += 'o';
i++;
} else if (command[i] == '(' && command[i+1] == 'a') {
result += "al";
i += 3;
}
}
return result; 
    }
};
```
**Задача:**
**2413.Given a positive integer n, return the smallest positive integer that is a multiple of both 2 and n.**
**Решение:**
```cpp
class Solution {
public:
    int smallestEvenMultiple(int n) {
        int ans = 2;
while (ans % n != 0) {
ans += 2;
}
return ans;
    }
};
```