# Code Quality Guidelines

## Overview

MeridianAlgo maintains high standards for code quality to ensure our projects are maintainable, secure, and performant. These guidelines apply to all contributions across our repositories.

## General Principles

### Code Quality Standards

- **Readability First**: Code should be self-documenting and easy to understand
- **Consistency**: Follow established patterns and conventions within each project
- **Testability**: Write code that can be easily tested and validated
- **Performance**: Consider performance implications without premature optimization
- **Security**: Follow secure coding practices at all times

### Documentation Requirements

- **Public APIs**: Must have comprehensive documentation
- **Complex Logic**: Include inline comments explaining the approach
- **Configuration**: Document all configuration options and their defaults
- **Dependencies**: Document required dependencies and their versions

## Language-Specific Guidelines

### Python

#### Style Guide
- Follow **PEP 8** style guidelines
- Use **Black** for code formatting
- Maximum line length: **88 characters**
- Use **isort** for import organization

#### Code Structure
```python
# Imports (standard library, third-party, local)
import os
import sys
from typing import List, Optional

import numpy as np
import pandas as pd

from meridianalgo.core import BaseClass

# Constants
DEFAULT_TIMEOUT = 30
MAX_RETRIES = 3

# Classes and functions
class DataProcessor:
    """Process financial data with validation and error handling."""
    
    def __init__(self, config: dict) -> None:
        self.config = config
        self._validate_config()
    
    def process(self, data: List[dict]) -> Optional[pd.DataFrame]:
        """Process input data and return validated DataFrame.
        
        Args:
            data: List of data dictionaries to process
            
        Returns:
            Processed DataFrame or None if processing fails
            
        Raises:
            ValueError: If data format is invalid
        """
        pass
```

#### Testing
- Use **pytest** for unit testing
- Maintain **80%+ test coverage**
- Write both unit and integration tests
- Use type hints for better IDE support

### JavaScript/TypeScript

#### Style Guide
- Use **ESLint** with recommended configurations
- Use **Prettier** for code formatting
- Prefer **TypeScript** for new projects
- Use **CamelCase** for variables, **PascalCase** for classes

#### Code Structure
```typescript
// Imports
import { Logger } from './utils/logger';
import { DataProcessor } from './core/processor';

// Constants
const DEFAULT_TIMEOUT = 30000;
const MAX_RETRIES = 3;

// Interfaces
interface ProcessedData {
  id: string;
  timestamp: number;
  value: number;
}

// Classes
export class FinancialProcessor {
  private logger: Logger;
  
  constructor(config: ProcessorConfig) {
    this.logger = new Logger('FinancialProcessor');
    this.validateConfig(config);
  }
  
  /**
   * Process financial data with validation
   * @param data - Raw data to process
   * @returns Processed data or null if validation fails
   */
  public processData(data: RawData[]): ProcessedData[] | null {
    try {
      return this.validateAndTransform(data);
    } catch (error) {
      this.logger.error('Processing failed', error);
      return null;
    }
  }
}
```

#### Testing
- Use **Jest** for unit testing
- Maintain **80%+ test coverage**
- Include both unit and integration tests
- Use TypeScript for type safety

## Code Review Process

### Pre-Commit Checklist

Before submitting a pull request, ensure:

- [ ] Code follows project style guidelines
- [ ] All tests pass locally
- [ ] New code has appropriate test coverage
- [ ] Documentation is updated
- [ ] No sensitive data is committed
- [ ] Dependencies are properly declared
- [ ] Error handling is implemented
- [ ] Code is self-contained and reproducible

### Review Criteria

Pull requests are evaluated based on:

1. **Functionality**: Does the code work as intended?
2. **Quality**: Is the code well-written and maintainable?
3. **Testing**: Are tests comprehensive and reliable?
4. **Documentation**: Is the code properly documented?
5. **Security**: Does the code follow security best practices?
6. **Performance**: Are there any performance concerns?

## Testing Guidelines

### Unit Testing

- **Test Coverage**: Minimum 80% line coverage
- **Test Organization**: Group related tests together
- **Test Naming**: Use descriptive names that explain the scenario
- **Mocking**: Mock external dependencies appropriately

### Integration Testing

- **End-to-End Scenarios**: Test complete workflows
- **Database Integration**: Test database interactions
- **API Testing**: Test API endpoints and responses
- **Performance Testing**: Include performance benchmarks where relevant

