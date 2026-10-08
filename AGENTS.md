# Agent Instructions

## Purpose and scope

This academic Java Swing application manages emergencies, personnel, ranks,
vehicles, emergency types, and resource assignments using MVC and MySQL/JDBC.
Keep changes within the user's requested scope; avoid unrelated refactors.
Use `README.md` for human-facing project information and setup guidance.

## Repository map and responsibilities

| Path | Responsibility |
| --- | --- |
| `src/Main.java` | Entry point; Nimbus styling and Swing event-thread startup. |
| `src/vista/` | Swing windows, form fields, tables, and presentation. |
| `src/controlador/` | Event handlers, validation coordination, navigation, and DAO calls. |
| `src/modelo/` | Domain entities, JDBC DAOs, connection handling, and date formatting. |
| `src/util/Validaciones.java` | Shared input-validation utilities. |
| `GestionDeEmergencias.iml` | IntelliJ module and external library references. |
| `out/production/` | Existing compiled output; not authoritative source. |

Keep SQL and persistence changes in DAOs, presentation in views, and interaction
coordination in controllers. Follow the surrounding implementation rather than
introducing a new architecture for a small change.

## Coding and language conventions

- Preserve Spanish domain identifiers, UI text, and surrounding Spanish comments.
  Use neutral Spanish when extending them; retain library/API names as written.
- Match local formatting: Java classes use PascalCase, methods and fields use
  camelCase, and package names are lowercase. Preserve existing file line endings.
- Preserve Swing event-thread startup and existing listener/navigation patterns.
- Follow nearby JDBC prepared-statement and try-with-resources patterns.
- Do not hand-edit generated `.class` files or use them to represent source fixes.
  Do not edit IDE metadata or exported IDE files unless explicitly requested.

## Build and runtime prerequisites

- Java 17 is the README's documented target. A locally installed newer JDK does
  not change that target or establish compatibility; verify the selected JDK.
- This repository has no Maven/Gradle build definition or wrapper, automated test
  suite, bundled dependency JARs, or SQL schema/setup scripts.
- `GestionDeEmergencias.iml` references MySQL Connector/J 9.0.0 and JDatePicker
  1.3.4 JARs in the parent directory. Verify availability before attempting a build;
  those relative references do not make dependencies reproducibly available.
- Source imports `org.jdatepicker.impl`; the README's LGoodDatePicker entry is
  inconsistent with that usage. The module also retains an LGoodDatePicker entry.
  Do not substitute date-picker libraries without a requested migration.
- Before a requested build, resolve the JDK and dependency classpath explicitly.
  Before a requested launch, also confirm a graphical desktop is available.
  `src/Main.java` is the entry point; no verified clean-build command is supplied.
- Database-backed modules require MySQL and a compatible schema. Opening a module
  can trigger queries during controller construction; a visible main menu does
  not demonstrate that persistence or CRUD operations work.

## Data and credential boundaries

- Treat connection settings in `src/modelo/Conexion.java` as sensitive. Never copy
  credential values into documentation, logs, reports, commits, or examples.
- Require explicit user authorization before real database access, remote access,
  or destructive operations. Use an authorized disposable database for CRUD checks.
- Do not create or alter schemas, install dependencies, or migrate configuration
  merely to make an unrelated task runnable; establish the requested scope first.

## Verification checklist

- Review changed paths and the diff for scope, language consistency, and secrets.
- Run `git diff --check`; for documentation, verify headings and referenced paths.
- For code changes, compile only when prerequisites and task scope permit; report
  the actual JDK/classpath used and any blockers instead of claiming success.
- When authorized and runnable, check affected screens, validation, navigation,
  and relevant persistence behavior. Do not infer module coverage from menu launch.
- Report checks actually performed, their results, and anything still unverified.
  Documentation-only work needs structural review, not application execution.
