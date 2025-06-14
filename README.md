# Cursor Rules: Plan-Act-Test Workflow

A comprehensive set of Cursor IDE rules that implement a structured plan-act-test workflow for AI-assisted development. This system provides a methodical approach to complex coding tasks by breaking them into three distinct phases: planning, execution, and testing.

## Overview

This project contains Cursor IDE rules that enable:
- **Planning Phase**: Generate detailed, machine-readable implementation plans
- **Execution Phase**: Execute plans step-by-step with error handling and progress tracking
- **Testing Phase**: Automatically generate and run tests for modified files

## Files

### `plan-act-workflow.mdc`
The core workflow system that implements the plan/act cycle:
- **Planner Mode**: Triggered with `(plan)` or `/plan` - generates structured implementation plans
- **Executor Mode**: Triggered with `(act)` or `/act` - executes plans step-by-step
- Saves plans to `current_plan.md` for structured execution
- Tracks testable files and provides execution summaries

### `test-workflow.mdc`
The testing component that complements the plan-act workflow:
- **Tester Mode**: Triggered with `/test` - runs comprehensive testing on modified files
- Automatically generates unit tests for testable files
- Updates execution summaries with test results
- Provides full development cycle from planning to verification

## Usage

### Planning Phase
```
(plan) Implement user authentication system
```
or
```
/plan Implement user authentication system
```

### Execution Phase
```
(act)
```
or
```
/act
```

### Testing Phase
```
/test
```

## Key Features

- **Machine-readable plans**: Plans are saved in YAML-like format for reliable execution
- **Error handling**: Comprehensive error handling with user guidance options
- **Progress tracking**: Tracks modified files and execution status
- **Automated testing**: Generates and runs unit tests for modified code
- **Cross-platform compatibility**: Works with both Windows PowerShell and Unix shells
- **State management**: Clear mode transitions and state awareness

## Workflow Example

1. **Plan**: Use `/plan` to create a detailed implementation plan
2. **Review**: Review the generated plan in `current_plan.md`
3. **Execute**: Use `/act` to execute the plan step-by-step
4. **Test**: Use `/test` to run automated tests on modified files
5. **Summary**: Get comprehensive reports at each stage

## Installation

1. Copy the `.mdc` files to your Cursor rules directory
2. The rules will be automatically available in your Cursor IDE
3. Use the trigger commands to activate different workflow modes

## Benefits

- **Structured Development**: Clear separation of planning, execution, and testing phases
- **Quality Assurance**: Built-in testing ensures code quality
- **Traceability**: Complete audit trail from plan to tested implementation
- **Error Recovery**: Robust error handling with user guidance
- **Efficiency**: Automated workflows reduce manual overhead