NielsenIQ Aptitude Preparation - 100 MCQs

Short notes and 100 multiple-choice questions with answers and brief solutions where required.

---

Cover / Title: NielsenIQ - JR. Data Scientist Aptitude Prep

Sections:
1) Short notes for each JD area
2) 100 MCQs (A–E sections) with answers and solutions for quant/stat where required
3) Answer key summary

---

SHORT NOTES (Concise Study Sheet)

1) Python (Core & Advanced)
- Data structures: list (ordered, mutable), tuple (ordered, immutable), set (unordered, unique), dict (key->value), and list comprehensions: [expr for x in iterable if cond].
- OOPs: class defines attributes/methods; instance = object; inheritance allows subclass reuse/override; polymorphism = same interface, different implementations.
- Functional programming: lambda arg: expr (anonymous single-expression function); map(fn, iterable) returns iterator in Py3; filter(fn, iterable); reduce(fn, iterable) from functools.
- Advanced: decorators wrap functions: @decorator; generators use yield to produce sequence lazily; iterators implement __iter__ and __next__; exceptions via try/except/finally; create custom exceptions by subclassing Exception.
- File I/O & memory management: with open('file','r') as f; use json.load/dump and csv module or pandas.read_csv for structured files; shallow copy copy.copy() (references shared), deep copy copy.deepcopy() (recursive duplicate).

2) Pandas & NumPy
- NumPy arrays: ndarray with shape and dtype; vectorized operations are fast; broadcasting rules allow operations on compatible shapes.
- Indexing & slicing: arr[rows, cols], boolean masks; np.newaxis to change dims.
- Pandas DataFrame & Series: pd.read_csv(), Series is 1D, DataFrame is 2D. Use merge/on, join, pd.concat for combining tables. groupby + agg and pivot_table for reshaping.
- Data cleaning: df.dropna(), df.fillna(value), df.drop_duplicates(), df.astype(dtype) for conversions.
- Time series: pd.to_datetime(), set index to datetime, df.resample('M').mean(), rolling windows with .rolling().

3) Statistics & Probability
- Descriptive stats: mean, median, mode; variance = E[(X-μ)^2], sd = sqrt(variance); skewness measures asymmetry, kurtosis measures tailedness.
- Distributions: normal (continuous bell curve), binomial (discrete n trials, p success), Poisson (rare events, λ rate), uniform (equal probability).
- Inferential stats: CLT -> sample means approximate normal for large n; confidence interval: point estimate ± z*(σ/√n) or t*(s/√n) when σ unknown.
- Hypothesis testing: use appropriate test (z, t, chi-square, ANOVA); small p-value (<α) leads to rejecting H0; Type I error = α (false positive), Type II = β (false negative).
- Correlation & regression: Pearson measures linear correlation, Spearman measures rank (monotonic) correlation; linear regression fits y = β0 + β1 x via OLS, R^2 indicates fraction of variance explained.

4) Scikit-Learn (Machine Learning)
- Regression: LinearRegression (OLS), Ridge (L2 penalty), Lasso (L1 penalty). Evaluate with R^2, RMSE, MAE.
- Classification: LogisticRegression, DecisionTreeClassifier, RandomForestClassifier (ensemble), SVM, Naive Bayes.
- Metrics: confusion matrix (TP, TN, FP, FN), accuracy, precision = TP/(TP+FP), recall = TP/(TP+FN), F1 = 2*(prec*rec)/(prec+rec); ROC curve (TPR vs FPR) and AUC.
- Unsupervised: KMeans clusters into k clusters; PCA reduces dimensionality via eigen decomposition of covariance matrix.
- Pipelines & preprocessing: StandardScaler, MinMaxScaler, OneHotEncoder, train_test_split, cross-validation and hyperparameter search via GridSearchCV and Pipelines.

5) Quantitative Aptitude (Quant)
- Probability & Combinatorics: permutations nPr = n!/(n-r)!, combinations nCr = n!/(r!(n-r)!), Bayes theorem P(A|B) = P(B|A)P(A)/P(B).
- Data interpretation: read caselets/tables/graphs, compute percentages, growth rates, index numbers and ratios.
- Business Math: percentages, ratios, averages, profit & loss, simple/compound interest, mixtures & alligation.
- Algebra & series: Solve linear/quadratic equations, AP: a_n = a + (n-1)d, S_n = n/2*(2a+(n-1)d). GP: a*r^(n-1), S_n = a*(1-r^n)/(1-r) for r!=1.

---

100 MCQs (Organized by section) — Questions with answers and short solutions where applicable.

Section A — Python (Core & Advanced) — 25 questions
1. Which of the following is an immutable data type in Python?
A. list
B. dict
C. tuple
D. set
Answer: C

2. Given x = [1,2,3], which expression returns [2,3,4]?
A. [x[i]+1 for i in range(len(x))]
B. x+1
C. map(lambda a: a+1, x)
D. np.add(x,1)
Answer: A
Note: In Python 3, C returns a map object (iterator); to get a list wrap with list(). D requires x to be a numpy array.

3. Which method adds a key-value pair to a dictionary d?
A. d.add(k,v)
B. d.insert(k,v)
C. d[k] = v
D. d.put(k,v)
Answer: C

4. Which of the following defines a generator function?
A. def gen(): return [i for i in range(5)]
B. def gen(): yield from range(5)
C. def gen(): pass
D. gen = (i for i in range(5))
Answer: B

5. What does the following print?
def f(a, b=2):
    return a*b
print(f(3))
A. 6
B. 5
C. Error
D. None
Answer: A

6. Which is the correct way to open a file for writing text?
A. open('file.txt', 'r')
B. open('file.txt', 'w')
C. open('file.txt', 'rb')
D. open('file.txt', 'a+')
Answer: B

7. What does deepcopy do compared to copy?
A. Shallow copy
B. Only copies references
C. Recursively copies object graphs
D. Copies only immutable parts
Answer: C

8. Which decorator application is valid?
A. @staticmethod def f(): pass
B. def f(): @decorator pass
C. def @decorator f(): pass
D. decorator def f(): pass
Answer: A

9. Which is true about lambda in Python?
A. Can contain multiple statements
B. Must return None
C. Is an anonymous single-expression function
D. Can define class methods
Answer: C

10. Which will iterate over keys of dict d in insertion order (Python 3.7+)?
A. for k in d:
B. for k in d.keys():
C. list(d)
D. All of the above
Answer: D

11. What is the output of:
print([i for i in range(5) if i%2==0])
A. [1,3]
B. [0,2,4]
C. (0,2,4)
D. Error
Answer: B

12. Consider class inheritance:
class A: pass
class B(A): pass
Which is true?
A. B is a superclass of A
B. A is subclass of B
C. B inherits from A
D. None
Answer: C

13. Which exception is raised for division by zero?
A. ValueError
B. KeyError
C. ZeroDivisionError
D. TypeError
Answer: C

14. What does itertools.chain do?
A. Creates pipeline of decorators
B. Flattens multiple iterables into one sequence
C. Concatenates strings only
D. Splits iterables
Answer: B

15. Which statement creates a set from list l?
A. set(l)
B. {l}
C. [set(l)]
D. dict(l)
Answer: A

16. What is the right way to import only the sqrt function?
A. import math.sqrt
B. from math import sqrt
C. import sqrt from math
D. import math as sqrt
Answer: B

17. How to catch any exception but still access the exception object?
A. except e:
B. except Exception as e:
C. except Exception, e:
D. except:
Answer: B

18. For mutable default argument gotchas, which is recommended?
A. Use [] directly as default
B. Use None and set inside function
C. Use global variables
D. Use lambda default
Answer: B

19. What is list comprehension equivalent of:
res=[]
for i in arr:
    res.append(i*2)
A. [i*2 for i in arr]
B. (i*2 for i in arr)
C. {i*2 for i in arr}
D. None
Answer: A

20. What is the result of: "abc".upper() ?
A. "abc"
B. "ABC"
C. Error
D. None
Answer: B

