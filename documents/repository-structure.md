# Repository structure

Application source, runtime assets, build manifests, tests and operational tooling live in code/. Project documentation lives in documents/, with project-plan/ reserved for planning. The root README and GitHub metadata remain at repository level.

## Path changes

Flask, its template/static paths, the Procfile and instance database use code/ as the application root. Configure an existing GitHub-linked host to use code/ before its next release.

Original runtime and asset subdirectories retain their relative arrangement inside code/.

Existing tracked Python bytecode and the Civic SQLite database, where applicable, are removed from the published source tree and retained locally under ignored code/ paths. Moving a database into an ignored directory does not erase earlier Git history. No credentials, local databases or generated caches are added.

## Verification scope

Verification covers source compilation, Flask import, public template rendering and file paths. It does not certify the prototype authentication, role management, production session settings or mock classifier.

This change updates repository layout and configuration. It does not issue a deployment command or change external service settings. Existing GitHub-integrated hosts can still run their own configured automation when source is pushed.
