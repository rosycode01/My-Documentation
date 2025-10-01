# Setup & Project Creation – How I Made It Work

## Installing Quarkus SDK

I started by installing the **Quarkus SDK** on my system. At first, it felt like installing another tool, but I reminded myself that this was my **foundation for every project I’d build**.

## Setting Up My IDE

I installed plugins for **VS Code**. This made my coding smoother because my IDE could now:

- Understand Quarkus projects
- Suggest code completions
- Let me **live-reload** changes instantly

I realized that a proper setup is **half the battle** — it saves so much time later.

## Creating My First Project

Using **Maven**, I created a new Quarkus project. At first, the folder structure looked overwhelming, but I explored each folder slowly:

- `src/main/java` → for my **Java code**
- `resources` → for **configuration and static files**
- `pom.xml` → for **managing dependencies**

I ran:

bash
mvn quarkus:dev

- Added a simple **REST endpoint**
- Tweaked **configuration files**
- Watched how changes reflected **immediately**

This hands-on approach **cemented what I learned in the fundamentals**.

## ✅ Summary for Beginners

- **First**, understand why you’re learning Quarkus — what problems it solves and why it’s special.
- **Then**, take your time to **install the SDK, set up your IDE, and create your first project**. Don’t rush — exploring the project structure is key.
- **Finally**, **experiment!** Quarkus’ live reload makes this fun and lets you **learn fast**.
