# What is Version Control?

Version Control, a.k.a. Source Code Management, is the process of tracking and implementing changes in software code. Version Control systems uses safeguards to track changes made by individual developers, by catching conflicting code and preventing loss of work due to overwrites.

## Benefits of Version Control

The primary benefits of every good version control system are as follows.

1. A complete change history of all files. This grants the ability to revert to previous versions of your software, which is useful in determining the root cause of more complicated bugs.
2. Traceability. An annotated history helps future developers understand what a piece of code is doing and why it was designed to work that way. It is particularly important for integrating legacy code harmoniously into newer projects.
3. Branching and merging. Branching allows developers to work concurrently on a project without encountering change collisions. Each branch can then be merged into the main branch, provided the changes made do not conflict. 

## Best Practices

* Commit often.
* Make sure your version is the latest version.
* Make detailed notes.
* Review changes before committing.
* Use branches.
* Agree on a workflow.

# What is Git?

Git is an open source distributed version control system. It was developed by Linus Torvalds in 2005 and is the most widely used version control system of today. It prioritizes performance, security, and flexibility in its design.

## Performance

Git uses a combination of delta encoding, compression, stored directory content, and metadata to format repository files and track version history. This combination makes it easy to keep track of renamed or rearranged files, as opposed to other version control systems, which only rely on the name of the file.

Git is a distributed system; unlike a centralized system, development does not halt when the original goes offline. Distributed version control systems provide each developer with a complete copy of the project's source code. Developers can continue committing changes to their remote repository, and push all changes to the main repository when it's back online.