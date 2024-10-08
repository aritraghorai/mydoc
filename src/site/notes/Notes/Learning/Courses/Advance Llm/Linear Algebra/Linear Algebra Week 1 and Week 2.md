---
{"dg-publish":true,"permalink":"/notes/learning/courses/advance-llm/linear-algebra/linear-algebra-week-1-and-week-2/"}
---

## Example Of Linear Algebra
![Linear Algebra Example.png](/img/user/assets/Linear%20Algebra%20Example.png)

***This is an classic Machine learning algorithm example where we implement linear regression.Using this algorithm we find the optimal value m and b.***

![Linear Algebra 2.png](/img/user/assets/Linear%20Algebra%202.png)


![Linear Algebra 3.png](/img/user/assets/Linear%20Algebra%203.png)

## Common Vector and matrix operation
### System Of linear equation
![Pasted image 20240820094927.png](/img/user/assets/Pasted%20image%2020240820094927.png)

![Linear Algebra System of sentense.png](/img/user/assets/Linear%20Algebra%20System%20of%20sentense.png)

1. First system two sentence contain two information so system is complete and non-singular.
2. System 2 Two sentence contain only single information so system is redundant and singular.
3. System 3 two sentence contain two different contradictory information so system is contradictory and singular.

### Sentence to equation
![Linear Algebra Sentence to equation.png](/img/user/assets/Linear%20Algebra%20Sentence%20to%20equation.png)

![Linear Algebra Q1.png](/img/user/assets/Linear%20Algebra%20Q1.png)

![Pasted image 20240820100156.png](/img/user/assets/Pasted%20image%2020240820100156.png)

### Type of System of equation
![Linear Algebra Types.png](/img/user/assets/Linear%20Algebra%20Types.png)

![Linear Algebra 22.png](/img/user/assets/Linear%20Algebra%2022.png)

### What is linear equation?
![Linear Algebra Example-1.png](/img/user/assets/Linear%20Algebra%20Example-1.png)

### Plot Of Linear equation
![Linear Algebra Plot.png](/img/user/assets/Linear%20Algebra%20Plot.png)

#### Unique solution
![Linear Algebra Unque Solution Plot.png](/img/user/assets/Linear%20Algebra%20Unque%20Solution%20Plot.png)
#### Infinite Solution
![Linear Algebra MS.png](/img/user/assets/Linear%20Algebra%20MS.png)

#### No Solution
![Linear Algebra NS.png](/img/user/assets/Linear%20Algebra%20NS.png)

![Linear Algebra Summert.png](/img/user/assets/Linear%20Algebra%20Summert.png)

### System of equation as matrix
#### Linear Dependence
![Linear Algebra Linear Dependent.png](/img/user/assets/Linear%20Algebra%20Linear%20Dependent.png)
#### Matrix are singular
![Linear Algebra Matix Singular.png](/img/user/assets/Linear%20Algebra%20Matix%20Singular.png)

![Linear Algebra.png](/img/user/assets/Linear%20Algebra.png)

![Linear Algebra-1.png](/img/user/assets/Linear%20Algebra-1.png)

![Linear Algebra-2.png](/img/user/assets/Linear%20Algebra-2.png)

### Determinant
![Linear Algebra Determinant.png](/img/user/assets/Linear%20Algebra%20Determinant.png)

![Linear Algebra Check Singular with determinant.png](/img/user/assets/Linear%20Algebra%20Check%20Singular%20with%20determinant.png)

#### 3 * 3 Matrix determinant
![Linear Algebra 3 * 3 Deterniannt.png](/img/user/assets/Linear%20Algebra%203%20*%203%20Deterniannt.png)


### Note 
**Determinant**:If Determinant value is 0 then matrix is singular else matrix is non singular.

## Solving System of linear equation Elimination Method
### Example Non Singular with Unique Solution
![Linear Algebra Sol 1.png](/img/user/assets/Linear%20Algebra%20Sol%201.png)

**Solution Steps**
1. Divide equation 1 by 5 and equation 2 with 4.
2. E1 - E2
3. By doing these we can get b=2
4. By putting b value E1 we can get a as 3.
### Example Where system is Singular(Redundant)
![Linear Algebra E2.png](/img/user/assets/Linear%20Algebra%20E2.png)

