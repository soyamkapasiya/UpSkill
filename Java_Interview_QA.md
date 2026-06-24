# ☕ Java Technical Interview — Complete Q&A Reference

> A comprehensive, structured reference covering **Core Java, Spring Boot, REST APIs,
> Microservices, JPA/Hibernate, Collections, Concurrency, and Design Principles.**
>
> Formatted for **senior-level interview preparation** — 80 questions, all with one-line answers.

---

## 📑 Table of Contents

### Core Java Fundamentals

1. [What is the difference between JDK, JRE, and JVM?](#what-is-the-difference-between-jdk-jre-and-jvm)
2. [How does Garbage Collection work in Java?](#how-does-garbage-collection-work-in-java)
3. [Difference between == and equals()](#difference-between-==-and-equals)
4. [Why must hashCode() be overridden with equals()?](#why-must-hashcode-be-overridden-with-equals)
5. [What is an Immutable Class? How to create one?](#what-is-an-immutable-class-how-to-create-one)
6. [Why Is String Immutable?](#why-is-string-immutable)
7. [Explain HashMap internal working](#explain-hashmap-internal-working)
8. [Difference between ArrayList and LinkedList](#difference-between-arraylist-and-linkedlist)
9. [Heap vs Stack Memory](#heap-vs-stack-memory)
10. [Explain Constant String Pool](#explain-constant-string-pool)
11. [Difference between throw and throws](#difference-between-throw-and-throws)
12. [String vs StringBuilder vs StringBuffer](#string-vs-stringbuilder-vs-stringbuffer)
13. [Abstract Class vs Interface](#abstract-class-vs-interface)

### Java 8+ Features

14. [What are Functional Interfaces?](#what-are-functional-interfaces)
15. [Explain Java 8 Streams with a real use case](#explain-java-8-streams-with-a-real-use-case)
16. [What is Lambda Expression?](#what-is-lambda-expression)
17. [Difference between map() and flatMap()](#difference-between-map-and-flatmap)
18. [What is Optional and why is it used?](#what-is-optional-and-why-is-it-used)
19. [What are default methods in interfaces?](#what-are-default-methods-in-interfaces)
20. [Difference between Predicate, Function, Supplier, Consumer](#difference-between-predicate-function-supplier-consumer)
21. [Java 8 Features Overview](#java-8-features-overview)

### Collections Framework

22. [Explain ConcurrentModificationException](#explain-concurrentmodificationexception)
23. [Comparable vs Comparator](#comparable-vs-comparator)
24. [Difference between HashMap, Hashtable, and ConcurrentHashMap](#difference-between-hashmap-hashtable-and-concurrenthashmap)
25. [How does HashMap handle collisions internally?](#how-does-hashmap-handle-collisions-internally)
26. [What changed in HashMap after Java 8?](#what-changed-in-hashmap-after-java-8)
27. [Why does HashSet not allow duplicate elements?](#why-does-hashset-not-allow-duplicate-elements)
28. [Can a HashMap key be mutable?](#can-a-hashmap-key-be-mutable)

### Multithreading and Concurrency

29. [What is Thread lifecycle?](#what-is-thread-lifecycle)
30. [Difference between synchronized and Lock](#difference-between-synchronized-and-lock)
31. [Difference between Checked and Unchecked Exceptions](#difference-between-checked-and-unchecked-exceptions)
32. [Difference between Thread.start() and run()](#difference-between-threadstart-and-run)
33. [Java Memory Model (JMM) and volatile keyword](#java-memory-model-jmm-and-volatile-keyword)

### Spring Framework and Spring Boot

34. [What is Dependency Injection?](#what-is-dependency-injection)
35. [Difference between @Component, @Service, @Repository](#difference-between-component-service-repository)
36. [Difference between @Controller and @RestController](#difference-between-controller-and-restcontroller)
37. [What is @Autowired? Types of Injection](#what-is-autowired-types-of-injection)
38. [What is Spring Boot Auto-Configuration?](#what-is-spring-boot-auto-configuration)
39. [What is Spring Boot Actuator?](#what-is-spring-boot-actuator)
40. [What Is the Lifecycle of a Spring Bean?](#what-is-the-lifecycle-of-a-spring-bean)
41. [How does @Transactional work internally?](#how-does-transactional-work-internally)
42. [What are Spring Boot Starters?](#what-are-spring-boot-starters)
43. [How to Create Custom Annotations in Spring Boot](#how-to-create-custom-annotations-in-spring-boot)
44. [How Spring Handles Dependency Injection Using Reflection](#how-spring-handles-dependency-injection-using-reflection)
45. [Difference Between @Qualifier and @Primary](#difference-between-qualifier-and-primary)
46. [How to Handle Exceptions Globally in Spring Boot](#how-to-handle-exceptions-globally-in-spring-boot)
47. [What Does @SpringBootApplication Include?](#what-does-springbootapplication-include)
48. [Why Do We Make a Constructor Private?](#why-do-we-make-a-constructor-private)
49. [RestTemplate vs WebClient](#resttemplate-vs-webclient)
50. [Constructor Injection vs Setter Injection](#constructor-injection-vs-setter-injection)
51. [Difference Between @Component and @Configuration](#difference-between-component-and-configuration)

### REST API Design

52. [What Are REST Principles?](#what-are-rest-principles)
53. [REST vs SOAP](#rest-vs-soap)
54. [Difference Between PUT and PATCH](#difference-between-put-and-patch)
55. [Difference Between POST and PUT](#difference-between-post-and-put)
56. [What Is Idempotency?](#what-is-idempotency)
57. [What Are HTTP Status Codes?](#what-are-http-status-codes)

### Microservices Architecture

58. [What Is Microservices Architecture?](#what-is-microservices-architecture)
59. [Difference Between Monolith and Microservices](#difference-between-monolith-and-microservices)
60. [How do microservices communicate with each other?](#how-do-microservices-communicate-with-each-other)
61. [What is Feign Client?](#what-is-feign-client)
62. [What is Service Discovery?](#what-is-service-discovery)
63. [What is an API Gateway?](#what-is-an-api-gateway)
64. [What is a Circuit Breaker?](#what-is-a-circuit-breaker)
65. [What is Saga Pattern?](#what-is-saga-pattern)
66. [How do you handle Distributed Transactions?](#how-do-you-handle-distributed-transactions)
67. [How do you secure Microservices using OAuth2 / JWT?](#how-do-you-secure-microservices-using-oauth2-jwt)
68. [What is Distributed Tracing?](#what-is-distributed-tracing)
69. [Role of Config Server in Spring Cloud](#role-of-config-server-in-spring-cloud)
70. [Monitoring Microservices in Production](#monitoring-microservices-in-production)

### JPA and Hibernate

71. [Difference between JPA and Hibernate](#difference-between-jpa-and-hibernate)
72. [What is an Entity?](#what-is-an-entity)
73. [Lazy vs Eager Loading](#lazy-vs-eager-loading)
74. [What is the N+1 Problem?](#what-is-the-n1-problem)
75. [What is @Query annotation?](#what-is-query-annotation)
76. [Difference between JPQL and Native Query](#difference-between-jpql-and-native-query)
77. [What is Cascade Type?](#what-is-cascade-type)
78. [What is Dirty Checking in Hibernate?](#what-is-dirty-checking-in-hibernate)
79. [Hibernate Session, Persistence Context, and First-Level Cache](#hibernate-session-persistence-context-and-first-level-cache)

### Design Principles

80. [SOLID Principles](#solid-principles)

---


# 📂 Core Java Fundamentals

## What is the difference between JDK, JRE, and JVM?

1. What is the difference between JDK, JRE, and JVM? Difference between JDK, JRE, and JVM 


###


###


###


### 1. JVM (Java Virtual Machine) 


 JVM is an abstract machine that executes Java bytecode.

**Key Responsibilities**
- Loads .class files
- Verifies bytecode (security)
- Converts bytecode → machine code (via JIT)
- Manages memory (Heap, Stack, Metaspace)
- Handles Garbage Collection

**Key Components**
- Class Loader Subsystem
- Runtime Data Areas
  - Heap
  - Stack
  - Method Area (Metaspace)
- Execution Engine
  - Interpreter
  - JIT Compiler
- Garbage Collector

**Important Points**
- JVM is platform-dependent
- Same bytecode → different JVM implementations (Windows/Linux/Mac)
- You cannot write Java without JVM

**Interview Line:** JVM provides “Write Once, Run Anywhere” by abstracting OS and hardware differences. 


###


###


###


### 2. JRE (Java Runtime Environment) JRE is the runtime environment required to run Java applications.

**Contains**
- JVM
- Core Java libraries (java.lang, java.util, etc.)
- Supporting files & native libraries What JRE Can Do
- Run Java applications
- Cannot compile Java code

**Formula** JRE = JVM + Libraries Example If a production server only runs Java apps:
- JRE is sufficient
- JDK is not required 


###


###


###


### 3. JDK (Java Development Kit) JDK is a full-fledged development kit used to develop, compile, debug, and run Java applications.

**Contains**
- JRE
- Compiler (javac)
- Debugger (jdb)
- Tools:
  - jar
  - javadoc
  - jconsole
  - jmap, jstack, jcmd

**Formula** JDK = JRE + Development Tools

**Used By**
- Developers
- Build servers (CI/CD)
- Local development environments 


📊

**Comparison Table** Feature JVM JRE JDK Executes bytecode ✅ ✅ ✅

**Contains** JVM ❌ ✅ ✅ Java libraries ❌ ✅ ✅ Compiler (javac) ❌ ❌ ✅ Debug & monitoring tools ❌ ❌ ✅ Used for development ❌ ❌ ✅ 


🔑

**Real-World** Production Perspective (10+ Years Experience)
- Local / CI / Build Server → JDK
- Production Runtime → JRE (or slim JDK image)
- Docker (Modern Practice) → Use JRE-based or distroless images
- Java 11+ → No separate JRE download, JDK includes runtime 


🧠

**Common Follow**-up Interview Questions 

Q: Is JRE still relevant after Java 11? ✅ Technically yes, but Oracle stopped distributing standalone JRE. JDK is used instead. Q: Can JVM run non-Java languages? ✅ Yes — Kotlin, Scala, Groovy compile to bytecode. Q: Is JVM platform-independent? ❌ JVM is platform-dependent ✅ Java bytecode is platform-independent 


🎯 One-Line Summary (Perfect for Interviews) JVM executes bytecode, JRE provides runtime environment, and JDK provides tools to develop and run Java applications.

---


## How does Garbage Collection work in Java?

How does Garbage Collection work in Java? 


###


###


###


### 1. What is Garbage Collection? Garbage Collection in Java is an automatic memory management process performed by the JVM to reclaim heap memory by removing objects that are no longer reachable. Key Principle: GC removes objects that are unreachable, not objects that are “unused”. 


###


###


###


### 2. Object

**Lifecycle** & Reachability Reachable Objects An object is considered alive if it is reachable from:
- Local variables (stack)
- Static variables
- Active threads
- JNI references 

Unreachable Objects
- No reference path from GC Roots GC Roots Include:
- Thread stacks
- Static fields
- JNI references
- Active thread objects 


###


###


###


### 3. JVM Heap Structure (Generational GC) Heap Generations 


🟢 Young Generation
- Eden Space – new objects created here
- Survivor S0 / S1 – objects that survive GC 


🔵 Old Generation
- Long-lived objects
- Promoted from Young Gen 


🟣 Metaspace (Not Heap)
- Class metadata
- Native memory (Java 8+) 


###


### 4.

**Types of** Garbage Collection


###


###


### 1. Minor GC
- Happens in Young Generation
- Fast
- Copies surviving objects to Survivor space
- Frequent


###


###


### 2. Major GC
- Happens in Old Generation
- Slower
- More expensive


###


###


### 3. Full GC
- Cleans entire heap
- Causes Stop-The-World (STW)
- Worst for performance 


###


###


###


### 5. How GC Decides What to Collect Mark-and-Sweep Algorithm (Conceptual)


###


###


### 1. Mark – Identify reachable objects


###


###


### 2. Sweep – Remove unreachable objects


###


###


### 3. Compact – Defragment memory (optional) 


###


###


###


### 6. Popular Garbage Collectors 


 Serial GC
- Single-threaded
- Small applications
- High STW pauses Parallel GC (Throughput GC)
- Multi-threaded
- High throughput
- Default until Java 8 

CMS (Deprecated)
- Low pause times
- Concurrent marking
- Fragmentation issues G1 GC (Default Java 9+)
- Region-based
- Predictable pause times
- Compacts memory ZGC / Shenandoah (Java 11+)
- Ultra-low latency
- Concurrent GC
- Large heaps 


###


###


###


### 7. Stop-The-World (STW) Explained
- Application threads pause
- GC threads run
- Causes latency spikes
- Goal of modern GC: minimize STW 


###


### 8.

**Example:** Object Promotion Flow for (int i = 0; i < 10000; i++) { byte[] data = new byte[1024]; }
- Objects created in Eden
- Minor GC triggered
- Surviving objects → Survivor space
- After threshold → Old Generation 


###


###


###


### 9. Important JVM GC Options (Interview Gold) -Xms512m -Xmx1024m -XX:+UseG1GC -XX:MaxGCPauseMillis=200 -XX:+HeapDumpOnOutOfMemoryError 


🔥

**Common Interview** Pitfalls ❌ System.gc() guarantees GC ✅ GC may happen, not guaranteed ❌ Object with no reference is immediately deleted ✅ Only deleted when GC runs ❌ GC works on Stack ✅ GC works only on Heap 


🧠 Real Production Insight (10+ Years)
- Memory leaks = unreleased references
- Prefer G1GC for microservices
- Monitor using:
  - jvisualvm
  - jstat
  - jconsole
- Tune GC only after profiling 


🎯

**One-Line Interview** Answer Java Garbage Collection automatically reclaims heap memory by identifying unreachable objects using GC roots and generational algorithms, minimizing manual memory management.

---


## Difference between == and equals()

Difference between == and equals() 

Difference between == and equals() in Java 

 1. == Operator

**What it does**
- Compares references (memory addresses) for objects
- Compares actual values for primitives Behavior
- For primitives: compares value
- For objects: checks whether both references point to the same object in memory Example String a = new String("Java"); String b = new String("Java"); System.out.println(a == b); // false 

Reason: a and b point to different objects, even though the content is the same. 2. equals() Method

**What it does**
- Compares logical equality (content) of objects
- Defined in java.lang.Object
- Often overridden in classes like String, Integer, Date Default Implementation (Object class) public boolean equals(Object obj) { return this == obj; } So unless overridden, equals() behaves exactly like ==. Example String a = new String("Java"); String b = new String("Java"); System.out.println(a.equals(b)); // true

**Reason:** String overrides equals() to compare character content.


### 3.

**Comparison Table** Aspect == equals() Type Operator Method Compares primitives Value Not applicable Compares objects Reference Content (if overridden) Can be overridden No Yes Defined in Java language Object class Common usage Identity check Logical equality


###


###


### 4. String-Specific Case (Very

**Common Interview** Trap) String s1 = "Java"; String s2 = "Java"; System.out.println(s1 == s2); // true System.out.println(s1.equals(s2)); // true

**Reason:**
- String literals are stored in the String Constant Pool
- Both references point to the same pooled object String s3 = new String("Java"); System.out.println(s1 == s3); // false


###


###


### 5. Custom Objects Example class Employee { int id; Employee(int id) { this.id = id; } } Employee e1 = new Employee(1); Employee e2 = new Employee(1); System.out.println(e1 == e2); // false System.out.println(e1.equals(e2)); // false

**Reason:**
- equals() not overridden
- Inherited from Object, so reference comparison To fix: @Override public boolean equals(Object obj) { if (this == obj) return true; if (!(obj instanceof Employee)) return false; Employee e = (Employee) obj; 

 return id == e.id; }


### 6.

**Relationship Between** equals() and hashCode() Contract
- If equals() is overridden, hashCode() must also be overridden
- Equal objects must return the same hash code

**Why it matters**
- Collections like HashMap, HashSet depend on this contract
- Violating it causes unexpected behavior


### 7.

**Real-World** Usage Guidelines (Senior Perspective)
- Use ==:
  - For primitives
  - For singleton checks
  - For enum comparison
- Use equals():
  - For business object comparison
  - For String, Wrapper classes
  - Inside collections


### 8.

**One-Line Interview** Answer == compares reference equality (or primitive values), while equals() compares logical equality and can be overridden to compare object content.

---


## Why must hashCode() be overridden with equals()?

Why must hashCode() be overridden with equals() 

Defined in java.lang.Object: Contract Rules


###


###


### 1. If two objects are equal according to equals(), they must return the same hashCode()


###


###


### 2. If two objects have the same hashCode, they may or may not be equal 3. hashCode() must be consistent during an object’s lifetime if fields used in equals() do not change This contract is critical for hash-based collections.


### 2.

**Why This Contract** Exists Hash-based collections (HashMap, HashSet, HashTable) use a two-step lookup: 1. hashCode() → determine bucket index 2. equals() → find the exact object within the bucket If hashCode() is not consistent with equals(), the lookup mechanism breaks.

---


## What is an Immutable Class? How to create one?

---


## How does Garbage Collection work in Java?

How does Garbage Collection work in Java?](#how-does-garbage-collection-work-in-java)
3. [

---


## Difference between == and equals()

Difference between == and equals()](#difference-between-==-and-equals)
4. [

---


## Why must hashCode() be overridden with equals()?

Why must hashCode() be overridden with equals()?](#why-must-hashcode-be-overridden-with-equals)
5. [What is an Immutable Class? How to create one?](#what-is-an-immutable-class-how-to-create-one)
6. [

---


## What is an Immutable Class? How to create one?

---

## How does Garbage Collection work in Java?

How does Garbage Collection work in Java?](#how-does-garbage-collection-work-in-java)
3. [

---

## Difference between == and equals()

Difference between == and equals()](#difference-between-==-and-equals)
4. [

---

## Why must hashCode() be overridden with equals()?

Why must hashCode() be overridden with equals()?](#why-must-hashcode-be-overridden-with-equals)
5. [What is an Immutable Class? How to create one?](#what-is-an-immutable-class-how-to-create-one)
6. [

---

## What is an Immutable Class? How to create one?

What is Immutable class? How to create one?


###


###


### 1. What Is an Immutable Class? An immutable class is a class whose state cannot be changed after the object is created. Once an immutable object is constructed:
- Its field values remain constant
- No setter methods can modify it
- Any “change” results in a new object Common Examples
- String
- Integer
- LocalDate
- BigDecimal


###


###


### 2. Why Immutability Is Important Key Advantages
- Thread-safe by design (no synchronization required)
- Safe to use as HashMap keys
- Easier to reason about and debug
- No side effects
- Prevents accidental state changes

**Real-World** Usage
- Configuration objects
- Value objects (DTOs in functional style)
- Cache keys
- Money, date, and ID objects


### 3.

**Characteristics** of an Immutable Class To make a class immutable, it must follow these rules:


###


###


### 1. Declare the class as final
  - Prevents subclassing that could introduce mutability


###


###


### 2. Make all fields private and final


###


###


### 3. Do not provide setter methods


###


###


### 4. Initialize all fields via constructor


###


###


### 5. Perform defensive copying for mutable fields


###


###


### 6. Return copies, not references, for mutable objects


###


###


### 4. How to Create an Immutable Class (Step-by-Step)

**Example:** Immutable Employee public final class Employee { private final int id; private final String name; private final Date joiningDate; public Employee(int id, String name, Date joiningDate) { 

 this.id = id; this.name = name; this.joiningDate = new Date(joiningDate.getTime()); // defensive copy } public int getId() { return id; } public String getName() { return name; } public Date getJoiningDate() { return new Date(joiningDate.getTime()); // defensive copy } }

**Why Defensive** Copying? Date is mutable. Without copying:
- External code could modify internal state
- Immutability would be broken


### 5.

**What Happens** Without Defensive Copying Date d = new Date(); Employee e = new Employee(1, "A", d); d.setTime(0); // modifies Employee state indirectly This breaks immutability if defensive copying is not used.


###


###


### 6. Immutable vs Mutable Class Comparison Aspect Immutable Mutable State change Not allowed Allowed Thread safety Inherent Needs synchronization 

HashMap key usage Safe Risky

**Performance** May create more objects Fewer objects Debugging Easy Complex


###


###


### 7. Immutability and String (Interview Favorite)
- String is immutable to:
  - Enable String Constant Pool
  - Improve security (e.g., class loading, file paths)
  - Allow safe sharing across threads String s = "Java"; s.concat("8"); System.out.println(s); // Java


###


###


### 8. Builder Pattern for Complex Immutable Objects When constructors become large: public final class User { private final String name; private final int age; private User(Builder b) { this.name = b.name; this.age = b.age; } public static class Builder { private String name; private int age; public Builder name(String name) { this.name = name; return this; } public Builder age(int age) { this.age = age; 

 return this; } public User build() { return new User(this); } } }


### 9.

**Common Interview** Pitfalls
- Marking fields final but returning mutable references
- Forgetting defensive copies
- Allowing subclassing
- Using mutable objects as map keys


### 10.

**One-Line Interview** Answer An immutable class is a class whose state cannot be changed after creation; it is created by making the class final, fields private and final, removing setters, and using defensive copying for mutable fields.


###


###


### 11. Follow-up Questions Interviewers Ask
- Why is String immutable?
- How does immutability help in concurrency?
- Can an immutable class contain mutable objects?
- Difference between final and immutable?

---


## Why Is String Immutable?

Why Is String Immutable? a) String Constant Pool (Memory Optimization)
- String literals are stored in a shared pool
- Multiple references can point to the same object
- Immutability ensures shared objects are safe String s1 = "Java"; String s2 = "Java"; // points to same object If String were mutable, changing s1 would affect s2. b) Security
- Strings are used in:
  - Class loading
  - File paths
  - Database URLs
  - Network connections
- Immutability prevents malicious modification after validation c) Thread Safety
- Multiple threads can share the same String safely
- No synchronization needed d) HashCode Caching
- String caches its hash code
- Improves performance in HashMap lookups

**One-Line Interview** Answer String is immutable to enable safe pooling, improve performance, ensure security, and provide thread safety.

---


## Explain HashMap internal working

Explain HashMap internal working


###


###


### 1. What Is HashMap? HashMap is a hash table–based implementation of the Map interface that stores data as key–value pairs. Key Properties
- Allows one null key, multiple null values
- Not thread-safe
- No insertion order guarantee
- Average time complexity: O(1) for get() and put()


###


###


### 2. Core Internal Data Structure Internally, HashMap uses: Node<K, V>[] table; Each array index is called a bucket. Each bucket can contain:
- A single Node
- A linked list of nodes (before Java 8)
- A balanced red-black tree (Java 8+ when collisions are high)


###


###


### 3. How put() Works Internally Step-by-Step Flow


###


###


### 1. Compute hash int hash = (key == null) ? 0 : (h = key.hashCode()) ^ (h >>> 16);


###


###


### 2. Calculate bucket index index = (n - 1) & hash; (n = table length, always power of 2)


###


###


### 3. Check bucket
- If empty → insert new node
- If occupied:
  - Compare keys using equals()
  - If key exists → replace value
  - Else → handle collision


###


###


### 4. Collision handling
- Add node to linked list
- If list size exceeds threshold → treeify


###


###


### 4. Collision Handling (Java 8+) 


Treeification Rules
- Bucket size ≥ 8
- Table size ≥ 64
- Converts linked list → Red-Black Tree

**Benefits**
- Lookup improves from O(n) → O(log n)


###


###


### 5. How get() Works Internally


###


###


### 1. Compute hash of key


###


###


### 2. Calculate bucket index


###


###


### 3. Traverse:
  - Single node
  - Linked list
  - Tree


###


###


### 4. Match using:
  - hashCode()
  - equals() Returns value or null.


###


###


### 6. Resize and Rehashing Default Settings
- Initial capacity: 16
- Load factor: 0.75 Resize Condition size > capacity × loadFactor

**What Happens** During Resize
- Capacity doubles
- All entries are rehashed
- Nodes redistributed into new buckets This is an expensive operation.


###


###


### 7. Why Capacity Is Power of 2
- Faster index calculation using bitwise AND
- Uniform distribution of keys
- Better performance than modulo (%)


###


###


### 8. Role of equals() and hashCode() Method Role hashCode() Determines bucket equals() Identifies exact key Violating the contract breaks HashMap behavior.


###


###


### 9. Null Key Handling
- null key always stored in bucket 0
- Hash value = 0
- Only one null key allowed


###


###


### 10. Java 7 vs Java 8 Differences Aspect Java 7 Java 8+ Collision structure Linked List List → Red-Black Tree Worst-case get() O(n) O(log n) Resize behavior Head insertion Preserves order

**Performance** Lower Improved


###


###


### 11. Thread Safety Issue (Important)
- HashMap is not thread-safe
- Concurrent modification may cause:
  - Data loss
  - Infinite loops (Java 7)
- Use:
  - Collections.synchronizedMap()
  - ConcurrentHashMap


### 12.

**Common Interview** Pitfalls
- Mutable keys in HashMap
- Poor hashCode() implementation
- Ignoring resize cost
- Using HashMap in multi-threaded code without protection


### 13.

**One-Line Interview** Answer HashMap stores key–value pairs in buckets using hashCode-based indexing, resolves collisions via linked lists or red-black trees (Java 8+), and relies on equals() for key comparison.

---


## Difference between ArrayList and LinkedList

Difference between ArrayList and LinkedList ArrayList uses a dynamic array offering fast random access, while LinkedList uses a doubly linked list optimized for insertions and deletions at the ends but slower for access.

---


## Heap vs Stack Memory

---


## Why Is String Immutable?

Why Is String Immutable?](#why-is-string-immutable)
7. [

---


## Explain HashMap internal working

Explain HashMap internal working](#explain-hashmap-internal-working)
8. [

---


## Difference between ArrayList and LinkedList

Difference between ArrayList and LinkedList](#difference-between-arraylist-and-linkedlist)
9. [Heap vs Stack Memory](#heap-vs-stack-memory)
10. [

---


## Heap vs Stack Memory

---

## Why Is String Immutable?

Why Is String Immutable?](#why-is-string-immutable)
7. [

---

## Explain HashMap internal working

Explain HashMap internal working](#explain-hashmap-internal-working)
8. [

---

## Difference between ArrayList and LinkedList

Difference between ArrayList and LinkedList](#difference-between-arraylist-and-linkedlist)
9. [Heap vs Stack Memory](#heap-vs-stack-memory)
10. [

---

## Heap vs Stack Memory

Heap vs Stack memory


###


###


### 1. Basic

**Definition** Stack Memory
- Used for method execution
- Stores:
  - Method call frames
  - Local variables
  - Method parameters
  - Reference variables
- Memory is thread-specific Heap Memory
- Used for object storage
- Stores:
  - Objects
  - Instance variables
- Memory is shared across threads


### 2.

**Key Differences** (Comparison Table) Aspect Stack Memory Heap Memory

**Purpose** Method execution Object storage Scope Thread-local Shared Lifetime Method call duration Until GC Speed Faster Slower Memory size Small Large Thread safety Inherently safe Requires synchronization GC involvement No Yes Memory errors StackOverflowError OutOfMemoryError


###


###


### 3. How Memory Is Allocated Stack Allocation void method() { int x = 10; // stored in stack Object obj = new Object(); // reference in stack }
- Stack frame created on method call
- Automatically removed when method returns
- Follows LIFO (Last In, First Out) Heap Allocation Object obj = new Object();
- Object created in heap
- Reference stored in stack
- Accessible by multiple threads

---


## Explain Constant String Pool

Explain Constant String Pool The Constant String Pool (CSP) is a special memory area inside the Java heap where String literals are stored to optimize memory usage and improve performance.


###


###


### 1. What Is the Constant String Pool?
- A shared pool of unique String objects
- Managed by the JVM
- Stores:
  - String literals ("Java")
  - Interned strings (intern())

**Purpose**
- Avoid creating duplicate String objects
- Enable reuse of immutable String instances


###


###


### 2. How String Literals Work String s1 = "Java"; String s2 = "Java";

**What happens**:
- JVM checks the Constant String Pool
- "Java" does not exist → created and stored in pool
- s1 and s2 both reference the same object

**Result:** s1 == s2 // true


###


###


### 3. Strings Created Using new String s1 = "Java"; String s2 = new String("Java");

**What happens**:
- "Java" literal goes to the pool
- new String("Java") creates a new object in heap
- s2 points to a different object

**Result:** s1 == s2 // false s1.equals(s2) // true


###


###


### 4. Role of intern() Method String s1 = new String("Java"); String s2 = s1.intern();

**What happens**:
- JVM checks pool for "Java"
- If present → returns pooled reference
- If absent → adds to pool

**Result:** s1 == s2 // false "Java" == s2 // true

**Use Case**
- Reduce memory when handling many duplicate strings
- Useful in parsing, caching, configuration-heavy systems


###


###


### 6. Why String Pool Is Safe Because String is immutable:
- Multiple references can safely point to same object
- No risk of accidental modification
- Enables aggressive sharing If String were mutable, pooling would be unsafe.


### 7.

**Performance** and Memory

**Benefits**

**Benefits**
- Reduces memory footprint
- Faster equality checks using ==
- Improves startup and runtime performance Cost
- intern() lookup has overhead
- Overuse may increase GC pressure


### 8.

**Common Interview** Traps
- Saying String pool is not in heap (wrong in Java 7+)
- Confusing heap object with pooled object
- Assuming all Strings go to pool (only literals and interned ones)
- Overusing intern() blindly


### 9.

**Real-World** (Senior Perspective)
- JVM already pools literals aggressively
- Avoid calling intern() unless:
  - Strings repeat heavily
  - Memory profiling proves benefit
- Modern JVMs handle pooling efficiently


### 10.

**One-Line Interview** Answer The Constant String Pool is a JVM-managed shared memory area that stores unique String literals and interned strings to reduce memory usage and improve performance through reuse.

---


## Difference between throw and throws

Difference between throw and throws, and parent class of exceptions


###


###


### 1. Difference between throw and throws throw
- Used to explicitly throw an exception
- Used inside a method
- Throws one exception at a time
- Used when you want to create and raise an exception manually Example if (age < 18) { throw new IllegalArgumentException("Age must be >= 18"); }

**Key Points**
- Followed by an exception object
- Control immediately moves to the caller
- Commonly used for business validation throws
- Used to declare exceptions
- Used in the method signature
- Declares multiple exceptions
- Transfers responsibility to the caller Example public void readFile() throws IOException, SQLException { // risky code } 

Key Points
- Followed by exception class names
- Does not throw anything by itself
- Mainly used for checked exceptions


###


###


### 3. Can throw Be Used Without throws? Yes, in these cases:
- When throwing unchecked exceptions
- When exception is handled inside the method throw new RuntimeException("Error"); // no throws required


### 10.

**One-Line Interview** Answers throw vs throws throw is used to explicitly raise an exception, while throws is used to declare exceptions that a method may propagate.

---


## String vs StringBuilder vs StringBuffer

String vs StringBuilder vs StringBuffer These three classes are used to handle character sequences in Java, but they differ significantly in mutability, thread safety, and performance.


###


###


### 1. String

**Key

**Characteristics****
- Immutable
- Stored in String Constant Pool (for literals)
- Thread-safe by design
- Any modification creates a new object Example String s = "Java"; s = s.concat("8");

**What happens**:
- "Java" remains unchanged
- A new "Java8" object is created
- Old object may become eligible for GC

**Pros**
- Thread-safe
- Secure
- Memory-efficient due to pooling

**Cons**
- Poor performance for frequent modifications


###


###


### 2. StringBuilder

**Key

**Characteristics****
- Mutable
- Not thread-safe
- Introduced in Java 5
- Designed for single-threaded performance Example StringBuilder sb = new StringBuilder("Java"); sb.append("8");

**What happens**:
- Same object is modified
- No new object creation

**Pros**
- Fast
- Best for heavy string manipulation
- No synchronization overhead

**Cons**
- Not safe in multi-threaded environments


###


###


### 3. StringBuffer 

Key

**Characteristics**
- Mutable
- Thread-safe
- All methods are synchronized
- Legacy class (Java 1.0) Example StringBuffer sb = new StringBuffer("Java"); sb.append("8");

**Pros**
- Safe in multi-threaded environment

**Cons**
- Slower than StringBuilder due to synchronization
- Rarely used in modern applications


### 4.

**Comparison Table** Aspect String StringBuilder StringBuffer Mutability Immutable Mutable Mutable Thread safety Yes No Yes Synchronization Not needed None Method-level

**Performance** Slow for modifications Fastest Slower than Builder Memory usage High (many objects) Efficient Efficient Introduced in Java 1.0 Java 5 Java 1.0


###


###


### 6. Thread Safety Explanation
- String is safe because it cannot change
- StringBuffer is safe due to synchronization
- StringBuilder is unsafe but faster


### 7.

**When to Use** What (Senior Guidance) 

Use String when:
- Values are constant
- Few or no modifications
- Security matters (passwords, file paths) Use StringBuilder when:
- Frequent modifications
- Single-threaded context
-

**Performance**-critical code Use StringBuffer when:
- Legacy code
- Multi-threaded string manipulation (rare)
- Thread safety is mandatory and simple


### 9.

**One-Line Interview** Answer String is immutable and thread-safe, StringBuilder is mutable and fast but not thread-safe, and StringBuffer is mutable and thread-safe but slower due to synchronization.

---


## Abstract Class vs Interface

---


## Explain Constant String Pool

Explain Constant String Pool](#explain-constant-string-pool)
11. [

---


## Difference between throw and throws

Difference between throw and throws](#difference-between-throw-and-throws)
12. [

---


## String vs StringBuilder vs StringBuffer

String vs StringBuilder vs StringBuffer](#string-vs-stringbuilder-vs-stringbuffer)
13. [Abstract Class vs Interface](#abstract-class-vs-interface)


### Java 8+ Features

14. [

---


## Abstract Class vs Interface

---

## Explain Constant String Pool

Explain Constant String Pool](#explain-constant-string-pool)
11. [

---

## Difference between throw and throws

Difference between throw and throws](#difference-between-throw-and-throws)
12. [

---

## String vs StringBuilder vs StringBuffer

String vs StringBuilder vs StringBuffer](#string-vs-stringbuilder-vs-stringbuffer)
13. [Abstract Class vs Interface](#abstract-class-vs-interface)


### Java 8+ Features

14. [

---

## Abstract Class vs Interface

Abstract class vs Interface Abstract classes and interfaces are both used to achieve abstraction in Java, but they serve different design purposes and have important differences


###


###


### 1. Basic

**Definition** Abstract Class
- A class declared using the abstract keyword
- Can contain abstract and concrete methods
- Represents an “is-a” relationship with shared state and behavior Interface
- A contract that defines what a class can do
-

**Contains** method declarations (with some implementations allowed since Java 8)
- Represents capability or role-based abstraction


### 2.

**Key Differences** (Comparison Table) Aspect Abstract Class Interface Keyword abstract interface Method types Abstract + concrete Abstract, default, static Field types Instance variables allowed Only public static final constants 

Constructors Yes No Multiple inheritance No Yes (multiple interfaces) Access modifiers Any Methods are public by default State Can maintain state Cannot maintain instance state Functional interface No Yes (single abstract method)


###


###


### 3. Method Implementation Differences Abstract Class Example abstract class Vehicle { int speed; abstract void move(); void accelerate() { speed += 10; } } Interface Example interface Flyable { int MAX_HEIGHT = 1000; void fly(); default boolean canFly() { return true; } } | Scenario |

**Resolution** | | -------------------- | ------------- | | Class method present | Class wins | | Two default methods | Must override | | Abstract vs default | Abstract wins |


###


###


### 4. Multiple Inheritance Abstract Class class Car extends Vehicle { }
- Can extend only one class Interface class Plane implements Flyable, Runnable { }
- Can implement multiple interfaces
- Solves the diamond problem using default method rules


###


###


### 5. Java 8+ Interface Enhancements (Important) Interfaces can now have:
- default methods (with implementation)
- static methods Why added:
- To allow backward compatibility (e.g., adding methods to collections) Abstract classes had these capabilities from the beginning.


###


###


### 6. State and Variables Abstract Class
- Can have instance variables
- Can maintain state across methods Interface
- Variables are implicitly:
  - public
  - static
  - final
- Cannot hold mutable state


### 7.

**When to Use** Abstract Class (Senior Guidance) Use an abstract class when:
- You want to share state + behavior
- You control the class hierarchy
- You expect future base functionality
- Classes are closely related

**Example:**
- Base service classes
- Template pattern


### 8.

**When to Use** Interface (Senior Guidance) Use an interface when:
- You need multiple inheritance
- You want to define a capability/contract
- You want loose coupling
- You expect third-party implementations

**Example:**
- APIs
- SPI designs
- Callback mechanisms


### 9.

**Common Interview** Traps
- Saying interfaces cannot have implementations (false since Java 8)
- Forgetting interface variables are constants
- Confusing “is-a” with “can-do”
- Overusing abstract classes where interfaces fit better


### 10.

**Real-World** Design Insight (10+ Years)
- Interfaces define contracts
- Abstract classes provide skeletal implementations
- Prefer interfaces in public APIs
- Use abstract classes internally for shared logic


### 11.

**One-Line Interview** Answer An abstract class provides shared state and behavior with single inheritance, while an interface defines a contract supporting multiple inheritance and loose coupling.

**Common Follow**-up Questions Interviewers Ask
- Can an interface extend another interface?
- How does Java resolve default method conflicts?
- Can an abstract class implement an interface?
- Why were default methods introduced?
- Interface vs abstract class in Spring

---

# 📂 Java 8+ Features


## What are Functional Interfaces?

What are Functional Interfaces? 

What Are Functional Interfaces in Java?


### 1.

**Definition** A Functional Interface is an interface that contains exactly one abstract method.
- Introduced formally in Java 8
- Enables lambda expressions and method references
- Annotated with @FunctionalInterface (optional but recommended)


###


###


### 2. Why Functional Interfaces Were Introduced Before Java 8:
- Anonymous classes were verbose
- Poor readability for single-method behavior Java 8:
- Functional interfaces enable concise, functional-style programming


###


###


### 3. Basic Example @FunctionalInterface interface Calculator { int add(int a, int b); } Using Lambda: Calculator c = (a, b) -> a + b;


###


###


### 4. Rules of Functional Interfaces


###


###


### 1. Must have only one abstract method


###


###


### 2. Can have:
  - Multiple default methods
  - Multiple static methods


###


###


### 3. Can override methods from Object 4. @FunctionalInterface enforces compile-time check


###


###


### 5. Functional Interface vs Normal Interface Aspect Functional Interface Normal Interface Abstract methods Exactly one One or more Lambda support Yes No Java 8 usage Core feature Regular


###


###


### 7. Example with Streams list.stream() .filter(s -> s.startsWith("A")) // Predicate .map(String::toUpperCase) // Function .forEach(System.out::println); // Consumer


###


###


### 8. Custom Functional Interface Example @FunctionalInterface interface Validator<T> { 

 boolean validate(T t); }

**Usage:** Validator<String> v = s -> s.length() > 5;


### 11.

**One-Line Interview** Answer A functional interface is an interface with exactly one abstract method, enabling lambda expressions and functional-style programming in Java.


### 12.

**Common Follow**-up Questions
- Can a functional interface extend another interface? Yes, a functional interface can extend another interface, as long as the total number of abstract methods remains exactly one.
- Difference between Function and Predicate? Function<T,R> Transform input to output, Predicate<T> Evaluate condition Function transforms data, while Predicate evaluates conditions and returns a boolean.
- How does method reference work? A method reference is a shorthand for a lambda expression that calls an existing method.
-

**What happens** if two abstract methods exist? Result The interface is no longer a functional interface Lambda expressions cannot be used Compilation error if annotated with @FunctionalInterface

---


## Explain Java 8 Streams with a real use case

Explain Java 8 Streams with a real use case Java 8 Streams Explained with a Real

**Use Case**


###


###


### 1. What Are Java 8 Streams? A Stream represents a sequence of elements that supports functional-style operations such as filtering, mapping, and reducing.

**Key

**Characteristics****
- Does not store data
- Works on a data source (Collection, Array, I/O)
- Lazy evaluation
- One-time use
- Can be sequential or parallel


###


###


### 2. Stream Pipeline Structure A stream pipeline has three parts:


###


###


### 1. Source


###


###


### 2. Intermediate operations


###


###


### 3. Terminal operation collection.stream() .filter(...) 

 .map(...) .collect(...);


### 3.

**Real-World**

**Use Case**: Order Processing System Scenario You are working on an e-commerce system. Each order has:
- orderId
- customerType (REGULAR / PREMIUM)
- amount
- status (SUCCESS / FAILED) Requirement


###


###


### 1. Filter successful orders


###


###


### 2. Only for PREMIUM customers


###


###


### 3. Apply 10% discount


###


###


### 4. Collect final payable amounts


###


###


### 4. Traditional Approach (Without Streams) List<Double> result = new ArrayList<>(); for (Order order : orders) { if (order.getStatus() == Status.SUCCESS && order.getCustomerType() == CustomerType.PREMIUM) { result.add(order.getAmount() * 0.9); } }

**Problems:**
- Verbose
- Harder to read
- Mixed business logic and iteration


###


###


### 5. Stream-Based Solution (Java 8 Style) List<Double> discountedAmounts = 

 orders.stream() .filter(o -> o.getStatus() == Status.SUCCESS) .filter(o -> o.getCustomerType() == CustomerType.PREMIUM) .map(o -> o.getAmount() * 0.9) .collect(Collectors.toList());

**Benefits**:
- Declarative
- Readable
- Easy to maintain
- Business intent is clear


###


###


### 6. Intermediate vs Terminal Operations Intermediate Operations (Lazy)
- filter
- map
- flatMap
- sorted
- distinct Terminal Operations (Trigger Execution)
- forEach
- collect
- reduce
- count
- findFirst


###


###


### 7. Lazy Evaluation Explained stream.filter(x -> { System.out.println("Filtering " + x); return x > 5; }); Nothing happens until a terminal operation is called.


###


###


### 8. Short-Circuiting Example orders.stream() .filter(o -> o.getAmount() > 1000) .findFirst(); Stops processing once first match is found.


###


###


### 9. Parallel Streams (Use Carefully) orders.parallelStream() .map(Order::getAmount) .sum();

**When to Use**
- Large datasets
- CPU-intensive tasks
- Stateless operations When to Avoid
- I/O operations
- Shared mutable state
- Small collections


###


###


### 10. Common Stream Operations in Real Projects Operation

**Use Case** filter() Validation map() Transformation flatMap() Flatten nested data collect() Convert to list/map groupingBy() Reports partitioningBy() Split data


###


###


### 11. Stream vs Collection (Important Interview Point) Streams Collections Process data Store data Lazy Eager One-time use Reusable Functional style Imperative


### 12.

**Performance** &

**Best Practice**s (Senior Insight)
- Prefer streams for readability, not micro-optimization
- Avoid modifying external variables inside streams
- Use method references where clarity improves
- Measure before using parallel streams


### 13.

**One-Line Interview** Answer Java 8 Streams provide a declarative, functional way to process collections through lazy, composable operations with clear business intent.


### 14.

**Common Follow**-up Questions
- 

---


## What is Lambda Expression?

What is Lambda Expression? A lambda expression is a concise way to represent an anonymous function—a block of code that can be passed as data and executed later. Lambdas were introduced in Java 8 to support functional programming and to reduce boilerplate code.


### 1.

**Definition** A lambda expression:
- Represents a single method implementation
- Is used mainly with functional interfaces
- Eliminates the need for anonymous inner classes


###


###


### 2. Basic Syntax 

(parameters) -> expression or (parameters) -> { statements; } Examples // Traditional anonymous class Runnable r1 = new Runnable() { public void run() { System.out.println("Running"); } }; // Lambda expression Runnable r2 = () -> System.out.println("Running");


###


###


### 3. Relationship with Functional Interfaces A lambda expression can only be used where a functional interface is expected.

**Example:** @FunctionalInterface interface Calculator { int add(int a, int b); } Calculator c = (a, b) -> a + b;


###


###


### 4. How Lambda Expressions Work Internally
- Lambdas are not anonymous classes
- JVM uses invokedynamic
- Lambda instances may be:
  - Cached
  - Reused
- Improves performance compared to anonymous classes


###


###


### 5. Type Inference 

The compiler infers:
- Parameter types
- Return type (a, b) -> a + b No need to write types explicitly.


###


###


### 7. Variable Capture (Effectively Final) Lambdas can access:
- Local variables
- Instance variables
- Static variables Rule:
- Local variables must be final or effectively final int x = 10; Runnable r = () -> System.out.println(x); // x cannot be modified later


###


###


### 8. Common

**Use Case**s
- Stream API
- Event handling
- Callbacks
- Comparator implementation
- Strategy pattern

**Example:** list.sort((a, b) -> a.getAge() - b.getAge());


###


###


### 9. Limitations of Lambda Expressions
- Cannot have constructors
- Cannot declare instance variables
- Cannot change captured local variables
- Can only implement one abstract method


### 11.

**One-Line Interview** Answer A lambda expression is a concise way to represent an implementation of a functional interface, enabling functional-style programming in Java. Difference between map() and flatMap() Both map() and flatMap() are intermediate stream operations, but they serve different purposes in stream processing.


###


###


### 1. Core Difference (High-Level) Operation

**Purpose** map() One-to-one transformation flatMap() One-to-many transformation + flattening 2. map() Explained What map() Does
- Transforms each element into one element
-

**Output** stream size = input stream size
- Used for simple transformation Example List<String> names = List.of("java", "spring"); List<String> result = names.stream() .map(String::toUpperCase) .toList();

**Output** ["JAVA", "SPRING"] 

 3. flatMap() Explained What flatMap() Does
- Transforms each element into a stream
- Then flattens all resulting streams into one stream
- Used when each element produces multiple elements Example List<List<String>> data = List.of( List.of("Java", "Spring"), List.of("Docker", "Kubernetes") ); List<String> result = data.stream() .flatMap(List::stream) .toList();

**Output** ["Java", "Spring", "Docker", "Kubernetes"]


###


###


### 4. Visual Difference (Conceptual) map() Stream<T> → map → Stream<R> flatMap() Stream<T> → map (Stream<R>) → flatten → Stream<R>


###


###


### 5. Common

**Real-World**

**Use Case** Scenario: Orders and Items class Order { List<Item> items; } 

Using map() (Wrong) Stream<List<Item>> stream = orders.stream() .map(Order::getItems);

**Result:**
- Stream of lists
- Hard to process Using flatMap() (Correct) Stream<Item> stream = orders.stream() .flatMap(o -> o.getItems().stream());

**Result:**
- Single stream of items


###


###


### 6. Handling Optional with flatMap Problem with map Optional<Optional<String>> result = Optional.of("java") .map(s -> Optional.of(s.toUpperCase()));

**Correct with** flatMap Optional<String> result = Optional.of("java") .flatMap(s -> Optional.of(s.toUpperCase()));


### 7.

**Comparison Table** Aspect map() flatMap() Input →

**Output** One-to-one One-to-many

**Output** stream Nested possible Flattened

**Use case** Simple transform Flattening structures 

Typical usage map(String::length) flatMap(Collection::stream)


### 8.

**Common Interview** Traps
- Using map() instead of flatMap() for nested collections
- Forgetting to convert collection to stream inside flatMap
- Thinking flatMap is slower (it is not conceptually slower)


### 9.

**One-Line Interview** Answer map() transforms each element into one element, while flatMap() transforms each element into a stream and flattens the result into a single stream.

---


## Difference between map() and flatMap()

Difference between map() and flatMap()?
- forEach() vs stream().forEach()?
- How does parallel stream work internally?
- Why streams are single-use?

---


## What is Optional and why is it used?

What is Optional and why is it used? Optional is a container object introduced in Java 8 that may or may not contain a non-null value. Its primary goal is to explicitly represent the absence of a value and reduce NullPointerException (NPE) risks.


###


###


### 1. What Is Optional?
- Located in java.util
- Wraps a value that can be:
  - Present
  - Absent
- Forces callers to handle the “no value” case consciously Creation Examples Optional<String> o1 = Optional.of("Java"); // value must be non-null Optional<String> o2 = Optional.ofNullable(null); // empty Optional Optional<String> o3 = Optional.empty(); // explicitly empty


###


###


### 2. Why Was Optional Introduced? 

Problems Before Java 8
- Returning null:
  - Was ambiguous
  - Caused frequent NullPointerException
  - Had no compiler-level indication User user = service.getUser(); // can be null user.getName(); // NPE risk With Optional Optional<User> user = service.getUser(); user.map(User::getName).orElse("Unknown"); Now:
- Absence is explicit
- Caller must decide what to do


###


###


### 3. Key

**Benefits** of Optional


###


###


### 1. Explicit Null Handling
- Makes it clear that a value may be absent


###


###


### 2. Reduces NullPointerException
- Encourages safe access patterns


###


###


### 3. Improves API Design
- Method signature communicates intent Optional<User> findUserById(String id);


###


###


### 4. Functional-Style Operations
- Works seamlessly with:
  - map
  - flatMap
  - filter


###


###


### 4. Common Optional Operations Safe Access optional.ifPresent(value -> System.out.println(value)); Default Value String name = optional.orElse("Default"); Lazy Default (Preferred) String name = optional.orElseGet(() -> computeDefault()); Exception on Absence User user = optional.orElseThrow(() -> new NotFoundException());


### 5.

**Real-World**

**Use Case** Repository Layer Optional<User> findByEmail(String email); Service Layer User user = repo.findByEmail(email) .orElseThrow(() -> new UserNotFoundException()); This avoids:
- Returning null
- Repeated null checks


###


###


### 6. What Optional Should NOT Be Used For (Important) Do NOT:
- Use Optional for:
  - Fields
  - Method parameters
  - Serialization (DTOs, entities)
- Use Optional.get() without checking 

Bad Example Optional<String> name;

**Reason:**
- Adds overhead
- Breaks frameworks (JPA, Jackson)

---


## What are default methods in interfaces?

What are default methods in interfaces? Default methods are methods in an interface that have a method implementation. They were introduced in Java 8 to allow interfaces to evolve without breaking existing implementations.


###


###


### 1. Why Were Default Methods Introduced? Before Java 8:
- Interfaces could have only abstract methods
- Adding a new method to an interface would:
  - Break all implementing classes Problem

**Example (**Pre–Java 8) interface PaymentService { void pay(); } Adding a new method: interface PaymentService { void pay(); void refund(); // breaks all implementations }


###


###


### 2. What Is a Default Method? 

A default method:
- Is declared using the default keyword
- Has a method body
- Is inherited by implementing classes automatically Syntax interface PaymentService { void pay(); default boolean supportsRefund() { return false; } }


###


###


### 3. How Default Methods Work
- Implementing classes:
  - May use the default implementation
  - May override it
- No need to modify existing classes


###


###


### 6. Default Methods and Multiple Inheritance (Diamond Problem) Conflict Scenario interface A { default void show() { System.out.println("A"); } } interface B { default void show() { System.out.println("B"); } } class C implements A, B { // compilation error } 

Resolution (Mandatory Override) class C implements A, B { @Override public void show() { A.super.show(); // or B.super.show() } }


### 10.

**One-Line Interview** Answer Default methods are interface methods with implementations, introduced in Java 8 to allow interface evolution without breaking existing implementations.

---


## Difference between Predicate, Function, Supplier, Consumer

Difference between Predicate, Function, Supplier, Consumer These four are core functional interfaces from java.util.function, widely used in streams, lambdas, and functional-style programming.


###


###


### 1. Predicate

**Purpose** Represents a boolean-valued condition. Method Signature boolean test(T t);

**Use Case** 

Filtering, validation, conditional checks. Example Predicate<Integer> isEven = n -> n % 2 == 0; Stream Usage list.stream() .filter(isEven) .forEach(System.out::println);


###


###


### 2. Function

**Purpose** Represents a transformation from one value to another. Method Signature R apply(T t);

**Use Case** Mapping, conversion, data transformation. Example Function<String, Integer> length = String::length; Stream Usage list.stream() .map(length) .forEach(System.out::println);


###


###


### 3. Consumer

**Purpose** Represents an operation that accepts input and returns nothing. Method Signature void accept(T t); 

Use Case Side effects like logging, printing, persisting. Example Consumer<String> printer = System.out::println; Stream Usage list.stream().forEach(printer);


###


###


### 4. Supplier

**Purpose** Represents a provider of values with no input. Method Signature T get();

**Use Case** Lazy object creation, factory methods, defaults. Example Supplier<UUID> uuidSupplier = UUID::randomUUID;


### 5.

**Comparison Table** (Very Important) Interface Input

**Output** Method Typical Use Predicate T boolean test() filter, validate Function<T,R> T R apply() map, transform Consumer T void accept() side effects Supplier none T get() create, supply


### 9.

**One-Line Interview** Answer 

Predicate checks conditions, Function transforms data, Consumer performs actions without returning a value, and Supplier provides values without input.

---


## Java 8 Features Overview

---

# 📂 Java 8+ Features


## What are Functional Interfaces?

What are Functional Interfaces?](#what-are-functional-interfaces)
15. [

---


## Explain Java 8 Streams with a real use case

Explain Java 8 Streams with a real use case](#explain-java-8-streams-with-a-real-use-case)
16. [

---


## What is Lambda Expression?

What is Lambda Expression?](#what-is-lambda-expression)
17. [

---


## Difference between map() and flatMap()

Difference between map() and flatMap()](#difference-between-map-and-flatmap)
18. [

---


## What is Optional and why is it used?

What is Optional and why is it used?](#what-is-optional-and-why-is-it-used)
19. [

---


## What are default methods in interfaces?

What are default methods in interfaces?](#what-are-default-methods-in-interfaces)
20. [

---


## Difference between Predicate, Function, Supplier, Consumer

Difference between Predicate, Function, Supplier, Consumer](#difference-between-predicate-function-supplier-consumer)
21. [Java 8 Features Overview](#java-8-features-overview)


### Collections Framework

22. [

---


## Java 8 Features Overview

---

# 📂 Java 8+ Features

## What are Functional Interfaces?

What are Functional Interfaces?](#what-are-functional-interfaces)
15. [

---

## Explain Java 8 Streams with a real use case

Explain Java 8 Streams with a real use case](#explain-java-8-streams-with-a-real-use-case)
16. [

---

## What is Lambda Expression?

What is Lambda Expression?](#what-is-lambda-expression)
17. [

---

## Difference between map() and flatMap()

Difference between map() and flatMap()](#difference-between-map-and-flatmap)
18. [

---

## What is Optional and why is it used?

What is Optional and why is it used?](#what-is-optional-and-why-is-it-used)
19. [

---

## What are default methods in interfaces?

What are default methods in interfaces?](#what-are-default-methods-in-interfaces)
20. [

---

## Difference between Predicate, Function, Supplier, Consumer

Difference between Predicate, Function, Supplier, Consumer](#difference-between-predicate-function-supplier-consumer)
21. [Java 8 Features Overview](#java-8-features-overview)


### Collections Framework

22. [

---

## Java 8 Features Overview

Java 8 feature Java 8 introduced lambdas, streams, functional interfaces, default methods, Optional, and a modern date-time API, enabling functional programming and cleaner, more expressive Java code.

---

# 📂 Collections Framework


## Explain ConcurrentModificationException

Explain ConcurrentModificationException and how to handle it


###


###


### 1. What is ConcurrentModificationException? ConcurrentModificationException is a runtime exception thrown by Java collections when a collection is structurally modified while being iterated, outside of the iterator’s own methods.
- It is part of java.util
- It is fail-fast, not thread-safe
- It usually indicates a programming error


###


###


### 2. What Does “Structural Modification” Mean? Structural modification = any operation that changes the size or structure of the collection, such as:
- add()
- remove()
- clear() (Not just changing element values.)


###


###


### 3. Why Does ConcurrentModificationException Occur? Root Cause Most Java collections (ArrayList, HashMap, HashSet) use a fail-fast iterator.
- Collection maintains an internal modCount
- Iterator stores expectedModCount
- If they differ → CME is thrown This prevents:
- Inconsistent iteration
- Undefined behavior


###


###


### 4. Common Scenarios That Cause CME 4.1 Modifying Collection While Iterating (Same Thread) List<String> list = new ArrayList<>(List.of("A", "B", "C")); for (String s : list) { if (s.equals("B")) { list.remove(s); // CME } }

**Reason:**
- Enhanced for-loop uses an iterator internally
- list.remove() modifies structure directly


### 5.

**Correct Ways** to Handle ConcurrentModificationException 5.1 Use Iterator’s remove() Method (Single Thread) Iterator<String> it = list.iterator(); while (it.hasNext()) { if (it.next().equals("B")) { it.remove(); // SAFE } } Why this works:
- Iterator updates expectedModCount
- Collection and iterator stay in sync 5.2 Use removeIf() (Java 8+ Preferred) list.removeIf(s -> s.equals("B"));
- Clean
- Safe
- Internally handles iteration correctly 5.3 Use Concurrent Collections (Multi-threaded) Use concurrent collections instead of ArrayList, HashMap. 

Example: CopyOnWriteArrayList List<String> list = new CopyOnWriteArrayList<>();
- No CME
- Iterates over a snapshot
- Good for read-heavy workloads

**Example:** ConcurrentHashMap Map<String, String> map = new ConcurrentHashMap<>(); 5.4 Synchronize Explicitly (Less Preferred) synchronized (list) { Iterator<String> it = list.iterator(); while (it.hasNext()) { if (it.next().equals("B")) { it.remove(); } } } Works but:
- Error-prone
- Scalability issues


### 9.

**One-Line Interview** Answer 

ConcurrentModificationException occurs when a collection is structurally modified while being iterated using a fail-fast iterator, and it should be handled using iterator removal, safe APIs like removeIf, or concurrent collections.

---


## Comparable vs Comparator

Comparable vs Comparator Both Comparable and Comparator are used for sorting objects, but they differ in where the comparison logic lives, flexibility, and use cases.


###


###


### 1. Basic

**Definition** Comparable
- Defines the natural ordering of a class
- Comparison logic is part of the class itself
- Located in java.lang
- int compareTo(T o); Comparator
- Defines external/custom ordering
- Comparison logic is separate from the class
- Located in java.util
- int compare(T o1, T o2);


### 3.

**Key Differences** (Comparison Table) Aspect Comparable Comparator Package java.lang java.util 

Method compareTo() compare() Sorting type Natural ordering Custom ordering Where logic lives Inside class Outside class Multiple sort orders No Yes Class modification Required Not required Used by default Yes Only when provided


### 4.

**Example:** Comparable class Employee implements Comparable<Employee> { int id; @Override public int compareTo(Employee e) { return Integer.compare(this.id, e.id); } }

**Usage:** Collections.sort(list);


### 5.

**Example:** Comparator Comparator<Employee> byName = (e1, e2) -> e1.name.compareTo(e2.name);

**Usage:** Collections.sort(list, byName);


###


###


### 6. Multiple Sorting with Comparator (Java 8+) Comparator<Employee> comp = Comparator.comparing(Employee::getName) .thenComparing(Employee::getId);


###


###


### 7. Relationship with equals() (Interview Favorite) Comparable Rule If compareTo() returns 0, equals() should return true Breaking this rule causes issues in:
- TreeSet
- TreeMap


###


###


### 8. Usage in Collections 

Collection Uses Comparable Uses Comparator TreeSet Yes Optional TreeMap Yes Optional Collections.sort Yes Optional Stream.sorted Yes Optional


### 9.

**When to Use** What (Senior Guidance) Use Comparable When:
- There is one natural ordering
- Ordering is intrinsic to the object
- You control the class Use Comparator When:
- Multiple sorting strategies are needed
- You cannot modify the class
- Sorting is context-dependent


### 10.

**Common Interview** Traps
- Forgetting Comparable modifies class
- Violating equals–compareTo contract
- Overusing Comparable for multiple orderings
- Not using Comparator chaining


### 11.

**One-Line Interview** Answer Comparable defines a class’s natural ordering internally, while Comparator defines external, customizable ordering strategies.

---


## Difference between HashMap, Hashtable, and ConcurrentHashMap

Difference between HashMap, Hashtable, and ConcurrentHashMap


###


###


### 1. HashMap

**What it is**
- Non-synchronized map implementation
- Allows one null key and multiple null values Thread-safety
- Not thread-safe
- Concurrent modifications can cause:
  - Data inconsistency
  - Infinite loops (pre-Java 8 resize issue)

**Performance**
- Fastest in single-threaded scenarios
- No locking overhead

**Use case**
- Single-threaded code
- Thread-safe access guaranteed externally


###


###


### 2. Hashtable

**What it is**
- Legacy synchronized map (since early Java)
- Does not allow null key or null value Thread-safety
- Thread-safe via method-level synchronization
- Every operation locks the entire map

**Performance**
- Poor scalability under concurrency
- High contention Why it’s discouraged
- Coarse-grained locking
- Obsolete design
- Replaced by ConcurrentHashMap


###


###


### 3. ConcurrentHashMap

**What it is**
- High-performance, thread-safe map from java.util.concurrent
- Designed for high concurrency Thread-safety
- Thread-safe with fine-grained locking
- Java 8+:
  - Locking at bucket level
  - CAS (Compare-And-Swap)
- Reads are mostly lock-free Null handling
- Does not allow null keys or values
- Prevents ambiguity in concurrent reads

**Performance**
- Excellent under multi-threading
- Scales well with CPU cores

**Use case**
- High-concurrency systems
- Caches
- Shared mutable state Side-by-Side Comparison (Very Important) 

Feature HashMap Hashtable ConcurrentHashMap Thread-safe No Yes Yes Synchronization None Method-level Fine-grained

**Performance** High (single thread) Poor High Null key Yes (1) No No Null value Yes No No Legacy No Yes No Fail-fast iterator Yes No Weakly consistent Scalability Poor Poor Excellent Iterator Behavior (Interview Trap)
- HashMap
  - Fail-fast
  - Throws ConcurrentModificationException
- Hashtable
  - Not fail-fast
  - Enumeration is thread-safe but outdated
- ConcurrentHashMap
  - Weakly consistent iterator
  - Does not throw ConcurrentModificationException
  - Reflects some but not necessarily all changes Java 8+ Internal Changes (Senior Insight) ConcurrentHashMap
- No more segment-level locks
- Uses:
  - CAS
  - Synchronized blocks on buckets
- Better memory and CPU efficiency

**When I Use** Which (Practical Answer)
- HashMap
  - Default choice
  - When thread safety is not required
- ConcurrentHashMap
  - Any shared mutable map in multi-threaded code
- Hashtable
  - Almost never
  - Only for legacy code maintenance

**Common Interview** Trap Questions Q: Can we make HashMap thread-safe? Yes, via Collections.synchronizedMap(), but it still uses coarse-grained locking and does not scale well. Q: Why does ConcurrentHashMap not allow null? To avoid ambiguity between “no mapping” and “mapped to null” in concurrent reads.

**One-Line Interview** Answer HashMap is non-thread-safe and fast, Hashtable is thread-safe but uses coarse-grained synchronization and is legacy, while ConcurrentHashMap provides high-performance thread-safe access using fine-grained locking and non-blocking reads.

---


## How does HashMap handle collisions internally?

How does HashMap handle collisions internally? A collision occurs in a HashMap when two different keys produce the same hash index. HashMap resolves collisions using a bucket-based data structure that evolved significantly in Java


###


###


### 8. High-Level Idea
- HashMap internally uses an array of buckets
- Each bucket can store multiple entries
- When collisions happen, entries are stored together in the same bucket
- Retrieval still works using equals() comparison Step-by-Step Internal Working


###


###


### 1. Hash Calculation For a key: 1. hashCode() is called


###


###


### 2. HashMap applies a spread function to reduce collisions


###


###


### 3. Index is calculated using: index = (n - 1) & hash Where n = table capacity (always power of 2)


###


###


### 2. Bucket Selection
- HashMap finds the target bucket using the calculated index
- If the bucket is empty → entry is placed directly


###


###


### 3. Collision Handling (Before Java 8)
- Each bucket was a LinkedList
- On collision:
  - New entry added to the list
- Lookup time degrades from O(1) to O(n)


###


###


### 4. Collision Handling (Java 8+) From Java 8 onward:
- Buckets start as LinkedList
- When collisions exceed a threshold:
  - LinkedList converts to a Red-Black Tree This improves worst-case performance.

**Treeification** (Very Important Interview Point) Conditions for Tree Conversion A bucket is converted from list → tree when:
- Number of entries in bucket ≥ 8 (TREEIFY_THRESHOLD)
- HashMap capacity ≥ 64 If capacity is smaller:
- HashMap resizes instead of treeifying

**Untreeification**
- If entries reduce below 6
- Tree converts back to a linked list 

Data Structures Used Java Version Bucket Structure Java 7 and earlier LinkedList Java 8+ LinkedList → Red-Black Tree Lookup Process with Collision


###


###


### 1. Calculate hash


###


###


### 2. Locate bucket


###


###


### 3. If single entry → return


###


###


### 4. If list:
  - Traverse and compare using equals()


###


###


### 5. If tree:
  - Perform tree lookup (O(log n)) Why equals() Matters
- Hash collision does not mean key equality
- equals() determines actual key match
- Incorrect equals() leads to:
  - Duplicate keys
  - Data loss
  - Retrieval failures

**Performance** Impact Scenario Time Complexity 

No collision O(1) Collision (list) O(n) Collision (tree) O(log n)

**Common Interview** Trap Questions Q: Does HashMap allow duplicate keys? No. If equals() returns true, value is replaced. Q: Can poor hashCode() break performance? Yes. All entries may fall into one bucket. Q: Why power-of-2 capacity? Enables fast index calculation using bitwise AND.

**One-Line Interview** Answer HashMap handles collisions by storing multiple entries in the same bucket; before Java 8 it used linked lists, and from Java 8 onward it converts heavily collided buckets into red-black trees to maintain performance.

---


## What changed in HashMap after Java 8?

What changed in HashMap after Java 8? Java 8 introduced major internal improvements to HashMap focused on performance, predictability, and safety under heavy collisions—without changing its external API.


###


###


### 1. LinkedList → Red-Black Tree (Biggest Change) 

Before Java 8
- Each bucket stored entries in a LinkedList
- Worst-case lookup time: O(n)
- Vulnerable to performance degradation and DoS attacks Java 8+
- Buckets start as LinkedList
- Convert to Red-Black Tree when collisions are high
- Worst-case lookup time becomes O(log n)

**Treeification** conditions
- Bucket size ≥ 8
- Table capacity ≥ 64


###


###


### 2. Tree

**Untreeification**
- When entries in a tree bucket drop below 6
- Tree converts back to LinkedList
- Avoids unnecessary tree overhead


###


###


### 3. Improved Hash Spreading Function Java 8 improved the internal hash mixing logic:
- Better distribution of keys across buckets
- Reduces collision probability
- Improves overall performance


###


###


### 4. Safer Resize Behavior Before Java 8
- During resize, linked lists could reverse order
- In multi-threaded misuse, this caused:
  - Infinite loops
  - CPU spikes Java 8+
- Resize logic preserves bucket order
- Eliminates infinite loop risk during resize


### 5.

**Performance** Under Collision Attacks
- Tree bins mitigate worst-case behavior
- Protects against malicious inputs that generate same hashCode()
- Important for public-facing systems


###


###


### 6. No Change in External Behavior

**Important interview** clarification:
- API did not change
- Still:
  - Not thread-safe
  - Allows one null key
  - Allows multiple null values All changes are internal optimizations. Before vs After Java 8 (Summary Table) Aspect Java 7 and Earlier Java 8+ Bucket structure LinkedList List → Red-Black Tree Worst-case lookup O(n) O(log n) Resize safety Risky Safe Collision handling Weak Strong 

DoS resistance Low High

**Common Interview** Trap Questions Q: Does HashMap become thread-safe in Java 8? No. HashMap is still not thread-safe. Q: Does HashMap always use trees now? No. Trees are used only when collision threshold is exceeded. Q: Does treeification happen immediately on collision? No. Only after threshold and capacity conditions are met.

**One-Line Interview** Answer After Java 8, HashMap introduced tree-based buckets using red-black trees for high-collision scenarios, improving worst-case lookup time from O(n) to O(log n) and making resizing safer and more predictable.

---


## Why does HashSet not allow duplicate elements?

Why does HashSet not allow duplicate elements? HashSet does not allow duplicate elements because it is designed to enforce uniqueness using hashing and equality checks. Internally, it relies on a HashMap, where each element is stored as a key, and keys in a map must be unique. Internal Implementation (Key Insight)
- HashSet is backed by a HashMap
- Each element added to the set becomes a key in the map
- All values are a dummy constant object Conceptually: HashMap<E, Object> map; private static final Object PRESENT = new Object(); When you do: set.add("A");

**Internally:** map.put("A", PRESENT); Since HashMap does not allow duplicate keys, HashSet automatically enforces uniqueness. How Duplicate Detection Works When you add an element to a HashSet: 1. hashCode() is called to find the bucket


###


###


### 2. If a bucket already contains an element:
  - equals() is called


###


###


### 3. If equals() returns true:
  - Element is considered a duplicate
  - It is not added No exception is thrown; the operation simply returns false. Role of hashCode() and equals() (Very Important)
- hashCode() → determines bucket location
- equals() → determines actual equality Contract
- If equals() returns true, hashCode() must be equal
- Violating this contract breaks HashSet behavior

**What Happens** if hashCode / equals are Incorrect
- Duplicate logical objects may be added
- Lookup may fail
- Data corruption in collections This is a common production bug.

**Performance** Implication Operation Time Complexity add O(1) average contains O(1) average Worst case (poor hash):
- O(n) or O(log n) (Java 8+ tree bins)

**Common Interview** Trap Questions Q: Does HashSet maintain insertion order? No. Use LinkedHashSet if ordering is required. Q: Can HashSet contain null? Yes. One null element is allowed. Q: How does HashSet know two objects are duplicates? Using hashCode() and equals(). 

One-Line Interview Answer HashSet does not allow duplicate elements because it is internally backed by a HashMap, where each element is stored as a unique key, and duplicates are detected using hashCode() and equals().

---


## Can a HashMap key be mutable?

Can a HashMap key be mutable?

**What happens** if it is? Yes, a HashMap key can be mutable, but it should never be mutable. Using a mutable key breaks the internal contract of HashMap and leads to unpredictable behavior.

**Why HashMap** Keys Should Be Immutable HashMap relies on two methods of the key:
- hashCode()
- equals() These are used to:


###


###


### 1. Compute the bucket index


###


###


### 2. Locate the entry within the bucket If a key’s state changes after insertion, its hashCode() and/or equals() may change.

**What Happens** Internally (Step-by-Step)


###


###


### 1. Key Inserted map.put(key, value);
- hashCode() is computed
- Entry stored in bucket A


###


###


### 2. Key is Mutated key.setId(200); // affects hashCode/equals Now:
- hashCode() changes
- Logical identity changes


###


###


### 3. Lookup Fails map.get(key); // returns null Why?
- HashMap looks in bucket B (new hash)
- Entry still exists in bucket A
-

**Result:** entry becomes unreachable Consequences of Mutable Keys
- get() returns null
- containsKey() fails
- remove() fails
- Memory leaks (entries can’t be removed)
- Duplicate logical keys can exist
- Data corruption These bugs are silent and extremely hard to debug.

**Example (**Classic Interview Scenario) class Employee { 

 int id; // hashCode & equals use id } Map<Employee, String> map = new HashMap<>(); Employee e = new Employee(1); map.put(e, "Alice"); e.id = 2; map.get(e); // null When Is a Mutable Key Safe? Only when:
- Mutable fields are not used in hashCode() / equals()
- Logical identity remains unchanged But this is fragile and risky.

**Best Practice**s (Strong Interview Answer)
- Use immutable keys:
  - String
  - Integer
  - Long
- Make key fields:
  - final
  - Set via constructor
- Do not expose setters for key fields
- Ensure equals() and hashCode() are consistent and stable

**Common Interview** Trap Questions Q: Does HashMap prevent mutable keys? No. It’s a developer responsibility. Q: Will HashMap rehash if key changes? No. HashMap has no way to detect mutation. Q: Does ConcurrentHashMap solve this? No. Same rule applies.

**One-Line Interview** Answer A HashMap key can be mutable, but mutating it after insertion breaks hashCode/equals consistency, making the entry unreachable and causing unpredictable behavior.

---

# 📂 Multithreading and Concurrency


## What is Thread lifecycle?

What is Thread lifecycle? The thread lifecycle describes the different states a thread goes through from creation to termination during its execution in the JVM. Java defines thread states via java.lang.Thread.State.


###


###


### 1. Thread

**Lifecycle** States Java threads go through six well-defined states: NEW → RUNNABLE → BLOCKED / WAITING / TIMED_WAITING → RUNNABLE → TERMINATED


###


###


### 2. NEW State

**Meaning**
- Thread object is created
- start() is not yet called

**Characteristics**
- Thread exists only as an object
- No system resources allocated Example 

Thread t = new Thread(() -> {}); // State: NEW

**Interview Note** Calling run() directly does not change the state to RUNNABLE.


###


###


### 3. RUNNABLE State

**Meaning**
- Thread is ready to run or running
- JVM has handed it to OS scheduler Important Detail In Java:
- RUNNING and READY are combined into RUNNABLE Example t.start(); // State: RUNNABLE Whether it actually runs depends on OS scheduling.


###


###


### 4. BLOCKED State

**Meaning**
- Thread is waiting to acquire a monitor lock
- Happens with synchronized Example synchronized (lock) { 

 // another thread is holding the lock } Key Point
- BLOCKED is only for monitor lock contention
- Not related to wait() or sleep()


###


###


### 5. WAITING State

**Meaning**
- Thread is waiting indefinitely
- Until another thread explicitly wakes it up

**Caused By**
- Object.wait()
- Thread.join()
- LockSupport.park() Example lock.wait(); // State: WAITING

**Resume Trigger**
- notify() / notifyAll()
- Joined thread completes


###


###


### 6. TIMED_WAITING State

**Meaning**
- Thread waits for a specified amount of time 

Caused By
- Thread.sleep(time)
- wait(time)
- join(time)
- parkNanos() Example Thread.sleep(1000); // State: TIMED_WAITING After timeout, thread moves back to RUNNABLE.


###


###


### 7. TERMINATED State

**Meaning**
- Thread execution is complete
- run() method exits normally or with exception

**Characteristics**
- Cannot be restarted
- Calling start() again throws IllegalThreadStateException Example // run() completes // State: TERMINATED


###


###


### 8. State Transition Summary From To Trigger 

NEW RUNNABLE start() RUNNABLE BLOCKED Waiting for monitor lock RUNNABLE WAITING wait(), join() RUNNABLE TIMED_WAITING sleep(), timed wait WAITING RUNNABLE notify(), join completes TIMED_WAITING RUNNABLE Timeout expires RUNNABLE TERMINATED run() finishes


###


###


### 9. Important Interview Clarifications RUNNABLE does NOT mean running
- It means eligible to run
- Actual execution depends on OS scheduler sleep() does NOT release lock
- Thread remains owner of any acquired monitor 

wait() releases lock
- Allows other threads to acquire the monitor


### 10.

**Common Interview** Traps
- Saying there is a separate RUNNING state (incorrect)
- Confusing BLOCKED with WAITING
- Assuming sleep() releases lock
- Thinking a thread can be restarted

---


## Difference between synchronized and Lock

Difference between synchronized and Lock Both synchronized and Lock are used to control concurrent access to shared resources, but they differ significantly in capabilities, flexibility, and control.


###


###


### 1. Basic

**Definition** synchronized
- A language-level keyword
- Implicitly uses monitor locks
- Lock acquisition and release are handled by JVM Lock
- An interface from java.util.concurrent.locks
- Explicit locking mechanism
- Provides advanced concurrency features


###


###


### 3. Lock Acquisition & Release 

synchronized synchronized (lock) { // critical section }
- Lock is released automatically, even if an exception occurs Lock lock.lock(); try { // critical section } finally { lock.unlock(); }
- Developer must release the lock explicitly
- Missing unlock() causes deadlock


###


###


### 4. Advanced Features of Lock 1. tryLock() Allows avoiding deadlock by trying to acquire lock conditionally: if (lock.tryLock()) { try { // work } finally { 

 lock.unlock(); } }

---


## Difference between Checked and Unchecked Exceptions

---

# 📂 Collections Framework


## Explain ConcurrentModificationException

Explain ConcurrentModificationException](#explain-concurrentmodificationexception)
23. [

---


## Comparable vs Comparator

Comparable vs Comparator](#comparable-vs-comparator)
24. [

---


## Difference between HashMap, Hashtable, and ConcurrentHashMap

Difference between HashMap, Hashtable, and ConcurrentHashMap](#difference-between-hashmap-hashtable-and-concurrenthashmap)
25. [

---


## How does HashMap handle collisions internally?

How does HashMap handle collisions internally?](#how-does-hashmap-handle-collisions-internally)
26. [

---


## What changed in HashMap after Java 8?

What changed in HashMap after Java 8?](#what-changed-in-hashmap-after-java-8)
27. [

---


## Why does HashSet not allow duplicate elements?

Why does HashSet not allow duplicate elements?](#why-does-hashset-not-allow-duplicate-elements)
28. [

---


## Can a HashMap key be mutable?

Can a HashMap key be mutable?](#can-a-hashmap-key-be-mutable)


### Multithreading and Concurrency

29. [

---

# 📂 Multithreading and Concurrency


## What is Thread lifecycle?

What is Thread lifecycle?](#what-is-thread-lifecycle)
30. [

---


## Difference between synchronized and Lock

Difference between synchronized and Lock](#difference-between-synchronized-and-lock)
31. [Difference between Checked and Unchecked Exceptions](#difference-between-checked-and-unchecked-exceptions)
32. [

---


## Difference between Checked and Unchecked Exceptions

---

# 📂 Collections Framework

## Explain ConcurrentModificationException

Explain ConcurrentModificationException](#explain-concurrentmodificationexception)
23. [

---

## Comparable vs Comparator

Comparable vs Comparator](#comparable-vs-comparator)
24. [

---

## Difference between HashMap, Hashtable, and ConcurrentHashMap

Difference between HashMap, Hashtable, and ConcurrentHashMap](#difference-between-hashmap-hashtable-and-concurrenthashmap)
25. [

---

## How does HashMap handle collisions internally?

How does HashMap handle collisions internally?](#how-does-hashmap-handle-collisions-internally)
26. [

---

## What changed in HashMap after Java 8?

What changed in HashMap after Java 8?](#what-changed-in-hashmap-after-java-8)
27. [

---

## Why does HashSet not allow duplicate elements?

Why does HashSet not allow duplicate elements?](#why-does-hashset-not-allow-duplicate-elements)
28. [

---

## Can a HashMap key be mutable?

Can a HashMap key be mutable?](#can-a-hashmap-key-be-mutable)


### Multithreading and Concurrency

29. [

---

# 📂 Multithreading and Concurrency

## What is Thread lifecycle?

What is Thread lifecycle?](#what-is-thread-lifecycle)
30. [

---

## Difference between synchronized and Lock

Difference between synchronized and Lock](#difference-between-synchronized-and-lock)
31. [Difference between Checked and Unchecked Exceptions](#difference-between-checked-and-unchecked-exceptions)
32. [

---

## Difference between Checked and Unchecked Exceptions

Difference between Checked and Unchecked exceptions


###


###


### 1. What Are Exceptions in Java? An exception is an event that disrupts the normal flow of a program during runtime. All exceptions in Java are part of the exception hierarchy rooted at Throwable. Main branches:
- Exception
- Error


###


###


### 2. Checked Exceptions

**Definition** Checked exceptions are exceptions that are checked at compile time. The compiler forces the developer to:
- Handle the exception using try-catch, or
- Declare it using throws Examples
- IOException
- SQLException
- FileNotFoundException
- ClassNotFoundException Example Code public void readFile() throws IOException { FileReader reader = new FileReader("data.txt"); } If not handled or declared, compilation fails.

**When to Use**
- When an error is recoverable
- When the caller can reasonably take corrective action


###


###


### 3. Unchecked Exceptions

**Definition** Unchecked exceptions are not checked at compile time. They occur at runtime, and the compiler does not force handling. Examples
- NullPointerException
- ArrayIndexOutOfBoundsException
- ArithmeticException
- IllegalArgumentException All unchecked exceptions extend RuntimeException. Example Code int result = 10 / 0; // ArithmeticException 

Compiles successfully, fails at runtime.

**When to Use**
- Programming errors
- Invalid assumptions
- Bugs that should be fixed in code, not handled at runtime


### 4.

**Key Differences** (Comparison Table) Aspect Checked Exception Unchecked Exception Compile-time checking Yes No Extends Exception (excluding RuntimeException) RuntimeException Handling mandatory Yes No Typical cause External conditions Programming bugs Recoverable Often Rarely Example IOException NullPointerException


###


###


### 5. Exception Hierarchy (Important Interview Concept) Throwable ├── Error └── Exception ├── Checked Exceptions └── RuntimeException (Unchecked)
- Error represents serious issues (OutOfMemoryError) and should not be caught
- Only Exception and its subclasses are meant to be handled


### 6.

**Real-World** Usage Guidelines (Senior Perspective) Use Checked Exceptions When:
- Failure is expected and recoverable
- External systems are involved (file, DB, network)
- Business flow depends on error handling 

Use Unchecked Exceptions When:
- Contract violations occur
- Method preconditions are not met
- Bugs need fixing, not handling

---


## Difference between Thread.start() and run()

Difference between Thread.start() and run() 1 start() – Creates a new thread
- start() tells the JVM to create a new OS-level thread
- JVM internally calls run() in a separate call stack
- Execution is asynchronous
- Thread goes through lifecycle states: NEW → RUNNABLE → RUNNING → TERMINATED Thread t = new Thread(() -> { 

 System.out.println(Thread.currentThread().getName()); }); t.start();

**Output** thread name: Thread-0 (or similar) 2 run() – Just a normal method call
- run() executes in the current thread
- No new thread is created
- No concurrency
- Behaves like any regular method Thread t = new Thread(() -> { System.out.println(Thread.currentThread().getName()); }); t.run();

**Output** thread name: main Key Interview Line (Use This) "start() creates a new execution path by asking JVM to spawn a new thread, whereas calling run() directly is just a normal method invocation on the current thread without any concurrency." Internal JVM Behavior (18+ yrs justification)
- start() is a native method
- It:
  - Registers thread with JVM scheduler
  - Allocates a new stack
  - Calls run() internally when the thread is scheduled public synchronized void start() { if (threadStatus != 0) throw new IllegalThreadStateException(); start0(); // native }

**Common Interview** Follow-ups (Answer Ready) ❓ Can we call start() twice? ❌ No – throws IllegalThreadStateException ✅ A thread can be started only once ❓ Why run() is not synchronized but start() is?
- start() changes thread state → must be thread-safe
- run() is application logic ❓ In Spring Boot, do we use Thread.start() directly? ❌ Rarely ✅ We prefer:
- @Async
- TaskExecutor
- CompletableFuture
- Virtual Threads (Java 21+) Because thread lifecycle management is a framework responsibility 

Real-World Rule (Production Experience) "If you see run() being called directly in production code, it’s almost always a bug."

---


## Java Memory Model (JMM) and volatile keyword

Java Memory Model (JMM) and volatile keyword


###


###


### 1. Java Memory Model (JMM): What it actually defines The Java Memory Model is not about JVM heap layout or GC. It is a formal contract (JSR-133) that defines:
- Visibility: when writes by one thread become observable by another
- Ordering: what reordering of reads/writes is allowed
- Atomicity: which operations are indivisible
- Happens-Before relationships It exists because:
- CPUs reorder instructions
- Compilers reorder instructions
- Caches are not coherent in a simple way
- JVM must run consistently on all architectures Without JMM, multithreaded Java would be undefined.


###


###


### 2. Core abstraction: Happens-Before (HB) Happens-Before is the only thing that guarantees visibility + ordering. If A happens-before B, then:
- All memory writes visible to A are visible to B
- A’s effects are observed before B executes If there is no happens-before, behavior is legal but unpredictable Key Happens-Before rules


###


###


### 1. Program Order Rule
  - Within a single thread, earlier actions HB later actions


###


###


### 2. Monitor Lock Rule
  - unlock(monitor) HB lock(monitor) on same monitor


###


###


### 3. Volatile Rule
  - Write to a volatile variable HB subsequent read of same variable


###


###


### 4. Thread Start Rule
  - Thread.start() HB any action in started thread


###


###


### 5. Thread Join Rule
  - All actions in a thread HB successful return from Thread.join()


###


###


### 6. Transitivity
  - If A HB B and B HB C, then A HB C Interviewers often ask this explicitly.


###


###


### 3. What JMM allows the JVM/CPU to do Reordering types allowed (unless constrained)
- Load → Load
- Load → Store
- Store → Load
- Store → Store Reordering is legal unless it violates happens-before. This is why naïve double-checked locking was broken pre-Java 5. 4. volatile: what it guarantees and what it does not Guarantees provided by volatile


###


###


### 1. Visibility A write to a volatile variable:
- Is immediately flushed to main memory
- Invalidates other thread caches for that variable A read:
- Always sees the latest write


###


###


### 2. Ordering (Memory Barriers) 

volatile introduces memory fences:
- Volatile write:
  - StoreStore barrier
  - StoreLoad barrier
- Volatile read:
  - LoadLoad barrier
  - LoadStore barrier Effect:
- Code before a volatile write cannot be reordered after it
- Code after a volatile read cannot be reordered before it This is critical.


###


###


### 3. Happens-Before volatile write →HB→ volatile read What volatile does NOT guarantee


###


###


### 1. Atomicity (except for single read/write) This is a classic trap. volatile int x; x++; // NOT atomic Because:
- Read
- Increment
- Write Multiple steps → race condition Atomic only for:
- Single read/write of primitives (except long/double pre-Java 5) 5. volatile vs synchronized 

Aspect volatile synchronized Visibility Yes Yes Ordering Yes Yes Atomicity No Yes Mutual exclusion No Yes Blocking No Yes

**Use case** State flags, publication Critical sections Rule of thumb:
- If only visibility + ordering → volatile
- If compound invariants → synchronized / locks


### 6.

**Safe Publication** and volatile One of the most important real-world uses of volatile is safe publication.

**Example:** broken publication class Holder { int x; } Holder h; Thread A: h = new Holder(); h.x = 42; Thread B: if (h != null) { print(h.x); // could be 0 without HB } Because:
- Reference write and field write can be reordered Fix with volatile 

volatile Holder h; Now:
- Writes before assigning h HB any read of h
- Fields are fully visible


### 7.

**Double-Checked** Locking (DCL)

**Correct post**-Java 5 implementation class Singleton { private static volatile Singleton instance; static Singleton getInstance() { if (instance == null) { synchronized (Singleton.class) { if (instance == null) { instance = new Singleton(); } } } return instance; } } Why volatile is mandatory:
- Object creation involves:


###


###


### 1. Allocate memory


###


###


### 2. Initialize fields


###


###


### 3. Assign reference Without volatile, steps 2 and 3 may reorder. 8. final fields and JMM (often missed in interviews) Final fields have special visibility guarantees. If:
- Object is properly constructed
- Reference does not escape constructor Then:
- Final fields are visible without synchronization This is why immutable objects are thread-safe by design. 9. volatile vs Atomic* classes AtomicInteger:
- Uses volatile + CAS
- Provides atomic read-modify-write
- Built on Unsafe / VarHandles Use:
- Counters
- Sequence generators
- Lock-free algorithms volatile alone is insufficient for these.


###


###


### 10. When volatile is the right choice Correct use cases:
- State flags (shutdown, initialized)
- One-time publication
- Double-checked locking
- Read-mostly configuration
- Versioning / sequence visibility Incorrect use cases:
- Counters
- Compound invariants
- Multi-field consistency


###


###


### 11. Interview trick questions you should expect


###


###


### 1. Is volatile faster than synchronized?
  - Yes for contention-free visibility, but not a replacement


###


###


### 2. Does volatile guarantee atomicity?
  - Only for single read/write


###


###


### 3. Can volatile replace locks?
  - No, unless invariants are trivial


###


###


### 4. Why was DCL broken earlier?
  - No happens-before guarantees pre-JSR-133


###


###


### 5. Is volatile implemented using locks?
  - No, it uses memory barriers


###


###


### 12. One-line interview summary The Java Memory Model defines visibility, ordering, and atomicity through happens-before rules. volatile provides visibility and ordering guarantees via memory barriers but does not provide atomicity or mutual exclusion. Java memory management and how JVM cleans unreachable objects

---

# 📂 Spring Framework and Spring Boot


## What is Dependency Injection?

What is Dependency Injection? Dependency Injection (DI) is a design principle in which an object’s dependencies are provided from the outside, instead of the object creating them itself. In simple terms: Objects do not create their dependencies; dependencies are injected into them.


###


###


### 1. Problem Without Dependency Injection Tight Coupling Example class OrderService { private PaymentService paymentService = new PaymentService(); } Problems
- Strong coupling to PaymentService
- Difficult to unit test
- Hard to replace implementation
- Violates SOLID principles


###


###


### 2. What Dependency Injection Solves DI addresses:
- Tight coupling
- Poor testability
- Rigid design
- Difficult maintenance 

With DI:
- Classes depend on abstractions
- Implementations can be swapped easily
- Code becomes modular and testable


###


###


### 3. Dependency Injection Example Using Constructor Injection class OrderService { private final PaymentService paymentService; public OrderService(PaymentService paymentService) { this.paymentService = paymentService; } } Now:
- OrderService does not know how PaymentService is created
- Dependency is injected externally


### 4.

**Types of** Dependency Injection


###


###


### 1. Constructor Injection (Recommended) class UserService { private final UserRepository repo; public UserService(UserRepository repo) { this.repo = repo; } }

**Why preferred**:
- Immutable dependencies
- Mandatory dependencies enforced
- Easy unit testing


###


###


### 2. Setter Injection class UserService { private UserRepository repo; public void setRepo(UserRepository repo) { this.repo = repo; } }

**Use case**:
- Optional dependencies


###


###


### 3. Field Injection (Not Recommended) class UserService { @Autowired private UserRepository repo; }

**Problems:**
- Hidden dependencies
- Hard to test
- Breaks immutability


###


###


### 5. Dependency Injection vs Dependency Inversion (Interview Trap) Dependency Injection
- How dependencies are provided Dependency Inversion Principle (DIP)
- What to depend on (abstractions, not concrete classes) DI is a technique to implement DIP.


###


###


### 6. DI and Inversion of Control (IoC)
- IoC: Framework controls object creation and lifecycle
- DI: A form of IoC where dependencies are injected In frameworks like Spring:
- Container creates objects
- Resolves dependencies
- Injects them automatically


### 7.

**Real-World**

**Benefits** (Senior Perspective)
- Loose coupling
- Easy unit testing (mocking)
- Cleaner architecture
- Better scalability
- Supports microservices and modular design Example test: OrderService service = new OrderService(mockPaymentService); No framework required.


### 8.

**Common Interview** Traps
- Confusing DI with IoC
- Thinking DI is framework-specific
- Using field injection everywhere
- Injecting concrete classes instead of interfaces


### 9.

**When to Use** Dependency Injection
- Almost always in enterprise applications
- Service layers
- Controllers
- Repositories
- Any code requiring flexibility and testability


### 10.

**One-Line Interview** Answer 

Dependency Injection is a design principle where an object receives its dependencies from external sources instead of creating them, promoting loose coupling and testability.

---


## Difference between @Component, @Service, @Repository

Difference between @Component, @Service, @Repository All three annotations are Spring stereotype annotations used to declare beans, but they convey different semantic meanings and enable specific framework behaviors.


###


###


### 1. Common Ground (Very Important First Point)
- All three are specializations of @Component
- All are detected via component scanning
- All create Spring-managed beans
- From a pure DI perspective, they are functionally equivalent @Component @Service @Repository Spring treats them differently by intent and additional behavior, not by bean creation. 2. @Component – Generic Stereotype

**Purpose**
- General-purpose annotation
- Used when a class does not clearly belong to service or repository layers

**Typical Usage**
- Utility classes
- Helper classes
- Adapter classes
- Generic components Example @Component public class JwtUtil { public String generateToken() { return "token"; } }

**Interview Insight** Use @Component when no specific role fits. 3. @Service – Business Logic Layer

**Purpose**
- Marks a service-layer component
- Represents business logic
- Improves readability and architectural clarity

**Typical Usage**
- Business services
- Transaction orchestration
- Domain operations Example @Service public class OrderService { public void placeOrder() { // business logic } } 

Important Note
- @Service does not add extra behavior by default
- It is mainly semantic
- Often used with @Transactional

**Interview Insight** @Service clearly communicates intent to developers and tools. 4. @Repository – Persistence Layer (Most Important Difference)

**Purpose**
- Marks a data access component
- Used for DAO / Repository layer

**Typical Usage**
- Database operations
- JPA repositories
- JDBC / ORM access Example @Repository public class UserRepository { public User findById(Long id) { return null; } }


###


###


### 5. Exception Translation (Key Technical Difference) Why @Repository Is Special Spring applies automatic exception translation to classes annotated with @Repository.
- Converts low-level exceptions:
  - SQLException
  - Hibernate exceptions
- Into Spring’s unchecked DataAccessException hierarchy Without @Repository SQLException // leaks to service layer With @Repository DataAccessException // consistent, unchecked This enables:
- Cleaner service code
- Database-agnostic exception handling


### 6.

**Comparison Table** (Interview Favorite) Aspect @Component @Service @Repository Layer Generic Business Persistence Semantic meaning Generic bean Business logic Data access Auto-detected Yes Yes Yes Exception translation No No Yes Recommended usage Utilities Services DAOs / Repos


### 7.

**Common Interview** Traps
- Saying they are completely identical (partially false)
- Using @Component everywhere
- Not knowing about exception translation
- Using @Service for repositories


### 8.

**Real-World** (Senior-Level

**Best Practice**)
- Controller layer → @RestController
- Service layer → @Service
- Repository layer → @Repository
- Helpers / utils → @Component This:
- Improves readability
- Enforces clean architecture
- Helps AOP, tooling, and monitoring


### 9.

**One-Line Interview** Answer @Component is a generic stereotype, @Service marks business logic, and @Repository marks data access components and enables automatic exception translation.

---


## Difference between @Controller and @RestController

Difference between @Controller and @RestController Both annotations are used in Spring MVC to handle HTTP requests, but they serve different purposes and produce different types of responses.


###


###


### 1. Core Difference (One-Line Answer) @Controller is used for MVC applications that return views, while @RestController is used for REST APIs that return data (JSON/XML) directly. 2. @Controller

**Purpose**
- Used in Spring MVC
- Returns view names
- Typically works with:
  - JSP
  - Thymeleaf
  - Freemarker Example @Controller public class UserController { @GetMapping("/user") public String getUser(Model model) { model.addAttribute("name", "John"); return "user"; // view name } }

**Key Points**
- Return value is interpreted as view name
- Requires:
  - ViewResolver
- To return JSON, you must use @ResponseBody @ResponseBody @GetMapping("/user") public User getUser() { return new User("John"); } 3. @RestController

**Purpose**
- Used to build RESTful web services
- Returns response body directly
- Automatically serializes objects to:
  - JSON (default)
  - XML (if configured) Example @RestController public class UserController { @GetMapping("/user") 

 public User getUser() { return new User("John"); } }

**Key Points**
- No view resolution
- No @ResponseBody required
- Ideal for:
  - Microservices
  - APIs
  - Backend-for-frontend services


### 4.

**Relationship Between** Them @RestController = @Controller + @ResponseBody This is not conceptual—it is literally how Spring defines it.


### 5.

**Comparison Table** (Interview Favorite) Aspect @Controller @RestController Application type MVC (server-side UI) REST APIs Return type View name Data (JSON/XML) ViewResolver used Yes No @ResponseBody required Yes (for JSON) No Typical usage Web applications Microservices


###


###


### 6. Content Negotiation @RestController
- Uses HttpMessageConverter
- Converts Java objects to JSON/XML based on:
  - Accept header
  - Configuration @Controller
- Uses ViewResolver
- Converts model data to UI views


### 7.

**Real-World** Usage (Senior Perspective)
- Use @Controller when:
  - Building server-side rendered UI
  - Using MVC with templates
- Use @RestController when:
  - Building APIs
  - Microservices
  - SPA backend (React, Angular)

---


## What is @Autowired?

**Types of** Injection

What is @Autowired?

**Types of** Injection @Autowired is a Spring annotation used to automatically inject dependencies into a Spring-managed bean. Spring resolves the dependency from its ApplicationContext (IoC container) and injects it at runtime.


###


###


### 1. What is @Autowired?

**Definition**
- Belongs to org.springframework.beans.factory.annotation
- Performs dependency injection by type
- Can be applied on:
  - Constructor
  - Setter
  - Field 

Core Idea Spring finds a matching bean and injects it automatically without manual wiring.


###


###


### 2. How @Autowired Works Internally (Interview Insight)


###


###


### 1. Spring creates bean instances


###


###


### 2. Scans for injection points (@Autowired)


###


###


### 3. Resolves dependency by:
  - Type (primary)
  - Name (if needed)


###


###


### 4. Injects the dependency


###


###


### 5. Completes bean initialization


### 3.

**Types of** Dependency Injection Using @Autowired


###


###


### 1. Constructor Injection (Recommended) @Service public class OrderService { private final PaymentService paymentService; @Autowired public OrderService(PaymentService paymentService) { this.paymentService = paymentService; } } Why It’s

**Best Practice**
- Mandatory dependencies enforced
- Supports immutability
- Easy unit testing
- Prevents partially constructed objects Spring 4.3+
- @Autowired is optional if there is a single constructor


###


###


### 2. Setter Injection 

@Service public class UserService { private UserRepository repo; @Autowired public void setRepo(UserRepository repo) { this.repo = repo; } }

**When to Use**
- Optional dependencies
- Dependencies that may change


###


###


### 3. Field Injection (Not Recommended) @Service public class ProductService { @Autowired private ProductRepository repo; } Problems
- Hidden dependencies
- Hard to test
- Breaks immutability
- Tight coupling to Spring


###


###


### 4. Injection

**Resolution** Rules (Very Important) By Type (Default) @Autowired private PaymentService paymentService; Multiple Beans of Same Type @Qualifier("paypalService") 

@Autowired private PaymentService paymentService; or @Primary @Service public class PaypalService implements PaymentService {}


###


###


### 5. Optional Dependencies @Autowired(required = false) private AuditService auditService; Preferred (Java 8+): @Autowired private Optional<AuditService> auditService; 6. @Autowired vs Constructor Injection Without Annotation @Service public class OrderService { public OrderService(PaymentService paymentService) { this.paymentService = paymentService; } }
- Works because Spring sees a single constructor
- Cleaner and preferred


### 7.

**Common Interview** Traps
- Thinking @Autowired injects by name (it injects by type first)
- Using field injection everywhere
- Forgetting @Qualifier with multiple beans
- Believing @Autowired is mandatory for constructor injection


### 8.

**Real-World** (Senior-Level

**Best Practice**s)
- Prefer constructor injection
- Avoid field injection
- Use @Qualifier explicitly
- Keep dependencies minimal
- Design for testability


### 9.

**One-Line Interview** Answer @Autowired is used to automatically inject Spring-managed dependencies, supporting constructor, setter, and field injection, with constructor injection being the recommended approach.

---


## What is Spring Boot Auto-Configuration?

What is Spring Boot Auto-Configuration? Spring Boot Auto-Configuration is a mechanism by which Spring Boot automatically configures Spring beans based on:
- Classpath dependencies
- Existing beans
- Application properties In simple terms: Spring Boot looks at what you have on the classpath and configures the application automatically, without explicit configuration.


###


###


### 1. Why Auto-Configuration Was Introduced Problem in Traditional Spring
- Large amount of manual configuration
- Explicit bean definitions for:
  - DataSource
  - TransactionManager
  - DispatcherServlet
  - Jackson, JPA, Security, etc. This slowed down development and increased complexity. 

Spring Boot Solution
- Provide sensible defaults
- Configure common components automatically
- Allow overriding when needed


###


###


### 2. How Auto-Configuration Works (High-Level Flow)


###


###


### 1. Application starts with @SpringBootApplication 2. @EnableAutoConfiguration is activated


###


###


### 3. Spring Boot scans:
  - Classpath
  - Environment properties
  - Existing beans


###


###


### 4. Conditional auto-configuration classes are applied


###


###


### 5. Beans are created automatically


###


###


### 3. Key Annotation Involved @SpringBootApplication This is a meta-annotation that includes: @SpringBootConfiguration @EnableAutoConfiguration @ComponentScan @EnableAutoConfiguration
- Core annotation responsible for auto-configuration
- Triggers loading of auto-config classes


###


###


### 4. Where Auto-Configuration Classes Come From Auto-configuration classes are listed in: META-INF/spring.factories 

 (For newer versions, also META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports) Example entry: org.springframework.boot.autoconfigure.EnableAutoConfiguration=\ org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration,\ org.springframework.boot.autoconfigure.web.servlet.WebMvcAutoConfiguration Spring Boot loads these classes at startup.


###


###


### 5. Conditional Annotations (Core Concept) Auto-configuration is driven by conditional annotations. Common Conditions
- @ConditionalOnClass
- @ConditionalOnMissingBean
- @ConditionalOnProperty
- @ConditionalOnWebApplication
- @ConditionalOnBean Example @ConditionalOnClass(DataSource.class) @ConditionalOnMissingBean(DataSource.class) public class DataSourceAutoConfiguration { }

**Meaning**:
- If DataSource is on classpath
- AND no DataSource bean exists → Spring Boot creates one


###


###


### 6. Real

**Example:** DataSource Auto-Configuration If you add: spring-boot-starter-data-jpa And configure: spring.datasource.url=... spring.datasource.username=... spring.datasource.password=... Spring Boot automatically creates:
- DataSource
- EntityManagerFactory
- TransactionManager No XML or Java config required.


###


###


### 7. Overriding Auto-Configuration (Very Important) Auto-configuration is not forced. Override by:


###


###


### 1. Defining your own bean @Bean public DataSource dataSource() { return customDataSource(); 

}


###


###


### 2. Disabling auto-config @SpringBootApplication(exclude = DataSourceAutoConfiguration.class)


###


###


### 3. Using properties spring.autoconfigure.exclude=...


###


###


### 8. Auto-Configuration vs Component Scanning Feature Auto-Configuration Component Scanning

**Purpose** Configure infrastructure beans Discover application beans Trigger Classpath + conditions Package scanning Bean creation Automatic Explicit via annotations Used for Framework setup Business logic


###


###


### 9. Why Auto-Configuration Is Powerful
- Faster development
- Fewer configuration errors
- Consistent defaults
- Production-ready setups
- Perfect for microservices


### 10.

**Common Interview** Traps
- Thinking auto-configuration is magic (it’s conditional logic)
- Confusing auto-configuration with component scanning
- Forgetting it can be overridden
- Assuming it always runs (conditions may fail)


### 11.

**One-Line Interview** Answer Spring Boot auto-configuration automatically configures Spring beans based on classpath, properties, and conditions, reducing manual configuration while allowing easy overrides.

---


## What is Spring Boot Actuator?

What is Spring Boot Actuator? Spring Boot Actuator is a Spring Boot module that provides production-ready features to monitor, manage, and observe an application at runtime via HTTP endpoints or JMX. In simple terms: Actuator tells you how your application is behaving in production.


###


###


### 1. Why Actuator Is Needed In real-world systems, especially microservices, you must know:
- Is the app running?
- Is it healthy?
- Is the database reachable?
- How much memory/CPU is used?
- How many requests are coming? Without Actuator:
- You must build custom monitoring endpoints
- More code, more bugs 

Actuator provides all this out of the box.


###


###


### 2. What Actuator Provides Actuator exposes management endpoints that give insights into:
- Application health
- Metrics
- Environment properties
- Thread dumps
- Heap dumps
- Logging configuration
- Application info


###


###


### 6. How to Enable Actuator Dependency spring-boot-starter-actuator Enable Endpoints management.endpoints.web.exposure.include=health,info,metrics By default:
- Only health and info are exposed


###


###


### 7. Security (Very Important) Actuator endpoints can expose sensitive data.

**Best practice**s:
- Do NOT expose all endpoints publicly
- Protect endpoints using Spring Security
- Expose only what is needed management.endpoints.web.exposure.include=health,metrics management.endpoint.health.show-details=when_authorized


###


###


### 8. Actuator in Microservices & Cloud Actuator is critical for:
- Kubernetes liveness & readiness probes
- Autoscaling (HPA)
- Centralized monitoring
- Observability

**Example:** livenessProbe: httpGet: path: /actuator/health/liveness


###


###


### 9. Actuator vs Logging (Interview Insight) Logging Actuator What happened What is happening now Historical Real-time 

 Debugging Monitoring & operations Both are required in production systems.


### 11.

**One-Line Interview** Answer Spring Boot Actuator provides production-ready monitoring and management endpoints that expose application health, metrics, and runtime information.

---


## What Is the

**Lifecycle** of a Spring Bean?

What Is the

**Lifecycle** of a Spring Bean? The Spring Bean lifecycle describes the sequence of steps Spring follows to create, initialize, use, and destroy a bean managed by the Spring container. Understanding this is critical for DI, AOP, transactions, and performance tuning.


###


###


### 1. High-Level Bean

**Lifecycle** Flow Bean Instantiation → Dependency Injection → Aware callbacks → BeanPostProcessor (before init) → Initialization callbacks → BeanPostProcessor (after init) → Bean ready for use 

 → Destruction callbacks


###


###


### 2. Detailed Step-by-Step

**Lifecycle** 2.1 Bean Instantiation
- Spring creates the bean instance using:
  - Constructor
  - Factory method

**Example:** @Component class OrderService { public OrderService() {} } At this stage:
- Bean exists
- Dependencies are NOT injected yet 2.2 Dependency Injection (Populate Properties)
- Spring injects dependencies:
  - Constructor injection
  - Setter injection
  - Field injection Annotations processed:
- @Autowired
- @Value
- @Inject 

2.3 Aware Interfaces (Optional Callbacks) If the bean implements Aware interfaces, Spring injects context-related objects. Common ones:
- BeanNameAware
- BeanFactoryAware
- ApplicationContextAware
- EnvironmentAware

**Example:** class MyBean implements BeanNameAware { public void setBeanName(String name) {} } 2.4 BeanPostProcessor (Before Initialization)
- Spring invokes: postProcessBeforeInitialization() Used for:
- Custom processing
- Annotation handling

**Examples:**
- @Autowired processing
- @PostConstruct detection
- AOP preparation 2.5 Initialization Callbacks Spring initializes the bean using one or more methods: 

Option 1: @PostConstruct @PostConstruct public void init() {}

**Option 2**: InitializingBean public void afterPropertiesSet() {}

**Option 3**: Custom init method @Bean(initMethod = "init") 2.6 BeanPostProcessor (After Initialization)
- Spring invokes: postProcessAfterInitialization() This is where:
- AOP proxies are created
- Transactional behavior is applied

**Example:**
- @Transactional
- @Async 2.7 Bean Ready for Use
- Bean is fully initialized
- Stored in container
- Available for injection
- Business logic executes here


###


###


### 3. Destruction Phase Triggered when:
- Application context shuts down
- Bean is removed (scope dependent) Destruction Callbacks

**Option 1**: @PreDestroy @PreDestroy public void destroy() {}

**Option 2**: DisposableBean public void destroy() {}

**Option 3**: Custom destroy method @Bean(destroyMethod = "cleanup")


###


###


### 4. Complete

**Lifecycle** Order (Interview Gold)


###


###


### 1. Constructor called


###


###


### 2. Dependencies injected


###


###


### 3. Aware interfaces invoked


###


###


### 4. BeanPostProcessor.beforeInit() 5. @PostConstruct 6. afterPropertiesSet()


###


###


### 7. Custom init method


###


###


### 8. BeanPostProcessor.afterInit()


###


###


### 9. Bean in use 

10. @PreDestroy 11. destroy()


###


###


### 5. Special Notes (Very Important) Prototype Beans
- Created every time
- Destruction callbacks NOT managed by Spring Singleton Beans
- Single instance
- Full lifecycle managed


###


###


### 6. Bean

**Lifecycle** vs Application

**Lifecycle**
- Bean lifecycle happens inside
- Application lifecycle is broader


### 7.

**Common Interview** Traps
- Confusing BeanPostProcessor with BeanFactoryPostProcessor
- Thinking @PostConstruct runs before DI
- Assuming prototype beans are destroyed automatically
- Forgetting AOP happens after initialization


### 8.

**Real-World** (Senior-Level

**Best Practice**s)
- Use @PostConstruct for initialization logic
- Avoid heavy logic in constructors
- Use @PreDestroy for resource cleanup
- Prefer constructor injection
- Keep beans lightweight


### 9.

**One-Line Interview** Answer 

The Spring bean lifecycle includes instantiation, dependency injection, initialization callbacks, post-processing, usage, and destruction managed by the Spring container.

---


## How does @Transactional work internally?

How does @Transactional work internally? (Propagation + Isolation) @Transactional is not magic. Internally, Spring uses AOP (proxy-based interception) to manage transactions. At runtime:


###


###


### 1. Spring creates a proxy for the bean


###


###


### 2. Method call goes through the proxy


###


###


### 3. Proxy delegates to TransactionInterceptor


###


###


### 4. Transaction is started / joined / suspended based on Propagation


###


###


### 5. DB transaction behavior is controlled using Isolation


###


###


### 6. On method exit:
  - Commit if success
  - Rollback if exception matches rollback rules


### 2.

**Internal Flow** (Step-by-Step)

**Step 1**: Bean Proxy Creation
- Enabled by:
  - @EnableTransactionManagement
  - or auto-enabled in Spring Boot
- Spring wraps beans having @Transactional with:
  - JDK Dynamic Proxy (if interface)
  - CGLIB Proxy (if class) ⚠

**Important interview** point Self-invocation does NOT trigger @Transactional 

Step 2: Method Interception When a transactional method is called: Client → Proxy → TransactionInterceptor → Target Method TransactionInterceptor:
- Reads TransactionAttribute metadata
- Decides propagation, isolation, timeout, rollback rules

**Step 3**: PlatformTransactionManager Spring delegates transaction handling to:
- PlatformTransactionManager
  - DataSourceTransactionManager (JDBC)
  - JpaTransactionManager (JPA/Hibernate) This manager:
- Opens DB connection
- Sets isolation level
- Manages commit/rollback


###


###


### 3. Propagation (MOST IMPORTANT IN INTERVIEWS) Propagation defines how a method behaves when a transaction already exists. Common Propagation Types 


###


###


###


### 1. REQUIRED (Default) @Transactional
- Join existing transaction
- Create new if none exists 

📌

**Use case**
- Service layer business logic 📌

**Real-world** example OrderService.placeOrder() -> PaymentService.pay() -> InventoryService.reserve() All run in same transaction 


###


###


###


### 2. REQUIRES_NEW @Transactional(propagation = REQUIRES_NEW)
- Suspend existing transaction
- Start a new, independent transaction 📌

**Use case**
- Audit logs
- Notifications
- Error logging 📌 Interview trick Even if outer transaction rolls back, inner REQUIRES_NEW can still commit 


###


###


###


### 3. SUPPORTS
- Join transaction if exists
- Otherwise run non-transactionally 📌 Rarely used 


###


###


###


### 4. NOT_SUPPORTED
- Always run without transaction
- Suspends existing transaction 📌

**Example:**
- Heavy read operations
- Reporting queries 


###


###


###


### 5. MANDATORY
- Must run inside a transaction
- Throws exception if none exists 📌 Used in strict transactional APIs 


###


###


###


### 6. NEVER
- Must NOT run inside transaction
- Throws exception if transaction exists 


###


###


###


### 7. NESTED
- Creates a savepoint inside existing transaction
- Requires DB support (e.g., PostgreSQL) 📌 Partial rollback support ❌ Checked exceptions DO NOT rollback by default Custom Rollback @Transactional(rollbackFor = Exception.class)


### 6.

**Common Interview** Traps (VERY IMPORTANT) 

❌ Self-Invocation public void methodA() { methodB(); // @Transactional ignored } ✅

**Solution:**
- Call via proxy
- Move method to another bean ❌ Private Methods
- @Transactional does NOT work on private methods ❌ Wrong Layer
- @Transactional on Controller → BAD
- Correct layer → Service


### 7.

**Real-World**

**Best Practice**s ✅ Use @Transactional at service layer ✅ Prefer REQUIRED ✅ Use REQUIRES_NEW only when really needed ✅ Keep transactions short ✅ Avoid external API calls inside transaction


### 8.

**How to Explain** in 60 Seconds (Interview Answer) "@Transactional works using Spring AOP. Spring creates a proxy around the bean and intercepts method calls using TransactionInterceptor. Based on propagation, it decides whether to join, suspend, or create a new transaction. Isolation controls how concurrent transactions interact and is enforced by the 

database. On method completion, Spring commits or rolls back based on exception rules. The default propagation is REQUIRED and rollback happens only for runtime exceptions."

---


## What are Spring Boot Starters?

What are Spring Boot Starters? Spring Boot Starters are predefined dependency descriptors that group commonly used libraries together so you can quickly enable a feature with minimal configuration. They follow the principle of convention over configuration. In simple terms: A starter is a single dependency that pulls in all required transitive dependencies for a specific functionality.

**Why Starters** Exist (Problem They Solve) Before Spring Boot:
- Developers had to manually add multiple dependencies
- Version compatibility was a major issue
- XML / Java config was heavy
- Dependency conflicts were common Spring Boot Starters:
- Reduce dependency management effort
- Ensure compatible versions
- Enable faster project bootstrap
- Encourage best practices How Starters Work Internally A starter is:
- A normal Maven/Gradle dependency
- Has no application code
-

**Contains** only POM metadata
- Uses transitive dependencies

**Example:** <dependency> <groupId>org.springframework.boot</groupId> <artifactId>spring-boot-starter-web</artifactId> </dependency>

**Internally this** pulls:
- Spring MVC
- Embedded Tomcat
- Jackson
- Validation
- Logging (Logback) All versions are controlled by:
- spring-boot-dependencies (BOM)

**Relationship Between** Starters and Auto-Configuration Starters and Auto-Configuration work together, but they are not the same thing.
- Starter: Brings libraries into classpath
- Auto-configuration: Configures beans based on classpath presence

**Example:**
- spring-boot-starter-data-jpa adds Hibernate + JPA APIs
- Auto-config creates:
  - EntityManagerFactory
  - DataSource
  - TransactionManager

**Commonly Used** Spring Boot Starters Starter

**Purpose** spring-boot-starter-web REST APIs, MVC 

spring-boot-starter-data-jpa JPA + Hibernate spring-boot-starter-security Authentication & Authorization spring-boot-starter-actuator Monitoring & metrics spring-boot-starter-test Testing support spring-boot-starter-validation Bean validation spring-boot-starter-aop Aspect-Oriented Programming

**Naming Convention** All official starters follow: spring-boot-starter-*

**Examples:**
- spring-boot-starter-web
- spring-boot-starter-cache
- spring-boot-starter-mail Third-party starters follow: <vendor>-spring-boot-starter-*

**Example:**
- mybatis-spring-boot-starter

**Custom Starters** (Advanced Interview Topic) You can create your own starter to standardize configuration across projects. A custom starter contains:


###


###


### 1. Auto-configuration module


###


###


### 2. Starter module (POM only) Key components:
- META-INF/spring.factories (Spring Boot 2.x)
- META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports (Boot 3.x)
- @AutoConfiguration
- @ConditionalOnClass
- @ConditionalOnProperty

**Use case**:
- Internal frameworks
- Shared platform libraries
- Company-wide standards How Starters Differ From Plain Dependencies Plain Dependency Starter Single library Curated set of libraries Manual version control Version managed by BOM More configuration Auto-config enabled Higher conflict risk Minimal conflicts

**Common Interview** Traps


###


###


### 1. Starter ≠ Auto-configuration


###


###


### 2. Starters do not contain logic


###


###


### 3. Removing a starter may break auto-config


###


###


### 4. Starters rely on classpath detection


###


###


### 5. Starters reduce but do not eliminate configuration

**One-Line Interview** Answer Spring Boot starters are curated dependency descriptors that bundle commonly used libraries and work with auto-configuration to enable features with minimal setup and consistent dependency management.

---


## How to Create Custom Annotations in Spring Boot

How to Create Custom Annotations in Spring Boot Custom annotations in Spring Boot are used to add metadata and encapsulate cross-cutting behavior such as validation, security, logging, or configuration. They are heavily used internally by Spring (@Transactional, @Async, @RestController).


###


###


### 1. Basic Structure of a Custom Annotation A Java annotation is defined using @interface. @Target(ElementType.METHOD) @Retention(RetentionPolicy.RUNTIME) public @interface LogExecutionTime { } Explanation
- @Target defines where the annotation can be used
- @Retention(RUNTIME) is mandatory so Spring can read it at runtime
- By default, annotations have no behavior; they are just metadata


###


###


### 2. Making the Annotation Do Something (AOP Approach) In Spring, custom annotations usually work with AOP (Aspect-Oriented Programming).

**Step 1**: Create the Annotation @Target(ElementType.METHOD) @Retention(RetentionPolicy.RUNTIME) public @interface LogExecutionTime { } 

 Step 2: Create an Aspect @Aspect @Component public class LoggingAspect { @Around("@annotation(LogExecutionTime)") public Object logExecution(ProceedingJoinPoint joinPoint) throws Throwable { long start = System.currentTimeMillis(); Object result = joinPoint.proceed(); long end = System.currentTimeMillis(); System.out.println( joinPoint.getSignature() + " executed in " + (end - start) + " ms" ); return result; } }

**Internal Flow**


###


###


### 1. Spring scans beans


###


###


### 2. Detects @Aspect


###


###


### 3. Creates proxy for beans having annotated methods


###


###


### 4. Advice is executed when method is invoked


###


###


### 3. Custom Annotation With Parameters @Target(ElementType.METHOD) @Retention(RetentionPolicy.RUNTIME) public @interface Retry { int attempts() default 3; }

**Usage:** @Retry(attempts = 5) public void callExternalService() { } Aspect: @Around("@annotation(retry)") public Object retry(ProceedingJoinPoint pjp, Retry retry) throws Throwable { int attempts = retry.attempts(); Throwable lastException = null; for (int i = 0; i < attempts; i++) { try { return pjp.proceed(); } catch (Throwable ex) { lastException = ex; } 

 } throw lastException; }


###


###


### 4. Meta-Annotations (Very Important for Interviews) You can compose annotations using other Spring annotations.

**Example:** Custom Controller Annotation @Target(ElementType.TYPE) @Retention(RetentionPolicy.RUNTIME) @RestController @RequestMapping("/api") public @interface ApiController { }

**Usage:** @ApiController public class UserController { } Spring treats this exactly like: @RestController @RequestMapping("/api") 

This is how annotations like @RestController are built internally.


###


###


### 5. Conditional Annotations (Advanced) Custom conditional annotations are built using @Conditional. @Target(ElementType.TYPE) @Retention(RetentionPolicy.RUNTIME) @Conditional(OnFeatureEnabledCondition.class) public @interface ConditionalOnFeatureEnabled { } Condition: public class OnFeatureEnabledCondition implements Condition { @Override public boolean matches(ConditionContext context, AnnotatedTypeMetadata metadata) { return Boolean.parseBoolean( context.getEnvironment().getProperty("feature.enabled") ); } }


###


###


### 6. Custom Validation Annotations Very common interview topic.

**Step 1**: Annotation 

@Target(ElementType.FIELD) @Retention(RetentionPolicy.RUNTIME) @Constraint(validatedBy = PhoneValidator.class) public @interface ValidPhone { String message() default "Invalid phone number"; Class<?>[] groups() default {}; Class<? extends Payload>[] payload() default {}; }

**Step 2**: Validator public class PhoneValidator implements ConstraintValidator<ValidPhone, String> { @Override public boolean isValid(String value, ConstraintValidatorContext context) { return value != null && value.matches("\\d{10}"); } }

**Usage:** @ValidPhone private String phone;


### 7.

**Common Mistakes** (Interview Traps)


###


###


### 1. Missing RetentionPolicy.RUNTIME


###


###


### 2. Expecting annotation to work without AOP or processor


###


###


### 3. Using @Transactional-style behavior on private methods


###


###


### 4. Forgetting @Component on Aspect


###


###


### 5. Confusing annotations with interceptors or filters


### 8.

**When NOT to** Use Custom Annotations
- Simple logic that can be expressed directly
- One-off business logic
-

**Performance**-critical hot paths (AOP overhead)


### 9.

**How to Explain** in 1 Minute (Interview Answer) Custom annotations in Spring Boot are metadata definitions created using @interface. By themselves they do nothing, but Spring processes them using AOP, reflection, or conditional configuration. Common implementations use aspects, meta-annotations, or validators. Internally Spring detects these annotations at runtime and applies behavior using proxies or bean post-processors.

---


## How Spring Handles Dependency Injection Using Reflection

How Spring Handles Dependency Injection Using Reflection Spring’s dependency injection (DI) is fundamentally based on reflection, combined with metadata processing, bean lifecycle management, and runtime proxying. Reflection allows Spring to inspect classes, constructors, fields, and methods at runtime, without knowing them at compile time.


###


###


### 1. High-Level Flow At a high level, Spring performs DI in four phases:


###


###


### 1. Classpath scanning and metadata reading


###


###


### 2. Bean definition creation


###


###


### 3. Bean instantiation using reflection


###


###


### 4. Dependency injection and initialization 

Reflection is used heavily in steps 3 and 4.


###


###


### 2. Bean Discovery and Metadata Reading When Spring starts:
- It scans the classpath for:
  - @Component, @Service, @Repository, @Controller
  - @Configuration, @Bean
- Spring does not load classes immediately
- It uses ASM bytecode reading to read annotation metadata efficiently At this stage:
- No reflection-based object creation yet
- Spring only builds BeanDefinition objects (metadata) A BeanDefinition contains:
- Bean class name
- Scope (singleton/prototype)
- Constructor info
- Autowire mode
- Lazy/init/destroy metadata


###


###


### 3. Bean Instantiation Using Reflection When Spring decides to create a bean: Constructor

**Resolution** Spring uses reflection to:
- Inspect all constructors
- Decide which constructor to use based on:
  - @Autowired
  - Number of parameters
  - Availability of candidate beans

**Internally:** Constructor<?>[] constructors = beanClass.getDeclaredConstructors(); 

 Then: constructor.newInstance(resolvedDependencies); Key points:
- Constructor injection is resolved first
- If multiple constructors exist:
  - @Autowired wins
  - Otherwise, the constructor with maximum resolvable parameters is chosen


###


###


### 4. Dependency

**Resolution** Process For each constructor parameter, field, or method parameter, Spring:


###


###


### 1. Determines the dependency type


###


###


### 2. Looks it up in the BeanFactory


###


###


### 3. Applies qualifiers (@Qualifier, @Primary)


###


###


### 4. Resolves scopes and proxies if required Reflection is used to:
- Inspect parameter types
- Read annotations
- Match candidates dynamically


###


###


### 5. Field Injection Using Reflection For field injection: @Autowired private UserRepository repository; Spring internally: Field field = beanClass.getDeclaredField("repository"); 

field.setAccessible(true); field.set(beanInstance, resolvedDependency);

**Important interview** points:
- setAccessible(true) bypasses Java access checks
- This is why even private fields can be injected
- Field injection happens after object construction


###


###


### 6. Setter / Method Injection For setter or arbitrary method injection: @Autowired public void setService(OrderService service) { } Spring:
- Scans methods via reflection
- Resolves method parameters
- Invokes method dynamically

**Internally:** method.invoke(beanInstance, resolvedDependency);


###


###


### 7. Role of BeanPostProcessors (Critical) Dependency injection is actually performed by BeanPostProcessors, especially:
- AutowiredAnnotationBeanPostProcessor
- CommonAnnotationBeanPostProcessor 

Flow:


###


###


### 1. Bean instance is created (constructor)


###


###


### 2. BeanPostProcessor scans fields and methods


###


###


### 3. Reflection is used to inject dependencies 4. @PostConstruct is invoked Without BeanPostProcessors:
- @Autowired would not work
- Custom annotations would not be processed


###


###


### 8. Handling Proxies (AOP, Transactions, Lazy) If a dependency:
- Is transactional
- Is scoped
- Is lazy
- Uses AOP Spring may inject a proxy instead of the real object. Reflection is used to:
- Inspect interfaces
- Generate proxies (JDK or CGLIB)
- Inject proxy references This ensures:
- Lazy initialization
- Transaction boundaries
- Cross-cutting concerns


###


###


### 9. Circular Dependency Handling (Reflection + Caching) For singleton beans: Spring uses:
- Three-level cache


###


###


### 1. Fully initialized beans


###


###


### 2. Early references


###


###


### 3. Bean factories Reflection allows Spring to:
- Create a partially initialized object
- Inject early reference
- Complete wiring later Constructor-based circular dependencies fail because:
- Reflection-based instantiation cannot complete without dependencies


###


###


### 10. Why Constructor Injection Is Preferred (Interview Favorite) Reasons:
- Dependencies are explicit
- Object is immutable after creation
- Easier to test
- No need for reflective field access Spring still uses reflection, but:
- Injection happens during object creation
- No setAccessible(true) hacks


### 11.

**Performance** Considerations
- Reflection is slower than direct calls
- Spring minimizes cost by:
  - Caching constructors, fields, methods
  - Using bytecode scanning instead of class loading
- DI happens once at startup, not per request So performance impact is negligible in real applications.


### 12.

**How to Explain** in 60 Seconds (Interview Answer) Spring uses reflection to inspect classes, constructors, fields, and methods at runtime. It first builds bean metadata, then creates objects using reflective 

constructor invocation. Dependencies are resolved from the BeanFactory and injected using reflection via field access or method invocation. BeanPostProcessors like AutowiredAnnotationBeanPostProcessor perform the actual injection. Reflection also enables proxy injection, lazy loading, and transaction management.

---


## Difference Between @Qualifier and @Primary

Difference Between @Qualifier and @Primary Annotations Both @Qualifier and @Primary are used in Spring to resolve ambiguity when multiple beans of the same type exist. The key difference lies in who controls the selection and how explicit the wiring is.


###


###


### 1. The Core Problem They Solve public interface PaymentService { } @Service public class CardPaymentService implements PaymentService { } @Service public class UpiPaymentService implements PaymentService { } Now Spring has two beans of type PaymentService. @Autowired private PaymentService paymentService; // ambiguity Spring throws: 

NoUniqueBeanDefinitionException 2. @Primary

**What It Does** @Primary tells Spring: “If multiple beans of the same type exist, use this one by default.” Example @Service @Primary public class CardPaymentService implements PaymentService { } Now this works: @Autowired private PaymentService paymentService;

**Key

**Characteristics****
- Applied on bean definition
- Acts as a default choice
- Used when no qualifier is specified
- Global preference 3. @Qualifier

**What It Does** @Qualifier tells Spring: 

“Inject this specific bean, not the default one.” Example @Service("upiPayment") public class UpiPaymentService implements PaymentService { } @Autowired @Qualifier("upiPayment") private PaymentService paymentService;

**Key

**Characteristics****
- Applied at injection point
- Explicit selection
- Overrides @Primary
- Local and precise


###


###


### 4. Precedence Rule (Very Important Interview Point) @Qualifier always overrides @Primary Even if a bean is marked @Primary, Spring will inject the bean specified by @Qualifier.

---


## How to Handle Exceptions Globally in Spring Boot

How to Handle Exceptions Globally and Define Custom Exception Handling in Spring Boot Global exception handling in Spring Boot is achieved by centralizing error handling logic so that controllers remain clean and consistent responses are returned across the application.


###


###


### 1. Why Global Exception Handling Is Needed Without global handling:
- Controllers become cluttered with try–catch blocks
- Error responses are inconsistent
- Logging and monitoring are scattered Spring solves this using controller advice and exception resolvers. 2. @ControllerAdvice and @RestControllerAdvice @ControllerAdvice
- Applies to all controllers
- Used for MVC applications (views + REST) @RestControllerAdvice
- Combination of:
  - @ControllerAdvice
  - @ResponseBody
- Preferred for REST APIs


###


###


### 3. Basic Global Exception Handler @RestControllerAdvice public class GlobalExceptionHandler { @ExceptionHandler(RuntimeException.class) public ResponseEntity<String> handleRuntime(RuntimeException ex) { return ResponseEntity .status(HttpStatus.INTERNAL_SERVER_ERROR) .body(ex.getMessage()); } 

} This:
- Catches exceptions thrown from any controller
- Converts them into HTTP responses


###


###


### 4. Custom Exceptions Define Custom Exception public class ResourceNotFoundException extends RuntimeException { public ResourceNotFoundException(String message) { super(message); } } Throw from Service Layer if (user == null) { throw new ResourceNotFoundException("User not found"); }


###


###


### 5. Handling Custom Exceptions Globally @ExceptionHandler(ResourceNotFoundException.class) public ResponseEntity<ErrorResponse> handleNotFound(ResourceNotFoundException ex) { return ResponseEntity .status(HttpStatus.NOT_FOUND) 

 .body(new ErrorResponse("NOT_FOUND", ex.getMessage())); }


###


###


### 6. Structured Error Response (Best Practice) Create a common error model: public class ErrorResponse { private String code; private String message; private LocalDateTime timestamp; }

**Benefits**:
- Consistent API contracts
- Better frontend and client handling
- Easier logging and monitoring


###


###


### 7. Validation Exception Handling Handling @Valid Errors @ExceptionHandler(MethodArgumentNotValidException.class) public ResponseEntity<Map<String, String>> handleValidation( MethodArgumentNotValidException ex) { Map<String, String> errors = new HashMap<>(); ex.getBindingResult().getFieldErrors() 

 .forEach(error -> errors.put( error.getField(), error.getDefaultMessage())); return ResponseEntity.badRequest().body(errors); }


###


###


### 8. Handling Constraint Violations @ExceptionHandler(ConstraintViolationException.class) public ResponseEntity<String> handleConstraint(ConstraintViolationException ex) { return ResponseEntity.badRequest().body(ex.getMessage()); }


###


###


### 9. Handling JSON and Request Errors Common exceptions:
- HttpMessageNotReadableException
- MissingServletRequestParameterException
- MethodArgumentTypeMismatchException These can be handled centrally to return clear client errors.


###


###


### 10. Exception Handling Flow (Internal)


###


###


### 1. Controller throws exception


###


###


### 2. Spring DispatcherServlet catches it


###


###


### 3. HandlerExceptionResolver chain is invoked 4. @ControllerAdvice is checked


###


###


### 5. Matching @ExceptionHandler method is called


###


###


### 6. Response is written Spring uses:
- ExceptionHandlerExceptionResolver
- ResponseStatusExceptionResolver
- DefaultHandlerExceptionResolver


### 15.

**How to Explain** in 60 Seconds (Interview Answer) Spring Boot handles global exception handling using @ControllerAdvice or @RestControllerAdvice. These intercept exceptions thrown by controllers and convert them into consistent HTTP responses using @ExceptionHandler methods. Custom exceptions are defined in the service layer and mapped centrally, keeping controllers clean and ensuring consistent error handling across the application.

---


## What Does @SpringBootApplication Include?

What Does @SpringBootApplication Include? @SpringBootApplication is a composed (meta) annotation that acts as the main entry point of a Spring Boot application. It combines multiple core Spring annotations to enable auto-configuration, component scanning, and Java-based configuration.


### 1.

**Definition** (What’s Inside) Internally, @SpringBootApplication is defined as: @Target(ElementType.TYPE) @Retention(RetentionPolicy.RUNTIME) @Documented @Inherited @SpringBootConfiguration @EnableAutoConfiguration @ComponentScan public @interface SpringBootApplication { 

} This definition is part of Spring Framework.


###


###


### 2. Included Annotations Explained 1. @SpringBootConfiguration
- Specialized version of @Configuration
- Marks the class as a source of bean definitions
- Ensures it is picked up during startup Difference from @Configuration:
- Semantic clarity (Boot-specific)
- Functionally the same 2. @EnableAutoConfiguration
- Core of Spring Boot
- Enables auto-configuration based on classpath
- Uses conditional annotations such as:
  - @ConditionalOnClass
  - @ConditionalOnMissingBean
  - @ConditionalOnProperty

**Internal mechanism**:
- Reads auto-config classes from:
  - META-INF/spring.factories (Boot 2.x)
  - META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports (Boot 3.x) This is how:
- DataSource
- JPA
- Web server
- Security are auto-configured 

 3. @ComponentScan
- Scans for Spring components:
  - @Component
  - @Service
  - @Repository
  - @Controller
- Default scan base:
  - Package of the main class and all sub-packages

**Important interview** point: Package structure matters in Spring Boot.


###


###


### 3. Why This Annotation Is Important Without @SpringBootApplication, you would need: @Configuration @EnableAutoConfiguration @ComponentScan Boot combines them to:
- Reduce boilerplate
- Enforce conventions
- Simplify setup Custom Component Scan @SpringBootApplication(scanBasePackages = "com.mycompany") Rarely needed if package structure is correct.


###


###


### 5. Execution Flow (High Level) 1. main() calls SpringApplication.run()


###


###


### 2. Spring Boot:
  - Creates ApplicationContext
  - Performs component scan
  - Applies auto-configuration


###


###


### 3. Embedded server starts


### 6.

**Common Interview** Traps
- Thinking @SpringBootApplication is mandatory (it is not, but recommended)
- Misplacing the main class in a sub-package
- Forgetting that auto-configuration can be excluded
- Confusing @EnableAutoConfiguration with component scanning


### 7.

**One-Minute Interview** Answer @SpringBootApplication is a composite annotation that includes @SpringBootConfiguration, @EnableAutoConfiguration, and @ComponentScan. Together, they enable Java-based configuration, automatic setup based on classpath and properties, and component scanning starting from the main application package. It acts as the primary bootstrap annotation in Spring Boot.

---


## Why Do We Make a Constructor Private?

Why Do We Make a Constructor Private? Making a constructor private is a deliberate design decision used to control object creation, enforce constraints, and apply design patterns.


###


###


### 1. Prevent Object Instantiation A private constructor prevents creating objects using new. public class Utility { private Utility() { } } 

 Use case:
- Utility/helper classes (Math, Collections)
- Classes containing only static methods

**Interview line:** A private constructor enforces non-instantiability.


###


###


### 2. Implement Singleton Pattern Ensures only one instance of a class exists. public class Singleton { private static final Singleton INSTANCE = new Singleton(); private Singleton() { } public static Singleton getInstance() { return INSTANCE; } }

**Why private**:
- Prevents external creation
- Controls lifecycle Follow-up interview discussion:
- Thread safety
- Lazy vs eager initialization
- Enum singleton


###


###


### 3. Factory Method Pattern Object creation is controlled via static factory methods. public class User { 

 private User(String name) { } public static User of(String name) { return new User(name); } }

**Benefits**:
- Meaningful method names
- Can return cached or subclass instances
- Can control validation


###


###


### 4. Immutable Classes Private constructors help enforce immutability. public final class Money { private final BigDecimal amount; private Money(BigDecimal amount) { this.amount = amount; } public static Money of(BigDecimal amount) { return new Money(amount); } } Prevents:
- Invalid states
- Inconsistent object creation


###


###


### 5. Static-Only Classes Common in constants classes. public final class Constants { 

 private Constants() { throw new AssertionError("No instances allowed"); } } Ensures:
- No accidental instantiation
- Clear intent


###


###


### 6. Enforcing Controlled Subclassing A private constructor can prevent subclassing entirely. public class Base { private Base() { } }

**Result:**
- No subclass can call super()
- Used in final utility designs


###


###


### 7. Framework-Level Use (Spring / JPA) In Spring:
- Private constructors are sometimes used for:
  - Utility classes
  - Factory beans However:
- Spring cannot instantiate beans with only private constructors unless:
  - Reflection is explicitly allowed
  - Factory methods are used In JPA:
- Entity constructors must be at least protected
- Private constructors break proxy creation 

Interview trap: Private constructor is not suitable for JPA entities.


###


###


### 8. Prevent Object Creation via Reflection (Partial) A private constructor discourages instantiation, but:
- Reflection can still access it using setAccessible(true)
- Not a full security guarantee True prevention requires:
- Enum-based design
- SecurityManager (legacy)


### 9.

**When NOT to** Use Private Constructors
- For Spring-managed beans (unless factory-based)
- For JPA entities
- When subclassing is required
- When framework instantiation is expected


### 10.

**One-Minute Interview** Answer A private constructor is used to control object creation. It prevents direct instantiation, supports design patterns like Singleton and Factory Method, enforces immutability, and is commonly used in utility or constants classes. It also helps restrict subclassing and maintain consistent object state.

---


## RestTemplate vs WebClient

RestTemplate vs WebClient – Differences and Which One to Use RestTemplate and WebClient are both HTTP clients provided by Spring, but they belong to different programming models and target different generations of applications. This question is often used to test understanding of blocking vs non-blocking, reactive programming, and modern Spring design.


###


###


### 1. High-Level Difference Aspect RestTemplate WebClient Programming model Blocking Non-blocking / Reactive Thread usage One thread per request Event-loop based Introduced in Early Spring Spring 5 Status Maintenance mode Actively developed Reactive support No Yes Backpressure No Yes Spring recommendation Legacy Preferred


###


###


### 2. RestTemplate

**What It Is**
- A synchronous, blocking HTTP client
- Built on traditional servlet-based I/O
- Uses:
  - HttpURLConnection
  - Apache HttpClient
  - OkHttp

**Example:** ResponseEntity<User> response = restTemplate.getForEntity("/users/1", User.class);

**Thread behavior**:
- Calling thread blocks until response is received 

Characteristics
- Simple and easy to use
- Familiar imperative style
- Each request:
  - Occupies a thread
  - Scales poorly under high concurrency Spring status: RestTemplate is in maintenance mode and will not receive major enhancements.


###


###


### 3. WebClient

**What It Is**
- A non-blocking, reactive HTTP client
- Part of Spring Framework WebFlux
- Uses:
  - Reactor Netty
  - Asynchronous I/O

**Example:** Mono<User> user = webClient.get() .uri("/users/1") .retrieve() .bodyToMono(User.class);

**Thread behavior**:
- Non-blocking
- Uses a small number of event-loop threads
- Frees threads while waiting for response

**Characteristics**
- Supports reactive streams (Mono, Flux)
- Backpressure-aware
- Scales better for I/O-heavy workloads
- Can be used in:
  - Reactive apps
  - Traditional Spring MVC apps


###


###


### 4. Blocking vs Non-Blocking (Interview Critical) RestTemplate
- Thread waits for response
- Poor resource utilization under load
- Suitable for low to moderate traffic WebClient
- Thread does not wait
- Better CPU and memory utilization
- Designed for high concurrency Key interview line: WebClient does not make the code faster; it makes the system more scalable.


###


###


### 5. Error Handling Differences RestTemplate
- Throws exceptions on non-2xx responses
- Try–catch based handling WebClient
- Functional error handling
- Supports fine-grained response inspection

**Example:** .retrieve() .onStatus(HttpStatus::is4xxClientError, response -> Mono.error(new RuntimeException("Client error")))


###


###


### 6. Timeout and Configuration RestTemplate
- Timeouts configured via HTTP client
- Less flexible WebClient
- Native timeout and retry support
- Integrates well with reactive operators


###


###


### 7. Can WebClient Be Used in Blocking Code? Yes. User user = webClient.get() .uri("/users/1") .retrieve() .bodyToMono(User.class) .block();

**Important interview** note: Calling .block() defeats the purpose of non-blocking I/O but is sometimes acceptable in legacy code.


###


###


### 8. Migration Strategy (Real-World)
- Existing synchronous apps:
  - Keep RestTemplate short-term
  - Gradually migrate to WebClient
- New development:
  - Use WebClient by default Spring Boot guidance:
- RestTemplate is not deprecated
- WebClient is the strategic choice


### 9.

**Performance** Consideration (Interview Trap)
- WebClient is not automatically faster
-

**Benefits** appear when:
  - High concurrency
  - Many outbound I/O calls
  - Microservices communicating heavily For low traffic:
- RestTemplate is sufficient
- Simpler mental model


### 10.

**When to Use** Which One Use RestTemplate When:
- Legacy codebase
- Low concurrency
- Simple synchronous flows
- No reactive stack Use WebClient When:
- New applications
- High concurrency
- Reactive stack
- Microservices
- Streaming responses


### 11.

**One-Minute Interview** Answer RestTemplate is a blocking, synchronous HTTP client and is now in maintenance mode. WebClient is a non-blocking, reactive HTTP client introduced in Spring 5 and is the recommended choice for new applications. WebClient scales better under high concurrency and supports reactive streams, while RestTemplate is simpler and suitable for legacy or low-throughput use cases.

---


## Constructor Injection vs Setter Injection

Constructor Injection vs Setter Injection –

**Pros** and

**Cons** Constructor injection and setter injection are two common ways to inject dependencies in Spring. This question is frequently used to assess design principles, immutability, testability, and framework understanding.


###


###


### 1. Constructor Injection

**How It Works** Dependencies are provided through the class constructor. @Service public class OrderService { private final PaymentService paymentService; public OrderService(PaymentService paymentService) { this.paymentService = paymentService; } }

**Pros**


###


###


### 1. Mandatory Dependencies Are Enforced
  - Object cannot be created without required dependencies
  - Prevents partially initialized objects


###


###


### 2. Immutability
  - Fields can be final
  - State cannot change after construction


###


###


### 3. Better Testability
  - Easy to create objects in unit tests
  - No container needed


###


###


### 4. Fail-Fast Behavior
  - Missing dependencies cause startup failure


###


###


### 5. Preferred by Spring
  - Official Spring recommendation
  - Works well with auto-wiring

**Cons**


###


###


### 1. Large Constructors
  - Too many dependencies indicate poor design
  - Violates Single Responsibility Principle


###


###


### 2. Circular Dependencies
  - Constructor-based circular dependencies cannot be resolved by Spring


###


###


### 2. Setter Injection

**How It Works** Dependencies are injected via setter methods. @Service public class OrderService { private PaymentService paymentService; @Autowired public void setPaymentService(PaymentService paymentService) { this.paymentService = paymentService; } }

**Pros**


###


###


### 1. Optional Dependencies
  - Suitable when dependency is optional
  - Can be injected conditionally


###


###


### 2. Resolvable Circular Dependencies
  - Spring can resolve circular dependencies using setters


###


###


### 3. Flexible Configuration
  - Dependency can be changed after object creation

**Cons**


###


###


### 1. Partially Initialized Objects
  - Object can exist without required dependency
  - Risk of NullPointerException


###


###


### 2. Weaker Encapsulation
  - Allows mutation of internal state


###


###


### 3. Less Test-Friendly
  - Requires setter calls or container


###


###


### 4. Not Thread-Safe by Design
  - Mutable dependencies


###


###


### 3. Side-by-Side Comparison (Interview-Ready) Aspect Constructor Injection Setter Injection Dependency type Mandatory Optional Immutability Supported Not supported Fail-fast Yes No Circular dependency Not supported Supported Testability High Medium Thread safety Better Weaker Spring recommendation Yes Limited use


###


###


### 4. Field Injection (Why It Is Discouraged) Although commonly seen: @Autowired private PaymentService paymentService; 

Problems:
- Hard to test
- Reflection-based injection
- Hidden dependencies
- Violates clean design principles

**Interview tip:** Field injection is discouraged for production-quality code.


### 5.

**Best Practice**s (Senior-Level Answer)
- Use constructor injection by default
- Use setter injection only for optional dependencies
- Avoid field injection
- Refactor classes with too many constructor parameters


###


###


### 6. Circular Dependency Interview Discussion Constructor injection:
- Fails fast
- Forces better design Setter injection:
- Allows circular dependencies
- Often hides architectural problems


### 7.

**One-Minute Interview** Answer Constructor injection is preferred because it enforces mandatory dependencies, supports immutability, improves testability, and fails fast. Setter injection is useful for optional dependencies and can resolve circular dependencies but risks partially initialized objects. For production code, constructor injection should be the default choice.

---


## Difference Between @Component and @Configuration

Difference Between @Component and @Configuration Both @Component and @Configuration are used to register beans in Spring, but they serve different purposes and have very different behavior at runtime.


###


###


### 1. High-Level Difference Aspect @Component @Configuration

**Purpose** Generic component registration Java-based configuration Typical use Services, helpers, components Defining @Bean methods Bean method behavior Plain method calls Proxy-intercepted Singleton guarantee No (for @Bean methods) Yes Internal proxying No Yes (CGLIB) Both are part of Spring Framework. 2. @Component

**What It Is**
- A generic stereotype annotation
- Indicates that the class is a Spring-managed bean
- Picked up via component scanning @Component public class EmailService { } 

Variants:
- @Service
- @Repository
- @Controller All are semantically specialized forms of @Component. Behavior of @Component with @Bean Methods @Component public class AppConfig { @Bean public ServiceA serviceA() { return new ServiceA(); } @Bean public ServiceB serviceB() { return new ServiceB(serviceA()); } }

**Problem:**
- serviceA() is a plain Java method call
- Each call creates a new instance
- Singleton contract is broken

**Interview line:** @Component does not enforce singleton semantics for @Bean methods. 3. @Configuration

**What It Is**
- A specialized configuration annotation
- Used to define bean factory methods
- Ensures correct lifecycle and scoping @Configuration public class AppConfig { @Bean public ServiceA serviceA() { return new ServiceA(); } @Bean public ServiceB serviceB() { return new ServiceB(serviceA()); } }

**What Happens** Internally (Critical Interview Point)
- Spring creates a CGLIB proxy of the configuration class
- Calls to serviceA() are intercepted
- Spring returns the same singleton bean from the container
- Ensures proper dependency wiring Key interview line: @Configuration guarantees singleton behavior of @Bean methods by using CGLIB proxying. 4. @Configuration Is a Specialized @Component Important fact: @Configuration is meta-annotated with @Component

**Meaning**:
- @Configuration classes are also Spring beans
- But with enhanced behavior


###


###


### 5. Full vs Lite Configuration Full Configuration @Configuration
- CGLIB enhanced
- Singleton guarantees
- Recommended for bean definitions Lite Configuration @Component
- No proxy enhancement
- No method interception
- Risky for inter-bean calls Spring internally treats these differently.


### 6.

**When to Use** What (Real-World Guidance) Use @Component When:
- Writing business logic
- Creating services, helpers, listeners
- No @Bean methods needed Use @Configuration When:
- Defining infrastructure beans
- Creating explicit bean graphs
- Wiring third-party libraries
- Using multiple @Bean methods that depend on each other


### 7.

**Common Interview** Traps
- Saying both are the same (incorrect)
- Using @Component for configuration classes
- Not understanding CGLIB proxying
- Breaking singleton behavior unknowingly
- Forgetting that @Configuration is also a component


### 8.

**One-Minute Interview** Answer @Component is a generic stereotype annotation used to register a class as a Spring bean. @Configuration is a specialized form used for Java-based configuration and ensures correct singleton behavior for @Bean methods using CGLIB proxying. While @Configuration is itself a @Component, it provides additional guarantees that @Component does not.


###


###


### 9. Quick Interview Summary
- @Component → simple bean
- @Configuration → bean factory with proxying
- Use the right annotation to avoid subtle bugs

---

# 📂 REST API Design


## What Are REST Principles?

What Are REST Principles? REST (Representational State Transfer) is an architectural style for designing scalable, maintainable web APIs. REST is not a protocol and not a standard—it defines constraints that, when followed, produce RESTful systems.


###


###


### 1. Client–Server Separation Principle
- Client and server are independent
- UI concerns are separated from data/storage concerns

**Benefits**
- Independent evolution
- Better scalability
- Clear responsibility boundaries

**Interview line** REST enforces separation of concerns between client and server.


###


###


### 2. Statelessness Principle
- Each request must contain all information required to process it
- Server does not store client state Implications
- No HTTP session on server
- Authentication info (JWT, token) sent on every request

**Benefits**
- Horizontal scalability
- Simpler server design
- Fault tolerance

**Interview trap** Stateless does not mean “no authentication”; it means no server-side session state.


###


###


### 3. Resource-Based Design Principle
- Everything is a resource
- Resources are identified using URIs

**Examples:** /users /users/123 /orders/456/items Rules:
- Use nouns, not verbs
- Resource identity is stable

**Interview line** REST APIs are resource-oriented, not action-oriented.


###


###


### 4. Uniform Interface (Most Important) This is the core of REST and has four sub-constraints. a) Resource Identification
- Each resource has a unique URI b) Manipulation Through Representations
- Client interacts using representations (JSON, XML)
- Same resource can have multiple representations c) Self-Descriptive Messages
- Requests and responses contain enough metadata
- HTTP methods, headers, status codes matter d) Hypermedia as the Engine of Application State (HATEOAS)
- Responses can contain links to related actions
- Clients discover actions dynamically

**Interview reality**: HATEOAS is part of REST, but rarely fully implemented in real systems.


###


###


### 5. Use of Standard HTTP Methods REST maps CRUD semantics to HTTP verbs. HTTP Method

**Meaning** GET Read resource POST Create resource 

PUT Replace resource PATCH Partial update DELETE Remove resource Key rule:
- GET must be safe and idempotent
- PUT and DELETE must be idempotent
- POST is not idempotent


###


###


### 6. Proper Use of HTTP Status Codes REST relies heavily on standard HTTP status codes.

**Examples:**
- 200 OK
- 201 Created
- 204 No Content
- 400 Bad Request
- 401 Unauthorized
- 403 Forbidden
- 404 Not Found
- 409 Conflict
- 500 Internal Server Error

**Interview line:** Status codes are part of REST’s uniform interface.


###


###


### 7. Cacheability Principle
- Responses must explicitly state whether they are cacheable Headers:
- Cache-Control
- ETag
- Last-Modified

**Benefits**:
- Reduced latency
- Reduced server load


###


###


### 8. Layered System Principle
- Client does not know if it is talking to:
  - Load balancer
  - API gateway
  - Microservice
  - Proxy

**Benefits**:
- Security
- Scalability
- Observability


###


###


### 9. Code on Demand (Optional) Principle
- Server can send executable code (e.g., JavaScript) Notes:
- Optional
- Rarely used in REST APIs
- Not common in backend interviews


###


###


### 10. REST Constraints Summary Table Constraint Mandatory Client–Server Yes 

Stateless Yes Cacheable Yes Uniform Interface Yes Layered System Yes Code on Demand Optional


###


###


### 11. REST vs RESTful (Interview Trap)
- REST: Architectural principles
- RESTful API: An API that follows REST constraints Most APIs are: “REST-inspired”, not strictly RESTful


### 12.

**Common Interview** Mistakes
- Using verbs in URLs (/getUser)
- Using GET for updates
- Ignoring HTTP status codes
- Using sessions
- Confusing REST with JSON over HTTP


### 13.

**One-Minute Interview** Answer REST is an architectural style based on constraints like client–server separation, statelessness, resource-based URIs, uniform interface using standard HTTP methods and status codes, cacheability, and layered systems. When these principles are followed, APIs become scalable, maintainable, and loosely coupled.

---


## REST vs SOAP

---


## Difference between Thread.start() and run()

Difference between Thread.start() and run()](#difference-between-threadstart-and-run)
33. [

---


## Java Memory Model (JMM) and volatile keyword

Java Memory Model (JMM) and volatile keyword](#java-memory-model-jmm-and-volatile-keyword)


### Spring Framework and Spring Boot

34. [

---

# 📂 Spring Framework and Spring Boot


## What is Dependency Injection?

What is Dependency Injection?](#what-is-dependency-injection)
35. [

---


## Difference between @Component, @Service, @Repository

Difference between @Component, @Service, @Repository](#difference-between-component-service-repository)
36. [

---


## Difference between @Controller and @RestController

Difference between @Controller and @RestController](#difference-between-controller-and-restcontroller)
37. [

---


## What is @Autowired?

**Types of** Injection

What is @Autowired?

**Types of** Injection](#what-is-autowired-types-of-injection)
38. [

---


## What is Spring Boot Auto-Configuration?

What is Spring Boot Auto-Configuration?](#what-is-spring-boot-auto-configuration)
39. [

---


## What is Spring Boot Actuator?

What is Spring Boot Actuator?](#what-is-spring-boot-actuator)
40. [

---


## What Is the

**Lifecycle** of a Spring Bean?

What Is the

**Lifecycle** of a Spring Bean?](#what-is-the-lifecycle-of-a-spring-bean)
41. [

---


## How does @Transactional work internally?

How does @Transactional work internally?](#how-does-transactional-work-internally)
42. [

---


## What are Spring Boot Starters?

What are Spring Boot Starters?](#what-are-spring-boot-starters)
43. [

---


## How to Create Custom Annotations in Spring Boot

How to Create Custom Annotations in Spring Boot](#how-to-create-custom-annotations-in-spring-boot)
44. [

---


## How Spring Handles Dependency Injection Using Reflection

How Spring Handles Dependency Injection Using Reflection](#how-spring-handles-dependency-injection-using-reflection)
45. [

---


## Difference Between @Qualifier and @Primary

Difference Between @Qualifier and @Primary](#difference-between-qualifier-and-primary)
46. [

---


## How to Handle Exceptions Globally in Spring Boot

How to Handle Exceptions Globally in Spring Boot](#how-to-handle-exceptions-globally-in-spring-boot)
47. [

---


## What Does @SpringBootApplication Include?

What Does @SpringBootApplication Include?](#what-does-springbootapplication-include)
48. [

---


## Why Do We Make a Constructor Private?

Why Do We Make a Constructor Private?](#why-do-we-make-a-constructor-private)
49. [

---


## RestTemplate vs WebClient

RestTemplate vs WebClient](#resttemplate-vs-webclient)
50. [

---


## Constructor Injection vs Setter Injection

Constructor Injection vs Setter Injection](#constructor-injection-vs-setter-injection)
51. [

---


## Difference Between @Component and @Configuration

Difference Between @Component and @Configuration](#difference-between-component-and-configuration)


### REST API Design

52. [

---

# 📂 REST API Design


## What Are REST Principles?

What Are REST Principles?](#what-are-rest-principles)
53. [REST vs SOAP](#rest-vs-soap)
54. [

---


## REST vs SOAP

---

## Difference between Thread.start() and run()

Difference between Thread.start() and run()](#difference-between-threadstart-and-run)
33. [

---

## Java Memory Model (JMM) and volatile keyword

Java Memory Model (JMM) and volatile keyword](#java-memory-model-jmm-and-volatile-keyword)


### Spring Framework and Spring Boot

34. [

---

# 📂 Spring Framework and Spring Boot

## What is Dependency Injection?

What is Dependency Injection?](#what-is-dependency-injection)
35. [

---

## Difference between @Component, @Service, @Repository

Difference between @Component, @Service, @Repository](#difference-between-component-service-repository)
36. [

---

## Difference between @Controller and @RestController

Difference between @Controller and @RestController](#difference-between-controller-and-restcontroller)
37. [

---

## What is @Autowired? Types of Injection

What is @Autowired?

**Types of** Injection](#what-is-autowired-types-of-injection)
38. [

---

## What is Spring Boot Auto-Configuration?

What is Spring Boot Auto-Configuration?](#what-is-spring-boot-auto-configuration)
39. [

---

## What is Spring Boot Actuator?

What is Spring Boot Actuator?](#what-is-spring-boot-actuator)
40. [

---

## What Is the Lifecycle of a Spring Bean?

What Is the

**Lifecycle** of a Spring Bean?](#what-is-the-lifecycle-of-a-spring-bean)
41. [

---

## How does @Transactional work internally?

How does @Transactional work internally?](#how-does-transactional-work-internally)
42. [

---

## What are Spring Boot Starters?

What are Spring Boot Starters?](#what-are-spring-boot-starters)
43. [

---

## How to Create Custom Annotations in Spring Boot

How to Create Custom Annotations in Spring Boot](#how-to-create-custom-annotations-in-spring-boot)
44. [

---

## How Spring Handles Dependency Injection Using Reflection

How Spring Handles Dependency Injection Using Reflection](#how-spring-handles-dependency-injection-using-reflection)
45. [

---

## Difference Between @Qualifier and @Primary

Difference Between @Qualifier and @Primary](#difference-between-qualifier-and-primary)
46. [

---

## How to Handle Exceptions Globally in Spring Boot

How to Handle Exceptions Globally in Spring Boot](#how-to-handle-exceptions-globally-in-spring-boot)
47. [

---

## What Does @SpringBootApplication Include?

What Does @SpringBootApplication Include?](#what-does-springbootapplication-include)
48. [

---

## Why Do We Make a Constructor Private?

Why Do We Make a Constructor Private?](#why-do-we-make-a-constructor-private)
49. [

---

## RestTemplate vs WebClient

RestTemplate vs WebClient](#resttemplate-vs-webclient)
50. [

---

## Constructor Injection vs Setter Injection

Constructor Injection vs Setter Injection](#constructor-injection-vs-setter-injection)
51. [

---

## Difference Between @Component and @Configuration

Difference Between @Component and @Configuration](#difference-between-component-and-configuration)


### REST API Design

52. [

---

# 📂 REST API Design

## What Are REST Principles?

What Are REST Principles?](#what-are-rest-principles)
53. [REST vs SOAP](#rest-vs-soap)
54. [

---

## REST vs SOAP

1. Fundamental Difference Aspect REST SOAP 

Nature Architectural style Protocol Transport HTTP (mostly) HTTP, SMTP, JMS Message format JSON, XML, others XML only Coupling Loosely coupled Tightly coupled Contract Optional (OpenAPI) Mandatory (WSDL)

**Performance** Lightweight Heavy Flexibility High Low

---


## Difference Between PUT and PATCH

Difference Between PUT and PATCH PUT and PATCH are both HTTP methods used to update resources, but they have different semantics, expectations, and use cases.


###


###


### 1. Core Difference (One-Line Summary)
- PUT → Replace the entire resource
- PATCH → Partially update the resource


###


###


### 2. PUT (Full Replacement)

**Definition** PUT replaces the entire representation of a resource with the payload sent by the client. If a field is missing in the request:
- It is assumed to be removed or reset Example PUT /users/10 { "id": 10, "name": "John", "email": "john@example.com" }

**Server behavior**:
- Existing /users/10 is fully replaced
- Any omitted fields are lost

**Characteristics**
- Idempotent
- Not safe (modifies state)
- Requires full resource representation
- Client must know complete state


###


###


### 3. PATCH (Partial Update)

**Definition** PATCH applies a partial modification to a resource. Only fields present in the request are changed. 

Example PATCH /users/10 { "email": "new@mail.com" }

**Server behavior**:
- Only email is updated
- Other fields remain unchanged

**Characteristics**
- Not strictly idempotent (depends on implementation)
- Not safe
- Payload represents a change, not a full state
- More flexible


###


###


### 4. Side-by-Side Comparison (Interview Table) Aspect PUT PATCH Update type Full replace Partial modify Payload Complete resource Only changed fields Idempotent Yes Depends Resource knowledge Required Not required Risk of data loss High if misused Low Complexity Simple More complex


###


###


### 5. Idempotency Nuance (Senior-Level Point) PUT 

PUT /users/10 { "name": "John" }

**Calling multiple** times:
- Same final state
- Idempotent PATCH PATCH /users/10 { "loginCount": +1 }

**Calling multiple** times:
- Different result
- Not idempotent However:
- PATCH can be idempotent if implemented carefully


###


###


### 6. HTTP Status Codes Typical responses: Method Success Codes PUT 200, 204 PATCH 200, 204 If resource does not exist:
- PUT may create (depending on design)
- PATCH usually returns 404


###


###


### 7. REST Design

**Best Practice**s Use PUT when:
- Client owns full resource state
- Replacing configuration or settings
- Idempotency is important Use PATCH when:
- Partial updates are common
- Large resources
- Mobile or UI-driven updates


### 8.

**Common Interview** Traps
- Saying PUT and PATCH are the same
- Using PUT for partial updates
- Ignoring idempotency rules
- Using PATCH without defining behavior


### 9.

**How to Explain** in 30 Seconds (Interview Answer) PUT replaces the entire resource and is idempotent, meaning repeated requests result in the same state. PATCH applies partial updates and modifies only the fields provided, and its idempotency depends on the implementation. PUT requires the full resource representation, while PATCH is used for partial changes.


### 10.

**Senior-Level** Closing Line PUT represents a desired final state; PATCH represents a change to the current state.

---


## Difference Between POST and PUT

Difference Between POST and PUT POST and PUT are both HTTP methods used to send data to the server, but they differ significantly in semantics, idempotency, and responsibility for resource identification. This is one of the most common REST interview questions.


###


###


### 1. Core Difference (One-Line Summary)
- POST → Create a new subordinate resource
- PUT → Create or replace a resource at a known URI


###


###


### 2. POST

**Definition** POST submits data to a server to create a new resource or trigger processing.

**Characteristics**
- Not idempotent
- Server decides the resource URI
- Can be used for:
  - Creation
  - Actions
  - Non-CRUD operations Example POST /orders { "productId": 10, "quantity": 2 } Response: 201 Created Location: /orders/123

**Calling it** twice:
- Creates two orders


###


###


### 3. PUT

**Definition** PUT creates or replaces a resource at a client-known URI. 

Characteristics
- Idempotent
- Client knows the resource identifier
- Full replacement semantics Example PUT /orders/123 { "id": 123, "productId": 10, "quantity": 2 }

**Calling it** multiple times:
- Resource state remains the same


###


###


### 4. Side-by-Side Comparison (Interview Table) Aspect POST PUT Idempotent No Yes Resource URI Server-generated Client-known

**Purpose** Create / Process Create or Replace Safe No No Typical status 201 Created 200 / 204 Duplicate calls Create duplicates Same result


###


###


### 5. Resource Creation Rule (Important Interview Point)
- Use POST when:
  - Client does not know resource ID
  - Server generates ID
- Use PUT when:
  - Client already knows resource ID
  - Resource is uniquely addressable


###


###


### 6. Can PUT Create a Resource? Yes, if designed that way. PUT /users/100 If /users/100 does not exist:
- Server may create it
- Still idempotent Interview note: PUT can create a resource, but POST cannot replace one.


###


###


### 7. Idempotency Explained Simply
- POST + retry = duplicate data risk
- PUT + retry = safe This matters in:
- Network failures
- Load balancers
- Distributed systems


### 8.

**Common Interview** Traps
- Saying POST is for update
- Using PUT for partial updates
- Ignoring idempotency
- Not returning Location header for POST


### 9.

**How to Explain** in 30 Seconds (Interview Answer) 

POST is used to create a new resource where the server assigns the URI and is not idempotent. PUT is used to create or replace a resource at a known URI and is idempotent. Repeating a PUT request results in the same state, while repeating a POST request creates multiple resources.


### 10.

**Senior-Level** Closing Line POST creates; PUT replaces. POST is action-oriented; PUT is state-oriented.

---


## What Is Idempotency?

What Is Idempotency? Idempotency is a fundamental concept in REST, HTTP, and distributed systems. An operation is idempotent if performing it multiple times produces the same result as performing it once.


###


###


### 1. Formal

**Definition** An operation is idempotent if repeated execution with the same input does not change the final state beyond the first execution. Key idea:
- Same request
- Same server state
- No additional side effects


###


###


### 2. Idempotency in HTTP (REST Context) HTTP defines idempotency for certain methods. HTTP Method Idempotent Reason 

GET Yes Read-only PUT Yes Full replacement DELETE Yes Delete once or many times POST No Creates new resource PATCH Depends Implementation-specific Important:
- Idempotent ≠ Safe
- Idempotent operations can still modify state


###


###


### 3. Examples GET (Idempotent and Safe) GET /users/1 Called 10 times:
- Same response
- No state change PUT (Idempotent) PUT /users/1 { 

 "name": "Alice" } Called multiple times:
- User remains identical DELETE (Idempotent) DELETE /users/1 First call:
- User deleted Second call:
- User already deleted
- Final state is same POST (Not Idempotent) POST /orders Called twice:
- Two orders created


###


###


### 4. Why Idempotency Matters (Very Important) Idempotency is critical for:
- Network retries
- Timeouts
- Client-side retry logic
- Load balancers
- Distributed systems

**Interview line:** Idempotency makes APIs reliable in the presence of failures.


###


###


### 5. Idempotency vs Safety (Common Interview Trap) Concept

**Meaning** Safe No state change Idempotent Same final state

**Examples:**
- GET → Safe + Idempotent
- PUT → Not safe but idempotent
- POST → Neither safe nor idempotent


###


###


### 6. Making POST Idempotent (Advanced Topic) Although POST is not idempotent by default, it can be made idempotent using: Idempotency Key Idempotency-Key: abc-123

**Server behavior**:
- Store key + response
- Repeat request returns same response

**Common use** cases:
- Payments
- Order creation


###


###


### 7. Idempotency in Databases

**Examples:**
- UPDATE users SET status='ACTIVE' WHERE id=1 → idempotent
- UPDATE users SET login_count = login_count + 1 → not idempotent


### 8.

**Common Interview** Mistakes
- Confusing idempotency with caching
- Saying POST is idempotent
- Ignoring retries
- Not understanding final-state semantics


### 9.

**One-Minute Interview** Answer Idempotency means that performing the same operation multiple times results in the same final state as performing it once. In REST, HTTP methods like GET, PUT, and DELETE are idempotent, while POST is not. Idempotency is essential for handling retries and failures in distributed systems.


### 10.

**Senior-Level** Closing Line Idempotency is about the final state, not the number of times an operation is executed.
- Idempotency vs atomicity Idempotency → Repeating an operation gives the same final result Atomicity → An operation happens completely or not at all

---


## What Are HTTP Status Codes?

What Are HTTP Status Codes? HTTP status codes are standard numeric responses sent by a server to indicate the result of an HTTP request. They tell the client what happened to the request at the protocol level, not the business level. They are a core part of HTTP and RESTful API design. Why HTTP Status Codes Exist HTTP status codes help to:
- Communicate success or failure clearly
- Standardize client–server interaction
- Enable proper error handling and retries
- Improve observability and debugging
- Enforce REST semantics Key interview line: HTTP status codes describe the outcome of the request, not business logic. Status Code Classification HTTP status codes are grouped by their first digit: Range Category

**Meaning** 1xx Informational Request received, processing 2xx Success Request successfully processed 3xx Redirection Further action required 

4xx Client Error Client made a mistake 5xx Server Error Server failed to handle request 1xx – Informational Responses These indicate that the request was received and processing is continuing.

**Examples:**
- 100 Continue – Client may continue sending the request
- 101 Switching Protocols

**Usage:**
- Rare in REST APIs
- Mostly used internally by HTTP clients and servers 2xx – Success Responses (Most Important) These indicate the request was successfully handled. Common 2xx Status Codes 200 OK
- Request succeeded
- Response body usually present

**Example:** GET /users/1 → 200 OK 201 Created
- Resource successfully created
- Typically returned by POST
- Should include a Location header

**Example:** POST /orders → 201 Created Location: /orders/123 204 No Content
- Request succeeded
- No response body

**Common use**:
- DELETE
- PUT with no response payload 3xx – Redirection Responses These indicate the client must take additional action. Common 3xx Codes
- 301 Moved Permanently
- 302 Found
- 304 Not Modified

**Usage:**
- Browsers
- Caching
- CDNs In REST APIs:
- Mostly used for caching (304)
- Rare otherwise 

 4xx – Client Error Responses (Interview Favorite) These indicate the client sent an invalid request. Common 4xx Status Codes 400 Bad Request
- Malformed request
- Invalid input
- JSON parse errors 401 Unauthorized
- Authentication required or failed
- Missing or invalid token Important: 401 means “not authenticated”, not “not allowed”. 403 Forbidden
- Client is authenticated
- But lacks permission Key distinction: 401 = who are you? 403 = you are not allowed. 404 Not Found
- Resource does not exist

**Example:** GET /users/999 → 404 

 409 Conflict
- Request conflicts with current state
- Duplicate resource creation
- Version conflict Common in:
- Payments
- Order systems 422 Unprocessable Entity
- Request is syntactically valid
- Semantic validation failed

**Example:**
- Field-level validation errors 5xx – Server Error Responses These indicate the server failed to process a valid request. Common 5xx Status Codes 500 Internal Server Error
- Generic server failure
- Unhandled exception 502 Bad Gateway
- Invalid response from upstream server
- Common in microservices 

503 Service Unavailable
- Server temporarily unavailable
- Maintenance or overload 504 Gateway Timeout
- Upstream service did not respond in time HTTP Status Codes in REST APIs (Best Practice Mapping) Scenario Status Code Successful GET 200 Resource created 201 Successful DELETE 204 Invalid request 400 Authentication failure 401 Authorization failure 403 Resource not found 404 

Duplicate request 409 Validation error 422 Server failure 500

**Common Interview** Mistakes
- Returning 200 for every response
- Using 500 for validation errors
- Confusing 401 and 403
- Putting business errors in HTTP status codes
- Ignoring proper status codes in REST APIs

**One-Minute Interview** Answer HTTP status codes are standardized numeric codes returned by a server to indicate the result of an HTTP request. They are grouped into informational, success, redirection, client error, and server error categories. Proper use of status codes is essential for RESTful API design, clear communication, and reliable client–server interaction.

---

# 📂 Microservices Architecture


## What Is Microservices Architecture?

What Is Microservices Architecture? Microservices architecture is an architectural style where an application is built as a collection of small, independent services, each responsible for a single business capability. Each service is independently developed, deployed, scaled, and owned.


###


###


### 1. Core

**Definition** 

Microservices architecture structures an application as a set of loosely coupled, independently deployable services that communicate over lightweight protocols, typically HTTP or messaging.


### 2.

**Key

**Characteristics****


###


###


### 1. Single Responsibility per Service
- Each service owns one business capability
-

**Example:** Order, Payment, Inventory as separate services Benefit:
- Clear boundaries
- Easier maintenance and evolution


###


###


### 2. Independent Deployment
- Services can be deployed without redeploying the entire system
- Enables faster releases and safer rollbacks

**Interview line:** Independent deployment is the biggest advantage of microservices.


###


###


### 3. Decentralized Data Management
- Each service owns its own database
- No shared database across services Why:
- Loose coupling
- Independent schema evolution Important rule: Database-per-service is a core microservices principle.


###


###


### 4. Technology Heterogeneity
- Different services can use different technologies
-

**Example:** Java for core services, Node.js for BFF, Python for ML Benefit:
- Right tool for the job


###


###


### 5. Lightweight Communication
- REST over HTTP
- Async messaging (Kafka, RabbitMQ) Avoid:
- Tight coupling
- Synchronous chatty calls


###


###


### 6. Built for Failure
- Failures are expected
- Services must handle:
  - Timeouts
  - Retries
  - Circuit breakers

**Interview line:** In microservices, failure is a normal condition, not an exception.


###


###


### 3. Microservices vs Monolith Aspect Monolith Microservices Deployment Single unit Independent services 

Scalability Scale whole app Scale per service Coupling Tight Loose Tech stack Single Multiple Failure impact Global Isolated Complexity Low initially Higher operationally


### 4.

**Benefits** of Microservices
- Faster development cycles
- Independent scaling
- Better fault isolation
- Team autonomy
- Easier adoption of new technologies


###


###


### 5. Challenges of Microservices (Very Important) Microservices introduce distributed system complexity:
- Network latency
- Partial failures
- Data consistency
- Distributed transactions
- Observability complexity
- Operational overhead

**Interview line:** Microservices trade simplicity of code for complexity of operations.


###


###


### 6. Data Consistency in Microservices
- No ACID transactions across services
- Use:
  - Event-driven architecture
  - Eventual consistency
  - Saga pattern Key idea: Strong consistency is replaced by eventual consistency.


### 7.

**When to Use** Microservices Good fit when:
- Large, complex domain
- Multiple teams
- High scalability requirements
- Independent release cadence Not a good fit when:
- Small team
- Simple application
- Tight timelines
- Limited DevOps maturity

**Interview trap**: Microservices are not a default choice.

---


## Difference Between Monolith and Microservices

Difference Between Monolith and Microservices 

The difference between Monolith and Microservices is primarily about how an application is structured, deployed, and evolved over time.


###


###


### 1. Monolithic Architecture

**Definition** A monolith is an application where all components are packaged and deployed as a single unit.
- UI, business logic, and data access live in one codebase
- Single deployment artifact (JAR/WAR)
- Usually backed by a single database

**Characteristics**
- Simple to develop initially
- Easy local debugging
- Strong in-process calls
- Centralized data model


###


###


### 2. Microservices Architecture

**Definition** Microservices architecture structures an application as a collection of small, independent services, each owning a specific business capability.
- Independent codebases
- Independent deployments
- Each service owns its data
- Communicate over network (HTTP/messaging)


###


###


### 3. Side-by-Side Comparison Aspect Monolith Microservices Codebase Single Multiple 

Deployment Single unit Independent services Scaling Scale whole app Scale per service Technology stack Usually one Multiple allowed Database Shared Database per service Communication In-process Network calls Failure impact Entire app affected Isolated to service Operational complexity Low High DevOps maturity needed Low High


###


###


### 4. Development & Team Perspective Monolith
- Easier for small teams
- Simple CI/CD pipeline
- Coordination easier
- Changes require full redeploy Microservices
- Teams own services end-to-end
- Parallel development
- Independent releases
- Requires strong DevOps culture

**Interview line:** Microservices scale teams better; monoliths scale simplicity better.


###


###


### 5. Data Management Differences Monolith
- Single database
- Strong ACID transactions
- Simple joins Microservices
- Database per service
- No cross-service joins
- Eventual consistency
- Saga pattern for workflows Key rule: Sharing a database breaks microservices boundaries.


### 6.

**Performance** & Communication Monolith
- Fast in-memory calls
- Low latency
- No network overhead Microservices
- Network latency
- Requires retries, timeouts
- Needs resilience patterns Interview insight: 

Microservices trade performance for flexibility and resilience.


###


###


### 7. Failure Handling Monolith
- Single bug can crash entire app
- Limited fault isolation Microservices
- Failure is isolated
- Requires circuit breakers
- Designed for partial failure


### 8.

**When to Use** What (Very Important) Choose Monolith When:
- Application is small or medium
- Team is small
- Requirements are stable
- Time-to-market is critical Choose Microservices When:
- Large and complex domain
- Multiple teams
- Independent scaling required
- Frequent releases needed

**Interview trap**: Microservices are not a default architecture.


###


###


### 9. Evolution Path (Common

**Real-World** Scenario) Most successful systems follow:


###


###


### 1. Start with monolith


###


###


### 2. Modularize internally


###


###


### 3. Extract microservices gradually This avoids premature complexity.


### 10.

**One-Minute Interview** Answer A monolith is a single deployable application where all components are tightly coupled, making it simpler to develop and operate initially. Microservices break the application into small, independently deployable services that own their data and scale independently. While microservices improve scalability and team autonomy, they introduce distributed system complexity and require mature DevOps practices.


### 11.

**Senior-Level** Closing Line Monoliths optimize for simplicity; microservices optimize for change and scale.

---


## How do microservices communicate with each other?

How do microservices communicate with each other? (REST, Kafka) Microservices communicate with each other using synchronous and asynchronous communication patterns. The choice depends on latency requirements, coupling, scalability, and failure handling.


###


###


### 1. REST (HTTP/HTTPS – Synchronous Communication)

**How it works**
- Services expose HTTP APIs (usually JSON).
- One service directly calls another and waits for a response.
- Typically implemented using Spring Boot, ASP.NET, Node.js, etc. 

Characteristics
- Request–response model
- Human-readable payloads (JSON)
- Stateless communication
- Easy to debug and test

**Pros**
- Simple and widely understood
- Language and platform independent
- Easy integration with external systems
- Works well with API Gateways and load balancers

**Cons**
- Tight temporal coupling (caller waits for response)
- Latency increases with chained calls
- Risk of cascading failures
- Not ideal for high-throughput event streams

**When to use**
- CRUD operations
- Real-time user-driven workflows
- Service-to-service calls where immediate response is required
- Low to moderate traffic


###


###


### 2. Kafka (Event-Driven – Asynchronous Communication)

**How it works**
- Services publish events to Kafka topics.
- Other services consume events independently.
- Producer does not know who the consumer is.

**Characteristics**
- Asynchronous and non-blocking
- Event-based communication
- High throughput and durability
- Loose coupling between services

**Pros**
- Highly scalable and fault-tolerant
- Decouples producers and consumers
- Supports replay of events
- Excellent for streaming and data pipelines

**Cons**
- Increased system complexity
- Eventual consistency
- Requires schema management (Avro/Protobuf)
- Debugging is harder than REST

**When to use**
- Event-driven architectures
- High-volume telemetry or analytics data
- Audit logs and data pipelines
- Long-running workflows
- Cross-domain communication

---


## What is Feign Client?

What is Feign Client? Feign Client is a declarative HTTP client used in Spring Boot / Spring Cloud microservices to simplify service-to-service REST communication. Instead of writing boilerplate code using RestTemplate or WebClient, Feign allows you to define an interface, and Spring automatically generates the HTTP client implementation at runtime. Why Feign Client is needed (Problem it solves) Without Feign:
- You write manual HTTP calls
- Handle URLs, headers, serialization, and error handling yourself
- Code becomes repetitive and harder to maintain Feign abstracts all this by:
- Reducing boilerplate
- Making REST calls look like local method calls
- Integrating cleanly with Spring Cloud components

**Example (**Conceptual) @FeignClient(name = "order-service") public interface OrderClient { @GetMapping("/orders/{id}") OrderResponse getOrder(@PathVariable String id); } Calling orderClient.getOrder("123"):
- Resolves service via service discovery (Eureka / K ubernetes DNS)
- Builds HTTP request
- Executes REST call
- Maps response to OrderResponse

**Key Features**


###


###


### 1. Declarative Style
- No explicit HTTP client code
- Interface-driven design


###


###


### 2. Service Discovery Integration
- Works seamlessly with Eureka, Consul, Kubernetes
- Uses service name instead of hardcoded URL


###


###


### 3. Load Balancing
- Integrated with Spring Cloud LoadBalancer
- Automatically distributes traffic across instances


###


###


### 4. Fault Tolerance
- Integrates with Resilience4j
- Supports circuit breaker, retry, fallback


###


###


### 5. Request Interceptors
- Add headers (auth tokens, correlation IDs)
- Logging and tracing support Feign vs RestTemplate vs WebClient Aspect Feign RestTemplate WebClient Style Declarative Imperative Reactive Boilerplate Very Low High Medium Service Discovery Native Manual Manual Load Balancing Built-in Manual Manual Reactive No No Yes Best For Sync service calls Legacy apps Reactive systems

**When to use** Feign Client
- Synchronous REST communication between microservices
- Spring-based microservice ecosystems
- Readable, maintainable code
- Integration with service discovery and resilience patterns

**Senior-Level** Considerations (Interview Points)
- Feign is blocking by default
- Avoid chaining Feign calls (risk of latency amplification)
- Always configure:
  - Timeouts
  - Retries
  - Circuit breakers
- Use Feign for north-south or simple east-west traffic, not bulk data movement

---


## What is Service Discovery?

What is Service Discovery? Service Discovery is a mechanism that allows microservices to dynamically find and communicate with each other without hard-coding network locations (IP addresses or ports). In a microservices environment, services are dynamic:
- Instances scale up and down
- IPs and ports change frequently
- Services may restart or move across nodes Service discovery solves this by maintaining a central registry of available services and their instances. Why Service Discovery is needed Without service discovery:
- Services depend on fixed IPs/URLs
- Scaling and failover break communication
- Deployments become fragile With service discovery:
- Services discover each other at runtime
- Load balancing becomes automatic
- Failures are handled transparently How Service Discovery works (High level flow)


###


###


### 1. Service instance starts


###


###


### 2. It registers itself with the service registry


###


###


### 3. Registry stores service name, IP, port, health status


###


###


### 4. Client queries registry to locate a service


###


###


### 5. Request is routed to a healthy instance

**Types of** Service Discovery


###


###


### 1. Client-Side Discovery Flow
- Client asks registry for service instances
- Client chooses an instance (load balancing)
- Client makes direct call Examples
- Netflix Eureka
- Spring Cloud LoadBalancer

**Pros**
- Simple architecture
- Flexible client-side load balancing

**Cons**
- Client is tightly coupled to registry
- Every client must implement discovery logic


###


###


### 2. Server-Side Discovery Flow
- Client calls a load balancer or gateway
- Load balancer queries registry
- Request is forwarded to an instance Examples
- Kubernetes Service
- AWS ALB / NLB
- Istio / Envoy

**Pros**
- Client is unaware of service instances
- Centralized routing and load balancing

**Cons**
- Additional infrastructure component Popular Service Discovery Tools Netflix Eureka
- Client-side discovery
- Service instances register themselves
- Often used with Spring Cloud Kubernetes Service Discovery
- DNS-based discovery
- Services accessed via stable service names
- Native load balancing Consul
- Supports health checks
- Multi-datacenter support
- Key-value store capabilities Service Discovery vs Load Balancing 

Aspect Service Discovery Load Balancing

**Purpose** Find service instances Distribute traffic Scope Naming and lookup Traffic routing Awareness Knows instances Knows traffic Used Together Yes Yes Service discovery locates services; load balancing chooses which instance to call.

**Senior-Level** Interview Points
- Service discovery eliminates tight coupling
- Essential for auto-scaling and resilience
- Client-side vs server-side discovery trade-offs
- Kubernetes has built-in discovery, often replacing Eureka
- Service discovery works best with circuit breakers and retries

---


## What is an API Gateway?

What is an API Gateway? An API Gateway is a single entry point for all client requests to a backend system, typically used in microservices architectures. 

It sits between clients (UI, mobile apps, external systems) and backend services, and handles cross-cutting concerns centrally instead of pushing them into each service. Why API Gateway is needed (real-world reason) In a microservices system, exposing every service directly to clients creates problems:
- Clients need to know many service URLs
- Each service must implement security, logging, throttling
- Any change in backend affects clients
- Difficult to control traffic, versions, and failures API Gateway solves this by acting as a façade.

**Core Responsibilities**


###


###


### 1. Request Routing
  - Routes incoming requests to the correct backend service
  -

**Example:** /users → user-service /orders → order-service


###


###


### 2. Authentication & Authorization
  - JWT validation, OAuth2, API keys
  - Offloads security from services


###


###


### 3. Rate Limiting & Throttling
  - Protects backend from abuse or traffic spikes


###


###


### 4. Request / Response Transformation
  - Modify headers, payloads
  - Aggregate multiple service responses into one


###


###


### 5. Load Balancing
  - Distributes traffic across service instances


###


###


### 6. API Versioning
  - /v1, /v2 routing without changing clients


###


###


### 7. Observability
  - Centralized logging, metrics, tracing


###


###


### 8. Circuit Breaking / Timeout Handling
  - Prevents cascading failures Typical Architecture Flow 

Client → API Gateway → Microservices (User, Order, Payment, etc.) Client never talks directly to services. API Gateway vs Load Balancer (Interview Favorite) Aspect API Gateway Load Balancer Level Application layer Network/transport Routing URL/path based Instance based Security Yes Limited Transformation Yes No Aggregation Yes No Load balancer distributes traffic API Gateway manages APIs

**When NOT to** use API Gateway
- Very small monolith
- Extremely low-latency systems (adds a hop)
- Internal-only communication where service mesh is sufficient Common Implementations
- Spring Cloud Gateway
- Netflix Zuul (older)
- Kong
- NGINX
- Cloud-managed gateways (AWS, Azure, GCP)

**One-Line Interview** Answer 

API Gateway is a centralized entry point that handles routing, security, throttling, transformation, and monitoring for backend services, especially in microservices architectures.

---


## What is a Circuit Breaker?

What is a Circuit Breaker? A Circuit Breaker is a resilience pattern used in distributed systems to prevent cascading failures when a dependent service is slow, unresponsive, or failing. Instead of repeatedly calling a failing service, the circuit breaker stops the calls temporarily, allowing the system to recover and remain responsive. Why Circuit Breaker is required (real-world problem) In microservices:
- Service A calls Service B
- Service B becomes slow or down
- Threads in Service A get blocked
- Thread pool exhausts
- Service A also starts failing
- Entire system goes down This is called cascading failure. Circuit Breaker prevents this by failing fast. How Circuit Breaker works (conceptual flow)


###


###


### 1. Monitor calls to a remote service


###


###


### 2. Track failures, timeouts, slow responses


###


###


### 3. If failures exceed a threshold → open the circuit


###


###


### 4. Stop calling the failing service


###


###


### 5. After some time → test again


###


###


### 6. If healthy → resume traffic Circuit Breaker States (Very Important for Interview)


###


###


### 1. Closed
- Normal state
- All requests are allowed
- Failures are monitored


###


###


### 2. Open
- Failure threshold exceeded
- Requests are not sent to the remote service
- Immediate failure (fail-fast)


###


###


### 3. Half-Open
- After a wait duration
- Limited test requests are allowed
- If successful → move to Closed
- If failed → back to Open What Circuit Breaker Protects
- Thread pools
- CPU and memory
- Downstream services
- Overall system availability Circuit Breaker vs Retry (Common Trap Question) Aspect Circuit Breaker Retry

**Purpose** Stop calls Repeat calls 

When used Service is unhealthy Transient failures Risk Low Can amplify failures

**Best practice** Use with retry Retry with limits Important: Retry without circuit breaker can make outages worse. Circuit Breaker vs Timeout
- Timeout: Limits how long to wait for a response
- Circuit Breaker: Decides whether to call at all Both should be used together.

**Example (**Spring Boot – Conceptual) @CircuitBreaker(name = "orderService", fallbackMethod = "fallback") public Order getOrder(String id) { return orderClient.getOrder(id); } public Order fallback(String id, Exception ex) { return new Order("DEFAULT"); } 

Key idea: fallback ensures graceful degradation.

**Where Circuit** Breaker is Implemented
- Application level (libraries)
- API Gateway
- Service Mesh

**When NOT to** use Circuit Breaker
- In-memory or local method calls
- Very low-latency, ultra-critical paths (must be carefully tuned)
- When failure is acceptable and fast

**One-Line Interview** Answer Circuit Breaker is a resilience pattern that stops calls to a failing service after a threshold of failures, preventing cascading failures and enabling fast recovery.

---


## What is Saga Pattern?

What is Saga Pattern? The Saga Pattern is a data consistency pattern used in microservices to manage distributed transactions without using a two-phase commit (2PC). A saga breaks a large transaction into a sequence of local transactions, where each step updates its own database, and if any step fails, compensating transactions are executed to undo the previous steps. Why Saga Pattern is needed In microservices:
- Each service has its own database
- ACID transactions cannot span services
- 2PC is:
  - Slow
  - Tightly coupled
  - Not scalable
  - Single point of failure Saga provides eventual consistency instead of strong consistency.

**Core Concept**
- Transaction is split into N steps
- Each step:
  - Executes a local DB transaction
  - Publishes an event or triggers next step
- On failure:
  - Previously completed steps are compensated

**Types of** Saga Pattern (Very Important for Interview)


###


###


### 1. Choreography-based Saga (Event-driven)
- No central coordinator
- Services communicate via events
- Each service reacts to events and emits the next event Example flow:


###


###


### 1. Order Service creates order


###


###


### 2. Emits OrderCreated


###


###


### 3. Payment Service processes payment


###


###


### 4. Emits PaymentCompleted


###


###


### 5. Inventory Service reserves stock

**Failure handling**:
- Payment fails → emit PaymentFailed
- Order Service listens → cancels order

**Pros**:
- Loose coupling
- High scalability

**Cons**:
- Hard to track flow
- Complex debugging
- Event sprawl


###


###


### 2. Orchestration-based Saga (Coordinator-driven)
- A Saga Orchestrator controls the flow
- Orchestrator tells services what to do
- Services report success/failure Example flow:


###


###


### 1. Orchestrator → Order Service: create order


###


###


### 2. Orchestrator → Payment Service: charge payment


###


###


### 3. Orchestrator → Inventory Service: reserve stock

**Failure handling**:
- Payment fails → Orchestrator calls compensation:
  - Cancel order

**Pros**:
- Clear control flow
- Easier monitoring
- Centralized logic

**Cons**:
- Orchestrator can become complex
- Slight coupling

**Compensation** Transactions (Key Interview Point)
- Not a rollback
- Must be explicitly designed
- Must be:
  - Idempotent
  - Safe to retry
  - Eventually consistent

**Example:**
- Reserve inventory →

**Compensation** = Release inventory
- Charge payment →

**Compensation** = Refund payment Saga vs 2PC (Classic Comparison) Aspect Saga 2PC Consistency Eventual Strong Coupling Loose Tight Scalability High Low

**Failure handling**

**Compensation** Blocking Microservices fit Yes No Saga Pattern Challenges
- Complex error handling
- Data inconsistency window
- Idempotency required
- Message duplication handling
- Exactly-once delivery not guaranteed

**Where Saga** is commonly used
- Order management systems
- Payment workflows
- Booking systems
- E-commerce checkout
- Any long-running business transaction

**One-Line Interview** Answer Saga Pattern is a distributed transaction pattern that maintains data consistency across microservices using a sequence of local transactions with compensating actions instead of 2-phase commit.

---


## How do you handle Distributed Transactions?

How do you handle Distributed Transactions? In microservices, I avoid distributed ACID transactions and handle consistency using event-driven patterns and eventual consistency. The primary approach is Saga Pattern, supported by idempotency, retries, and compensation.


###


###


### 1. Avoid 2-Phase Commit (2PC) I do not use XA / 2PC in microservices because:
- Tight coupling between services
- Blocking behavior
- Poor scalability
- Single point of failure
- Not cloud-native 2PC is acceptable only in legacy monoliths or tightly coupled systems.


###


###


### 2. Use Saga Pattern (Primary Strategy) 

I model a business transaction as a series of local transactions, each with a compensating action. Two execution styles:
- Choreography (event-driven using Kafka)
- Orchestration (central saga coordinator) Each service:
- Commits its own database transaction
- Publishes an event
- Never shares its database Failure → execute compensating steps.


###


###


### 3. Ensure Idempotency (Critical) Because retries and duplicate events are common:
- APIs are idempotent
- Each request carries a transactionId / sagaId
- Duplicate messages are safely ignored

**Example:**
- Payment charged once even if event is received multiple times


###


###


### 4. Reliable Messaging (Outbox Pattern) To avoid DB commit but event publish failure: Transactional Outbox Pattern
- Write business data + event in the same DB transaction
- Background process publishes events to Kafka
- Ensures atomicity between DB and messaging


###


###


### 5. Eventual Consistency with

**Compensation**
- Temporary data inconsistency is accepted
- System converges to a consistent state
- Compensating actions are business-aware, not rollbacks

**Example:**
- Payment success → inventory fails → refund payment


###


###


### 6. Timeout, Retry, and Circuit Breaker
- Timeouts prevent thread blocking
- Retries for transient failures (with backoff)
- Circuit breakers prevent cascading failures
- Never retry blindly without limits


###


###


### 7. Observability & Monitoring
- Distributed tracing (traceId, spanId)
- Centralized logs and metrics
- Saga state tracking table for long-running flows


###


###


### 8. When I Would Use 2PC Very rare cases:
- Single vendor DB
- Strong consistency required
- Low throughput
- Small number of participants Even then, I prefer refactoring toward Saga.

**Sample Interview**-Ready Answer (Concise) In microservices, I handle distributed transactions using Saga Pattern with eventual consistency. Each service performs a local transaction and publishes events. On failure, compensating actions are executed. I avoid 2-phase commit and rely on idempotency, reliable messaging (outbox pattern), retries, and circuit breakers to ensure consistency and resilience.

---


## How do you secure Microservices using OAuth2 / JWT?

How do you secure Microservices using OAuth2 / JWT? In a microservices architecture, I secure services using OAuth 2.0 for authorization and JWT for stateless authentication, typically with a central Identity Provider (IdP). The goal is centralized authentication, decentralized authorization, and zero trust between services.


###


###


### 1. High-Level Security Model
- Authentication → handled by an Identity Provider
- Authorization → enforced at:
  - API Gateway
  - Individual microservices
- Identity propagation → via JWT
- No session state in services


###


###


### 2. OAuth2 Roles in Microservices Identity Provider (Authorization Server)
- Authenticates users / clients
- Issues JWT access tokens
- Manages users, roles, scopes

**Examples:**
- Keycloak
- Azure AD
- Okta
- Auth0 Resource Server (Microservice)
- Validates JWT
- Authorizes requests based on scopes/roles
- Does not authenticate users directly


###


###


### 3. Token Flow (Client → Gateway → Services)


###


###


### 1. Client authenticates with IdP


###


###


### 2. IdP issues JWT access token


###


###


### 3. Client sends token in Authorization: Bearer <token>


###


###


### 4. API Gateway:
  - Validates token
  - Applies coarse-grained authorization


###


###


### 5. Microservices:
  - Re-validate token
  - Apply fine-grained authorization


###


###


### 4. Why JWT (Important Interview Point)
- Self-contained (claims inside token)
- No DB lookup per request
- Stateless → horizontally scalable
- Works well with gateways and service meshes JWT typically contains:
- sub (user/client)
- exp, iat
- scope / roles
- iss, aud


###


###


### 5. Gateway-Level Security At API Gateway:
- Token validation
- Rate limiting
- IP filtering
- Scope-based access Reduces attack surface on backend services.


###


###


### 6. Service-to-Service Security (Very Important)

**Approach 1**: OAuth2 Client Credentials Flow
- Each service has its own clientId/secret
- Token issued for service identity
- Used for synchronous REST calls

**Approach 2**: Token Propagation
- Forward the incoming JWT to downstream services
- Maintains user context Used when authorization depends on end-user identity.


###


###


### 7. JWT Validation in Microservices Each service:
- Validates token signature using public key (JWK)
- Verifies:
  - issuer (iss)
  - audience (aud)
  - expiration (exp)
- Maps roles/scopes to authorities No call to IdP on every request.


###


###


### 8. Fine-Grained Authorization
- Role-based access control (RBAC)
- Scope-based authorization
- Attribute-based checks if needed

**Example:**
- order.read
- order.write


###


###


### 9. Token Expiry & Refresh Strategy
- Short-lived access tokens (5–15 min)
- Refresh tokens handled only by client
- Microservices never see refresh tokens


###


###


### 10. Security

**Best Practice**s
- HTTPS everywhere
- Short token lifetime
- Do not trust gateway blindly (defense in depth)
- Rotate signing keys
- Use mTLS for internal traffic if required
- Protect secrets via vaults


### 11.

**Common Interview** Traps & Answers Q: Why validate JWT again in microservice if gateway already did? Because gateways can be bypassed; zero-trust model requires each service to protect itself. Q: Where do you store sessions? No sessions; JWT is stateless. Q: Can JWT be revoked? Not directly; use short expiry, token blacklist only if absolutely needed.


### 12.

**One-Line Interview** Answer I secure microservices using OAuth2 for authorization and JWT for stateless authentication. A central IdP issues tokens, the API Gateway performs initial validation, and each microservice independently validates JWTs and enforces fine-grained authorization, following a zero-trust model.

---


##

---


## Difference Between PUT and PATCH

Difference Between PUT and PATCH](#difference-between-put-and-patch)
55. [

---


## Difference Between POST and PUT

Difference Between POST and PUT](#difference-between-post-and-put)
56. [

---


## What Is Idempotency?

What Is Idempotency?](#what-is-idempotency)
57. [

---


## What Are HTTP Status Codes?

What Are HTTP Status Codes?](#what-are-http-status-codes)


### Microservices Architecture

58. [

---

# 📂 Microservices Architecture


## What Is Microservices Architecture?

What Is Microservices Architecture?](#what-is-microservices-architecture)
59. [

---


## Difference Between Monolith and Microservices

Difference Between Monolith and Microservices](#difference-between-monolith-and-microservices)
60. [

---


## How do microservices communicate with each other?

How do microservices communicate with each other?](#how-do-microservices-communicate-with-each-other)
61. [

---


## What is Feign Client?

What is Feign Client?](#what-is-feign-client)
62. [

---


## What is Service Discovery?

What is Service Discovery?](#what-is-service-discovery)
63. [

---


## What is an API Gateway?

What is an API Gateway?](#what-is-an-api-gateway)
64. [

---


## What is a Circuit Breaker?

What is a Circuit Breaker?](#what-is-a-circuit-breaker)
65. [

---


## What is Saga Pattern?

What is Saga Pattern?](#what-is-saga-pattern)
66. [

---


## How do you handle Distributed Transactions?

How do you handle Distributed Transactions?](#how-do-you-handle-distributed-transactions)
67. [

---


## How do you secure Microservices using OAuth2 / JWT?

How do you secure Microservices using OAuth2 / JWT?](#how-do-you-secure-microservices-using-oauth2-jwt)
68. [What is Distributed Tracing?](#what-is-distributed-tracing)
69. [

---

##

---

## Difference Between PUT and PATCH

Difference Between PUT and PATCH](#difference-between-put-and-patch)
55. [

---

## Difference Between POST and PUT

Difference Between POST and PUT](#difference-between-post-and-put)
56. [

---

## What Is Idempotency?

What Is Idempotency?](#what-is-idempotency)
57. [

---

## What Are HTTP Status Codes?

What Are HTTP Status Codes?](#what-are-http-status-codes)


### Microservices Architecture

58. [

---

# 📂 Microservices Architecture

## What Is Microservices Architecture?

What Is Microservices Architecture?](#what-is-microservices-architecture)
59. [

---

## Difference Between Monolith and Microservices

Difference Between Monolith and Microservices](#difference-between-monolith-and-microservices)
60. [

---

## How do microservices communicate with each other?

How do microservices communicate with each other?](#how-do-microservices-communicate-with-each-other)
61. [

---

## What is Feign Client?

What is Feign Client?](#what-is-feign-client)
62. [

---

## What is Service Discovery?

What is Service Discovery?](#what-is-service-discovery)
63. [

---

## What is an API Gateway?

What is an API Gateway?](#what-is-an-api-gateway)
64. [

---

## What is a Circuit Breaker?

What is a Circuit Breaker?](#what-is-a-circuit-breaker)
65. [

---

## What is Saga Pattern?

What is Saga Pattern?](#what-is-saga-pattern)
66. [

---

## How do you handle Distributed Transactions?

How do you handle Distributed Transactions?](#how-do-you-handle-distributed-transactions)
67. [

---

## How do you secure Microservices using OAuth2 / JWT?

How do you secure Microservices using OAuth2 / JWT?](#how-do-you-secure-microservices-using-oauth2-jwt)
68. [What is Distributed Tracing?](#what-is-distributed-tracing)
69. [

---

## What is Distributed Tracing?

What is Distributed Tracing?

What is Distributed Tracing?

What is Distributed Tracing? 

Distributed tracing is a technique used in microservices architectures to track a single request as it flows across multiple services, threads, and network boundaries. It helps answer:
- Where did the request go?
- Which service is slow or failing?
- Why is end-to-end latency high? In a distributed system, logs alone are not enough because one request generates logs in multiple services.

**Core Concept** A single client request is broken into spans, and all spans together form a trace.
- Trace → end-to-end journey of a request
- Span → one unit of work (e.g., service call, DB query) Each trace is identified by a traceId, and each span has a spanId. Why Distributed Tracing is Needed Without tracing:
- You see isolated logs
- Hard to debug latency issues
- Root cause analysis is slow With tracing:
- Full request visibility
- Latency breakdown per service
- Faster production debugging
- Essential for microservices and async systems How Distributed Tracing Works (High Level)


###


###


### 1. Request enters the system (API Gateway / first service) 2. A traceId is generated


###


###


### 3. Trace context is propagated via HTTP headers


###


###


### 4. Each service creates spans


###


###


### 5. Spans are sent to a tracing backend


###


###


### 6. Trace is visualized end-to-end Key Headers (Interview Detail) Common headers:
- traceparent (W3C standard)
- X-B3-TraceId
- X-B3-SpanId These headers propagate tracing context across services. Tools & Libraries Zipkin
- Distributed tracing backend
- Stores and visualizes traces
- Shows service dependency graphs and latency
- Requires instrumentation or tracing libraries Used mainly as:
- Trace collector
- UI for visualization Spring Cloud Sleuth
- Spring abstraction over tracing
- Automatically:
  - Generates traceId/spanId
  - Propagates context
  - Instruments REST, messaging, schedulers
- Historically integrated with Zipkin Note:
- Sleuth is deprecated in favor of OpenTelemetry in newer Spring versions 

 OpenTelemetry
- Vendor-neutral observability standard
- Covers:
  - Tracing
  - Metrics
  - Logs
- Replaces Sleuth going forward
- Supports many backends:
  - Zipkin
  - Jaeger
  - Grafana Tempo
  - Cloud providers OpenTelemetry is now the industry standard. Trace Context Propagation (Very Important)
- Trace context must flow across:
  - REST calls
  - Async threads
  - Kafka / messaging
- If context is lost, traces break Libraries like Sleuth / OpenTelemetry handle this automatically. Distributed Tracing vs Logging Aspect Logging Distributed Tracing Scope Single service Multiple services Correlation Manual Automatic (traceId) 

Latency analysis Poor Excellent Microservices fit Limited Essential Common

**Use Case**s
- Identify slow microservice
- Debug production issues
- Analyze dependency latency
- Validate SLAs
- Troubleshoot async workflows Interview Trap Questions & Answers Q: Is distributed tracing only for synchronous calls? No. It also supports async, messaging, and event-driven flows. Q: Do you need Zipkin if you use OpenTelemetry? OpenTelemetry is instrumentation; Zipkin is a backend. They serve different roles. Q: Does tracing impact performance? Minimal overhead if sampling is configured properly.

**One-Line Interview** Answer Distributed tracing tracks a request across multiple microservices using trace and span IDs, providing end-to-end visibility for latency analysis and debugging. Tools like Zipkin act as trace backends, while libraries like Sleuth and OpenTelemetry handle trace generation and propagation.

---


## Role of Config Server in Spring Cloud

Role of Config Server in Spring Cloud 

The Config Server in Spring Cloud provides centralized, externalized configuration management for distributed systems, especially microservices. Its primary role is to decouple configuration from application binaries, so configuration can be managed, changed, and versioned without rebuilding or redeploying services. What problem Config Server solves In microservices:
- Each service runs in multiple environments (dev, QA, prod)
- Each service has environment-specific properties
- Managing config inside JARs leads to:
  - Frequent rebuilds
  - Inconsistent configuration
  - Configuration drift
  - Security risks Config Server solves this by centralizing configuration.

**Core Responsibilities**


###


###


### 1. Centralized Configuration
- All service configs are stored in a single source of truth
- Typically backed by:
  - Git
  - Vault
  - File system
  - Cloud config stores Each microservice fetches its configuration at startup (and optionally at runtime).


###


###


### 2. Externalized Configuration
- Configuration is outside the application code
- Same artifact can be deployed across environments
- Environment differences are handled via config, not code


###


###


### 3. Environment & Profile Management Supports:
- Multiple environments: dev, qa, prod
- Spring profiles: application-dev.yml, order-service-prod.yml Config is resolved based on:
- Application name
- Active profile
- Label (Git branch/tag)


###


###


### 4. Dynamic Configuration Refresh With:
- /actuator/refresh
- Spring Cloud Bus (Kafka/RabbitMQ) You can:
- Update configuration
- Refresh beans without restarting services Used for:
- Feature flags
- Timeout tuning
- Rate limits
- Toggle integrations


###


###


### 5. Version Control & Auditability When backed by Git:
- Configuration is versioned
- Full audit history
- Rollback supported
- Change tracking across environments Very important for regulated systems.


###


###


### 6. Secure Configuration Management
- Sensitive properties (passwords, tokens) are:
  - Encrypted
  - Or fetched from secure stores (Vault, cloud key vaults)
- Encryption/decryption handled by Config Server


###


###


### 7. Consistency Across Services
- All services get configuration in a consistent format
- Prevents config mismatch between instances
- Reduces human error How Config Server fits in the architecture
- Config Server starts first
- Microservices bootstrap from Config Server
- Config Server itself is usually:
  - Highly available
  - Cached on client side
  - Secured Config Server vs application.yml (Interview Comparison) Aspect application.yml Config Server Scope Single service All services Central management No Yes Versioning Limited Full 

Runtime refresh No Yes Microservices fit Poor Excellent

**When NOT to** use Config Server
- Small monolith
- Very few services
- Static configuration
- When cloud-native config services fully replace it

**One-Line Interview** Answer Spring Cloud Config Server provides centralized, externalized, and version-controlled configuration for microservices, enabling environment-specific configuration, dynamic refresh, and consistency without rebuilding applications.

---


## Monitoring Microservices in Production

Monitoring Microservices in Production Monitoring microservices in production is about observability, not just uptime. I focus on metrics, logs, and traces, combined with alerting and dashboards, to ensure reliability, performance, and fast incident resolution.

**Core Monitoring** Pillars (Must Mention in Interview)


###


###


### 1. Metrics (What is happening?) Quantitative measurements of system behavior. Examples
- Request rate (RPS)
- Latency (P95, P99)
- Error rate (4xx, 5xx)
- CPU, memory, JVM heap
- Thread pools, connection pools Why
- Detect performance degradation
- Capacity planning
- SLA/SLO monitoring


###


###


### 2. Logs (Why did it happen?) Detailed, timestamped records of events.

**Best practice**s
- Structured logging (JSON)
- Correlation using traceId
- Centralized log aggregation
- No local-only logs in production Logs are used for root cause analysis, not alerting.


###


###


### 3. Distributed Tracing (Where did it happen?) Tracks a request across multiple services. What it provides
- End-to-end latency
- Service dependency visibility
- Identification of bottlenecks
- Debugging async and event-driven flows Tracing is critical for microservices, where one request touches many services.

**Tooling Stack** (Typical Production Setup) Metrics
- Prometheus – metrics collection
- Grafana – dashboards & visualization Logs
- Centralized logging stack (ELK / cloud logging)
- Log correlation via traceId Tracing
- OpenTelemetry – instrumentation
- Zipkin or Jaeger – trace backend Application-Level Monitoring

**Health Checks**
- Liveness: is the service running?
- Readiness: can it accept traffic? Used by orchestrators and load balancers.

**JVM & Spring** Boot Metrics
- Heap usage
- GC pauses
- Thread counts
- HTTP request stats
- DB connection pool usage These expose early warning signs before failures occur.

**Alerting Strategy** (Very Important) I avoid alerting on raw metrics. Alert on symptoms, not noise
- High error rate
- Sustained latency breach
- Availability drop
- Message backlog growth Avoid
- Alerting on CPU spikes alone
- Alert storms Alerts should be:
- Actionable
- Threshold-based with time windows
- Routed to the right team

**One-Line Interview** Answer I monitor microservices in production using metrics, centralized logs, and distributed tracing to achieve full observability. Metrics detect issues, tracing shows request flow and latency, and logs enable root cause analysis, all supported by actionable alerts and SLO-driven monitoring.

---

# 📂 JPA and Hibernate


## Difference between JPA and Hibernate

Difference between JPA and Hibernate Short answer first (what interviewers like): JPA is a specification; Hibernate is an implementation of that specification (and more). What is JPA? Java Persistence API (JPA) is a Java specification that defines how Java objects are mapped to relational database tables and how persistence should be handled. Key points:
- Part of Java EE / Jakarta EE
- Defines interfaces and annotations
- Does not provide implementation
- Ensures vendor independence

**Examples:**
- @Entity, @Table
- EntityManager
- JPQL JPA answers “what” persistence should look like, not “how” it is implemented. What is Hibernate? Hibernate ORM is a full-fledged ORM framework and a popular JPA implementation. Key points:
- Implements JPA interfaces
- Provides many extra features beyond JPA
- Can be used:
  - Via JPA (recommended in Spring Boot)
  - Directly using Hibernate APIs Hibernate answers “how persistence actually works”. 

Core Differences (Most Important Table) Aspect JPA Hibernate Type Specification Implementation Provided by Java/Jakarta EE Red Hat Vendor lock-in No Yes (if using Hibernate APIs) APIs Standard JPA + proprietary Portability High Lower Learning curve Easier Deeper Spring Boot default Yes (via Hibernate) Yes APIs Comparison JPA APIs
- EntityManager
- EntityTransaction
- JPQL Hibernate APIs (Extra)
- Session
- SessionFactory
- HQL
- Criteria API (advanced)
- Second-level cache
- Custom generators

**Interview tip:** Using Hibernate-specific APIs reduces portability. Features Hibernate Provides Beyond JPA Hibernate adds capabilities not defined by JPA, such as:
- Advanced caching (2nd-level cache)
- Custom ID generators
- Better batch processing control
- Filters and interceptors
- More flexible fetching strategies
- Multi-tenancy support This is why Hibernate is widely used even though JPA exists. How Spring Boot Uses Them (Very Important) In Spring Boot:
- You code against JPA
- Spring injects EntityManager
- Hibernate runs underneath as the provider This gives:
- Clean abstraction
- Ability to switch providers if needed
- Less vendor coupling

**Best practice**: “Use JPA APIs, fall back to Hibernate only when required.” JPQL vs HQL
- JPQL → defined by JPA, portable
- HQL → Hibernate-specific, more powerful Most JPQL queries run unchanged in Hibernate because Hibernate supports JPQL.

**Common Interview** Trap Questions Q: Can we use JPA without Hibernate? Yes. Other implementations exist (EclipseLink, OpenJPA). Q: Is Hibernate mandatory for JPA? No. Hibernate is just one implementation. Q: Should we avoid Hibernate-specific features? Prefer JPA first; use Hibernate-specific features only when they solve real problems. When I Choose Each
- JPA
  - Standard CRUD
  - Business applications
  - Long-term maintainability
  - Framework neutrality
- Hibernate-specific
  -

**Performance** tuning
  - Advanced caching
  - Legacy DB quirks
  - High-volume batch jobs

**One-Line Interview** Answer JPA is a standard specification that defines ORM behavior, while Hibernate is a concrete ORM framework that implements JPA and provides additional advanced features. In Spring Boot, I code against JPA and use Hibernate as the provider.

---


##

---


## Role of Config Server in Spring Cloud

Role of Config Server in Spring Cloud](#role-of-config-server-in-spring-cloud)
70. [

---


## Monitoring Microservices in Production

Monitoring Microservices in Production](#monitoring-microservices-in-production)


### JPA and Hibernate

71. [

---

# 📂 JPA and Hibernate


## Difference between JPA and Hibernate

Difference between JPA and Hibernate](#difference-between-jpa-and-hibernate)
72. [What is an Entity?](#what-is-an-entity)
73. [

---

##

---

## Role of Config Server in Spring Cloud

Role of Config Server in Spring Cloud](#role-of-config-server-in-spring-cloud)
70. [

---

## Monitoring Microservices in Production

Monitoring Microservices in Production](#monitoring-microservices-in-production)


### JPA and Hibernate

71. [

---

# 📂 JPA and Hibernate

## Difference between JPA and Hibernate

Difference between JPA and Hibernate](#difference-between-jpa-and-hibernate)
72. [What is an Entity?](#what-is-an-entity)
73. [

---

## What is an Entity?

What is an Entity?

What is an Entity?

What is an Entity? 

An Entity is a lightweight, persistent domain object that represents a table in a relational database. Each instance of an entity corresponds to one row in that table. In JPA, an entity is a POJO managed by the persistence context. Formal

**Definition** (Interview Style) An entity is a JPA-managed object that has a persistent identity and is mapped to a database table, with its lifecycle controlled by the persistence context.

**Key

**Characteristics**** of an Entity


###


###


### 1. Persistent Identity
- Each entity has a primary key
- Identity remains the same across persistence operations
- Defined using @Id This is what differentiates an entity from a simple DTO.


###


###


### 2. Managed

**Lifecycle** An entity can be in different states:
- Transient – new, not associated with persistence context
- Managed (Persistent) – tracked by JPA
- Detached – no longer tracked
- Removed – scheduled for deletion JPA automatically tracks changes to managed entities (dirty checking).


###


###


### 3. POJO-Based
- No need to extend framework classes
- No dependency on Hibernate/JPA APIs in business logic
- Enables clean domain modeling


###


###


### 4. Mapped to Database Structure
- Table mapping via @Table
- Column mapping via @Column
- Relationships via @OneToMany, @ManyToOne, etc. Minimal Example @Entity @Table(name = "orders") public class Order { @Id @GeneratedValue private Long id; private String status; } Entity vs DTO (Very

**Common Interview** Question) Aspect Entity DTO

**Purpose** Persistence Data transfer Managed by JPA Yes No 

Has identity Yes No

**Lifecycle** Managed Plain object Used in API layer Should be avoided Recommended

**Best practice**: Do not expose entities directly from REST APIs. Important Rules for Entities


###


###


### 1. Must have a no-arg constructor (public or protected)


###


###


### 2. Must not be final


###


###


### 3. Fields or getters must be accessible


###


###


### 4. Equals & hashCode should be based on business key or identifier


###


###


### 5. Avoid heavy logic inside entities

**Common Pitfalls** (Senior-Level Insight)
- Using entities as API models
- Incorrect equals() / hashCode() implementation
- Eager fetching everywhere
- Treating entities like simple data holders Entity vs Table (Conceptual Difference)
- Entity → Object-oriented view
- Table → Relational view ORM bridges this object–relational impedance mismatch.

**One-Line Interview** Answer 

An entity is a JPA-managed domain object that represents a database table and has a persistent identity, with its lifecycle and state managed by the persistence context.

---


## Lazy vs Eager Loading

Lazy vs Eager Loading Lazy and Eager loading define when related entities are fetched from the database. The choice directly impacts performance, memory usage, and production stability. Lazy Loading

**Definition** Related data is not loaded immediately. It is fetched only when accessed. Default behavior
- @ManyToOne → EAGER (JPA default, often overridden)
- @OneToMany, @ManyToMany → LAZY

**How it works**
- Hibernate creates a proxy
- Actual SQL is executed when the relationship getter is accessed Example @OneToMany(fetch = FetchType.LAZY) private List<OrderItem> items;

**Pros**
- Better performance
- Lower memory usage
- Faster initial queries
- Scales well in microservices 

Cons
- Can cause LazyInitializationException if accessed outside transaction
- Requires awareness of transaction boundaries Eager Loading

**Definition** Related data is loaded immediately along with the parent entity.

**How it works**
- Hibernate fetches associations via:
  - JOIN
  - Or multiple SQL queries Example @ManyToOne(fetch = FetchType.EAGER) private Customer customer;

**Pros**
- Simple to use
- No lazy loading exceptions
- Good for small, fixed object graphs

**Cons**
-

**Performance** issues
- Over-fetching data
- N+1 query problems
- Hard to control at runtime Key Comparison (Interview Table) Aspect Lazy Loading Eager Loading 

Fetch timing On access Immediately Default for collections Yes No

**Performance** Better Risky Memory usage Low Higher Flexibility High Low Production safety High (when used correctly) Dangerous if misused LazyInitializationException (Very Important) Occurs when:
- Entity is loaded
- Persistence context is closed
- Lazy property is accessed later Example could not initialize proxy - no Session

**How I handle** it
- Fetch data inside service layer
- Use fetch joins
- DTO projections
- Never enable Open Session In View blindly 

How I Control Fetching (Best Practices)


###


###


### 1. Prefer LAZY by default Even override defaults where necessary.


###


###


### 2. Use Fetch Joins explicitly SELECT o FROM Order o JOIN FETCH o.items WHERE o.id = :id


###


###


### 3. Use DTO projections Avoid loading full entity graphs when not needed.


###


###


### 4. Batch fetching Reduces N+1 problem without eager loading. Lazy vs Eager vs Fetch Join (Important Insight)
- LAZY → when data is fetched
- EAGER → always fetch
- FETCH JOIN → fetch when needed, explicitly

**Senior rule** Lazy by default, eager by query, never eager by mapping.

**Common Interview** Trap Questions Q: Is eager loading bad? No, but dangerous if used globally. Q: Can lazy loading cause performance issues? Yes, if misused (N+1 problem). 

Q: Should OpenSessionInView be enabled? No by default. It hides design problems.

**One-Line Interview** Answer Lazy loading fetches related data only when accessed, while eager loading fetches it immediately. In production systems, I prefer lazy loading by default and explicitly control fetching using fetch joins or projections to avoid performance issues.

---


## What is the N+1 Problem?

What is the N+1 Problem? The N+1 problem is a performance issue in ORM frameworks where one initial query (1) triggers N additional queries, usually due to improper fetching of related entities. It typically occurs with lazy-loaded associations accessed inside a loop. Simple Explanation


###


###


### 1. One query fetches a list of parent entities


###


###


### 2. For each parent entity, another query is fired to fetch its related data


###


###


### 3. Total queries = 1 + N This leads to:
- Excessive database calls
- High latency
- Poor scalability Typical Example
- Fetch 100 orders
- Each order lazily loads customer or items
- Total queries = 1 (orders) + 100 (customers/items) 

 Why N+1 Happens
- Lazy loading used incorrectly
- Accessing relationships in loops
- Missing fetch strategy control
- ORM defaults hiding actual SQL behavior How to Identify N+1 in Production
- Sudden spike in DB queries
- High response time with low CPU usage
- Logs showing repetitive SELECT statements
- Traces showing DB time dominating request latency How I Solve the N+1 Problem (Interview-Critical)


###


###


### 1. Fetch Join (Preferred Solution) SELECT o FROM Order o JOIN FETCH o.items
- Loads parent and child in one query
- Most explicit and safest approach


###


###


### 2. DTO Projections SELECT new com.app.OrderDTO(o.id, c.name) FROM Order o JOIN o.customer c
- Fetch only required fields
- Avoids entity graph loading
- Best for read-heavy APIs


###


###


### 3. Batch Fetching hibernate.default_batch_fetch_size=50
- Groups lazy loads into batches
- Reduces N+1 to 1 + (N / batchSize)
- Useful when fetch join is not feasible


###


###


### 4. Entity Graphs
- Declarative way to define fetch plans
- Cleaner than hardcoding fetch joins everywhere
- Good for reuse What I Avoid (Important)
- Global EAGER fetching
- Enabling Open Session In View to “fix” lazy loading
- Fetching entire object graphs blindly These approaches hide the problem rather than solving it. N+1 vs Eager Fetching Trap Using EAGER fetch:
- May solve N+1
- But causes:
  - Over-fetching
  - Cartesian product explosion
  - Memory issues

**One-Line Interview** Answer 

The N+1 problem occurs when an ORM executes one query to fetch parent entities and then N additional queries to fetch related entities due to improper lazy loading, causing serious performance degradation.

---


## What is @Query annotation?

What is @Query annotation? The @Query annotation in Spring Data JPA is used to define custom database queries explicitly, instead of relying on derived query method names. It allows you to write JPQL or native SQL directly on repository methods. Why @Query is used Derived query methods:
- Become unreadable for complex logic
- Are limited for joins, projections, aggregations
- Hide performance issues @Query gives:
- Full control over the query
- Better readability for complex queries
- Predictable SQL behavior Basic

**Example (**JPQL) @Query("SELECT o FROM Order o WHERE o.status = :status") List<Order> findOrdersByStatus(@Param("status") String status); Key points:
- Uses entity name, not table name
- Uses entity fields, not column names
- Parsed and validated at startup Native Query Example @Query( value = "SELECT * FROM orders WHERE status = ?1", nativeQuery = true ) List<Order> findOrdersNative(String status); Use native queries when:
- Vendor-specific SQL is required
- Complex joins / hints
-

**Performance** tuning @Query vs Derived Query Methods Aspect Derived Queries @Query Readability Poor for complex queries Clear Control Limited Full

**Performance** tuning Hard Easy Compile-time safety Medium High (JPQL) 

Native SQL No Yes Named Parameters vs Positional Parameters Named (Recommended) @Query("SELECT o FROM Order o WHERE o.id = :id") Order findById(@Param("id") Long id); Positional @Query("SELECT o FROM Order o WHERE o.id = ?1") Order findById(Long id); Named parameters are:
- More readable
- Less error-prone @Modifying with @Query (Important Interview Point) Used for UPDATE / DELETE queries. @Modifying @Query("UPDATE Order o SET o.status = :status WHERE o.id = :id") int updateStatus(@Param("id") Long id, @Param("status") String status); Must be:
- Inside a transaction
- Used carefully (bypasses dirty checking) Projections with @Query @Query("SELECT new com.app.OrderDTO(o.id, o.status) FROM Order o") List<OrderDTO> fetchOrderSummary(); Helps:
- Avoid N+1 problem
- Reduce memory usage
- Improve performance

**Common Pitfalls**
- Using table names in JPQL
- Forgetting @Modifying for update/delete
- Mixing entity fields and DB column names
- Overusing native queries When I Prefer @Query
- Complex joins
- Fetch joins
- Aggregations
- Reporting queries
-

**Performance**-critical paths

**One-Line Interview** Answer @Query is a Spring Data JPA annotation used to define custom JPQL or native SQL queries on repository methods, providing full control over query behavior beyond derived method naming.

---


## Difference between JPQL and Native Query

Difference between JPQL and Native Query Short answer (what interviewers want): JPQL is object-oriented and database-agnostic, while Native Query is database-specific SQL executed directly on tables. JPQL (Java Persistence Query Language) JPQL is a JPA-defined, object-oriented query language that operates on entities and their relationships, not directly on database tables.

**Key

**Characteristics****
- Uses entity names and fields
- Database-independent
- Converted to SQL by JPA provider (Hibernate)
- Validated at startup
- Works with entity relationships and inheritance Example @Query("SELECT o FROM Order o WHERE o.status = :status") List<Order> findByStatus(String status);

**When I use** JPQL
- Standard CRUD and joins
- Fetch joins
- Portable applications
- Long-term maintainability Native Query Native Query uses database-specific SQL and operates directly on tables and columns. 

Key

**Characteristics**
- Uses table and column names
- Database-dependent
- Full SQL power
- Not fully validated at startup
- Tied to vendor features Example @Query( value = "SELECT * FROM orders WHERE status = ?1", nativeQuery = true ) List<Order> findByStatusNative(String status);

**When I use** Native Queries
- Vendor-specific SQL
- Complex reporting queries
-

**Performance** tuning
- Legacy schemas
- Database hints and optimizations Side-by-Side Comparison (Very Important) Aspect JPQL Native Query Defined by JPA Database Query target Entity model Tables 

Portability High Low Validation Startup-time Runtime Object relationships Yes Manual Vendor lock-in No Yes

**Performance** tuning Limited Full Fetch joins Yes Manual

**Performance** Perspective (Senior Insight)
- JPQL performance is usually good enough
- Hibernate generates optimized SQL
- Native queries give fine-grained control
- Overuse of native SQL increases maintenance cost

**Rule I follow**: JPQL first, native query only when there is a clear need.

**Mapping Results** in Native Queries
- Can map to:
  - Entities
  - DTOs
  - Scalar values
- Requires careful column aliasing
- More error-prone than JPQL 

Common Interview Trap Questions Q: Is native query always faster? No.

**Performance** depends on the generated SQL and indexes. Q: Can JPQL use DB-specific functions? Limited support. Native query is better for that. Q: Which one should be preferred in Spring Boot? JPQL, unless native SQL is required.

**One-Line Interview** Answer JPQL is a JPA-standard, object-oriented query language that works on entities and is database-independent, whereas native queries use database-specific SQL on tables, offering more control at the cost of portability.

---


## What is Cascade Type?

What is Cascade Type? Cascade type defines how persistence operations performed on a parent entity are automatically propagated to its related child entities. In simple terms: Cascade controls whether actions like save, update, or delete on a parent should also apply to its associations. Why Cascade is needed In object-oriented design:
- Objects have relationships
- Operations on a parent often imply operations on children Without cascade:
- You must manually save/update/delete related entities
- Code becomes error-prone and verbose 

Cascade provides controlled automation, not magic.

**Where Cascade** is used Cascade is applied on entity relationships, such as:
- @OneToMany
- @ManyToOne
- @OneToOne
- @ManyToMany

**Example:** @OneToMany(cascade = CascadeType.ALL) private List<OrderItem> items;

**Types of** Cascade (Very Important)


###


###


### 1. CascadeType.PERSIST
- Propagates persist (save) operation
- Saving parent automatically saves children cascade = CascadeType.PERSIST

**Use case**:
- New parent with new child entities


###


###


### 2. CascadeType.MERGE
- Propagates merge (update) operation
- Updating parent updates children cascade = CascadeType.MERGE 

 Use case:
- Updating detached entities with associations


###


###


### 3. CascadeType.REMOVE
- Propagates delete operation
- Deleting parent deletes children cascade = CascadeType.REMOVE Dangerous if misused

**Use case**:
- Strong ownership relationship (e.g., Order → OrderItems)


###


###


### 4. CascadeType.REFRESH
- Refreshing parent refreshes children from DB
- Rarely used in real systems


###


###


### 5. CascadeType.DETACH
- Detaching parent detaches children from persistence context
- Rarely used


###


###


### 6. CascadeType.ALL
- Shortcut for:
  - PERSIST
  - MERGE
  - REMOVE
  - REFRESH
  - DETACH cascade = CascadeType.ALL Cascade vs Orphan Removal (Very Common Confusion) cascade = REMOVE
- Deletes children when parent is deleted orphanRemoval = true
- Deletes child when removed from parent collection @OneToMany( mappedBy = "order", cascade = CascadeType.ALL, orphanRemoval = true ) private List<OrderItem> items; Interview insight
- Cascade controls operation propagation
- Orphan removal controls collection ownership Cascade is NOT Database Cascade Important clarification:
- JPA cascade → ORM-level
- DB cascade (ON DELETE CASCADE) → database-level They are independent and should not be mixed blindly. 

 When I Use Cascade (Senior Answer) I use cascade only when:
- Parent owns the lifecycle of child
- Child does not exist independently
- Business rules clearly define ownership

**Examples:**
- Order → OrderItem (Yes)
- User → Address (Maybe)
- Order → Customer (No)

**Common Mistakes** (Interview Gold)
- Using CascadeType.ALL everywhere
- Cascading REMOVE on @ManyToOne
- Confusing cascade with fetch type
- Expecting cascade to solve N+1 issues (it does not)

**One-Line Interview** Answer Cascade type defines how persistence operations on a parent entity are automatically propagated to its associated entities, such as persist, merge, or remove.

---


## What is Dirty Checking in Hibernate?

What is Dirty Checking in Hibernate and How Does It Work Internally? Dirty checking is a core Hibernate mechanism that automatically detects changes made to managed entities and synchronizes those changes with the database at flush/commit time—without requiring explicit update calls. 

 One-Line Interview Answer Dirty checking is Hibernate’s mechanism that tracks changes in managed entities and automatically generates SQL UPDATE statements during flush or transaction commit.

**Why Dirty** Checking Exists Without dirty checking, developers would need to:
- Explicitly call update() for every field change
- Manually track modified attributes
- Write error-prone persistence logic Dirty checking allows natural object-oriented programming: order.setStatus("CONFIRMED"); // No update() call Hibernate figures out what changed, when, and how.

**Preconditions** for Dirty Checking Dirty checking works only when:


###


###


### 1. Entity is in managed (persistent) state


###


###


### 2. Entity is associated with an active persistence context


###


###


### 3. Changes occur inside a transaction It does not work for:
- Detached entities
- DTOs
- Native SQL updates (outside Hibernate) Internal Working of Dirty Checking (Step by Step)


###


###


### 1. Entity is Loaded → Snapshot Created When Hibernate loads an entity:
- It stores the entity in the Persistence Context (First-Level Cache)
- It also stores a snapshot of the entity’s state (original values)

**Internally:**
- Snapshot = array/map of property values
- Stored in Hibernate’s internal EntityEntry


###


###


### 2. Application Modifies the Entity order.setStatus("SHIPPED"); At this point:
- Hibernate does nothing immediately
- No SQL is executed
- Entity is simply modified in memory


###


###


### 3. Flush is Triggered Flush happens when:
- Transaction commits
- JPQL/Criteria query is executed
- Explicit flush() is called Flush is not commit—it’s synchronization.


###


###


### 4. Dirty Checking Algorithm Runs Hibernate:


###


###


### 1. Iterates over managed entities


###


###


### 2. Compares:
  - Current entity state
  - Stored snapshot


###


###


### 3. Determines:
  - Which fields changed
  - Whether an UPDATE is required This comparison is field-by-field, not object-by-object.


###


###


### 5. SQL UPDATE is Generated (Only If Needed) If differences are found:
- Hibernate generates an UPDATE statement
- Only dirty columns are included (by default)

**Example:** UPDATE orders SET status = ? WHERE id = ? If nothing changed:
- No SQL is executed Important Internal Optimizations

**Dynamic Update** Hibernate can generate UPDATE SQL with only modified columns: @DynamicUpdate Trade-off:
- Smaller SQL
- Slight runtime overhead for SQL generation

**Bytecode Enhancement** (Advanced) 

With bytecode enhancement:
- Hibernate tracks changes at field-write time
- Avoids snapshot comparison
- Improves performance for large entities Used in:
- High-throughput systems
- Large domain models Dirty Checking vs Explicit Update Aspect Dirty Checking Explicit Update Developer effort Low High Error risk Low High

**Performance** Optimized Depends ORM friendly Yes No Recommended Yes No When Dirty Checking Does NOT Happen Very important interview traps:


###


###


### 1. Detached Entity entityManager.clear(); order.setStatus("CANCELLED"); // No update


###


###


### 2. Read-Only Transaction @Transactional(readOnly = true)


###


###


### 3. Native Queries
- Hibernate is bypassed


###


###


### 4. StatelessSession
- No persistence context
- No dirty checking

**Performance** Considerations (Senior Insight) Dirty checking can become expensive when:
- Persistence context contains thousands of entities
- Large object graphs are loaded
- Unnecessary entities are kept managed

**How I control** it:
- Clear persistence context when needed
- Use projections for read use cases
- Avoid long-running transactions
- Use batching and pagination Dirty Checking vs Flush vs Commit (Very Common Confusion)
- Dirty checking → Detects changes
- Flush → Executes SQL
- Commit → Finalizes transaction Flush can happen multiple times before commit. Relation to Hibernate
- Implemented internally by Hibernate ORM
- Core reason Hibernate feels “automatic”
- One of the biggest advantages over JDBC

**Final Interview**-Grade Summary Hibernate dirty checking works by keeping a snapshot of each managed entity when it is loaded. During flush, Hibernate compares the current state with the snapshot, detects changed fields, and generates SQL UPDATE statements automatically—without explicit update calls.

---


## Hibernate Session, Persistence Context, and First-Level Cache

Hibernate Session, Persistence Context, and First-Level Cache These three terms are closely related and often confused. The key is to understand scope, responsibility, and lifecycle.


###


###


### 1. Hibernate Session A Hibernate Session is the primary interface between the application and Hibernate. It represents a single unit of work with the database. Key responsibilities
- Create, read, update, delete entities
- Manage entity lifecycle states (transient, managed, detached, removed)
- Hold the persistence context
- Trigger dirty checking and flushing Important characteristics
- Not thread-safe
- Typically one session per transaction
- Short-lived In JPA terms:
- Session ≈ EntityManager Hibernate is provided by Hibernate ORM.


###


###


### 2. Persistence Context The Persistence Context is a logical container that tracks all managed entities within a session. Think of it as: “Hibernate’s working memory for entities”

**What it does**
- Tracks entity state changes
- Stores entity snapshots (for dirty checking)
- Ensures entity identity guarantee
- Decides what SQL needs to be executed on flush Critical rule Within one persistence context, only one object instance per database row exists.

**Example:** Order o1 = em.find(Order.class, 1L); Order o2 = em.find(Order.class, 1L); // o1 == o2 → true

**Lifecycle**
- Created when Session / EntityManager starts
- Destroyed when Session / EntityManager closes


###


###


### 3. First-Level Cache The First-Level Cache is the physical implementation of the persistence context. 

Important clarification: Persistence Context = concept First-Level Cache = implementation

**Characteristics**
- Enabled by default
- Scoped to one Session
- Cannot be disabled
- Stores managed entities keyed by primary key

**How They Work** Together (Flow)


###


###


### 1. Session starts


###


###


### 2. Persistence context is created


###


###


### 3. First-level cache is initialized


###


###


### 4. Entity is loaded:
  - DB hit (first time)
  - Stored in first-level cache


###


###


### 5. Subsequent fetch:
  - Returned from cache
  - No DB query


###


###


### 6. On flush:
  - Dirty checking runs
  - SQL is generated if needed


###


###


### 7. Session closes:
  - Persistence context destroyed
  - Cache cleared Example Behavior (Interview Favorite) @Transactional public void demo() { Order o1 = em.find(Order.class, 1L); // DB hit Order o2 = em.find(Order.class, 1L); // No DB hit } 

Why?
- Both calls hit the same persistence context
- Entity already exists in first-level cache Session vs Persistence Context vs First-Level Cache Aspect Session Persistence Context First-Level Cache Type API / Interface Logical concept Physical storage

**Purpose** DB interaction Entity state tracking Cache of entities Scope Per unit of work Per session Per session Identity guarantee Indirect Yes Yes Can be disabled No No No

**Common Interview** Traps “Is first-level cache same as second-level cache?” No.
- First-level → per session
- Second-level → shared across sessions “Does first-level cache improve performance?” 

Yes, but:
- Only within the same session
- Not a replacement for second-level cache “What happens on clear()?”
- Persistence context is cleared
- First-level cache emptied
- Entities become detached “Does JPQL bypass first-level cache?” No.
- JPQL queries check the persistence context first
- But may still execute SQL depending on query semantics

**Why This Matters** in Production
- Prevents duplicate objects
- Enables dirty checking
- Reduces unnecessary DB calls
- Can cause memory issues if session is too long-lived Senior best practice
- Keep transactions short
- Avoid loading large object graphs unnecessarily
- Use projections for read-only use cases

**One-Line Interview** Answer Hibernate Session is the unit-of-work API, the Persistence Context is the logical container that tracks managed entities, and the First-Level Cache is the internal cache implementation that stores those entities per session.

---

# 📂 Design Principles


## SOLID Principles

---


## Lazy vs Eager Loading

Lazy vs Eager Loading](#lazy-vs-eager-loading)
74. [

---


## What is the N+1 Problem?

What is the N+1 Problem?](#what-is-the-n1-problem)
75. [

---


## What is @Query annotation?

What is @Query annotation?](#what-is-query-annotation)
76. [

---


## Difference between JPQL and Native Query

Difference between JPQL and Native Query](#difference-between-jpql-and-native-query)
77. [

---


## What is Cascade Type?

What is Cascade Type?](#what-is-cascade-type)
78. [

---


## What is Dirty Checking in Hibernate?

What is Dirty Checking in Hibernate?](#what-is-dirty-checking-in-hibernate)
79. [

---


## Hibernate Session, Persistence Context, and First-Level Cache

Hibernate Session, Persistence Context, and First-Level Cache](#hibernate-session-persistence-context-and-first-level-cache)


### Design Principles

80. [SOLID Principles](#solid-principles)

---


# 📂 Core Java Fundamentals


## What is the difference between JDK, JRE, and JVM?

---

# 📂 Design Principles


## SOLID Principles

---

## Lazy vs Eager Loading

Lazy vs Eager Loading](#lazy-vs-eager-loading)
74. [

---

## What is the N+1 Problem?

What is the N+1 Problem?](#what-is-the-n1-problem)
75. [

---

## What is @Query annotation?

What is @Query annotation?](#what-is-query-annotation)
76. [

---

## Difference between JPQL and Native Query

Difference between JPQL and Native Query](#difference-between-jpql-and-native-query)
77. [

---

## What is Cascade Type?

What is Cascade Type?](#what-is-cascade-type)
78. [

---

## What is Dirty Checking in Hibernate?

What is Dirty Checking in Hibernate?](#what-is-dirty-checking-in-hibernate)
79. [

---

## Hibernate Session, Persistence Context, and First-Level Cache

Hibernate Session, Persistence Context, and First-Level Cache](#hibernate-session-persistence-context-and-first-level-cache)


### Design Principles

80. [SOLID Principles](#solid-principles)

---


# 📂 Core Java Fundamentals


## What is the difference between JDK, JRE, and JVM?

---

# 📂 Design Principles

## SOLID Principles

SOLID Principles SOLID is a set of five object-oriented design principles that help build maintainable, extensible, testable, and loosely coupled systems. I use them as design guidelines, not rigid rules.


###


###


### 1. Single Responsibility Principle (SRP)

**Definition** A class should have only one reason to change.

**How I apply it**
- Separate business logic from:
  - Validation
  - Persistence
  - Communication
- Small, focused classes 

Real example
- OrderService → orchestration only
- OrderValidator → validation
- OrderRepository → persistence

**Why it matters**
- Easier testing
- Safer changes
- Better readability

**Interview signal**
- SRP is about change reasons, not “one method per class”.


###


###


### 2. Open/Closed Principle (OCP)

**Definition** Software entities should be open for extension, closed for modification.

**How I apply it**
- Interfaces + polymorphism
- Strategy pattern
- Configuration-driven behavior Real example
- Adding a new payment method without changing existing code

**Why it matters**
- Avoids regression
- Enables feature growth
- Reduces risk in production


###


###


### 3. Liskov Substitution Principle (LSP)

**Definition** Subtypes must be substitutable for their base types without breaking behavior.

**How I apply it**
- Child classes must honor:
  - Contracts
  - Expected behavior
  - Exception semantics Bad sign
- Overriding methods and throwing unexpected exceptions
- Weakening preconditions

**Why it matters**
- Polymorphism safety
- Prevents runtime surprises


###


###


### 4. Interface Segregation Principle (ISP)

**Definition** Clients should not be forced to depend on interfaces they do not use.

**How I apply it**
- Small, focused interfaces
- Role-based interfaces Real example
- ReadableOrder
- WritableOrder instead of one large OrderService

**Why it matters**
- Cleaner APIs
- Less impact from changes
- Better testability


###


###


### 5. Dependency Inversion Principle (DIP)

**Definition** High-level modules should not depend on low-level modules. Both should depend on abstractions. 

How I apply it
- Constructor injection
- Interfaces over implementations
- Framework manages wiring Spring relevance
- Core principle behind:
  - Dependency Injection
  - Testability
  - Loose coupling

**Why it matters**
- Easier mocking
- Replace implementations safely
- Framework independence How SOLID Works Together (Important Insight)
- SRP keeps classes small
- OCP + LSP enable safe extension
- ISP avoids fat contracts
- DIP removes hard dependencies Together they:
- Reduce coupling
- Increase cohesion
- Improve long-term maintainability

**One-Line Interview** Answer SOLID principles are design guidelines that help create loosely coupled, extensible, and maintainable object-oriented systems. I apply them pragmatically to reduce change impact, improve testability, and avoid rigid designs.

---


> **Document Version:** 1.0 — **Last Updated:** June 2026
>
> **Prepared for:** Java Backend Developer —

**Senior Level** Interview Preparation

---


> **Document Version:** 1.0 — **Last Updated:** June 2026
>
> **Prepared for:** Java Backend Developer —

**Senior Level** Interview Preparation

---


> **Document Version:** 1.0 — **Last Updated:** June 2026
>
> **Prepared for:** Java Backend Developer — Senior Level Interview Preparation