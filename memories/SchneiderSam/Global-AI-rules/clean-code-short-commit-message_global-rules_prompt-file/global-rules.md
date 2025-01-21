# General Coding Principles

Your overarching goal is to produce code that is clean, efficient, and maintainable. 
You should always strive for readability, simplicity, and modularity, regardless of the programming language or context. 
Provide solutions in a supportive manner, ensuring that your recommendations are both actionable and adaptable. 
Avoid unnecessary complexity: keep your code open to iteration and future growth while preserving its clarity. 
Building upon these guiding principles, remember to respect language idioms, choose intuitive naming conventions, 
and consider best practices for error handling and testing from the outset. 
Whenever possible, aim for solutions that balance clarity with performance, factoring in future scalability and maintainability.

## Respect Language Idioms

Embrace the typical patterns and practices of the language you are using to enhance clarity and consistency. 
This improves maintainability and aligns with community standards.

## Write for Humans First

Code should be understandable at a glance, making it more approachable for collaborators and your future self. 
Avoid obfuscation or over-optimization that sacrifices readability.

## Future-Proof Your Design

Plan for growth and changing requirements, but do not overengineer. Keep your design flexible enough to adapt 
without complicating the initial implementation.

# Code Quality and Readability

## Clarity First

Write straightforward code that conveys its intent clearly. Minimize abstraction layers that obscure readability.

## Descriptive Naming

Use meaningful, consistent names for variables, functions, classes, and modules that reflect their purpose.

## Consistent Formatting

Follow established style guides and use automated tools to maintain uniform formatting across the codebase.

## Comment Thoughtfully

Provide comments or docstrings where necessary, but avoid restating what the code already expresses.

# Architecture and Modularity

## Encapsulate Complexity

Group related logic into self-contained modules or classes with clear, well-documented interfaces.

## Loose Coupling

Design components to function independently, using abstraction layers or interfaces to reduce interdependencies.

## Apply DRY

Refactor repetitive or duplicated code into shared utilities or functions to promote reuse and reduce bloat.

## Design for Extensibility

Structure your codebase so you can add new features and functionalities without requiring major rewrites.

# Error Handling and Testing

## Error Awareness

Implement robust error handling with clear messages and safe fallback paths for smoother recoveries.

## Write Tests Early

Create relevant tests at the outset of development to quickly capture edge cases and catch regressions.

## Iterative Validation

Run your tests frequently to ensure ongoing stability and to identify potential issues as your code evolves.

## Proactive Debugging

Leverage logging, tracing, and profiling to diagnose and resolve errors efficiently.

# Performance and Resource Management

## Choose Efficient Solutions

Adopt algorithms and data structures that suit your problem domain, optimizing for efficiency and scalability.

## Optimize When Necessary

Maintain clarity in your codebase; address performance bottlenecks only after conducting proper profiling.

## Manage Resources Properly

Follow best practices for handling external resources. For example, use `with` statements where applicable.

# Git Commands

Never use or ask me to use terminal commands for Git operations in the cascade chat.

# Commit Message in Cascade Chat

Write a short english commit message (maximum one sentence) for every change you make, and always format it in a code block. Use the following guidelines for consistent and descriptive commit messages:

prefix: short description (maximum one sentence)

Commit Prefixes: feat, fix, tweak, style, refactor, perf, test, docs, chore, ci, build, revert, hotfix, init, merge