**Solution Steps** E stands for equation
1. Divide E2 with 2
2. We can see both equation is same.
3. So any value of a=x ,b will be 10-x
4. So the equation can have multiple solution.
### Example Where system is Singular(Contradictory)
![Linear Algebra E3.png](/img/user/assets/Linear%20Algebra%20E3.png)
 **Solution Steps**
 1. Divide E2/2
 2. E1-E2
 3. We can see 0=2 which is an contradiction.

### Solving Equation with 3 variable
![Linear Algebra E4.png](/img/user/assets/Linear%20Algebra%20E4.png)
**Problem**
To solve this equation.
1.  Divide each equation with coefficient of a
2. Use E1 to remove a from other two equation
3. Then we will have 2 equation.
![Linear Algebra S1E4.png](/img/user/assets/Linear%20Algebra%20S1E4.png)
4. Not From In 2 new equation divide by coefficient of b
5. Remove B from two new equation and get c value
![Linear Algebra S2E4.png](/img/user/assets/Linear%20Algebra%20S2E4.png)
6. Now put c value in previous equation and get b value
7. Now put b and c value first equation and get a value.
![Linear Algebra S3E4.png](/img/user/assets/Linear%20Algebra%20S3E4.png)

## Solving Linear equation with Matrix Row Reduction Or Gaussian elimination

![Linear Algebra-4.png](/img/user/assets/Linear%20Algebra-4.png)

### Row Operation
#### Switching Matrix : It Preserve singularity of an matrix
![Linear Algebra Switching Matrix.png](/img/user/assets/Linear%20Algebra%20Switching%20Matrix.png)

#### Multiply a row by non zero scalar
![Linear Algebra Multoply.png](/img/user/assets/Linear%20Algebra%20Multoply.png)

#### Adding a row to another row
![Linear Algebra Adding a row with another.png](/img/user/assets/Linear%20Algebra%20Adding%20a%20row%20with%20another.png)

### Rank Of a matrix

#### Rank in system of information
![Linear Algebra Rank Example.png](/img/user/assets/Linear%20Algebra%20Rank%20Example.png)

#### Rank in a system of equation
![Linear Algebra System Equation.png](/img/user/assets/Linear%20Algebra%20System%20Equation.png)

#### Rank and singularity
***If rank and rows number same the matrix is non singular**
![Linear Algebra Rank And Singularity.png](/img/user/assets/Linear%20Algebra%20Rank%20And%20Singularity.png)

#### Row echelon and Rank calculation
##### Row Echelon Calculate

**Row echelon for singular matrix**

![Linear Algebra Row Echolon.png](/img/user/assets/Linear%20Algebra%20Row%20Echolon.png)

**Row echelon for non singular matrix**

![Linear Algebra-5.png](/img/user/assets/Linear%20Algebra-5.png)


##### Row Echelon and rank
![Linear Algebra-6.png](/img/user/assets/Linear%20Algebra-6.png)

##  Gaussian Elimination Algorithm [link](https://www.youtube.com/watch?v=Gkit1hUTsX8)
1. Create Augmented matrix
![Linear Algebra Augmented Matrix.png](/img/user/assets/Linear%20Algebra%20Augmented%20Matrix.png)
2. Select a pivot and make the pivot as 1
![Linear Algebra S2.png](/img/user/assets/Linear%20Algebra%20S2.png)
3. Replace the new row with old row and make button two row as zero
![Linear Algebra Pivoting.png](/img/user/assets/Linear%20Algebra%20Pivoting.png)
4.Now we will be getting a matrix pivot row as 1 and other are will be 0
![Linear Algebra S34.png](/img/user/assets/Linear%20Algebra%20S34.png)
5. We will repeat all steps and make all diagonal element 1
![Linear Algebra Diagonal 1.png](/img/user/assets/Linear%20Algebra%20Diagonal%201.png)
6. We will use back substitution and cal one row with other 
![Linear Algebra BS.png](/img/user/assets/Linear%20Algebra%20BS.png)

7. With back substitution We make all other element aspect diagonal make 0
![Linear Algebra-7.png](/img/user/assets/Linear%20Algebra-7.png)

#### Summery
![Linear Algebra-8.png](/img/user/assets/Linear%20Algebra-8.png)


 [[Notes/Learning/Courses/Advance Llm/Linear Algebra/Linear Algebra Week 3\|Linear Algebra Week 3]]