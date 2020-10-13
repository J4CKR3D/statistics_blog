## 08/10 - Homework 01

### Researches about theory (R)
#### **1_R.** 
[Wikipedia](https://en.wikipedia.org/wiki/Statistical_population) describes Statistical population as follows
> In statistics, a population is a set of similar items or events which is of interest for some question or experiment. A statistical population can be a group of existing objects (e.g. the set of all stars within the Milky Way galaxy) or a hypothetical and potentially infinite group of objects conceived as a generalization from experience (e.g. the set of all possible hands in a game of poker). A common aim of statistical analysis is to produce information about some chosen population. 

So we can define statistical population as a set of similiar existing or hypotetical object/events which study of the related data seems interesting for questions/experiments

In **descriptive statistics**, the population is intented to be a set of object on wich features will be noted and organized and used for the data analysis. In descriptive statistics, *dataset* is usually a precise description of the population attributes.

In **inferential statistics**, the population is actually composed just by a sample (so a subset) of the larger group, on wich data is harvested and used for the inference of the entire population. The main difference is that inferential statistics creates it's *dataset* only on a sample of the population and uses that data (known) to infer on the whole population (unknown). 

The main differneces in the two population is that:  
  - Descriptive Statistics analyze data and describes statistics of the entire population,  
  - On the other hand Inferential statistics aims to analyze data of a sample to make (as the name says) inference on the entire population.  
  
#### **2_R.**  
  -  We can describe **statistical attributes** as a specific characteristic of an object, like age, weigth or height;  
  - **statistical variables** on the other hand are logical sets of attributes that (as the name suggests) may vary, those can be conisdered a representation of attributes for a further data processing;  
  The two terms are *interchangeable* anyway.
  - With the term **Dataset** we describe a collection of data organized (usually) as a table, each column corresponds to a *variable* and each row corresponds to a given member of the dataset.  
  
#### **3_R.**  
   - A **univariate dataset** consists in a single attribute dataset, so we will have a single column table containing just the attribute we want to examine; For example, if we want to create a univariate dataset containing the weights of 10 apples we use the weight attribute of the apple to create the 1 column-10 rows dataset containing the data.
 - The number of occurence of a specific value for a specific attribute is known as **frequency ditribution**.  
 For example, we have this weight array (in grams):  
 ```w={22.0, 32.2, 44.3, 32.2, 21.9, 32.3, 22.0}```  
 we know that the distribution of 32.2 is 3/7.


  - Actually no, wen we use the dataset to create a distribution frequency, we lose part of the information.

 - The difference between the two amounts of data is actually considerable, in the dataset we have a **complete** correlation betwen attribute values and statistical units, on the other hand with the distribution we have a concise and brief version of the same data but with a loss in the correlation between statistical units and related values (as said in the previous point). We gain knowledge by losing information.

### Applications / Practice (A)
#### **1_A.**
  - [C# zip file](https://drive.google.com/file/d/1R2cDsJLh_hcP5wOe_d0STyCQVivkWqmY/view?usp=sharing)  
  - [VB.NET zip file](https://drive.google.com/file/d/1NY1Byu0iRMpn7ZTiBgfmChd4ixgGHpZA/view?usp=sharing)  
    
#### **2_A.**  
> A **Value Type** stores its contents in memory allocated on the stack. When you created a Value Type, a single space in memory is allocated to store the value and that variable directly holds a value. If you assign it to another variable, the value is copied directly and both variables work independently. Predefined datatypes, structures, enums are also value types, and work in the same way. Value types can be created at compile time and Stored in stack memory, because of this, Garbage collector can't access the stack.  
 
 ```
 #include <stdio.h>

int main(void){
    
    int a, b;
    
    // Here we are assigning the VALUE of b to a
    a = b;
    
    printf("a: %d, b:%d", a, b);
    
    b = 10;

    printf("a: %d, b:%d", a, b);
    
    return 0;
}
```  
The output of the code above is:
``` 
"a: 0; b: 0"
"a: 0; b: 10"
```  
In this case we are passing to a the **value** of b, so even if the value of b will be changed, the value of a will remain untouched since the last assignment.

> Reference Types are used by a reference which holds a reference (address) to the object but not the object itself. Because reference types represent the address of the variable rather than the data itself, assigning a reference variable to another doesn't copy the data. Instead it creates a second copy of the reference, which refers to the same location of the heap as the original value. Reference Type variables are stored in a different area of memory called the heap. This means that when a reference type variable is no longer used, it can be marked for garbage collection. Examples of reference types are Classes, Objects, Arrays, Indexers, Interfaces, **Pointers** etc.  

```
 #include <stdio.h>

int main(void){
    
    int b = 0;
    
    // Here we are assigning the memory address of b to te pointer p
    // and this is actually a 'passing by reference' scenario
    int *p = &b;
    
    printf("b:%d, p:%d", b, *p);
    
    b = 10;

    printf("b:%d, p:%d", b, *p);
    
    return 0;
}
```  
The output of the code above is:
``` 
"b: 0; p: 0"
"b: 10; p: 10" 
```  
so we can easily see that even without touching directly the pointer's value (but the varaible b instead), the pointer's value has been changed.  
Definitions source: [net-informations.com](http://net-informations.com/faq/general/valuetype-referencetype.htm)  

#### **3_A.**
  - I've implemented the Drag&Drop function in both the programs at point 1_A 

### Researches about applications (RA)
#### **1_RA.** 
 - The **C#** program deals with events handlers using a separate (form.designer.cs) file from the function's file (form.cs), in which it defines form's components position and dimensions and, for each component, it creates an array of handlers each one with a related function (defined in the function's main file).
 - The **VB.NET** program uses the same function's file instead, specifying in the signature, wich type of event that function will handle.
In my opinion the best approach among the two is the C# one, it's more structured and well defined even if less intuitive; On the other hand, the VB approach is faster, more user friendly and can let you spot a mistake in the event handling more easily.  
 
#### **2_RA.**  
 - In **C#**, the Program.cs file is the main file executed when we run the application.
The C# program uses form.designer.cs file, that (as said on the previous point) is file where the form's components are first initialized with the related positions and dimensions. Lastly (in this case) there is a Form.cs file, this is a Windows module class file where the functions are declared and defined.

 - In **VB.NET** we can find the form.Designer.vb file too, which the primary purpose is the same as the C# one, to initialize all the form's components.
 As said before, the events are declared and handled in the function's signature into the form.vb file. [starting point?]
 
