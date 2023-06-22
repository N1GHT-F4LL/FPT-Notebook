<div align="center">
  <h1>MAD101 - Assignment 2</h1>
  <h2>Deadline: June 21, 2023</h2>
</div>

---

### Q1: Describe an algorithm for determining string of n characters is a palindrome.

```pseudo
   function isPalindrome(string):
   left = 0
   right = length(string) - 1
   while left < right do:
      if string[left] is not e### Qual to string[right] then:
         return false
      left = left + 1
      right = right - 1
   return true
```

### Q2: Describe an algorithm that determines whether a function from a finite set of integers to another finite set of integers is onto.

```pseudo
   function isOnto(function, domainSet, codomainSet):
      for element in codomainSet:
         found = false
         for input in domainSet:
               if function(input) == element:
                  found = true
                  break
         if found == false:
               return false
      return true
```

### Q3: Determine whether each of the functions ${2^{n + 1}}$ and $2^{2n}$ is $O(2^n)$

- **Hàm: ${2^{n + 1}}$**, ta có ${2^{n + 1}} = {2.2^n}$, vì 2 là một hằng số, ta có thể coi nó như hằng số c trong định nghĩa của $O(2^n)$.

Do đó, ${2^{n+1}}$ thuộc ${O({2^n})}$

- **Hàm: ${2^{2n}}$**, ta có Ta biết rằng tăng nhanh hơn .
  Vì vậy, không thuộc .
  Kết luận:
  • Hàm là vì nó tăng cùng tốc độ với .
  • Hàm không phải là vì nó tăng nhanh hơn so với .

### Q4: Find the least integer n such that is for each of these functions.

(a) The highest power of x in this function is x^3, which means that f(x) is O(x^3). Therefore, the least integer n for this function is n = 4.

(b) Luỹ thừa cao nhất của x trong hàm này là , nghĩa là Do đó, số nguyên n nhỏ nhất cho hàm này là .

(c) Trong trường hợp này, lũy thừa cao nhất của x ở cả tử số và mẫu số là . Khi chia hai số hạng này, sẽ triệt tiêu, để lại một giá trị không đổi là 1. Do đó, và số nguyên n nhỏ nhất cho hàm này là .

(d) Lũy thừa cao nhất của x ở tử số là và lũy thừa cao nhất của ở mẫu số là . Chia hai số hạng này ta được hay . Do đó, và số nguyên n nhỏ nhất cho hàm này là .

### Q5: Show that for all real numbers and with and , if , then

### Q6:

demo

### Q7:

### Q8:

### Q9:

### Q10:

### Q11:

### Q12:

### Q13:
