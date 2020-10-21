<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

#### [Home](/index.md)

## 15/10 - Homework 02

### INDEX
[Researches about theory (R)](#researches-about-theory-r)
 - [4_R.](#4_r)
 - [5_R.](#5_r)
 - [6_R.](#6_r)
 
[Applications / Practice (A)](#applications--practice-a)
 - [4_A.- 5_A.](#4_a-and-5_a)
 - [6_A.](#6_a)
 
[Researches about applications (RA)](#researches-about-applications-ra)
 - [3_RA.](#3_ra)

### Researches about theory (R)  
### 4_R.  
> Level of measurement or scale of measure is a classification that describes the nature of information within the values assigned to variables.

The levels of classification has been developed by Stanley Smith Stevens those levels are 4 in total: **nominal**, **ordinal**, **interval**, and **ratio**.
This is an overview of the differencies between the various levels:  

| Incremental progress | Measure property |Mathematical operators | Advanced operations | Central tendency |  
| :---: | :---: | :---: | :---: | :---: |  
| Nominal | Classification, membership | =, ≠ | Grouping | Mode |  
| Ordinal | Comparison, level | >, <|Sorting | Median |  
| Interval | Difference, affinity | +, − | Yardstick | Mean, Deviation |  
| Ratio | Magnitude, amount | ×, / | Ratio | Geometric mean, Coefficient of variation |    

We could group those 4 levels in 2 main categories, **Qualitative** and **Quantitative** measurements:
 - **Qualitative**
    - **Nominal level**:
    In Nominal level, the variables can be divided into categories, as for example AM or PM hours
    - **Ordinal level**:
    Same is for the Ordinal level, variables can be categorized, but in this case the categories must be ordered too, for example grades like A+(31), A(29-30), B(26-28), ecc
 - **Quantitative**
    - **Interval level**: 
    The interval level is useful to define a degree of difference between items (not ratio) with an arbitrary zero. We could think about it as a numerica range. An example could be the temperature, more precisely the Celsius scale with a defined freezing and boiling point of water.
    - **Ratio level**: A Ratio scale possesses a meaningful and non-arbitrary zero value and doesn't have any kind of interval. It consists in an estimation between the magnitude of a continuous quantity and a unit magnitude of the same kind, so it's an "how much" measurement (informally). An example could be the temperature or other measurements of this kind.  
    
As the 2 main groups says, we can say that the levels in the **Qualitative** group can give us informationa about the Quality of the variables (like grades as i said in the example above), *Nominal* level gives us a classification of the variables, the *Ordinal* level is more of a comparison instead. **Quantitative** group level gives us more information about differencies in quantity of the variables, like the *interval* level or a certain amount like *Ratio* level.
 - *Sources*: [Wikipedia]( https://en.wikipedia.org/wiki/Level_of_measurement)  

### 5_R.  
With the terms **Data repository** in a real world or entrprise environment, we could refer to various types of repository. The most common referral to an enterprise environment is strictly related to a giant data storage (central or distributed), where all the data and metadata of the company is handled and managed through *relational* (or *non relational* but those are less used) *databases*.

 - **Operational systems**: refer to a system that is used to process the day-to-day transactions of an organization that aims to work efficiently and in a way to preserve the integrity of the transactional data.
 - **Transactional systems (OLTP)**: information systems typically facilitate and manage transaction-oriented applications. With the term *transaction* we might mean both an atomic change of state in the realm of databases transactions or an exchange of economic entities in the realm of business and finance.
 OLTP typically can process all types of queries, contrairly to other systems like **OLAP**
 - **Data warehouse**: Is a system used for reporting and data analysis, and is considered a core component of business intelligence. are central repositories of integrated data from one or more disparate sources. The data may pass through an operational data store and may require data cleansing for additional operations to ensure data quality before it is used in the DW for reporting but it's generally uploaded by the operational systems.
 - **Data mart**: The data mart is a subset of the data warehouse and is usually oriented to a specific business line or team. Whereas data warehouses have an enterprise-wide depth, the information in data marts pertains to a single department. So we can think to a *Data mart* as a building block of a *Data warehouse*.
 - **Online analytical processing (OLAP)**: is an approach to answer multi-dimensional analytical queries swiftly in computing. Typical applications of OLAP include business reporting for sales, marketing, management reporting, and so on. OLAP consists of three basic analytical operations:  
     - consolidation (roll-up), 
     - drill-down,
     - slicing and dicing.

    OLAP is generally characterized by much more complex queries, in a smaller volume contrairly to *OLTP*.
 - **Online event processing (OLEP)**: is based on distributed event logs to offer strong consistency in large-scale heterogeneous systems, it allows for more flexible distribution patterns and higher scalability, but with increased latency and without guaranteed upper bound to the processing time.

![Map](/images/hw02/data.png)

### 6_R.  

The *Online* version of the arithmetic mean, is based on the concept of data stream; A *data stream* is a continuous stream of data which is manipulated and processed to obtain a certain result and the items in the data stream aren't stored in memory, the only thing that will be stored is the computation result and it will be continuously updated until the end of the data stream that can be finite or infinite. We can define the well known concept of arithmetic mean as:  

$$
\frac{1}{n}\sum_{i=1}^n a_i
$$  

the online version of it is slightly different, the main idea is that we already have a computed mean that we'll call $$\overline{X}_{n-1}$$, so we just need to multiply $$\overline{X}_{n-1}$$ for n-1 that is the length of the data stream we used to compute $$\overline{X}_{n-1}$$ itself, add the new value $$X_n$$ and then divide everything for n:  

$$
\frac{\overline{X}_{n-1}(n-1) + X_n}{n}
$$

A more concise way to describe the above formula is:

$$
\overline{X}_{n-1} + \frac{1}{n} (X_n - \overline{X}_{n-1})
$$

As known as *Knuth Formula* or *Running Mean*.  
The Knuth formula is preferable to the naive one because allows to less memory occupation and eliminates the floating point related errors, the possibility of the data elimination from the batch and is overall faster to compute.

[back to top](#home)

---

### Applications / Practice (A)

### 4_A. and 5_A.

I've implemented both the Discrete and Continuous variable in the same program and in both languages:
 - [C# program](https://drive.google.com/file/d/1CvxlvdQH61YgLEa7LMariGX_cKcO9hUS/view?usp=sharing)
 - [VB Program](https://drive.google.com/file/d/1uK28wVMJzwy66-xaKvoD3bqgr9oH6uIV/view?usp=sharing)

### 6_A.  

Using a Naive Mean algorithm implementation over, for example, the Kahan one, could lead to several problems which results in an error or a wrong/imprecise result.  
Talking about programming related problems, we could have:
 - Buffer overflow,
 - Data absorption/cancellation
 - Approximation problems over big numbers
I've developed a simple [**C# program**](https://drive.google.com/file/d/1zQAqkidPUFRTBRL_DESqp-9sAQMXby-z/view?usp=sharing) that will explain all the problems related to a Naive implementation over the Kahan one.  
 
[back to top](#home)

---

### Researches about applications (RA)
### 3_RA.

As said at point [6_A](#6_a) the numeric representation in the computer memory could generates an error propagation that leads to the dewscribed errors.  
 - **Buffer Overflow***: the Buffer Overflow error is strictly related to the numeric representation in memory; An integer value in C# is actually an *int32* if not differently specified; A Double value, uses 64bit by default instead; even Floats uses 32 bits.
 That means that if we try to write a Double value into a Float variable, this will most certainly lead to an overflow error, especially for large numbers, because the double value excess bits will be written **outside** the memory register allocated for the Float value.
 To avoid that, it's useful to know what are the lower/higher supported value for the various data types and using them accordingly.
 - **Data absorption**: It's a common *approximation* error that we can encounter when we sum/subtract two numbers of different magnitude.
 Let's take for example the sum of $$3.45E+100 + 120$$ will result 3.45E+100. In this case the 120 will appear to be totally ignored because it will be *absorbed* into the higer magnitude of 3.45E+100.
 - **Data cancellation**: This kind of problem will  happen when we want to subtract relatively big and similiar numbers. As demonstrated in the 6_A program, this error will appear like a bad approximation, and in fact it kind of is, it strictly depends on the data type used.
 - **Approximation**: With both really long decimals and big numbers, the approximation of the Naive implementation will lead to a loss of data and an obvuois wrong result, as shownin the 6_A program.

[back to top](#home)
