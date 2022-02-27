# OOPS_C#-_Interview-Questions

<ol>
  <li>
    <b> Object-oriented programming (OOP) </b>

  OOP is a technique to develop logical modules, such as classes that contain properties, methods, fields, and events. An object is created in the program to represent a class.     Therefore, an object encapsulates all the features, such as data and behavior that are associated to a class.
  </li>
  
  <li>
    <b>Class </b>
    
Class is a user defined data type, which consists of data & behaviour
Class data is represented by field and behaviour is represented by methods
It holds its own data members and member functions, which can be accessed and used by creating instance of that class

  
  </li>
  
   <li>
    <b>Object</b>

Object is They are instance of classes. It is a basic unit of a system. 
An object is an entity that has attributes, behavior, and identity. 
The new operator is used to create an object of a class. 
  
  </li>
  
<li>
    <b> Basic features of OOPs </b>
     
- Polymorphism 
- Inheritance 
- Encapsulation 
- Abstraction
</li>
  
<li>
<b>Polymorphism  </b>
     
Polymorphism means one name, many forms. One function behaves in different forms

There are two types of polymorphism:
     
- Static or compile time polymorphism
		The mechanism of linking a function with an object during compile time is called static binding.
		There are two techniques to implement static polymorphism:
     
   Function overloading
        Method overloading is a concept where a class can have more than one method with the same name and different parameters
        Operator overloading
     
- Dynamic or runtime polymorphism

  Run-time polymorphism is achieved by method overriding. Method overriding allows us to have methods in the base and derived classes with the same name and the same parameters
  
  </li>
  
<li>
 <b>Inheritance</b>
  
Acquiring the properties of one class into another class is called inheritance. Inheritance provides reusability by allowing us to extend an existing class
The inheritance concept is based on a base class and derived class.
  
- Base class - is the class from which features are to be inherited into another class.
- Derived class - it is the class in which the base class features are inherited.
  
Types of Inheritance:
  
