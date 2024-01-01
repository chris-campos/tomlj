# TomlJ: A Java parser for Tom's Obvious, Minimal Language (TOML)

TomlJ is a complete [TOML](https://github.com/toml-lang/toml) parser with the
following attributes:

* Supports the latest TOML specification version (1.0.0).
* Provides detailed error reporting, including error position.
* Performs error recovery, allowing parsing to continue after an error.

It uses the [ANTLR](https://github.com/antlr/antlr4/) parser-generator and
runtime library.

## Usage

Parsing is straightforward:

```java
Path source = Paths.get("/path/to/file.toml");
TomlParseResult result = Toml.parse(source);
result.errors().forEach(error -> System.err.println(error.toString()));

String value = result.getString("a. dotted . key");
```

## Getting TomlJ

TomlJ is published to a Maven Central.

To include using Maven:
```xml
<dependency>
  <groupId>org.tomlj</groupId>
  <artifactId>tomlj</artifactId>
  <version>1.1.1</version>
</dependency>
```

To include using Gradle: `implementation 'org.tomlj:tomlj:1.1.1'`

## Links

- [GitHub project](https://github.com/tomlj/tomlj)
- [Online Java documentation](https://tomlj.org/docs/java/latest/org/tomlj/package-summary.html)
- [Issue tracker: Report a defect or feature request](https://github.com/tomlj/tomlj/issues/new)
- [StackOverflow: Ask "how-to" and "why-didn't-it-work" questions](https://stackoverflow.com/questions/ask?tags=tomlj)
