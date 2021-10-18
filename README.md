# Lifelong Learning Logger (L2Logger)

![logo](docs/apl_small_vertical_blue.png)

## Table of Contents

- [Introduction](#introduction)
- [Logger Term Definitions/Glossary](#logger-term-definitionsglossary)
- [Logger Output Format](#logger-output-format)
- [Interface/Usage](#interfaceusage)
- [Examples](#examples)
- [Tests](#tests)
- [Log Validation](#log-validation)
  - [Example](#example)
  - [Usage](#usage)
- [Changelog](#changelog)
- [Acknowledgements](#acknowledgements)

## Introduction

The Lifelong Learning Logger is a utility library provided for
producing logs in a convenient format for the provided l2metrics module,
but can also be used independently.

## Logger Term Definitions/Glossary

Strongly recommend starting here, detailed explanation of the terms used
throughout: [docs/definitions.md](./docs/definitions.md).

## Logger Output Format

Detailed explanations of the logging output structure/format can be seen via
[docs/log_format.md](./docs/log_format.md).

## Interface/Usage

At a high level, the library is used simply by creating an
instance of the logger object, then by invoking the `log_record`
 member function on it at least once per experience.

For a detailed explanation of the provided functions, see
[docs/interface.md](./docs/interface.md).

## Examples

See documentation in the examples folder at [examples/README.md](./examples/README.md).

## Tests

See documentation in the test folder at [test/README.md](./test/README.md).

## Log Validation

Logs generated by L2Logger should already be in the proper format for ingestion by the Metrics Framework. However, log validation can also be done manually using the provided `validate.py` module.

### Example

```bash
python -m l2logger.validate <path/to/log_directory>
```

### Usage

```
usage: python -m l2logger.validate [-h] log_dir

Validate log format from the command line

positional arguments:
  log_dir     Log directory of scenario

optional arguments:
  -h, --help  show this help message and exit
```

Note: This script only validates one instance of a scenario output; it does not run recursively on a directory containing multiple scenario logs.

## Changelog

See [CHANGELOG.md](./CHANGELOG.md) for a list of notable changes to the
project.

## Acknowledgements

Primary development of Lifelong Learning Logger (L2Logger) was funded by the DARPA Lifelong Learning Machines (L2M) Program.

© 2021 The Johns Hopkins University Applied Physics Laboratory LLC
