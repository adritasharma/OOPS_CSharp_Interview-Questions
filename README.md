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
		
	
</ol>
