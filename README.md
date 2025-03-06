# quality-check-solutions

This repository provides a mapping of data package quality checks implemented in EDI's **EML Congruence Checker (ECC)** and the **ezEML metadata editor** to supporting documents. These documents describe common solutions to issues that arise during the quality-checking process.  

## Purpose

The goal of this repository is to present this information in a structured format that can be consumed and parsed by ECC and ezEML applications. This enables users to:  
- Understand the nature of a particular issue.  
- Learn why addressing the issue is important.  
- Access actionable steps to resolve the issue.  

Currently, much of this information is shared through interactions with the data curation team. By formalizing and centralizing this guidance, we aim to empower data contributors to address quality check issues more efficiently.  

## Repository Structure  

The repository is organized as follows:  

- **`mapping.csv`**: A crosswalk file that links ECC and ezEML quality check identifiers to corresponding solution documents.  
- **`solutions/`**: A directory containing markdown-formatted documents. Each document describes a quality check issue and common solutions.  
- **`template.md`**: A template for creating new solution documents, ensuring consistency in format and content.  

## Contributing  

We welcome contributions to improve this repository. If you would like to add or update a solution document, please use the `template.md` file as a starting point and follow the repository's structure. 

Modifications, including pull requests, are made through the `development` branch. Once changes are reviewed and approved, they will be merged into the `main` branch.
