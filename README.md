# aidistill

# Federal AI Use Case Analysis Framework

This repository contains tools and documentation for analyzing and enhancing federal artificial intelligence (AI) use case documentation through structured analysis frameworks and automated processing workflows.

## Repository Structure

```
.
├── code/                  # Workflow automation scripts
├── doc/                   # Framework documentation
├── original/              # Source inventory data
└── processed/             # Enhanced inventory files
```

## Components

### Code
- `useCaseImprovement.json` - Workflow for enhancing AI use case documentation with structured analysis elements
- `useCaseTcqa.json` - Workflow for generating training data through topic-context-question-answer (TCQA) analysis

### Documentation
- `Improvement_Elements.md` - Defines the structured elements used for enhancing use case documentation:
  - Problem Statements
  - Solution Assertions
  - Value Categories
  - Technical Elements
  - Stakeholder Analysis
  
- `Improvement_Elements-Prompts.md` - Contains the prompt templates used for generating enhancement elements
- `Improvement_Elements-TCQA-Prompts.md` - Contains prompt templates for generating training data from enhanced use cases

### Data Files
- **Original/**
  - Source inventory files from federal AI use case collection efforts
  - Raw data in Excel and ZIP formats

- **Processed/**
  - Enhanced inventory files with additional analytical elements
  - Derived training data sets generated through TCQA analysis

## Usage

1. Original inventory data is processed using the n8n `useCaseImprovement.json` workflow to add structured analytical elements
2. Enhanced use cases are further processed using the n8n `useCaseTcqa.json` workflow to generate training data
3. Results are stored in the processed directory in Excel format

## Documentation

See the `doc/` directory for detailed information about:
- Analysis framework elements and definitions
- Prompt templates and usage guidelines
- Data structure specifications
- Processing workflow details

## Data Files

### Original Data
- `2024_consolidated_ai_inventory_raw_v1.xls` - Initial raw inventory data
- `2024_consolidated_ai_inventory_raw_v2.xls` - Updated raw inventory data
- `2024-Federal-AI-Use-Case-Inventory-main.zip` - Complete source data package

### Processed Data
- `2024_consolidated_ai_inventory_v1-Improved.xlsx` - Enhanced inventory with analytical elements
- `2024_consolidated_ai_inventory_v1-Improved-DerivedTrainingData.xlsx` - Generated training data

## Requirements

- n8n for running workflow automation scripts
- Microsoft Excel for viewing data files
- Text editor for viewing documentation files


## License

[TBD]
