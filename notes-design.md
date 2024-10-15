> [Ashwin Jayaprakash](https://ashwinjay.github.io/)
> [CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/)

# Table of Contents

* [About](#about)
* [Problem solving](#problem-solving)
* [Programming](#programming)
* [Computer fundamentals](#computer-fundamentals)
* [IDEs](#ides)
* [Best practices](#best-practices)
* [Code Katas](#code-katas)
* [Code reviews](#code-reviews)
* [System design basics](#system-design-basics)
* [Performance and deep dives](#performance-and-deep-dives)
* [Concurrency](#concurrency)
* [Distributed systems](#distributed-systems)
* [SQL](#sql)
* [Cloud](#cloud)
* [Testing](#testing)
* [Documentation and information management](#documentation-and-information-management)
* [Engineering excellence](#engineering-excellence)
* [Operational excellence](#operational-excellence)
* [Project maintenance and contributions](#project-maintenance-and-contributions)
* [Learning and leadership](#learning-and-leadership)
* ["Awesome" lists](#awesome-lists)

Created by [gh-md-toc](https://github.com/ekalinin/github-markdown-toc)

# About

This is an opinionated collection of reading material that I've collected over the years to help me become a better Engineer. It is not an exhaustive list. I share some more on a somewhat regular basis on [my Tech Blog](https://www.ashwinjayaprakash.com/search/label/tech). I also do a lot of general reading on leadership, culture, org building etc but I haven't found the time to share those.

# Problem solving

- [Situation, task, action, result](https://en.wikipedia.org/wiki/Situation,_task,_action,_result)
- [The Five W's (and H) approach](https://javaforu.blogspot.com/2011/06/five-ws-and-h-approach.html)

# Programming

* [How To Write Unmaintainable Code](https://www.doc.ic.ac.uk/~susan/475/unmain.html)
* [Clean Code by Robert Cecil Martin](https://www.google.com/search?q=Clean+Code+by+Robert+Cecil+Martin&ie=utf-8&oe=utf-8) ([Cheat sheet](https://www.bbv.ch/images/bbv/pdf/downloads/V2_Clean_Code_V3.pdf))
* [Principles of Effective Developers](https://www.youtube.com/live/mt4K6gHj5gE?feature=share)

# Computer fundamentals

* [Writing an OS in Rust](https://os.phil-opp.com/)
* [Writing a file system from scratch in Rust](https://blog.carlosgaldino.com/writing-a-file-system-from-scratch-in-rust.html)
* [What's in a Linux executable?](https://fasterthanli.me/blog/2020/whats-in-a-linux-executable/)
* [Wizard zines](https://wizardzines.com/)

# IDEs

  - [Learn to use the IDE/IntelliJ well](http://blog.jetbrains.com/idea/tag/30-days-guide/)
  - [IntelliJ IDEA Tips and Tricks by Anton Arhipov](https://youtu.be/ktRHoLHqu1I)
  - [IntelliJ Super Productivity in 45 Minutes](https://www.youtube.com/live/pX2jyeWs1qw?feature=share)
  - [IntelliJ IDEA. Debugger Essentials](https://youtu.be/59RC8gVPlvk)

# Best practices

* General
  * [SOLID design patterns](https://www.google.com/search?q=solid+design+patterns&ie=utf-8&oe=utf-8)
  * [Summary of OCP, SRP etc](http://programmers.stackexchange.com/questions/162643/why-is-clean-code-suggesting-avoiding-protected-variables/162657#162657)
  * [Venkat Subramaniam Design Patterns talks](https://www.youtube.com/results?search_query=venkat+subramaniam+design+patterns)
  * [GRASP design patterns](https://www.google.com/search?q=grasp+design+patterns&ie=utf-8&oe=utf-8)
  * [Domain-driven design by Eric J. Evans](https://www.google.com/search?q=eric+evan+sddd&ie=utf-8&oe=utf-8#q=Domain-driven+design+Book+by+Eric+J.+Evans)
  * [Applying UML and patterns by Craig Larman](https://www.google.com/search?q=craig+larman&ie=utf-8&oe=utf-8#q=Applying+UML+and+patterns+Book+by+Craig+Larman)
  * [Enterprise Integration Patterns by Gregor Hohpe](https://www.google.com/search?q=enterprise+integration+patterns&ie=utf-8&oe=utf-8)
  * [Refactoring, patterns, anti-patterns](https://sourcemaking.com/)
  * [Package by Feature](https://phauer.com/2020/package-by-feature/)
  * [Microservice architecture](https://microservices.io)
  * [Laws of UX](https://lawsofux.com/)
  * [Hexagonal Architecture and Payments Monolith decomposition - Johnny Willer](https://youtu.be/tBCLfRKQjew)
  * [Mateusz Chrzonstowski - My understanding of DDD & Clean Architecture on the example](https://youtu.be/KIj-q8uOUpM)
  * [I Made Everything Loosely Coupled. Does My App Fall Apart? - Gregor Hohpe](https://youtu.be/w9a7eI6BlVc)
* Java
  * [Best Practices for Designing and Implementing a Library in Java]( https://www.oracle.com/corporate/features/library-in-java-best-practices.html?evite=WWMK170414P00004)
  * [Effective Java, Third Edition Keepin' it Effective by Joshua Bloch](https://www.youtube.com/watch?v=hSfylUXhpkA)
  * [Josh Bloch on API design](https://www.google.com/search?q=josh+block+api+talk&ie=utf-8&oe=utf-8#q=josh+bloch+api+talk)
  * [Google Best Practices for Java Libraries](https://jlbp.dev/)
  * [Secure coding](https://www.oracle.com/java/technologies/javase/seccodeguide.html)
  * [Java Design Patterns](https://java-design-patterns.com/)
  * [Gang of Four Patterns in a Functional Light](https://www.youtube.com/watch?v=lZG74WbnhoE)
  * [Revisiting Design Patterns after 20 by Edson Yanaga](https://youtu.be/10dn_-TBzLE)
  * [Data-Oriented Programming in Java](https://www.youtube.com/watch?v=UQAw3pvZPCY)
  * [Programming Principles - slightly different from the ones above](http://webpro.github.io/programming-principles/)
  * [10 Reasons Why we Love Some APIs and Why we Hate Some Others by Lukas Eder](https://youtu.be/CYniPcoiI5g)
  * [Let's make a contract: the art of designing a Java API by Mario Fusco](https://www.youtube.com/watch?v=eRzi8beFBw4)
  * [Evolving Java-based APIs / Achieving API Binary Compatibility](https://wiki.eclipse.org/Evolving_Java-based_APIs_2)
  * [Trustin Lee: Writing a Java library with better experience](https://youtu.be/0eQbsVLxmMk)
  * [Date-Time Design Principles](https://docs.oracle.com/javase/tutorial/datetime/overview/design.html)
  * [The art of building Java APIs: Do's and Don'ts - Jonathan Giles](https://youtu.be/r1o6fUhAd8w)
  * [JooQ API design](https://blog.jooq.org/tag/api-design/)
  * [Java API design checklist](https://theamiableapi.com/2012/01/16/java-api-design-checklist/)
  * [12 recipes for using the Optional class as it’s meant to be used](https://blogs.oracle.com/javamagazine/12-recipes-for-using-the-optional-class-as-its-meant-to-be-used)
  * [Avoid](http://docs.oracle.com/javase/tutorial/essential/exceptions/runtime.html) [checked](http://www.artima.com/intv/handcuffs2.html) [exceptions](http://radio-weblogs.com/0122027/stories/2003/04/01/JavasCheckedExceptionsWereAMistake.html)
  * [A corner case cheat sheet for Java and JVM languages](https://ge0ffrey.github.io/ge0ffrey-presentations/cornerCaseCheatSheet/#/)
  * [Principles of Fluent API Design by David Beaumont](https://www.youtube.com/watch?v=VPu-ytfYTeU)
* Style
    - [Google style guide](https://google.github.io/styleguide/)
    - [A list of awesome style guides](https://github.com/kciter/awesome-style-guide#java)
    - Use tools to enforce a consistent, standard coding style (Checkstyle/PMD/FindBugs/SpotBugs/ErrorProne/Infer to do the first level checks)
    - Use IDEs and tools to format and fix compiler/IDE warnings
* APIs and CLIs
  * [Microsoft API guidelines](https://github.com/Microsoft/api-guidelines/blob/vNext/Guidelines.md)
  * [Google API design](https://cloud.google.com/apis/design/) 
  * [Kubernetes REST API conventions](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md)
  * [RESTful APIs and Events, created by Zalando](https://github.com/zalando/restful-api-guidelines)
  * [REST API tutorial](https://restfulapi.net/)
  * [Avoid Data Corruption in Your REST API with ETags](https://www.kennethlange.com/avoid-data-corruption-in-your-rest-api-with-etags/)
  * [Boost Your REST API with HTTP Caching](https://www.kennethlange.com/boost-your-rest-api-with-http-caching/) 
  * [REST API Checklist - Kenneth Lange](https://www.kennethlange.com/rest-api-checklist/)
  * [7 Tips for Designing a Better REST API](https://www.kennethlange.com/7-tips-for-designing-a-better-rest-api/)
  * [A guide to help you write better command-line programs](https://github.com/cli-guidelines/cli-guidelines)

# Code Katas

  - [c-guntur/paneer-tikka-masala: A Code Kata using a cooking recipe](https://github.com/c-guntur/paneer-tikka-masala) 
  - [c-guntur/java-katas: One repo to rule them all. All Java Katas in one repo](https://github.com/c-guntur/java-katas) 
  - [eclipse/eclipse-collections-kata: Collections Kata](https://github.com/eclipse/eclipse-collections-kata) 
  - [vmzakharov/mutate-test-kata: Code kata: using mutation testing to improve quality of unit tests](https://github.com/vmzakharov/mutate-test-kata) 
  - [forax/design-pattern-reloaded: Implementation of GoF design patterns in Java 8](https://github.com/forax/design-pattern-reloaded) 
  - [forax/java-guide: A guide of modern Java (Java 17)](https://github.com/forax/java-guide) 
  - [BNYMellon/CodeKatas: BNY Mellon Code Katas](https://github.com/BNYMellon/CodeKatas)

# Code reviews

- [Code review matters and manners](https://www.slideshare.net/trishagee/code-review-matters-and-manners) with [video](https://vimeo.com/182087729)
- [Building a code review culture](https://youtu.be/I0_N5MBYB5s)
- [Google Code Review Developer Guide](https://google.github.io/eng-practices/) 
- [Chromium Project - Respectful Code Reviews](https://chromium.googlesource.com/chromium/src/+/master/docs/cr_respect.md) 
- [Chromium Project - Respectful Changes](https://chromium.googlesource.com/chromium/src/+/master/docs/cl_respect.md)
- [A Software Engineer’s Guide to Giving Feedback that Actually Matters](https://shopify.engineering/software-engineers-guide-to-feedback-that-matters)
- [The Code Review Pyramid](https://www.morling.dev/blog/the-code-review-pyramid/)

# System design basics

(Also see [12 Factor](https://12factor.net/), [FURPS / Functional Usability Reliability Performance Supportability](https://en.wikipedia.org/wiki/FURPS))

- Requirements
  - Goals
  - Non goals
  - Scale
  - Constraints
  - Success measures
- Design - Basics
  - Customer journeys (Visit -> Search -> Add -> Sign in/up -> Checkout -> Order -> Invoice -> Payment -> Fulfillment -> Shipment -> Confirmation/Return/Cancel/Refund/Status/Notify)
  - APIs and Entities - CRUD
  - Services - Foreground and background
  - Stores
  - Reliable (consistent, available), scalable (latency, goodput), observable, maintainable, secure
- Design - Principles
  - Customer first
    - MVP
    - Necessary (support), sufficient (resistance), nice to have
  - Critical thinking
    - ROI
    - COGS
    - KPIs
    - Data and experiment driven
  - Tradeoffs
    - Simple, easy to reason and scale
    - Mechanical sympathy
    - Reduce toil and undifferentited heavy lifting
- Scope
  - CDN / Edge network / POP, Region / availability zone / cell 
- System - Loadbalancer
  - Healthcheck
  - Routing
  - DNS updates
  - TLS and Certs
- System - API Gateway
  - Protocols
  - Firewall
  - Rate limiting
  - Bounds check
  - Authz and authn
  - Routing
  - Logging
- Concept - Resilience
  - Timeout 
  - Retry
  - Jitter
  - Bulkhead
  - Circuit break
  - Backpressure
  - Memoize
  - Fault domain
- Concept - Reads, writes and operations
  - Space and compute complexity
    - Arrival time, wait time, service time
    - Read and write ratio
  - Consistency, availability, durability
    - Atomic, transactional, lease, lock
    - Eventually or strongly consistent
    - Durable
    - Synchronous, asynchronous
      - Commands (need to be worked upon, ideally by a single worker)
      - Events (already happened)
      - Query (deterministic queries that don't have random numbers etc produce repeatable results)
      - Checkpoint, write after/before logs, replay-idempotence, compensation-rollback
  - Critical path
    - Crosstalk, coordination, contention
    - Partition, replication, affinity, anti-affinity
    - Schema on read or write, filter and aggregate on read or write
    - Deduplication, pre-fetching, pre-aggregating
    - Batching, compression, retention, tiering
    - Online vs offline - Analytics, notifications, repairs, reconciliation
    - Caching, invalidation, summary or probabilistic structures
    - Scoring, sorting, constraint satisfaction
- Concept - Algorithms
  - Loadbalancing
    - Least used
    - Power of two random choices
    - Round robin
    - ...
  - Hashing
    - Consistent hash
    - Modulo hash
    - Rendezvous hash
    - ...
- Concept - Security
  - Authenticate and authorize
  - Encryption at rest and motion
  - Sign and verify
  - Governance, risk and compliance
  - Audit trail
  - Principles
    - SSO, RBAC ...
    - Least privilege
    - Short lived tokens
    - Key rotation
    - ...
- Concept - Operations
  - Measure, monitor, alert - Detect, escalate, respond, prevent
    - Cost
    - Performance
    - Errors
    - Capacity
    - Disruption and error budgets
    - Test - chaos and synthetic
    - SLO
  - Deploy safely
    - Feature flags and canary/blue green rollouts
    - Reduce toil
      - Auto repair
      - Auto scale up and back to zero
    
# Performance and deep dives

* General
  * [Latency numbers every programmer should know](https://gist.github.com/hellerbarde/2843375)
  * [Misery Metrics & Consequences - Gil Tene](https://www.youtube.com/watch?v=K1jasTyGLr8&list=WL&index=39)
  * [Square Engineering's "Fail Fast, Retry Soon" Performance Optimization Technique](https://www.youtube.com/watch?v=oRRr-AONvak&list=WL&index=58)
  * [Optimizing Servers for High-Throughput and Low-Latency at Dropbox](https://www.youtube.com/watch?v=X_v4G0qJ8PI&list=WL&index=34)
* Java
   - [JVM bytecode](http://blog.jamesdbloom.com/JavaCodeToByteCode_PartOne.html)
   - [JVM internals](http://blog.jamesdbloom.com/JVMInternals.html)
   - [No Free Lunch? Memory Allocation in the JVM](https://youtu.be/NY1S0M4i-xM)
   - [Java at Speed](https://youtu.be/ot3PESmNXhE)
   - [Aleksey Shipilёv's posts describing some elementary piece of knowledge about JVM](https://shipilev.net/jvm/anatomy-quarks/)
   - [JVM Anatomy 101](https://www.youtube.com/watch?v=BeMi8K0AFAc)
   - [Time To Really Learn Generics: A Java 8 Perspective](https://nofluffjuststuff.com/magazine/2016/09/time_to_really_learn_generics_a_java_8_perspective)
   - [Mastering the mechanics of Java method invocation](https://blogs.oracle.com/javamagazine/mastering-the-mechanics-of-java-method-invocation)
   - [Understanding Java method invocation with invokedynamic](https://blogs.oracle.com/javamagazine/understanding-java-method-invocation-with-invokedynamic)
   - [Behind the scenes: How do lambda expressions really work in Java?](https://blogs.oracle.com/javamagazine/behind-the-scenes-how-do-lambda-expressions-really-work-in-java)
   - [Understanding Gradle](https://www.youtube.com/playlist?list=PLWQK2ZdV4Yl2k2OmC_gsjDpdIBTN0qqkE)
   - [Secrets of Performance Tuning Java on Kubernetes by Bruno Borges](https://youtu.be/wApqCjHWF8Q)

# Concurrency

* [Brian Goetz on concurrency](https://www.google.com/search?q=brian+goetz+concurrency+talk&ie=utf-8&oe=utf-8#q=brian+goetz+concurrency+talk&tbm=vid)
* [Venkat Subramaniam concurrency talks](https://www.youtube.com/results?search_query=venkat+subramaniam+concurrency)
* [Concurrent programming in Java by Doug Lea](https://www.google.com/search?q=Concurrent+programming+in+Java+Book+by+Doug+Lea&ie=utf-8&oe=utf-8)
* [Roman Leventov's Code Review Checklist for Java Concurrency](https://github.com/code-review-checklists/java-concurrency)

# Distributed systems

* General
  * [An introduction to distributed systems](https://github.com/aphyr/distsys-class)
  * [High Scalability](http://highscalability.com/all-time-favorites/)
  * [Not Just Scale - Marc Brooker](https://brooker.co.za/blog/2024/06/04/scale.html)
* Resilience
  * [Stability Patterns and Antipatterns, Michael Nygard](https://youtu.be/IV2bQO9TfTk)
  * [10 patterns for more resilient applications - Uwe Friedrichsen](https://youtu.be/G4bv3_paII0)

# SQL

* [Practical SQL for Data Analysis - Haki Benita](https://hakibenita.com/sql-for-data-analysis) 
* [Awesome SQL Tips and Tricks - Voxxed Days Cluj - 2019](https://www.slideshare.net/VladMihalcea/awesome-sql-tips-and-tricks-voxxed-days-cluj-2019-189018546) 
* [How Query Engines Work](https://www.howqueryengineswork.com/)
* [How Modern SQL Databases Come up with Algorithms that You Would Have Never Dreamed Of by Lukas Eder - YouTube](https://www.youtube.com/watch?v=wTPGW1PNy_Y) 

# Cloud

* [Jerry Hargrove - Cloud Diagrams & Notes](https://www.awsgeek.com/)
* [open-guides/og-aws: Amazon Web Services — a practical guide](https://github.com/open-guides/og-aws) 
* [Amazon Web Services In Plain English](https://expeditedsecurity.com/aws-in-plain-english/) 
* [Amazon Web Services (also in plain English)](https://adayinthelifeof.nl/2020/05/20/aws.html) 
* [AWS services explained in one line each](https://news.ycombinator.com/item?id=23309269)

# Testing

- [Test Desiderata](https://medium.com/@kentbeck_7670/test-desiderata-94150638a4b3)
- [Cassandra testing guidelines](https://github.com/apache/cassandra/blob/trunk/TESTING.md)
- [Don't be mocked by your Mocks: Listening to your Tests](https://youtu.be/pKBjufM024U)
- [Testing legacy code when you dislike tests (and legacy code) by Maeve Revels](https://youtu.be/ufIGaySoQWY)
- [Effective Unit Testing by Eliotte Rusty Harold](https://youtu.be/fr1E9aVnBxw?si=ocFnR3BEG1qe9kFi)
- [Write awesome tests by Jeroen Mols](https://youtu.be/F8Gc8Nwf0yk?si=3imI_0e060kBBTo4)
- [An Ultimate Guide To BDD](https://www.youtube.com/watch?v=gXh0iUt4TXA)
- [The lazy programmer's guide to writing thousands of tests - Scott Wlaschin](https://youtu.be/IYzDFHx6QPY?si=jcT1rBy8DSdWft7P)
- [Property based testing](https://github.com/jlink/property-based-testing/blob/main/pbt-java/src/test/java/pbt/hwayne/can_afford.md) 
- [Integrating PIT Mutation Testing and GitHub Pages with GitHub Actions](https://4comprehension.com/integrating-pit-mutation-testing-and-github-pages-with-github-actions/)

# Documentation and information management

- [US Government plain language guidelines](https://plainlanguage.gov/)
- [Technical Writing Courses for Engineers](https://developers.google.com/tech-writing)
- [Effective software design documents](https://wecode.wepay.com/posts/effective-software-design-documents) & [
A generic design document template for documenting Micro services](https://github.com/wepay/design_doc_template)
- [Google Developer Documentation Style Guide](https://developers.google.com/style/)
- [The Modular Documentation Project Source Repository](https://github.com/redhat-documentation/modular-docs)
- [The Art of Code Comments - Sarah Drasner](https://youtu.be/yhF7OmuIILc)
- [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
- [Conventional Commits - specification for adding human and machine readable meaning to commit messages](https://www.conventionalcommits.org/en/v1.0.0/)
- [If Hemingway Wrote JavaDocs](https://www.youtube.com/watch?v=DEW_SRk6mCU)
- [Keep a Changelog](https://keepachangelog.com)

# Engineering excellence

* [We invested 10% to pay back tech debt; Here's what happened](https://blog.alexewerlof.com/p/tech-debt-day)

# Operational excellence

* [How to Best Use MTT* Metrics to Optimize Your Incident Response](https://www.infoq.com/articles/mtt-metrics-incident-response/)

# Project maintenance and contributions

- [Tanzu Community Engagement guidelines, community health measurements, and goals](https://github.com/vmware-tanzu/community-engagement)
- [Cassandra contribution guide](http://cassandra.apache.org/doc/latest/development/index.html) has a nice page on code review among other things
- [eclipse collections contributor guide](https://github.com/eclipse/eclipse-collections/blob/master/CONTRIBUTING.md#commit-messages)
- [Strimzi contributor guide](https://strimzi.io/contributing/guide/)
- [Contributing to Seldon Core](https://docs.seldon.io/projects/seldon-core/en/latest/developer/contributing.html)

# Learning and leadership

* [Barbara Oakley: "Learning How to Learn"](https://www.youtube.com/watch?v=vd2dtkMINIw)
* [Reading Research: A Guide for Software Engineers](https://brooker.co.za/blog/2020/05/25/reading.html)
* [Engineering You: Martin Thompson](https://youtu.be/S4LzzuMTqjs)
* [Understanding the role of a principal engineer](https://youtu.be/OcwpMBfZoek)

# "Awesome" lists

* [(My very own) Ashwin Jayaprakash's tech blog](https://www.ashwinjayaprakash.com/search/label/tech)
* ["Awesome" lists](https://www.google.com/search?q=awesome+lists)
* [A curated list of awesome Java frameworks, libraries and software](https://github.com/akullpp/awesome-java)
  
