# Steps to build an LSIF index

### Step 1: Generate SemanticDB files

Build class and SemanticDB files via [sbt](https://www.scala-sbt.org/) as follows.

```
sbt compile
```

### Step 2: Convert SemanticDB files to LSIF

Ensure that [lsif-semanticdb](https://github.com/sourcegraph/lsif-semanticdb) is installed.

```
lsif-semanticdb --semanticdbDir target/scala-2.12/classes/META-INF/semanticdb
```

This should generate a dump.lsif file in the root of the project.
