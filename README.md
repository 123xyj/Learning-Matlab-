# Learning-Matlab-
day_1

matlab中许多问题可百度、谷歌、help+代码得到。  如： pi；e^->exp();  ln->log;  开平方根->sqrt;  abs->取绝对值;  mean->算平均值，默认以列计算，算法与cat类似；  rem(a,b)->取余数；  prod->数组元素乘积（其运算规律类似于max）等。
save/load (name).mat    //可保存/读取工作区变量。
variable name应以字母开头，用_连接。不能取key words，如：Inf；eps；ans；NaN；pi等。
使用whos查看变量性质。  clear （name） 清除（单个）变量。  format设置格式。  %为注释。

A=[1 2 3; 4 5 6; 7 8 9]    %创建矩阵A，；代表分行。
A(2,3)                     %第二行第三列的元素。若行列数超过原矩阵，则会使原矩阵变大，未赋值的元素为0。
A(1:3,3)                   %一至三行，第三列的元素组成的矩阵。
A=start:step:end           %创建行向量，start开始，步距为step，以end结束。
A([1 3])                   %以A的第1和第3个元素创建行向量，若[]里有；则分行。
A([1 3],[1 2])             %第1、3行，1、2列交集元素组成矩阵。
[A B]                      %A B矩阵合为新矩阵。

+ - * / 都适用。
A'：A转置。    若计算符号前有 . 代表做对应元素的计算。    A/B为A*B^(-1)，但matlab对于逆的运算为迭代，即使B行列式为0也有数值。

max(A)                  %将A每列最大值取出，组成新的行向量。可用max(max(A))计算矩阵A元素中的最大值。
sort(A)                 %将A以列分块，每列自上而下，从小到大排列。
sortrows(A)             %将A以每行为整体，以第一个元素，按照大小排列。
size(A)                 %查看A的行列数。其中：size(A,1)为A的行数，size(A,2)为A的列数。
length(A)               %查看A行列数的最大值。
find(condition)         %根据condition，查找矩阵内元素位置。

eye(n) %n阶单位矩阵;   diag([number number     ]) %对角矩阵;   zeros(n1,n2) %0矩阵;   ones(n1,n2) %元素全为1的矩阵;   rand(n1,n2) %随机数字矩阵。
