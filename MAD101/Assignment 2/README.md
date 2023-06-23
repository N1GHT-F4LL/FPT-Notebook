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

1. **Hàm: ${2^{n + 1}}$**, ta có ${2^{n + 1}} = {2.2^n}$, vì 2 là một hằng số, ta có thể coi nó như hằng số c trong định nghĩa của $O(2^n)$.

Do đó, ${2^{n+1}}$ thuộc ${O({2^n})}$

2. **Hàm: ${2^{2n}}$**, ta có ${2^{2n} = ({2^n})^2}$

Vì ${({2^n})^2}$ tăng nhanh hơn ${2^n}$. Vì vậy ${2^{2n}}$ không thuộc ${O(2^n)}$.

#### Kết luận:

- Hàm ${2^{n + 1}}$ là ${O(2^n)}$ vì nó tăng cùng tốc độ với ${2^n}$.
- Hàm ${2^{2n}}$ không phải là ${O(2^n)}$ vì nó tăng nhanh hơn so với ${2^n}$.

### Q4: Find the least integer n such that is for each of these functions.

1. $f(x) = 2x^2 + x^3 \log(x)$

Luỹ thừa cao nhất của x trong hàm này là ${x^3}$ mà còn nhân với $log(x)$,có nghĩa là độ phức tạp của $f(x)$ lớn hơn $O(x^3)$ nhưng bé hơn $O(x^4)$. Do đó, số nguyên n nhỏ nhất cho hàm này là ${n = 4}$.

2. $f(x) = 3x^5 + (\log(x))^4$

Luỹ thừa cao nhất của x trong hàm này là ${x^5}$ , là độ phức tạp của $f(x)$ là $O(x^5)$ Do đó, số nguyên n nhỏ nhất cho hàm này là ${n = 5}$.

3. $f(x) = \frac{{x^4 + x^2 + 1}}{{x^4 + 1}}$

Trong trường hợp này, lũy thừa cao nhất của x ở cả tử số và mẫu số là 4. Khi chia hai số hạng này, sẽ triệt tiêu còn lại 1. Do đó độ phức tạp là $O(1)$, và số nguyên $n=1$.

4. $f(x) = \frac{x^3 + 5 \log(x)}{x^4 + 1}$

Lũy thừa cao nhất của x ở tử số là 3 và lũy thừa cao nhất của ở mẫu số là 4. Chia hai số hạng này ta được $\frac{1}{x}$ hay $x^{-1}$. Do đó, và số nguyên n nhỏ nhất cho hàm này là $-1$.

### Q5: Show that for all real numbers a and b with $a > 1$ and $b > 1$, if $f(x)$ is ${O(\log_b(x))}$, then $f(x)$ is ${O(\log_a(x))}$.

Để chứng minh rằng nếu $f(x)$ là $O(\log_b(x))$ với mọi số thực $a > 1$ và $b > 1$, thì $f(x)$ cũng là $O(\ log_a(x))$, ta cần chứng minh rằng tồn tại một hằng số dương $C$ và một số thực $x_0$ sao cho $|f(x)| \leq C \log_a(x)$ cho mọi $x \geq x_0$.

Giả sử rằng $f(x)$ là $O(\log_b(x))$, ta biết rằng tồn tại một hằng số dương $C'$ và một số thực $x_0'$ sao cho $|f(x)| \leq C' \log_b(x)$ với mọi $x \geq x_0'$.

Để chứng minh tuyên bố, ta có thể chọn $C = C'$ và $x_0 = x_0'$.

Bây giờ, hãy xem xét $x \geq x_0$. ta có:

$|f(x)| \leq C' \log_b(x)$ (từ giả thiết)

Vì $\log_b(x) = \frac{\log_a(x)}{\log_a(b)}$ (sử dụng đẳng thức logarit), nên ta có thể viết lại bất đẳng thức dưới dạng:

$|f(x)| \leq \frac{C'}{\log_a(b)} \log_a(x)$

Đặt $C = \frac{C'}{\log_a(b)}$, ta có:

$|f(x)| \leq C \log_a(x)$

Như vậy, ta đã chỉ ra rằng nếu $f(x)$ là $O(\log_b(x))$ với mọi số thực $a > 1$ và $b > 1$, thì $f(x)$ cũng là $ O(\log_a(x))$ cho tất cả $a > 1$.

### Q6: Evaluate these quantities.

1. $13 \mod 3$:

   Chia 13 cho 3 ta được thương là 4 và số dư là 1.

   Do đó, $13 \mod 3 = 1$.

2. $-97 \mod 11$:

   Chia -97 cho 11, ta được thương là -8 và số dư là 3.

   Do đó, $-97 \mod 11 = 3$.

3. $155 \mod 19$:

   Chia 155 cho 19, ta được thương là 8 và số dư là 3.

   Do đó, $155 \mod 19 = 3$.

4. $-221 \mod 23$:

   Chia -221 cho 23, ta được thương là -9 và số dư là 8.

   Do đó, $-221 \mod 23 = 8$.

### Q7: Show that if a, b, c, and m are integers such that $m\geq 2$, $c > 0$, and $a \equiv b(\mod m)$, then $ac \equiv bc (\mod mc)$.

Để chứng minh mệnh đề đã cho: nếu $a, b, c, m$ là các số nguyên sao cho $m \geq 2$, $c > 0$, và $a \equiv b (\mod m)$ thì $ac \equiv bc (\mod mc)$.

Ta bắt đầu bằng cách biểu diễn đồng dư đã cho $a \equiv b (\mod m)$ dưới dạng một phương trình, hàm ý rằng $a - b$ chia hết cho $m$. Ta có thể viết điều này như sau:

> $a - b = km$ với một số nguyên $k$.

Bây giờ, ta muốn chỉ ra rằng $ac \equiv bc (\mod mc)$. Điều này có nghĩa là ta cần chứng minh rằng $ac - bc$ chia hết cho $mc$. Hãy mở rộng phương trình:

> $ac - bc = c(a - b)$.

Thay thế biểu thức $a - b = km$ vào phương trình trên, ta có:

> $ac - bc = c(km)$.

Vì $c > 0$ và $m \geq 2$, ta có $c(km) = (ck)m$, điều này cho thấy rằng $ac - bc$ chia hết cho $mc$.

Do đó, ta có thể kết luận rằng nếu $a, b, c, m$ là các số nguyên sao cho $m \geq 2$, $c > 0$, và $a \equiv b (\mod m)$, thì $ac \equiv bc (\mod mc)$.

### Q8: Find each of these values.

1. $(192 \mod 41) \mod 9$

Đầu tiên, $192 \mod 41$. Chia 192 cho 41, được thương là 4 và số dư là 8.

Tiếp theo, $8 \mod 9$. Vì 8 đã nhỏ hơn 9 nên kết quả là 8.

Do đó, $(192 \mod 41) \mod 9 = 8$.

2. $(323 \mod 13)^2 \mod 11$

Đầu tiên, $323 \mod 13$. Chia 323 cho 13, được thương là 24 và số dư là 11.

Tiếp theo, $11^2 \mod 11$. Chia 121 cho 1, được thương là 11 và số dư là 0.

Do đó, $(323 \mod 13)^2 \mod 11 = 0$.

3. $(73 \mod 23)^2 \mod 31$

Đầu tiên, $73 \mod 23$. Chia 73 cho 23, được thương là 3 và số dư là 4.

Tiếp theo, $4^2 \mod 31$. Bình phương 4 được 16, và sau đó lấy modulo 31 kết quả là 16.

Do đó, $(73 \mod 23)^2 \mod 31 = 16$.

4. $(212 \mod 15)^3 \mod 22$

Đầu tiên, $212 \mod 15$. Chia 212 cho 15, được thương là 14 và số dư là 2.

Tiếp theo, ngoài: $2^3 \mod 22$. Lập phương 2 được 8, và sau đó lấy modulo 22 cho kết quả là 8.

Do đó, $(212 \mod 15)^3 \mod 22 = 8$.

### Q9: Use the Euclidean algorithm to find

> Thuật toán Euclide giúp chúng ta tìm ước chung lớn nhất bằng cách chia nhiều lần số lớn hơn cho số bé hơn và lấy phần dư cho đến khi số dư bằng 0. Sau đó, gcd là phần còn lại khác không cuối cùng gặp phải trong quy trình.

1. gcd(1, 5) = 1

$$
\begin{align*}
5 &= 1 \times 5 + 0 \\
1 &= 0 \times 1 + 1 \\
\end{align*}
$$

2. gcd(100, 101) = 1

$$
\begin{align*}
101 &= 100 \times 1 + 1 \\
100 &= 1 \times 100 + 0 \\
\end{align*}
$$

3. gcd(111, 201) = 3

$$
\begin{align*}
201 &= 111 \times 1 + 90 \\
111 &= 90 \times 1 + 21 \\
90 &= 21 \times 4 + 6 \\
21 &= 6 \times 3 + 3 \\
6 &= 3 \times 2 + 0 \\
\end{align*}
$$

### Q10: Prove that if $n$ is a positive integer such that the sum of the divisors of $n$ is $n + 1$, then $n$ is prime.

Để chứng minh rằng nếu $n$ là một số nguyên dương sao cho tổng các ước của $n$ là $n + 1$ thì $n$ là số nguyên tố, chúng ta có thể sử dụng phản chứng để chứng minh.

Giả sử rằng $n$ không phải là số nguyên tố. Điều này có nghĩa là $n$ có thể được phân tích thành hai số nguyên dương $a$ và $b$, trong đó $1 < a < n$ và $1 < b < n$. Vì vậy, chúng ta có thể viết $n = ab$.

Tổng các ước của $n$ có thể được biểu diễn như sau:

$1 + n + a + b$

Chúng ta biết rằng tổng các ước của $n$ bằng $n + 1$, vì vậy chúng ta có:

$1 + n + a + b= n + 1$

Rút gọn phương trình, ta có:

$a + b= 1$

Vì $a$ và $b$ là các số nguyên dương lớn hơn 1 nên tổng của chúng không thể bằng 1. Điều này mâu thuẫn với giả định của chúng ta.

Do đó, giả định ban đầu của chúng ta rằng $n$ không phải là số nguyên tố phải sai. Do đó, nếu tổng các ước của $n$ là $n + 1$, thì $n$ phải là số nguyên tố.

### Q11: Find the output of the recursive algorithm if input $n = 5$.

```
procedure f(n: integer):
   If n = 1 then return 2
      else return f(n − 1) · n;
```

1. Gọi hàm $f(5)$.
2. Vì $n = 5$ không bằng 1, chúng ta chuyển đến câu lệnh "else".
3. Trả về giá trị của $f(n - 1) \times n$, tức là $f(4) \times 5$.
4. Gọi hàm $f(4)$.
5. Vì $n = 4$ không bằng 1, chúng ta chuyển đến câu lệnh "else".
6. Trả về giá trị của $f(n - 1) \times n$, tức là $f(3) \times 4$.
7. Gọi hàm $f(3)$.
8. Vì $n = 3$ không bằng 1, chúng ta chuyển đến câu lệnh "else".
9. Trả về giá trị của $f(n - 1) \times n$, tức là $f(2) \times 3$.
10. Gọi hàm $f(2)$.
11. Vì $n = 2$ không bằng 1, chúng ta chuyển đến câu lệnh "else".
12. Trả về giá trị của $f(n - 1) \times n$, tức là $f(1) \times 2$.
13. Gọi hàm $f(1)$.
14. Vì $n = 1$ bằng 1, chúng ta trả về 2.
15. Thay thế $f(1)$ bằng 2, vậy $f(2) = f(1) \times 2 = 2 \times 2 = 4$.
16. Thay thế $f(2) = 4$ vào bước trước, vậy $f(3) = f(2) \times 3 = 4 \times 3 = 12$.
17. Thay thế $f(3) = 12$ vào bước trước, vậy $f(4) = f(3) \times 4 = 12 \times 4 = 48$.
18. Thay thế $f(4) = 48$ vào bước trước, vậy $f(5) = f(4) \times 5 = 48 \times 5 = 240$.

Vậy nên kết quả của thuật toán đệ quy trên với $n = 5$ là 240.

### Q12: How many positive integers not exceeding 100 are divisible by exactly one of 6 or 9?

Bước 1: Đếm số nguyên dương không vượt quá 100 chia hết cho 6.
Bội số lớn nhất của 6 không vượt quá 100 là $96 = 6 \times 16$. Vì vậy, có 16 số nguyên dương chia hết cho 6 và không vượt quá 100.

Bước 2: Đếm số nguyên dương không vượt quá 100 chia hết cho 9.
Bội số lớn nhất của 9 không vượt quá 100 là $99 = 9 \times 11$. Vì vậy, có 11 số nguyên dương chia hết cho 9 và không vượt quá 100.

Bước 3: Đếm số nguyên dương không vượt quá 100 chia hết cả cho 6 và 9.
Bội số chung lớn nhất của 6 và 9 không vượt quá 100 là $54 = 6 \times 9$. Vì vậy, có 1 số nguyên dương chia hết cho cả 6 và 9 và không vượt quá 100.

Bước 4: Số lượng tổng các số nguyên dương chia hết chính xác cho 6 hoặc 9 được tính bằng công thức: Tổng = Số lượng(chia hết cho 6) + Số lượng(chia hết cho 9) - Số lượng(chia hết cả cho 6 và 9)

Tổng = 16 + 11 - 1 $=> Tổng = 26$

Vậy có 26 số nguyên dương không vượt quá 100 mà chia hết chính xác cho một trong 6 hoặc 9.

### Q13: Find a recursive definition for the set of positive integers NOT divisible by 3.

```
function recursive_not_divisible_by_3(n):
    if n < 0:
        return set()
    elif n == 0:
        return {0}
    elif n % 3 == 0:
        s = recursive_not_divisible_by_3(n - 3)
        s.add(n - 1)
        s.add(n - 2)
    else:
        s = recursive_not_divisible_by_3(n - 1)
    return s
```