21. Which statement converts string s to JSON object?
A. json.dumps(s)
B. json.loads(s)
C. json.parse(s)
D. json.to_obj(s)
Answer: B

22. Which is true about Python’s GIL?
A. Allows true parallel threads for CPU-bound code
B. Prevents multiple native threads executing Python bytecodes at once
C. Only applies to multiprocessing
D. Was removed in Python 3
Answer: B

23. Which code creates a class attribute vs instance attribute?
A. class C: x=1 ; def __init__(self): self.y=2
B. class C: def __init__(self): x=1
C. class C: def __init__(self): self.x=1 ; y=2
D. None
Answer: A

24. Which built-in function returns an iterator of pairs (index, value)?
A. enumerate()
B. zip()
C. iteritems()
D. map()
Answer: A

25. Which of the following statements about decorators is true?
A. They modify classes only.
B. They take a function and return a modified function.
C. They can not accept arguments.
D. They require inheritance.
Answer: B

Section B — Pandas & NumPy — 20 questions
26. Which returns a DataFrame from CSV?
A. pd.load_csv()
B. pd.read_csv()
C. pd.read()
D. pd.Load()
Answer: B

27. Given arr = np.array([[1,2],[3,4]]). What is arr.shape?
A. (1,2)
B. (2,2)
C. (4,)
D. (2,)
Answer: B

28. Which operation performs concatenation of two DataFrames vertically?
A. pd.concat([df1, df2])
B. df1 + df2
C. df1.append_columns(df2)
D. pd.merge(df1, df2)
Answer: A

29. Which pandas method removes rows with any missing values?
A. dropna()
B. fillna()
C. replace()
D. isnull()
Answer: A

30. What does df.groupby('col').mean() do?
A. Filters rows
B. Computes mean for each group of col
C. Sorts df by col
D. Pivots the table
Answer: B

31. How to one-hot encode categorical column 'cat'?
A. pd.get_dummies(df['cat'])
B. df['cat'].astype('category')
C. df['cat'].onehot()
D. sklearn.OneHotEncoder requires DataFrame
Answer: A

32. NumPy broadcasting: which shapes are compatible for addition?
A. (3,1) and (3,)
B. (2,3) and (3,2)
C. (3,4) and (2,4)
D. (3,2) and (3,)
Answer: A

33. Which will drop duplicate rows in df?
A. df.drop_duplicates()
B. df.remove_duplicates()
C. df.unique()
D. df.clean()
Answer: A

34. To parse a column 'date' to datetime:
A. df['date'] = pd.to_datetime(df['date'])
B. df['date'].astype('date')
C. df.parse_dates('date')
D. pd.parse(df['date'])
Answer: A

35. What does np.reshape(arr, (2,3)) do if arr has 6 elements?
A. Changes shape to (2,3)
B. Transposes arr
C. Sorts arr
D. Flattens arr
Answer: A

36. How to merge df1 and df2 on column 'id' keeping all rows from df1?
A. pd.merge(df1, df2, on='id', how='left')
B. pd.concat(df1, df2)
C. df1.join(df2)
D. df1 + df2
Answer: A

37. Which indexing returns first 5 rows of df?
A. df[:5]
B. df.head(5)
C. df.iloc[:5]
D. All the above
Answer: D

38. What does .apply() allow in pandas?
A. Apply custom function to series / rows / columns
B. Only built-in aggregations
C. Only vectorized ops
D. No effect
Answer: A

39. Which is fastest for elementwise numeric operations?
A. Python list + loop
B. np.array vectorized operations
C. pandas apply with Python function
D. map with lambda
Answer: B

40. The difference between loc and iloc:
A. loc uses integer positions, iloc uses labels
B. loc uses labels, iloc uses integer positions
C. Both identical
D. loc for arrays only
Answer: B

41. Which returns correlation matrix for df numeric columns?
A. df.corr()
B. df.cov()
C. df.correlation()
D. pd.corr(df)
Answer: A

42. To resample a time-indexed df to monthly mean:
A. df.resample('M').mean()
B. df.rolling('M').mean()
C. df.groupby('M').mean()
D. df.aggregate('M', 'mean')
Answer: A

