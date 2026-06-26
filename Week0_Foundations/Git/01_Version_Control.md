# 01 Version Control

## What is Version Control?
Version Control is a system that records changes made to files over time and allows developers to restore previous versions whenever required. It helps developers maintain project history, collaborate with teams, and track modifications efficiently. Instead of creating multiple copies of files manually, Version Control maintains a structured timeline of changes and acts like a history book for a project.

## Why Do We Need Version Control?
Version Control is needed because manually managing multiple versions of files becomes confusing and inefficient. Without Version Control, developers often create files such as project_v2.py, project_final.py, and project_final_latest.py, making it difficult to determine which version is correct. Version Control provides a systematic way to track changes, collaborate with teams, recover previous versions, and maintain a complete history of the project.

## Types of Version Control Systems
### Local Version Control System

In a Local Version Control System, all project history is stored on a single machine. It is simple to use but lacks collaboration features and is vulnerable to data loss if the machine fails.

### Centralized Version Control System

In a Centralized Version Control System, a central server stores the entire project history and developers connect to that server to access files. Examples include SVN and Perforce. It simplifies collaboration but introduces a single point of failure.

### istributed Version Control System

In a Distributed Version Control System, every developer has a complete copy of the repository and its history. Git is an example of a Distributed Version Control System. This approach enables offline work, faster operations, and better reliability.

## Version Control vs Backup
A backup system simply stores copies of files, whereas Version Control tracks changes, maintains history, records authorship, and supports collaboration. Although Version Control can act as a backup mechanism, its primary purpose is to manage changes and facilitate teamwork.
## Benefits of Version Control
Version Control provides numerous advantages including change tracking, collaboration among developers, recovery of previous versions, accountability, experimentation through branching, and efficient project management. It helps teams maintain consistency and reliability throughout software development.
## Applications of Version Control
Version Control is widely used in Software Development, Cloud Engineering, DevOps, Infrastructure as Code, Data Science, Machine Learning, Web Development, and Documentation Management. Modern development workflows rely heavily on Version Control systems.

## Real World Example
Consider a team of three developers working on an e-commerce website. One developer is implementing the login page, another is developing the payment module, and the third is managing the product catalog. Without Version Control, exchanging files manually would lead to overwritten work and confusion. With Version Control, each developer can work independently, maintain a complete history of changes, and safely merge updates into the main project.