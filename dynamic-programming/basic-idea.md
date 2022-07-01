# Basic Idea

### 动态规划基本思路：

* Base case
* 状态
* 选择
* dp 数组定义

Example:

比如说换零钱问题 (LC 322)。Base case是amount == 0 则不需要零钱，返回0。状态是amount (需要换的总额）。选择是换那种面额的零钱。dp数组定义为“dp\[amount]意为‘换amount需要的最少零钱数’”。

### 动态规划三个要素：

* 状态转移方程
* 重叠子问题
* 最优子结构

### 基本优化思路：

* 时间优化
  * 重叠子问题
    * 自顶向下（recursion）: memo
    * 自底向上：DP table
* 空间优化
  * 如果只需要用到部分DP table&#x20;
