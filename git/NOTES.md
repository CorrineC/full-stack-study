# What is Version Control?

Version Control, a.k.a. Source Code Management, is the process of tracking and implementing changes in software code. Version Control systems uses safeguards to track changes made by individual developers, by catching conflicting code and preventing loss of work due to overwrites.

## Benefits of Version Control

The primary benefits of every good version control system are as follows.

1. A complete change history of all files. This grants the ability to revert to previous versions of your software, which is useful in determining the root cause of more complicated bugs.
2. Traceability. An annotated history helps future developers understand what a piece of code is doing and why it was designed to work that way. It is particularly important for integrating legacy code harmoniously into newer projects.
3. Branching and merging. Branching allows developers to work concurrently on a project without encountering change collisions. Each branch can then be merged into the main branch, provided the changes made do not conflict.

## Best Practices

- Commit often.
- Make sure your version is the latest version.
- Make detailed notes.
- Review changes before committing.
- Use branches.
- Agree on a workflow.

# What is Git?

Git is an open source distributed version control system. It was developed by Linus Torvalds in 2005 and is the most widely used version control system of today. The greatest criticism of Git is that it is difficult to learn, but its benefits far outweigh the costs for the majority of developers. It prioritizes performance, security, and flexibility in its design.

## Performance

Git uses a combination of delta encoding, compression, stored directory content, and metadata to format repository files and track version history. This combination makes it easy to keep track of renamed or rearranged files, as opposed to other version control systems, which only rely on the name of the file.

Git is a distributed system; unlike a centralized system, development does not halt when the original goes offline. Distributed version control systems provide each developer with a complete copy of the project's source code. Developers can continue committing changes to their remote repository, and push all changes to the main repository when it's back online.

## Security

Git secures change history against accidental and malicious change with a hashing algorithm called SHA1.

## Flexibility

Branches and tags are stored as part of the change history. This level of tracking, as well as Git's compatibility with a variety of existing systems and protocols, set Git apart from other version control systems.

# Why Git?

Git is for everyone, including, but not limited to:

- Developers. With Git, each developer gets a local repository with a full history of commits. Git's distributed system enables effective workflow around feature branches by avoiding blocking; developers don't have to wait for others' changes to be checked in. Lost repositories can also be replaced by cloning someone elses repositories. Additionally, Git has pull requests, which allow for project leads to control what is added to the master branch. These conveniences allow for continuous integration and delivery of software.
- Marketing. Shorter development cycles mean updates and fixes that would normally be rolled into one release can now be released as they are developed. Thus, marketing can build campaigns for more features with more specific audiences in mind.
- Product Management. Feature branch workflows provide flexibility when priorities change. Work on feature branches can be paused to address more time-critical issues, then picked up again immediately after with no time lost.
- Designers. Short development cycles also allow for rapid prototyping. Pull requests can be used as a formal meeting spot for discussing design changes.
- Customer Support. Bug fixes don't have to wait for the next major release anymore!
- Human Resources. Use Git to attract new programmers!
- Budget Management. The man hours saved with shorter development cycles is more than worth the time it takes to learn Git.

# What is an SSH Key?

An SSH key is a credential for the secure shell network protocol. It is used for remote communication (file transfer, network management, etc.) between machines on an unsecured network. It uses a combination of public and private key to encrypt data. The private key is not derived from the public key. SSH keys can be used in Git as lieu of a traditional password to push or pull remote repositories.

## Creating an SSH Key on Mac and Linux

1. Create a new SSH key using the email as a label
2. Specify a file location to save the key
3. Enter a secure passphrase (an additional layer of security)
4. Add the new key to ssh-agent (keychain)

# Git Archive

The `git archive` command creates an archive file from a specified reference point in a git repository. It has several output formats that utilize additional compression.