- **Single inheritance **
In this type of inheritance one derived class inherits from only one base class.
	
    ![image](https://user-images.githubusercontent.com/29271635/150377971-66d3b295-3532-4c58-9aa7-b59001e89970.png)

	

- **Hierarchical inheritance**
In this type of inheritance, multiple derived classes inherit from a single base class.
    ![image](https://user-images.githubusercontent.com/29271635/150377762-902d4cea-14a4-49a6-bb46-30e3a346cad8.png)
 
 
- **Multilevel inheritance**
In this type of inheritance the derived class inherits from a class, which in turn inherits from some other class. The Super class for one, is sub class for the other.
 
    ![image](https://user-images.githubusercontent.com/29271635/150377604-fc1baff7-5bef-4b74-a667-c608b58e73da.png)

 
- **Multiple inheritance** 
In this type of inheritance a single derived class may inherit from two or more than two base classes.This inheritance is not supported by C#.
  
    ![image](https://user-images.githubusercontent.com/29271635/150377497-a6a1764f-cfda-4b6c-9112-9ca3df90e9d3.png)
	
</li>
<li>
	
**Why multiple inheritance is not possible in c#?**
	
Due to the diamond problem.The diamond problem is an ambiguity that arises when two classes B and C inherit from A, and class D inherits from both B and C  (Multiple inheritance). If a method in D calls a method defined in A (and does not override it), and B and C have overridden that method differently, then via which class does it inherit: B, or C?
	
</li>
<li>
	
**Abstraction**
	
Abstraction is process of exposing only the relevant and essential features of an object to outside the world. and encapsulate the unnecessary things. Hiding can be achieved by using "private" access modifiers.
	
</li>
<li>
	
**Encapsulation** 

Wrapping of Data Members and member functions into a single unit to prevent unwanted access is called Encapsulation. Encapsulation uses five types of Access modifiers to encapsulate data. These modifiers are public, private, internal, protected and protected internal

</li>
<li>
	
**Access Modifiers**
	
Access modifiers are keywords in object-oriented languages that set the accessibility of classes, methods, and other members

- **Public**
There are no restrictions on accessing public members.

- **Private**
Access is limited to within the class definition. This is the default access modifier type if none is formally specified.

- **Protected**
Access is limited to within the class definition and any class that inherits from the class.

- **Internal**
Access is limited exclusively to classes defined within the current project assembly.

- **Protected Internal**
Access is limited to the current assembly and any class that inherits previous assembly class. All members in current project and all members in derived class can access the variables.

</li>
<li>
	
**Function OverLoading**
Having two or more methods with same name but different parameters, is known as method overloading.
Method overloading in can be performed  by two ways:
By changing number of arguments
By changing data type of the arguments
By changing the order of arguments

</li>
<li>
	

**Function OverRiding**

If we inherit a class into the derived class and provide a definition for one of the base class's function again inside the derived class, then that function is said to be overridden, and this mechanism is called Function Overriding.

	class baseClass {

	    // show() is 'virtual' here
	    public virtual void show()
	    {
		Console.WriteLine("Base class");
	    }
	}
	class derived : baseClass
	{

	    //'show()' is 'override' here
	    public override void show()
	    {
		Console.WriteLine("Derived class");
	    }
	}

</li>
<li>

**Constructor**
	
Constructor(s) in a class is/are special methods which get called automatically when an object of a class is created. The main use of constructors is to initialize private fields of the class while creating an instance for the class. 
Some of the key points regarding the Constructor are:
 
A class can have any number of constructors.
A constructor doesn't have any return type, not even void.
A static constructor cannot be a parameterized constructor.
	
Within a class you can create only one static constructor. 
	
Constructors can be divided into **5** types:
	
- **Default Constructor** : A constructor without any parameters which is called automatically when we do not declare any constructor  is called a default constructor.

The default constructor initializes:
All numeric fields in the class to zero.
All string and object fields to null.
 
- **Parameterized Constructor** : A constructor with at least one parameter is called a parameterized constructor. This can also be called as constructor overloading.
Note: Default constructors always initialize the objects with the same values. In case we want to initialize the class with different values, we can use Parameterized constructors.
	
- **Copy Constructor**: The constructor which creates an object by copying variables from another object is called a copy constructor.It allows us to initialize a new object with the existing object values.
	
	  Person p1 = new Person(1, "Adrita", "Sharma", "Dimapur");//Instance constructor.
	  Person p2 = new Person(p1); // Copy Constructor

- **Static Constructor**: Static constructor is used to initialize the static data members of the class. A static constructor does not take access modifiers or have parameters.

	 class employee
	 {  
		static employee(){}
	 }
	
- **Private Constructor** : When a constructor is created with a private specifier, it is not possible for other classes to derive from this class, neither is it possible to create an instance of this class. They are usually used in classes that contain static members only. 
 
**Constructor Overloading **
We can overload constructor by creating another constructor with same method name and different parameters 
	
</li>
<li>
	
**Destructor**

A destructor is a special method for a class and is invoked automatically when an object is finally destroyed. 
In C# you can never call them, the reason is one cannot destroy an object. .NET frameworks Garbage Collector (GC) has the control over the destructor.  
The name of the destructor is also same as that of the class but is followed by a prefix tilde (~).

</li>
<li>
	
**Static Class**
	
A static class cannot be instantiated or inherited. Static classes provide static methods which can be used without creating instance of that class. Eg. calculation formula methods. ConvertToDollar()
	
</li>
<li>	
	
**Sealed Class**
	
A sealed class is a class that cannot be inherited by any class but can be instantiated. A sealed class is often used to encapsulate a logic that needs to be used across the program but without any alteration to it.
	
</li>
<li>
	
**Abstract Class**
	
Abstract class is a special type of class which cannot be instantiated (i.e we cannot create an object of an abstract class) and acts as a base class for other classes. It is defined using "abstract" keyword.
The purpose of an abstract class is to provide basic or default functionality as well as common functionality that multiple derived classes can share and override.
It should have at least one method defined as abstract.
	
</li>
<li>
	
**Abstract method**
	
When a class contains an abstract method, that class must be declared as abstract. The abstract method has no implementation and thus, classes that derive from that abstract class, must provide an implementation for this abstract method.

</li>
<li>
	
**Virtual method**
	
A class can have a virtual method. The virtual method has an implementation. When we inherit from a class that has a virtual method, we can override the virtual method and provide additional logic, or replace the logic with your own implementation.

</li>
<li>
	
**Interface**
	
An interface looks like a class, but has no implementation. It contains declarations of methods and/or properties. Interfaces are inherited by classes, that must provide an implementation for each interface member declared.

</li>
<li>
	
**Difference between Abstract Class and Interface**
	
- Abstract class can have implementation for some of it’s member but interface cannot have implementation for any of its member
- Abstract class members are private by default and can have Access modifiers. But Interface members are public default and cannot have access modifiers.
- An interface can inherit from an interface only and cannot inherit from any class, but abstract class can inherit from any other abstract class as well as Interface
- A class can inherit from multiple interface but not multiple class.
- Interface cannot have fields but Abstract class can have fields.
	
</li>
<li>
	
**Similarities between Abstract Class and Interface**
	
- We cannot create instance of Abstract class as well as Interface
- Both of them act as base type.
- Both of them are incomplete.

**Explicit interface implementation**
	
If we have a class that inherits 2 Interfaces that have the same method signature we use explicit interface implementation to distinguish between the methods.
	
	interface I1 {
	    void printMethod();
	}

	interface I2 {
	    void printMethod();
	}

	// class C implements two interfaces
	class C : I1, I2 {
	    // Explicitly implements method of I2
	    void I2.printMethod()
	    {
		Console.WriteLine("I2 printMethod");
	    }
	}
	
</li>	

<li>
	
**Delegate**
	
A delegate is a reference type variable that holds the reference to a method. The reference can be changed at runtime

The following Func delegate takes two input parameters of int type and returns a value of int type:

	Func<int, int, int> sum;
	
We can **assign any method to the above func delegate**
	that takes two int parameters and returns an int value.

Example: Func
	
	class Program
	{
	    static int Sum(int x, int y)
	    {
		return x + y;
	    }

	    static void Main(string[] args)
	    {
		Func<int,int, int> add = Sum;

		int result = add(10, 10);

		Console.WriteLine(result); 
	    }
	}
	
</li>	

<li>
	
**Generics**
	
Generic is a concept that allows us to define classes and methods with placeholder. C# compiler replaces these placeholders with specified Type at compile time. The concept of generics is used to create general purpose classes and methods.
To define a generic class, we must use angle <> brackets. The angle brackets are used to declare a class or method as generic type

	public T GetData(int index)
	

	
## Collection
	
![image](https://user-images.githubusercontent.com/29271635/154806151-88b1e4fb-48fb-487a-8b3c-108ad032f049.png)

	
<li>
	
- **IEnumerable**
	
An IEnumerable is a list or a container which can hold some items. We can iterate through each element in the IEnumerable. We **cannot edit** the items like adding, deleting, updating, etc.
We have to iterate over the elements to get the count of items.
	
- **ICollection**
	
ICollection derives from IEnumerable and extends it’s functionality to add, remove, update element in the list. ICollection also holds the count of elements
	
- **IList**
	
IList extends ICollection. An IList can perform all operations combined from IEnumerable and ICollection (iterate, add, update, remove), and some more operations like inserting or removing an element in the middle of a list
	
We should use IList when we need access by index to your collection, add, update and delete elements. IEnumerable when we just need to enumerate over the collection.
	
- **IQueryable**
	
IQueryable extends ICollection. An IQueryable generates a LINQ to SQL expression that is executed over the database layer
	
We use IQueryable when we want only required records to be returned to client from SQL. Here filter gets applied in RDBMS
	
If we use IEnumerable and add filter, all records will go to client side and then the filter will get applied in memory.
	
	IEnumerable<Employee> emps = db.Employees.Where(x => x.EmpId == 2).ToList()
	
	-- SQL Query in Profiler:
	SELECT * FROM EMPLOYEES
	
	IQueryable<Employee> emps = db.Employees.Where(x => x.EmpId == 2).ToList()
	
	-- SQL Query in Profiler:
	SELECT * FROM EMPLOYEES WHERE EmpId = 2
	
	
Difference between IEnumerable and IQueryable is where the filter logic gets executed. If we are working with collection that are connected to database, then use IQueryable.
If we are working with in memory data collection, use IEnumerable.
	
	
## Dependency Management
	
<li>
	
**Coupled Code**
	
- Tightly Coupled:
		Group of classes highly dependent on one another.
- Loosely Coupled:
		Reducing dependencies of a class that uses different classes directly.
- Advantages of Loosely Coupled:
		Code Reusability
		Easier to maintain
		Easier for Unit Testing

</li>	
<li>
	
**Inversion of Control (IoC)**
	
The term Inversion of Control (IoC) refers to a programming style where the flow of a program has been inverted. i.e ClassA doesn’t control its dependency (create or fetch ClassB object), Here, dependencies are instantiated by a framework or runtime and supplied to the desired class as needed.
	
In .NET 4.5
	
	var container = new UnityContainer(); 
	container.RegisterType<IFileSaver, FileSaverAWS>();
 
In .NET Core, ( ConfigureServices Method in startup.cs file)
	
	services.AddScoped(typeof(IFileSaver), typeof(FileSaverAWS));

### “Inversion of control is principal and Dependency Injection is implementation”.

</li>

<li>
	
**Dependency Injection**
	
Software Design pattern that allows us to develop loosely coupled code i.e Reduced dependency on class that use or inherit other classes.
Interfaces are used to implement loose coupling.
Classes communicate through (inherit) interface rather than classes.

 
Eg:
SaveFile Functionality.
	
UserController has a function to save files. A class is created FileSaver.cs which has a fn `SaveFile()`.
	
Without DI:
	
	class UserController {
		public UserController() {
		   FileSaver filesSaver = new FileSaver();
		}
	}
	
Without DI:
	
	class UserController {
	
		private readonly IFileSaver _filesSaver;

		public UserController(IFileSaver filesSaver) {
		   _filesSaver = filesSaver;
		}
	}
	

	
</li>	
<li>
	
**Life cycle of Dependency Injection (DI)**
	
To implement dependency injection, we need to configure a DI container with classes that is participating in DI. DI Container has to decide whether to return a new instance of the service or provide an existing instance. In startup class, we perform this activity on ConfigureServices method.

- AddTransient
Transient lifetime services are created each time they are requested. This lifetime works best for lightweight, stateless services.

- AddScoped
Scoped lifetime services are created once per request.

- AddSingleton
Singleton lifetime services are created the first time they are requested 
	
![image](https://user-images.githubusercontent.com/29271635/154804600-8ed9ee27-0977-4fda-80a0-7ce31534e8a0.png)

## Multi Threading
	
<li>
	
**Thread**
	
A thread is defined as the execution path of a program. Each thread defines a unique flow of control.
	
It is a basic unit of CPU utilization. Thread has its own program area and memory area . A thread of execution is the smallest sequence of programmed instructions that can be managed independently by a scheduler. Threads are built into operating system. The thread class from .NET is just a way to create and manage threads. Threads can themselves split into two or more simultaneously running tasks .	
</li>
	
<li>
	
**Task**
	
A task is an object that represents some work that should be done. The task can tell if the work is completed and if the operation returns a result, the task gives you the result.
</li>
	
<li>
	
**Multithreading**
	
Multithreading is a process in which multiple threads work simultaneously. It is a process to achieve multitasking. It saves time because multiple tasks are being executed at a time.	
</li>	
	
	

<li>	
	
**Concurrency** : Concurrency means executing multiple tasks on same core.We have time slicing. Given Some time to T1 and switch to giving time to T2
	
**Parallelism** : Parallelism means executing multiple tasks on multiple cores  (hardware - can be multiple core/machine)
	
Concurrency is used to make our code non blocking. If we have a background task, the other task should not hang. Parallelism enhances paerformance.
</li>	
	

</ol>
