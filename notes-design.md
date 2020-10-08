# Designing, programming, testing, writing & other useful topics

> [Ashwin Jayaprakash](https://ashwinjay.github.io/)

> [CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/)

# Table of Contents
* [Product development lifecycle](#product-development-lifecycle)
* [Design mnemonics](#design-mnemonics---fdscarss)
* [Programming basics (mostly for Java)](#programming-basics-mostly-for-java)
* [Design basics](#design-basics)
* [Documentation and commit messages](#documentation-and-commit-messages)
* [Testing and code review](#testing-and-code-review)
* [Debugging and problem solving](#debugging-and-problem-solving)
* [APIs](#apis)
* [Computer fundamentals](#computer-fundamentals)
* [Concurrency](#concurrency)
* [Distributed systems](#distributed-systems)
* [Misc tech](#misc-tech)
* [Common sense coding preferences (mostly for Java)](#common-sense-coding-preferences-mostly-for-java)
  * [JVM](#jvm)
  * [Code generation](#code-generation)
     * [Lombok](#lombok)
     * [Misc Java](#misc-java)
  * [Dependency Injection](#dependency-injection)
     * [Guice](#guice)
     * [Lifecycle](#lifecycle)
  * [Style](#style)
     * [Visibility](#visibility)
     * [Member variables](#member-variables)
     * [Exceptions](#exceptions)
     * [Formatting](#formatting)
     * [Ordering of methods](#ordering-of-methods)
     * [Thread safety](#thread-safety)
     * [Naming](#naming)
     * [Constants](#constants)
     * [(Java)Docs, comments and logs](#javadocs-comments-and-logs)
  * [Non-Java files and resources](#non-java-files-and-resources)
  * [Unit tests](#unit-tests)

(TOC created by [gh-md-toc](https://github.com/ekalinin/github-markdown-toc))

# Product development lifecycle

(Keep in mind that the stages are iterative with feedback loops)

- Discovery
  - Scope
    - Goals
    - Non-goals
  - Assumptions
  - Risks
- Definition and planning
  - Resources
  - Dependencies
  - Roles and responsibilities ([RACI matrix](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix))
- Execution
  - Design and implementation
  - See design mnemonics
  - Follow up
    - Documentation
    - Training, troubleshooting and runbook
    - Operations
    - Support
    - Maintenance
- Sign-off
  - Feature completeness and acceptance
  - Proof of design and code quality
  - Proof of test quality (coverage, fuzz)
- Messaging
  - Marketing
  - Notifications

# Design mnemonics - "FDSCARSS"

(Also see [12 Factor](https://12factor.net/))

* **F**unctional requirements
  * Structure 
    * Goals and non-goals
    * Assumptions, tradeoffs and risks
    * Constraints (Skills, technology, cost, time, regulations)
    * Success measures (KPIs)
  * Fast, Inexpensive, Restrained, and Elegant (Dan Ward)
    * Necessary and sufficient
    * Usable, delightful and relevant (Minimal lovable and viable product)
    * Plan to deliver incremental value
* **D**ata and everything related
  * Core business logic (Algorithms and data structures)
  * Metadata
  * Data
  * Configurations
  * Code
  * Namespace and tenancy
  * Governance
    * Visibility and privacy
    * Residence and lifetime
    * Quality and lineage
* **S**ecurity (Shift left)
  * Authentication and authorization
  * Audit of code, roles, policies, infrastructure and logs
  * Secure and least privilege, by default
  * Minimize attack surface and impact
  * Update of security algorithms and software versions
  * Rotation of keys and certificates
* **C**ompatibility
  * Lifecycle (Install, update, troubleshoot, purge, uninstall)
  * Schemas, APIs & DTOs (Versions, contracts)
* **A**vailability, **R**eliability and **S**calability
  * Usage types, patterns and trends
    * Time of day, regions, growth, read-write ratios
    * Traffic shape, quality of service, back pressure, queue depth
    * CPU, network, disk limits
  * Concurrency and parallelism
    * Amdahl's law, Little's law, Universal scalability law  
    * Latency and throughput
  * ACID and CAP  
    * Caches, consistency
    * Routing, sharding, replication
  * Fault tolerance and recovery
    * Backup-restore, active-standby, active-active, hot-cold archive
  * Resilience
    * Graceful failure handling within and across failure domains
    * Ability to reason about system state inspite of failures
    * Ability to self-repair or recover in meaningful, but perhaps degraded modes
* **S**erviceability
  * Design with empathy - for user and the support/on-call person 
    * Clear and actionable status and error messages
    * Logs
    * Metrics
    * Healthchecks
    * Alerts
    * Documentation and runbooks
  * Testability
    * Unit tests
    * Fuzz tests
    * Property based tests
    * Component tests
    * Contract tests
    * Integration tests
    * Performance tests
    * Chaos tests
  * Reproducability
   * Environment
   * Trends and patterns (OS, network, disk)
  
# Programming basics (Mostly for Java)

* [How To Write Unmaintainable Code](https://www.doc.ic.ac.uk/~susan/475/unmain.html)
* Java coding standards (Oracle's guide has not been updated since 1999)
  * [Google style guide](https://google.github.io/styleguide/) 
  * [Sun's/Oracle's style guide is now stale](http://www.oracle.com/technetwork/java/index-135089.html)
  * [Secure coding](https://www.securecoding.cert.org/confluence/display/java/SEI+CERT+Oracle+Coding+Standard+for+Java) 
* [Effective Java by Joshua Bloch](https://www.google.com/search?q=Effective+Java+Book+by+Joshua+Bloch&ie=utf-8&oe=utf-8)
* [Clean Code by Robert Cecil Martin](https://www.google.com/search?q=Clean+Code+by+Robert+Cecil+Martin&ie=utf-8&oe=utf-8) ([Cheat sheet](https://www.bbv.ch/images/bbv/pdf/downloads/V2_Clean_Code_V3.pdf))
* [Java by Comparison - Become a Java Craftsman in 70 Examples by Simon Harrer, Jörg Lenhard, Linus Dietz](https://pragprog.com/book/javacomp/java-by-comparison)
* [Learn to use the IDE/IntelliJ well](http://blog.jetbrains.com/idea/tag/30-days-guide/)
* Follow the basic [Sun/Oracle/Google guidelines](https://github.com/kciter/awesome-style-guide#java)
* Use tools like Checkstyle/PMD/FindBugs/SpotBugs/ErrorProne/Infer to do the first level checks
* Use IntelliJ/Eclipse/IDE's formatting and fix compiler/IDE warnings

# Design basics

* [Best Practices for Designing and Implementing a Library in Java]( https://www.oracle.com/corporate/features/library-in-java-best-practices.html?evite=WWMK170414P00004)
* [SOLID design patterns](https://www.google.com/search?q=solid+design+patterns&ie=utf-8&oe=utf-8)
* [Summary of OCP, SRP etc](http://programmers.stackexchange.com/questions/162643/why-is-clean-code-suggesting-avoiding-protected-variables/162657#162657)
* [Venkat Subramaniam Design Patterns talks](https://www.youtube.com/results?search_query=venkat+subramaniam+design+patterns)
* [GRASP design patterns](https://www.google.com/search?q=grasp+design+patterns&ie=utf-8&oe=utf-8)
* [Domain-driven design by Eric J. Evans](https://www.google.com/search?q=eric+evan+sddd&ie=utf-8&oe=utf-8#q=Domain-driven+design+Book+by+Eric+J.+Evans)
* [Applying UML and patterns by Craig Larman](https://www.google.com/search?q=craig+larman&ie=utf-8&oe=utf-8#q=Applying+UML+and+patterns+Book+by+Craig+Larman)
* [Enterprise Integration Patterns by Gregor Hohpe](https://www.google.com/search?q=enterprise+integration+patterns&ie=utf-8&oe=utf-8)
* [Refactoring, patterns, anti-patterns](https://sourcemaking.com/)
* [Gang of Four Patterns in a Functional Light](https://www.youtube.com/watch?v=lZG74WbnhoE)
* [Programming Principles - slightly different from the ones above](http://webpro.github.io/programming-principles/)
* [Package by Feature](https://phauer.com/2020/package-by-feature/)
* [Microservice architecture](https://microservices.io)

# Documentation and commit messages

 - [US Government plain language guidelines](https://plainlanguage.gov/)
 - [Technical Writing Courses for Engineers](https://developers.google.com/tech-writing)
 - [Effective software design documents](https://wecode.wepay.com/posts/effective-software-design-documents) & [
A generic design document template for documenting Micro services](https://github.com/wepay/design_doc_template)
 - [Cassandra contribution guide](http://cassandra.apache.org/doc/latest/development/index.html) has a nice page on code review among other things
- [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
- [eclipse collections contributor guide](https://github.com/eclipse/eclipse-collections/blob/master/CONTRIBUTING.md#commit-messages)
- [Strimzi contributor guide](https://strimzi.io/contributing/guide/)
- [Google Developer Documentation Style Guide](https://developers.google.com/style/)
- [The Modular Documentation Project Source Repository](https://github.com/redhat-documentation/modular-docs)
- [The Art of Code Comments - Sarah Drasner](https://youtu.be/yhF7OmuIILc)
- [If Hemingway Wrote JavaDocs](https://www.youtube.com/watch?v=DEW_SRk6mCU)

# Testing and code review

- [Cassandra testing](https://github.com/apache/cassandra/blob/trunk/TESTING.md)
- [Clean coder cheat sheet](https://www.bbv.ch/images/bbv/pdf/downloads/V2_Clean_Code_V3.pdf)
- [Code review matters and manners](https://www.slideshare.net/trishagee/code-review-matters-and-manners) with [video](https://vimeo.com/182087729)
- [Building a code review culture](https://youtu.be/I0_N5MBYB5s)
- [Google Code Review Developer Guide](https://google.github.io/eng-practices/) 
- [Chromium Project - Respectful Code Reviews](https://chromium.googlesource.com/chromium/src/+/master/docs/cr_respect.md) 
- [Chromium Project - Respectful Changes](https://chromium.googlesource.com/chromium/src/+/master/docs/cl_respect.md)
 
# Debugging and problem solving
- [Situation, task, action, result](https://en.wikipedia.org/wiki/Situation,_task,_action,_result)
- [The Five W's (and H) approach](https://javaforu.blogspot.com/2011/06/five-ws-and-h-approach.html)

# APIs

* [10 Reasons Why we Love Some APIs and Why we Hate Some Others by Lukas Eder](https://youtu.be/CYniPcoiI5g)
* [Josh Bloch on API design](https://www.google.com/search?q=josh+block+api+talk&ie=utf-8&oe=utf-8#q=josh+bloch+api+talk)
* [Microsoft API guidelines](https://github.com/Microsoft/api-guidelines/blob/vNext/Guidelines.md)
* [Google API design](https://cloud.google.com/apis/design/) 
* [Kubernetes REST API conventions](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md)
* [Evolving Java-based APIs / Achieving API Binary Compatibility](https://wiki.eclipse.org/Evolving_Java-based_APIs_2)
* [REST API tutorial](https://restfulapi.net/)

# Computer fundamentals

* [Writing an OS in Rust](https://os.phil-opp.com/)
* [Writing a file system from scratch in Rust](https://blog.carlosgaldino.com/writing-a-file-system-from-scratch-in-rust.html)
* [What's in a Linux executable?](https://fasterthanli.me/blog/2020/whats-in-a-linux-executable/)
* [Wizard zines](https://wizardzines.com/)

# Concurrency

* [Brian Goetz on concurrency](https://www.google.com/search?q=brian+goetz+concurrency+talk&ie=utf-8&oe=utf-8#q=brian+goetz+concurrency+talk&tbm=vid)
* [Venkat Subramaniam concurrency talks](https://www.youtube.com/results?search_query=venkat+subramaniam+concurrency)
* [Concurrent programming in Java by Doug Lea](https://www.google.com/search?q=Concurrent+programming+in+Java+Book+by+Doug+Lea&ie=utf-8&oe=utf-8)
* [Roman Leventov's Code Review Checklist for Java Concurrency](https://github.com/code-review-checklists/java-concurrency)

# Distributed systems

* [An introduction to distributed systems](https://github.com/aphyr/distsys-class)
* [High Scalability](http://highscalability.com/all-time-favorites/)

# Misc tech

## Learning

* [Barbara Oakley: "Learning How to Learn"](https://www.youtube.com/watch?v=vd2dtkMINIw)
* [Reading Research: A Guide for Software Engineers](https://brooker.co.za/blog/2020/05/25/reading.html))
 
## "Awesome lists"

* ["Awesome" lists](https://www.google.com/search?q=awesome+lists)
* [A curated list of awesome Java frameworks, libraries and software](https://github.com/akullpp/awesome-java)

## Cloud
* [Jerry Hargrove - Cloud Diagrams & Notes](https://www.awsgeek.com/)
* [open-guides/og-aws: 📙 Amazon Web Services — a practical guide](https://github.com/open-guides/og-aws) 
* [Amazon Web Services In Plain English](https://expeditedsecurity.com/aws-in-plain-english/) 
* [Amazon Web Services (also in plain English)](https://adayinthelifeof.nl/2020/05/20/aws.html) 
* [AWS services explained in one line each](https://news.ycombinator.com/item?id=23309269)

# Common sense coding preferences (mostly for Java)

## JVM
 - [JVM bytecode](http://blog.jamesdbloom.com/JavaCodeToByteCode_PartOne.html)
 - [JVM internals](http://blog.jamesdbloom.com/JVMInternals.html)
 - [Aleksey Shipilёv's posts describing some elementary piece of knowledge about JVM](https://shipilev.net/jvm/anatomy-quarks/)

## Code generation

### Lombok

Restrict its use to the bare minimum.

 - `@Slf4j`
 - `@Getter`
 - `@Setter`
 - `@Data` if you want both get/set
 - `@EqualsAndHashcode` if `@Data` is not used and you want to be explicit about the fields

### Misc Java

 - Stick to plain Java and IDE code generation as much as possible without adding too much cruft
 - IDE assisted `equals/hashcode` if needed to customize objects stored in high performance collections

## Dependency Injection

### Guice

Stick to explicit Java in all places other than the one place where you bind things.

 - No Guice annotations in any class other than `AbstractModule`s
 - Rely on `@Provides` and `@Singleton` annotated methods to instantiate objects explicitly and bind/return them
 - Plain Java constructors invoked explicitly by the module's provider methods
 - Debatable: Use `@Inject` on 1 method in the module (which itself is injected) to contain the module's startup logic

```java
public class FruitModule extends AbstractModule {
  @Provides
  Apple makeApple(){
   return new Apple();
  }

  @Provides
  @Singleton
  Flour makeFlour(){
   return new WheatFlour();
  }

  @Provides
  ApplePie makeApplePie(Apple apple, Flour flour){
   return new ApplePie(apple, flour);
  }
}
```

### Lifecycle

 - `Autocloseable` if cleanup is required for manual `try/finally` - typically short lived but expensive objects with resources
 - `@PreDestroy` if the cleanup needs to be handled during shutdown - typically long lived objects

## Style

### Visibility

 - `private` + `final` in most cases
 - `package-local` + `final` if sub-class needs it
 - `package-local` method, class, constructor by default unless otherwise needed
 - `@VisibleForTesting` if `package-local` or `protected` method needs to be exposed for testing. Generally should be avoided as it may leak encapsulation
 - `@VisibleForTesting` if `package-local` or `protected` constructors on the other hand are much better as they declare all their dependencies upfront
 - `protected` constructor and perhaps fields of abstract classes that will be sub-classed from other packages

### Member variables

 - Non-`static` Fields are initialized in the constructor
 - Initialization at the site of field declaration is nice only if:
  - It is a `static` field
  - Non-`static` field but the field needs a default value when used in conjunction with Lombok or Hibernate validator

```java
@Getter
@Setter
public class PieRecipe {
    private static final int DEFAULT_FLOUR_GRAMS = 250;

    @NotBlank
    private String name;

    @Min(0)
    private int sugarGrams;

    @Min(100)
    private int flourGrams = DEFAULT_FLOUR_GRAMS;

    @Valid
    private List<Flavor> optionalFlavors;
}
```

### Exceptions

[No](http://docs.oracle.com/javase/tutorial/essential/exceptions/runtime.html) [checked](http://www.artima.com/intv/handcuffs2.html) [exceptions](http://radio-weblogs.com/0122027/stories/2003/04/01/JavasCheckedExceptionsWereAMistake.html).

### Formatting

Prefer readability over compactness while formatting code. Sometimes the IDE's automatic formatting may have to be overridden manually.

```java
public BigClass(
        int foo, String bar, float fizz, Object bizz, List<String> names) {
  ...
}

public BigClass(
        int foo, String bar, float fizz, Object bizz, 
        List<String> names, Map<String, Long> moreNames) {
  ...
}

void hello()  {
    world(
      xx, yy, zz, aa, bb, more, stillMore, manyMore, 
      others, moreOthers.values().stream().count()
    );
}

List<Integer> ids = allObjects
          .keySet()
          .stream()
          .filter(foo -> foo > 34)
          .map()
          .collect(Collectors.toList());
          
List<String> items = few
      ? new ImmutableList.Builder()
            .add("foo")
            .add("bar")
            .build()
      : Lists.newArrayList("aa", "bb", "cc", "dd", "ee", "ff", ....);
```

### Ordering of methods

```java
//In unit tests.

@BeforeClass
@BeforeMethod
@AfterMethod
@AfterClass
@Test testXX
@Test testYY
...
```

### Thread safety
 
 - By default all classes and methods are assumed not safe
 - Thread safe classes are marked by an explicit `@ThreadSafe` annotation
 
### Naming

 - Avoid plurals in package names
 - Prefer plural form of class name if it is a `Factory` or something similar. Ex: `JobExecutors` or `FooBuilders` or `Constants`
 - Some pointers from Java 8 Time API: [this](https://docs.oracle.com/javase/tutorial/datetime/overview/naming.html) & [that](https://docs.oracle.com/javase/tutorial/datetime/overview/design.html) 

### Constants

```java
public final class FooBarConstants {
    //"PROP" or "KEY" prefix for property or map keys.
    public static final String PROP_CONFIG_FILE_NAME = "app.config.file";
    
    //"VAL" prefix for fixed property or map values.
    public static final String VAL_DEFAULT_CONFIG_FILE_NAME = "conf/default.properties";
    
    //"VAR" prefix for template strings that can vary slightly.
    public static final String VAR_ERR_MSG_AGE = "The value [%s] provided for 'age' is invalid";
    
    //Private ctor and an abstract class. Prevent sub-classing and instantiation.
    private FooBarConstants() {
    }
}
```
 
### (Java)Docs, comments and logs

 - First time reference to nouns (Class or actors) use the literal names with correct capitalization or if available  `{@link LoanProcessor}` or `{@code Approval agent}`. Subsequent references may be in lower case (`the loan processor retries using ...`)
 - Follow proper punctuation and capitalization rules
 - Log and exception messages have parameters wrapped within brackets. Ex: `log.error("The directory [{}] does not exist", dirName.toString())`

## Non-Java files and resources

Prefer non-source code file and directory names like - `~/data-feed/all-lower-case-with-hyphens.csv`.

## Unit tests

We tend to focus on the "core" parts of the test but often ignore to clarify test boundaries, confirm the absence of unwanted start/end states and test for side effects.

- Establish the test boundary and system under test (a specific method of a specific class when unit testing). This means using the `Assert.assertXXX` methods even before the test mutates the state. i.e confirm your assumptions. It is also a great way to document the behavior and makes code reviews easy
  Ex: `assertEquals(0, customers.size())`
- Confirm that the parts that are not being tested and should not be affected are indeed untouched. i.e side-effect free. So, if mock objects are being used, it means doing something like:
```java 
  Mockito
     .verify(xx, never())
     .fooBar()
```
- Using `Assert.fail(xx)` more often to confirm that certain test code paths are not executed. 
   Ex: 
```java
   try { 
     //Actual test that triggers config ex
     ... 
     Assert.fail("Should've thrown config ex")
   } catch(ExpectedConfigException e) { 
     log.debug("Expected", e)
   }
```
