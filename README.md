# Cursor Rules Directory

A collection of Cursor IDE rules for enhanced AI-assisted development workflows. Each rule provides specialized functionality to improve code quality, development process, and productivity.

## Available Rules

### 🔄 Workflow Management

#### `plan-act-workflow.mdc`
**Plan/Act Workflow System** - Implements a structured two-phase development approach
- **Triggers**: `(plan)` or `/plan` for planning, `(act)` or `/act` for execution
- **Features**: Machine-readable plans, step-by-step execution, error handling, progress tracking
- **Use Case**: Complex development tasks requiring structured planning and methodical implementation

#### `test-workflow.mdc`
**Test Runner Workflow System** - Automated testing agent for quality assurance
- **Triggers**: `/test` 
- **Features**: Automatic unit test generation, test execution, summary updates
- **Use Case**: Automated testing of files marked as testable from the plan-act workflow

### 📋 Code Analysis

#### `review-workflow.mdc`
**Code Review Assistant** - Focused code analysis with evidence-based responses
- **Triggers**: `(review)` or `/review` on selected files/folders
- **Features**: Grounded analysis, claim-backed explanations, no speculation
- **Use Case**: Thorough code review sessions with verifiable, fact-based insights

### 🔧 Language-Specific Policies

#### `nrfx_logging.mdc`
**NRF C Code Logging Policy** - Enforces strict logging conventions for NRF development
- **Triggers**: Automatically applied to `**/*.c` and `**/*.h` files
- **Features**: Proactive logging standards, NRFX_LOG_INFO usage, float handling
- **Use Case**: NRF-based embedded development requiring consistent logging patterns

## Usage Patterns

### Complete Development Cycle
1. **Plan** → `/plan <task description>` - Generate implementation plan
2. **Act** → `/act` - Execute the plan step-by-step  
3. **Test** → `/test` - Run automated tests on modified files
4. **Review** → `/review` - Analyze and validate the implementation

### Standalone Operations
- **Quick Review**: `/review` on any file or folder for immediate analysis
- **NRF Development**: Automatic logging policy enforcement on C files
- **Testing Only**: `/test` on existing execution summaries

## Key Benefits

- **🎯 Structured Development**: Clear phases prevent rushed implementations
- **✅ Quality Assurance**: Built-in testing ensures code reliability  
- **📊 Traceability**: Complete audit trail from planning to testing
- **🔍 Evidence-Based Analysis**: Code review backed by actual code examples
- **⚡ Automated Workflows**: Reduced manual overhead in development cycles
- **🛡️ Policy Enforcement**: Consistent coding standards across projects

## Installation

1. Copy the `.mdc` files to your Cursor rules directory
2. Rules are automatically loaded and available in Cursor IDE
3. Use the trigger commands to activate specific workflows

## Contributing

Each rule is self-contained and can be modified independently. When adding new rules:
- Include clear trigger mechanisms
- Provide comprehensive documentation
- Follow the established pattern of mode-based operation
- Update this README to include the new rule

---

*Version: 2.0 | Last Updated: December 2024*