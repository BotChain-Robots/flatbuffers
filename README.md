# Flatbuffers

We use [Google's Flatbuffers](https://flatbuffers.dev) for serialization. The main benefit of Flatbuffers over other serialization libraries is that Flatbuffers is small and fast (it does not require an unpacking step).

This repository contains all the Flatbuffer definition files (`.fbs`). It should only contain definition files.

Unless there is a good reason to add fields to the middle of a schema, please only add new fields to the end of schema files (to help maintain backward compatibility).

## Compiling
The schema definitions need to be compiled into code files for the languages we use.

The documentation for Flatbuffer's `flatc` tool can be found [here](https://flatbuffers.dev/flatc).

The generated files should then be copied into the respective repositories. Flatbuffers offers backward and forward compatibility.

### Installation
#### MacOS
Install `flatc` with homebrew
```
brew install flatbuffers
```

### Generating
```
flatc --cpp <filename>
```
