# Campus Team Finder — Database Dump

## Overview

This repository contains the Neo4j database reconstruction export for the **Campus Team Finder** project, developed as part of the Database Modelling and Design coursework.

The export contains Cypher statements intended to reconstruct the graph database, including its nodes, relationships, properties, indexes, and constraints.

## Database Contents

The database models the following entities:

- **Student** — student profiles, academic details, and skills.
- **Project** — project information, descriptions, categories, and status.
- **Skill** — technical skills associated with students and projects.
- **Application** — applications submitted by students to projects.

The graph includes relationships such as `HAS_SKILL`, `OWNS`, `REQUIRES`, `SUBMITTED`, `FOR_PROJECT`, and `MEMBER_OF`.

## File Structure

```text
campus-team-finder-database-dump/
├── README.md
└── campus_team_finder_database_dump.cypher
```

## Requirements

- A Neo4j database instance.
- Access to Neo4j Browser or another Cypher query interface.

## How to Restore the Database

1. Create or select an **empty Neo4j database**.
2. Download `campus_team_finder_database_dump.cypher` from this repository.
3. Open the file in a text editor or code editor.
4. Execute its Cypher statements against the target database, using a method appropriate for the file's size and your Neo4j environment.
5. Verify that the nodes, relationships, indexes, and constraints have been created successfully.

**Important:** Run the reconstruction script against an empty target database. Its `CREATE` statements may create duplicates or conflict with existing uniqueness constraints if run against a populated database.

## Purpose

This file provides a readable, portable reconstruction script for the project's Neo4j graph data. It is intended to support database restoration, inspection, and academic evaluation.

## Notes

- This is a Cypher reconstruction export, not a native Neo4j binary backup.
- Successful restoration depends on the completeness and validity of the exported statements.
- Database credentials and `.env` files are intentionally excluded from this repository.

## Project

**Project name:** Campus Team Finder  
**Database:** Neo4j  
**Course:** Database Modelling and Design