43. Which loads a large CSV in chunks?
A. pd.read_csv(..., chunksize=10000)
B. pd.read_csv(..., iterator=True)
C. Both A and B
D. None
Answer: C

44. Which will convert categorical to codes?
A. df['cat'].cat.codes
B. pd.get_codes(df['cat'])
C. df.codes()
D. df['cat'].codes()
Answer: A

45. Which NumPy function computes dot product of two matrices A,B?
A. np.dot(A,B)
B. A.dot(B)
C. np.matmul(A,B)
D. All of the above
Answer: D

46. How to remove rows where column 'age' < 0?
A. df = df[df['age'] >= 0]
B. df.remove(df['age'] < 0)
C. df.drop(df['age'] < 0)
D. df.filter(df['age'] >= 0)
Answer: A

47. What does df.info() show?
A. Data types, non-null counts, memory usage
B. Statistical summary
C. Unique values only
D. Column names only
Answer: A

48. To change dtype of column 'x' to float:
A. df['x'] = df['x'].astype(float)
B. df['x'] = float(df['x'])
C. df.astype('float')
D. df.convert(float)
Answer: A

Section C — Statistics (State) & Probability — 20 questions
49. Sample mean of [2,4,6,8] is:
A. 4
B. 5
C. 5.5
D. 6
Answer: B
Solution: (2+4+6+8)/4 = 20/4 = 5

50. Variance of [1,1,1,1] is:
A. 0
B. 1
C. 0.25
D. Error
Answer: A

51. For a Normal distribution, about what percent of data lies within ±1 standard deviation?
A. 50%
B. 68%
C. 95%
D. 99.7%
Answer: B

52. A fair coin is tossed 3 times. Probability of exactly two heads:
A. 1/8
B. 3/8
C. 1/2
D. 3/4
Answer: B
Solution: C(3,2)*(1/2)^3 = 3/8

53. In binomial distribution with n=10, p=0.5, expected value (mean) is:
A. 2.5
B. 5
C. 10
D. 0.5
Answer: B

54. Poisson with λ=4, probability of 0 events:
A. e^-4
B. 4e^-4
C. 1 - e^-4
D. e^4
Answer: A
Solution: P(0)=e^{-λ} λ^0/0! = e^{-4}

55. CLT states that sample means approximate normal distribution as n→∞. True or False?
A. True
B. False
Answer: A

56. A two-sided 95% CI for mean with known σ uses z* =:
A. 1.28
B. 1.645
C. 1.96
D. 2.58
Answer: C

