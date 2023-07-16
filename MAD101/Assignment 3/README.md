<div align="center">
  <h1>MAD101 - Assignment 3</h1>
  <h2>Deadline: July 21, 2023</h2>
</div>

---

### Q1: For which values of $n$ are these graphs bipartite?

a) ${K_n}$

Để $K_n$ là một đồ thị nhị phân hoàn chỉnh, có nghĩa là mỗi đỉnh không phải lá phải được được kết nối với 2 đỉnh khác và . Đồ thị hoàn chỉnh là đồ thị nhị phân khi và chỉ khi $n$ là số lẻ. Vì vậy, $n$ có thể là $1, 3, 5, 7, 9...$

$\Rightarrow K_n$ là graphs bipartite $\Leftrightarrow n \in \{ 2k+1 \, | \, k \in \mathbb{N}^* \}$

b) ${C_n}$

c) ${W_n}$

d) ${Q_n}$

### Q2:

### Q3:

### Q4:

### Q5:

### Q6:

### Q7:

### Q8:

### Q9:

### Q10:

```run
const eggs = 3.49, sourCream = 2.49, milk = 4.99
const gel = 19.99, vitamines = 17.99
const taxable = gel + vitamines
const tax = taxable * 6.25 / 100
const total = eggs + sourCream + milk + taxable + tax
console.log(`Total: $${Math.round(total * 100) / 100}`);
```
