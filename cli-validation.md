# CLI Validation

Our command line app accepts a string of parameters and we need to validate them for correctness.

Write a method that accepts the entire command line argument as a single string input, checks the individual parameters it contains for correctness, and returns an integer response. See "Examples" section for example inputs to your method.

`int Validate(string parameters);`

## Input

The following parameters are valid inputs on the command line:

Parameter | Value
--- | ---
`--label` | a string of length between 3 and 10 characters (inclusive)
`--range` | an integer between 10 and 100 (inclusive)
`--help` | 

## Return

The validation method you write will return one of the three following values:

Value | Description
--- | ---
**-1** | if any invalid parameters are detected
**0** | if all parameters are valid
**1** | if help was specified and all parameters are valid

## Acceptance Criteria

* Parameters should be parsed from left to right
* Parameters are optional, however at least one parameter must be provided for a set of parameters to be considered valid
* Parameters are case-insensitive
* Additional whitespace should be ignored
* You should identify and handle any potential exceptions in your solution

## Examples

Use these as test data to confirm your solution is correct:

Input | Output
--- | ---
`--range g` | **-1**
`--help name` | **-1**
`--label` | **-1**
`--blah` | **-1**
`--label SOME_LABEL --range 10` | **0**
`--raNGe 44` | **0**
`--label --range` | **0**
`--label abc --help` | **1**
`--help --range 11` | **1**
`--Help` | **1**