57. Which test is suitable to compare means of two independent small samples where population variance unknown?
A. Z-test
B. Paired t-test
C. Independent samples t-test (Student's t)
D. Chi-square
Answer: C

58. Which correlation measures monotonic relationship (not necessarily linear)?
A. Pearson
B. Spearman
C. Kendall
D. Both B and C
Answer: B

59. Hypothesis: p-value = 0.03 with α=0.05. Conclusion?
A. Fail to reject H0
B. Reject H0
C. Accept H0
D. Increase α
Answer: B

60. Chi-square test is used for:
A. Comparing means
B. Testing independence between categorical variables
C. Regression
D. Time series
Answer: B

61. If correlation coefficient r = 0.8, R² is:
A. 0.8
B. 0.64
C. 0.2
D. 1.0
Answer: B

62. For a continuous distribution, probability at an exact point is:
A. >0
B. 0
C. 1
D. Undefined
Answer: B

63. Which is NOT a property of a probability distribution?
A. Non-negative probabilities
B. Sum/integral = 1
C. Probabilities can be greater than 1
D. Defined over sample space
Answer: C

64. If two events are independent, P(A∩B) equals:
A. P(A)+P(B)
B. P(A)P(B)
C. P(A|B)
D. P(A)/P(B)
Answer: B

65. A dataset has skewness > 0 — distribution is:
A. Left-skewed (long tail left)
B. Right-skewed (long tail right)
C. Symmetric
D. Bimodal
Answer: B

66. For linear regression residuals should ideally be:
A. Uniformly distributed
B. Normally distributed with mean zero and constant variance
C. Increasing trend
D. Only positive
Answer: B

67. Which is true of Type I and Type II errors?
A. Increasing α reduces type I error but increases type II
B. Increasing α increases type I error and reduces type II error
C. α has no effect on type II
D. Type I is false negative
Answer: B

68. The sample standard deviation divides by:
A. n
B. n-1 (for unbiased sample sd)
C. n+1
D. 2n
Answer: B

69. Which scenario is suitable for ANOVA?
A. Comparing means of three or more independent groups
B. Comparing two correlated proportions
C. Testing variance equality only
D. Regression diagnostics
Answer: A

Section D — Scikit-Learn (Machine Learning) — 15 questions
70. Which estimator is used for linear regression in scikit-learn?
A. LogisticRegression
B. LinearRegression
C. RandomForestRegressor
D. KMeans
Answer: B

71. Which is L1 regularization?
A. Ridge
B. ElasticNet
C. Lasso
D. None
Answer: C

72. Which metric is appropriate for regression?
A. Accuracy
B. RMSE
C. Precision
D. ROC-AUC
Answer: B

73. For binary classification, which curve plots TPR vs FPR across thresholds?
A. Precision-Recall
B. ROC curve
C. Lift chart
D. Learning curve
Answer: B

74. Which algorithm is ensemble of decision trees using bagging?
A. AdaBoost
B. Random Forest
C. Gradient Boosting
D. KNN
Answer: B

75. Which is unsupervised for dimensionality reduction?
A. PCA
B. LDA
C. LogisticRegression
D. RandomForest
Answer: A

76. Which scikit-learn tool helps find best hyperparameters using cross-validation?
A. GridSearchCV
B. train_test_split
C. StandardScaler
D. Pipeline
Answer: A

77. Which scaler centers data to zero mean and unit variance?
A. MinMaxScaler
B. StandardScaler
C. RobustScaler
D. Normalizer
Answer: B

78. Which algorithm is instance-based (lazy learner)?
A. SVM
B. KNN
C. Decision Tree
D. Naive Bayes
Answer: B

79. What does one-hot encoding do to a categorical feature with k categories?
A. Replaces with a single integer
B. Creates k binary columns (or k-1)
C. Normalizes values
D. Drops the feature
Answer: B

80. Which is true about ROC AUC score of 0.5?
A. Perfect classifier
B. Random chance
C. Completely wrong classifier
D. Not defined
Answer: B

81. Which cross-validation method uses k folds and rotates?
A. Holdout
B. K-Fold CV
C. LOOCV
D. Bootstrap
Answer: B

82. Feature selection that uses model coefficients (Lasso) is:
A. Filter method
B. Wrapper method
C. Embedded method
D. Manual selection
Answer: C

83. For imbalanced classification, which approach helps?
A. Use accuracy only
B. Use AUC, precision/recall, resampling or class weights
C. Underfit model intentionally
D. Remove minority class
Answer: B

Section E — Quantitative Aptitude (Quant) — 20 questions
84. Permutations: Number of ways to arrange letters in "ABC" is:
A. 3
B. 6
C. 9
D. 12
Answer: B
Solution: 3! = 6

85. Combinations: Choose 2 from 5 =:
A. 10
B. 5
C. 20
D. 15
Answer: A
Solution: C(5,2)=5*4/2=10

86. If probability of event A is 0.3, and B is 0.4 independent, P(A and B) =
A. 0.12
B. 0.7
C. 0.9
D. 0.1
Answer: A

87. A trader bought at $200 and sold at $260. Profit % = ?
A. 30%
B. 25%
C. 20%
D. 40%
Answer: A
Solution: (260-200)/200 = 60/200 = 0.30 = 30%

88. If a:b = 3:4 and a+b = 28, what is a?
A. 12
B. 16
C. 9
D. 7
Answer: A
Solution: total parts = 7, a = 3/7 * 28 = 12

89. Average of 10 numbers = 20. One number 50 is removed → new average of 9 numbers?
A. 16.67
B. 18.89
C. 20
D. 23
Answer: A
Solution: total = 200, new total = 150, new average = 150/9 ≈ 16.666...

90. If sum of AP first 5 terms is 40 and first term a=2, common difference d = ?
A. 3
B. 4
C. 5
D. 2
Solution: S5 = 5/2 * [2a + (5-1)d] = (5/2)*(4 + 4d) = 10*(1+d) = 40 → 1+d = 4 → d = 3
Answer: A

91. If GP has a=2, r=3, third term is:
A. 6
B. 18
C. 9
D. 3
Answer: B
Solution: third term = a*r^2 = 2*9 = 18

92. A bag has 3 red, 2 blue, 5 green balls. Random pick one — probability it is blue?
A. 2/10
B. 1/5
C. Both same
D. 1/2
Answer: A (which equals 1/5)

93. Bayes: If disease prevalence 1%, test sensitivity 99%, specificity 95%, probability person has disease given positive test ≈ ?
A. ~16.7%
B. ~66%
C. ~50%
D. ~90%
Solution: P(D|+) = 0.99*0.01 / (0.99*0.01 + 0.05*0.99) = 0.0099/(0.0099+0.0495)=0.0099/0.0594≈0.1667
Answer: A

94. A line graph shows sales from 2018:100, 2019:120, 2020:90. Percent change 2019→2020 =
A. -25%
B. -10%
C. -30%
D. 15%
Solution: (90-120)/120 = -30/120 = -0.25 = -25%
Answer: A

95. If 3x + 5 = 17, x = ?
A. 4
B. 3
C. 2
D. 6
Answer: A
Solution: 3x = 12 → x = 4

96. Mixture: 10 liters of milk 40% and 20 liters 20% — final concentration?
A. (10*40 +20*20)/30 = 800/30 = 26.67%
B. 30%
C. 28%
D. 25%
Answer: A

97. A number series: 2, 5, 10, 17, 26, ? Next =
A. 37
B. 35
C. 34
D. 38
Answer: A
Solution: pattern n^2 + 1 → 6^2 + 1 = 37

98. Compound interest: Principal 1000, rate 10% annually, compounded annually, amount after 2 years:
A. 1210
B. 1200
C. 1100
D. 1000
Solution: 1000*(1.1)^2 = 1210
Answer: A

99. If a train covers 180 km in 3 hours, speed =
A. 60 km/h
B. 50
C. 90
D. 70
Answer: A

100. If probability that a product is defective is 0.02, in batch of 50 expected defects ≈
A. 1
B. 2
C. 0.02
D. 50*0.98
Solution: expectation = n*p = 50*0.02 = 1
Answer: A

---

Answer Key Summary (Question:Answer)
1:C 2:A 3:C 4:B 5:A 6:B 7:C 8:A 9:C 10:D 11:B 12:C 13:C 14:B 15:A 16:B 17:B 18:B 19:A 20:B 21:B 22:B 23:A 24:A 25:B
26:B 27:B 28:A 29:A 30:B 31:A 32:A 33:A 34:A 35:A 36:A 37:D 38:A 39:B 40:B 41:A 42:A 43:C 44:A 45:D 46:A 47:A 48:A
49:B 50:A 51:B 52:B 53:B 54:A 55:A 56:C 57:C 58:B 59:B 60:B 61:B 62:B 63:C 64:B 65:B 66:B 67:B 68:B 69:A
70:B 71:C 72:B 73:B 74:B 75:A 76:A 77:B 78:B 79:B 80:B 81:B 82:C 83:B
84:B 85:A 86:A 87:A 88:A 89:A 90:A 91:B 92:A 93:A 94:A 95:A 96:A 97:A 98:A 99:A 100:A

---

File notes:
- I created two files in this commit: a Markdown file with the full content (this file) and a .docx file with the same textual content (plain UTF-8 text saved with .docx extension). If you need a true Word .docx binary file (with docx internal XML structure), tell me and I will generate a proper .docx binary and push it instead.

