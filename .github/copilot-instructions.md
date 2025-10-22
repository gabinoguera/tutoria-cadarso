# GitHub Copilot Instructions - CADARSO Project

## Project Overview
This is a **GitHub Copilot training repository** focused on "Vibecoding" (AI-assisted development) for Spanish-speaking IT teams. The project teaches practical AI coding techniques through real-world scenarios for a luxury hotel + watch retail business in Barcelona.

## Architecture & Structure

### Content Organization
- `Clase 1/` - Introduction to Vibecoding with SQL examples and tool setup
- `Clase 2/` - Practical use cases (documentation automation, system scripts)
- `test_apis_marketing.ipynb` - Live demo notebook for multilingual marketing APIs

### Key Learning Patterns
1. **Natural Language → Code**: Transform business requirements into functional scripts
2. **Documentation Generation**: Convert technical code (SAP/ABAP) into user manuals
3. **API Integration**: Build marketing automation with OpenAI APIs
4. **Network Automation**: Create Cisco device management scripts

## Development Workflows

### For Educational Content
- Content files use numbered prefixes (`0. guion.md`, `1. herramientas.md`) for workshop flow
- Markdown files contain both Spanish explanations and executable code examples
- Include real business context (hotel inventory, network infrastructure)

### For Demo Code
- Jupyter notebooks demonstrate live coding sessions
- Use Pydantic models for API data structures (`ProductType`, `ProductSpecs`)
- Include error handling patterns and logging for production-ready examples

## Project-Specific Conventions

### Language & Audience
- **Primary Language**: Spanish (documentation, comments, variable names)
- **Audience**: Mixed technical levels (IT support teams)
- **Business Context**: Dual business model (luxury hospitality + retail)

### Code Patterns
```python
# Follow this structure for API demos
class BusinessSpecificManager:
    def __init__(self, client_config):
        # Always include error handling
        # Use descriptive Spanish variable names
        
    async def proceso_automatizado(self):
        # Include step-by-step logging for educational value
        # Show both technical and business outcomes
```

### Documentation Style
- Use emoji headers for visual learning (`🎯`, `📋`, `🛠️`)
- Include both technical specs AND business impact
- Provide "Antes/Después" (Before/After) comparisons
- Reference specific line numbers in large files for workshop guidance

## Critical Integration Points

### OpenAI API Usage
- All API calls use environment variables for keys (`OPENAI_API_KEY`)
- Implement token usage tracking for cost awareness
- Include bilingual prompt engineering examples (Spanish business context → English API)

### Infrastructure Context
- Network scripts target Cisco devices (SSH connections, IOS commands)
- SAP integration patterns for enterprise data extraction
- Excel file processing workflows for business data imports

## Vibecoding Teaching Approach
When generating code for this project:
1. **Show the reasoning process** - explain why each approach works
2. **Include error scenarios** - demonstrate what happens when things go wrong
3. **Provide incremental complexity** - start simple, build sophistication
4. **Connect to business value** - always explain the practical impact

Example prompt pattern:
```
"Necesito un script que recorra equipos Cisco de un Excel y extraiga versiones de iOS"
→ Generate complete solution with error handling, logging, and business context
```