### Test Structure Example

```python
import pytest
from unittest.mock import Mock, patch
from meridianalgo.processor import DataProcessor

class TestDataProcessor:
    
    def setup_method(self):
        """Setup test fixtures before each test."""
        self.config = {"timeout": 30, "retries": 3}
        self.processor = DataProcessor(self.config)
    
    def test_process_valid_data_success(self):
        """Test processing of valid data returns expected results."""
        # Arrange
        test_data = [{"id": 1, "value": 100}]
        
        # Act
        result = self.processor.process(test_data)
        
        # Assert
        assert result is not None
        assert len(result) == 1
        assert result[0]["id"] == 1
    
    def test_process_invalid_data_raises_error(self):
        """Test processing invalid data raises ValueError."""
        # Arrange
        invalid_data = [{"invalid": "data"}]
        
        # Act & Assert
        with pytest.raises(ValueError, match="Invalid data format"):
            self.processor.process(invalid_data)
    
    @patch('meridianalgo.processor.external_api')
    def test_process_with_external_dependency(self, mock_api):
        """Test processing with mocked external dependency."""
        # Arrange
        mock_api.return_value = {"status": "success"}
        
        # Act
        result = self.processor.process_with_api()
        
        # Assert
        assert result["status"] == "success"
        mock_api.assert_called_once()
```

## Performance Guidelines

### Code Optimization

- **Profiling**: Profile code before optimizing
- **Bottlenecks**: Focus on critical performance bottlenecks
- **Memory Management**: Consider memory usage and cleanup
- **Caching**: Implement appropriate caching strategies

### Database Operations

- **Query Optimization**: Use efficient queries and indexes
- **Connection Management**: Properly manage database connections
- **Batch Operations**: Use batch processing for large datasets
- **Transaction Management**: Handle transactions appropriately

## Security Guidelines

### Input Validation

- **Sanitize Inputs**: Validate and sanitize all user inputs
- **Type Checking**: Use strict type checking
- **Length Limits**: Implement appropriate length limits
- **Format Validation**: Validate data formats and patterns

### Authentication & Authorization

- **Secure Storage**: Never store credentials in code
- **Environment Variables**: Use environment variables for secrets
- **Least Privilege**: Apply principle of least privilege
- **Session Management**: Implement secure session handling

## Tools and Automation

### Required Tools

- **Linting**: ESLint, Pylint, or equivalent
- **Formatting**: Prettier, Black, or equivalent
- **Testing**: Jest, pytest, or equivalent
- **Type Checking**: TypeScript, mypy, or equivalent

### CI/CD Integration

- **Automated Testing**: Run tests on every commit
- **Code Quality**: Automated code quality checks
- **Security Scanning**: Automated vulnerability scanning
- **Dependency Checks**: Automated dependency vulnerability checks

## Documentation Standards

### Code Documentation

- **Docstrings**: Comprehensive docstrings for all public functions
- **Comments**: Explain complex logic and business rules
- **Examples**: Provide usage examples in documentation
- **Changelog**: Maintain changelog for significant changes

### API Documentation

- **OpenAPI/Swagger**: For REST APIs
- **JSDoc**: For JavaScript APIs
- **Sphinx**: For Python documentation
- **Interactive Examples**: Include working examples

## Monitoring and Logging

### Logging Standards

- **Structured Logging**: Use structured logging formats
- **Log Levels**: Appropriate use of log levels (DEBUG, INFO, WARN, ERROR)
- **Sensitive Data**: Never log sensitive information
- **Performance Metrics**: Include performance metrics in logs

### Error Handling

- **Graceful Degradation**: Handle errors gracefully
- **Error Messages**: Provide clear, actionable error messages
- **Recovery**: Implement error recovery mechanisms
- **Monitoring**: Monitor error rates and patterns

## Continuous Improvement

### Code Quality Metrics

- **Code Coverage**: Track and maintain test coverage
- **Code Complexity**: Monitor cyclomatic complexity
- **Technical Debt**: Track and address technical debt
- **Performance Metrics**: Monitor key performance indicators

### Regular Reviews

- **Monthly Audits**: Regular code quality audits
- **Tool Updates**: Keep tools and dependencies updated
- **Guideline Updates**: Review and update guidelines regularly
- **Training**: Provide ongoing training for contributors

---

These guidelines are regularly updated to reflect best practices and community feedback. Last updated: January 2026
