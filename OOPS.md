# 📘 OOPs Interview Notes (Quick Revision)

## 📑 Table of Contents
- [1. What is OOPs?](#-1-what-is-oops)
- [2. Programming Paradigms](#-2-programming-paradigms)
- [3. Class & Object](#-3-class--object)
- [4. Memory Concept](#-4-memory-concept-important-)
- [5. 4 Pillars of OOPs](#-5-the-4-pillars-of-oops)
- [6. Types of Inheritance](#-6-types-of-inheritance)
- [7. Access Modifiers](#-7-access-modifiers)
- [8. Constructors & Destructors](#-8-constructors--destructors)
- [9. this & super](#-9-this--super)
- [10. Static & Final](#-10-static--final)
- [11. Abstract Class vs Interface](#-11-abstract-class-vs-interface)
- [12. Shallow vs Deep Copy](#-12-shallow-vs-deep-copy)
- [13. Composition vs Inheritance](#-13-composition-vs-inheritance)
- [14. Important Interview Concepts](#-14-important-interview-concepts)
- [15. Interface Special Points](#-15-interface-special-points)
- [16. Static Block](#-16-static-block)
- [17. Tight vs Loose Coupling](#-17-tight-vs-loose-coupling)
- [18. Getter & Setter](#-18-getter--setter)
- [19. Additional Important Concepts ⭐](#-19-additional-important-concepts-)
- [20. Rapid Fire](#-20-rapid-fire-)
- [21. Final Revision](#-21-final-one-liner-revision-)

---

## 🟦 1. What is OOPs?
Object-Oriented Programming is a paradigm where programs are designed using objects containing data and methods.

👉 One-line:
"OOP is a way of structuring programs using objects interacting with each other."

---

## 🟦 2. Programming Paradigms
- Monolithic → everything in one block  
- Procedural → functions (C language)  
- OOP → objects + real-world modeling  

---

## 🟦 3. Class & Object
Class → Blueprint  
Object → Instance  

💻 Example:
```java
class Car {
    String brand;
    void drive() {
        System.out.println("Driving...");
    }
}
```
---

## 🟦 4. Memory Concept (IMPORTANT 🔥)
- Class → no memory (just blueprint)  
- Object → stored in Heap  

👉 Memory Breakdown:
- Stack → local variables + references  
- Heap → actual objects  

👉 Memory allocation happens when constructor is called  

---

## 🟦 5. The 4 Pillars of OOPs

🔐 Encapsulation  
Binding data + methods and hiding data using private access.

☁️ Abstraction  
Show WHAT, hide HOW.

🧬 Inheritance  
Reuse code using parent-child relationship.

🎭 Polymorphism  
Same method behaves differently.

---

## 🟦 6. Types of Inheritance
- Single  
- Multilevel  
- Hierarchical  
- Multiple (via interface)  
- Hybrid  

⚠️ Java does NOT support multiple inheritance via class (Diamond Problem)

---

## 🟦 7. Access Modifiers
- public → everywhere  
- protected → package + subclass  
- default → same package  
- private → class only  

🏠 Example:
public = main gate  
private = bedroom  

---

## 🟦 8. Constructors & Destructors

Constructor:
- Same name as class  
- No return type  
- Called automatically  

Types:
- Default  
- Parameterized  
- Copy  
- Private  

Destructor:
- Java → Not present (Garbage Collector handles memory)  

---

## 🟦 9. this & super
- this → current object reference  
- super → parent class reference  

---

## 🟦 10. Static & Final

Static:
- Belongs to class  
- Shared among objects  

Final:
- variable → constant  
- method → cannot override  
- class → cannot inherit  

---

## 🟦 11. Abstract Class vs Interface

Abstract Class:
- Can have both abstract + normal methods  

Interface:
- Only method declarations (contract)  

👉 Use abstract when:
Common base exists  

👉 Use interface when:
Unrelated classes follow same rule  

---

## 🟦 12. Shallow vs Deep Copy

Shallow Copy:
- Copies reference  
- Same memory  

Deep Copy:
- Creates new object  
- Different memory  

---

## 🟦 13. Composition vs Inheritance

Inheritance → IS-A  
Composition → HAS-A ✅ (Preferred)  

👉 Reason:
More flexible, less dependency  

---

## 🟦 14. Important Interview Concepts

- Constructor Overloading → YES  
- Destructor Overloading → NO  
- Operator Overloading → NOT in Java  
- Virtual Functions → default in Java  
- Pure Virtual → abstract methods  

👉 Rule:
If class has 1 abstract method → it must be abstract  

---

## 🟦 15. Interface Special Points

- Variables → public static final  
- No constructors  
- Cannot create objects  

---

## 🟦 16. Static Block

- Runs once when class loads  
- Executes before main()  

---

## 🟦 17. Tight vs Loose Coupling

Tight Coupling → dependent ❌  
Loose Coupling → flexible ✅  

👉 Achieved using:
- Interfaces  
- Composition  

---

## 🟦 18. Getter & Setter

Getter → retrieve value  
Setter → update value  

👉 Used for:
Encapsulation  

---

## 🟦 19. Additional Important Concepts ⭐

🔥 Method Overloading Rules:
- Same name  
- Different parameters  

🔥 Method Overriding Rules:
- Same name + same parameters  
- Runtime binding  

🔥 Upcasting:
Animal a = new Dog();

🔥 Downcasting:
Dog d = (Dog) a;

🔥 instanceof:
if (a instanceof Dog)

🔥 Object Class:
- Parent of all classes  

🔥 toString():
Used to print object info  

🔥 equals():
Used to compare objects  

🔥 finalize():
Called before garbage collection (deprecated concept)  

---

## 🟦 20. Rapid Fire ⚡

Class vs Object → blueprint vs instance  
Heap vs Stack → objects vs references  
Abstract class object? → NO  
Interface constructor? → NO  
Multiple inheritance? → NO  
Overloading vs Overriding → compile vs runtime  

---

## 🟦 21. Final One-Liner Revision 🚀

Encapsulation → Hide data  
Abstraction → Hide complexity  
Inheritance → Reuse code  
Polymorphism → Many forms  

---

## 🟦 22. MUST-KNOW INTERVIEW QUESTIONS ⭐ (Very Important)

👉 Difference: Abstraction vs Encapsulation?

Encapsulation:
- Hides DATA  
- Achieved using private variables + getters/setters  

Abstraction:
- Hides IMPLEMENTATION  
- Achieved using abstract classes/interfaces  

👉 One-line:
Encapsulation = data hiding  
Abstraction = logic hiding  

---

👉 Difference: Abstract Class vs Interface?

Abstract Class:
- Can have constructors  
- Can have implemented methods  
- Single inheritance  

Interface:
- No constructors  
- Only abstract methods (Java 8+: default/static allowed)  
- Multiple inheritance  

---

👉 Difference: Overloading vs Overriding?

Overloading:
- Compile-time  
- Same method name, different parameters  

Overriding:
- Runtime  
- Same method + same parameters  

---

👉 What is Method Hiding?

If child class defines static method with same name → it hides parent method (not overriding).

---

👉 Can we override static method?

❌ NO  
(static methods are resolved at compile time)

---

👉 Can we override final method?

❌ NO  

---

👉 Can we inherit final class?

❌ NO  

---

👉 Can constructor be inherited?

❌ NO  
(but can be called using super())

---

👉 Why Java does not support Multiple Inheritance?

Because of:
👉 Diamond Problem (ambiguity in method call)

---

👉 What is Diamond Problem?

If two parent classes have same method → child gets confused which one to use.

---

👉 What is Dynamic Binding?

Method call resolved at runtime (used in overriding).

---

👉 What is Early Binding?

Method call resolved at compile time (overloading, static, final).

---

👉 What is Object Slicing?

(C++ concept)  
Not applicable in Java because Java uses references.

---

👉 What is Marker Interface?

Empty interface (no methods)

Example:
Serializable, Cloneable  

Used to "mark" a class.

---

👉 What is Functional Interface?

Interface with ONLY ONE abstract method  

Example:
Runnable  

Used in Lambda Expressions  

---

👉 What is Immutable Class?

Class whose object cannot be changed after creation  

Example:
String  

👉 Rules:
- Make class final  
- Make variables private + final  
- No setters  

---

👉 What is Singleton Class?

Only ONE object exists  

Use-case:
Database connection  

---

## 🟦 23. SCENARIO-BASED QUESTIONS (VERY IMPORTANT 🔥)

👉 When to use Abstract Class?
When classes share COMMON behavior  

👉 When to use Interface?
When classes are UNRELATED but follow SAME RULE  

---

👉 When to use Inheritance?
When there is IS-A relationship  

👉 When to use Composition?
When flexibility is needed (HAS-A) ✅  

---

👉 Why use Encapsulation?
- Security  
- Data control  
- Validation  

---

👉 Why use Abstraction?
- Reduce complexity  
- Hide implementation  

---

## 🟦 24. COMMON MISTAKES (INTERVIEW TRAPS ⚠️)

❌ Saying Java supports multiple inheritance via class  
❌ Saying constructors can be overridden  
❌ Confusing abstraction with encapsulation  
❌ Saying static methods are overridden  
❌ Forgetting heap vs stack difference  

---

## 🟦 25. FINAL INTERVIEW PUNCH LINES 🎯

👉 "Encapsulation ensures security, abstraction reduces complexity."

👉 "Polymorphism improves flexibility and scalability."

👉 "Inheritance promotes code reuse but composition is preferred for flexibility."

👉 "OOP models real-world entities into code, making systems modular and maintainable."


👉 Final Line:
"OOP helps build scalable, reusable, and maintainable systems using real-world modeling."

