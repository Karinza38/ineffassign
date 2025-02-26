ineffassign

Detect ineffectual assignments in Go code.  An assignment is ineffectual if the variable assigned is not thereafter used.

This tool misses some cases because it does not consider any type information in its analysis.  For example, assignments to struct fields are never marked as ineffectual.  It should, however, never give any false positives.

## Install

    go install github.com/gordonklaus/ineffassign@latest

## Usage

For basic usage, run the following command from the root of your project:

    ineffassign ./...

Which will analyze all packages beneath the current directory.

## Exit Codes

ineffassign returns 1 if any problems were found in the checked files.  It returns 3 if there were any invalid arguments.
