# Issue Reporting Guidelines

## Overview

Effective issue reporting helps us maintain and improve our projects. This document provides guidelines for reporting bugs, requesting features, and submitting other types of issues.

## Before Creating an Issue

### Search First

- **Check existing issues**: Search for similar issues before creating a new one
- **Review documentation**: Check if your question is answered in our documentation
- **Look for FAQs**: Review frequently asked questions and common issues

### Verify the Issue

- **Reproducible**: Ensure you can reproduce the issue consistently
- **Current Version**: Confirm you're using the latest version
- **Environment**: Check if the issue is environment-specific

## Issue Types

### Bug Reports

For unexpected behavior or errors in our software.

#### Bug Report Template

```markdown
## Bug Description
Brief description of the bug

## Steps to Reproduce
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

## Expected Behavior
Clear and concise description of what you expected to happen

## Actual Behavior
Clear and concise description of what actually happened

## Environment
- OS: [e.g. Windows 10, macOS 11.0, Ubuntu 20.04]
- Browser: [e.g. Chrome 91.0, Firefox 89.0]
- Version: [e.g. v1.2.3]
- Python/Node version: [e.g. Python 3.9.0, Node 16.4.0]

## Additional Context
Add any other context about the problem here

## Screenshots
If applicable, add screenshots to help explain your problem

## Logs
Include relevant error logs or console output
```

### Feature Requests

For new functionality or enhancements.

#### Feature Request Template

```markdown
## Feature Description
Clear and concise description of the feature

## Problem Statement
What problem does this feature solve? What limitations exist in the current implementation?

## Proposed Solution
How would you like this feature to work? Include specific details

## Alternatives Considered
What alternative solutions or approaches have you considered?

## Additional Context
Add any other context, mockups, or examples about the feature request

## Implementation Ideas (Optional)
If you have ideas about how to implement this feature, please share them
```

### Documentation Issues

For problems with documentation, guides, or examples.

#### Documentation Issue Template

```markdown
## Documentation Issue Type
- [ ] Typo/Grammar
- [ ] Incorrect Information
- [ ] Missing Information
- [ ] Unclear Explanation
- [ ] Broken Link
- [ ] Outdated Content

## Location
Specify the document, section, or URL where the issue is located

## Issue Description
Clear description of the documentation issue

## Suggested Fix (Optional)
If you have a suggested fix, please provide it

## Additional Context
Any additional context about the documentation issue
```

### Performance Issues

For performance-related problems.

#### Performance Issue Template

```markdown
## Performance Issue Description
Description of the performance problem

## Performance Metrics
- Expected performance: [e.g. <100ms response time]
- Actual performance: [e.g. 2-3 seconds response time]
- Frequency: [e.g. always, sometimes, under specific conditions]

## Environment Details
- Hardware specifications
- Software versions
- Network conditions
- Database size/configuration

## Steps to Reproduce
Steps to reproduce the performance issue

## Profiling Data (Optional)
If you have profiling data, please include it

## Additional Context
Any other relevant information about the performance issue
```

## Issue Labels

Our team uses labels to categorize and prioritize issues:

### Priority Labels

- **critical**: Critical issues affecting core functionality
- **high**: Important issues that should be addressed soon
- **medium**: Normal priority issues
- **low**: Minor issues or nice-to-have features

### Type Labels

- **bug**: Bug reports
- **enhancement**: Feature requests
- **documentation**: Documentation issues
- **performance**: Performance-related issues
- **security**: Security vulnerabilities (use private reporting)
- **question**: General questions

### Status Labels

- **needs-triage**: New issues awaiting review
- **needs-information**: Issues requiring more information
- **in-progress**: Issues being worked on
- **ready-for-review**: Issues ready for review
- **duplicate**: Duplicate issues
- **wontfix**: Issues that will not be fixed

## Issue Triage Process

### Initial Review

1. **Acknowledge**: We acknowledge receipt within 48 hours
2. **Categorize**: Apply appropriate labels and assign priority
3. **Clarify**: Request additional information if needed
4. **Assign**: Assign to appropriate team member

### Resolution Process

1. **Investigation**: Thorough investigation of the issue
2. **Development**: Implementation of fix or feature
3. **Testing**: Comprehensive testing of the solution
4. **Review**: Code review and quality assurance
5. **Release**: Deployment of the fix or feature
6. **Communication**: Update the issue with resolution details

## Communication Guidelines

### For Reporters

- **Be Responsive**: Respond to clarification requests promptly
- **Provide Details**: Include all relevant information upfront
- **Stay Professional**: Maintain professional and respectful communication
- **Follow Up**: Check back on your issue periodically

### For Maintainers

- **Acknowledge Promptly**: Respond to new issues quickly
- **Be Clear**: Provide clear explanations and next steps
- **Set Expectations**: Communicate timelines and priorities
- **Close Appropriately**: Close issues with clear resolution details

## Security Issues

### Private Reporting

**Do not report security vulnerabilities in public issues.** Instead:

1. **Email**: security@meridianalgo.org
2. **Include**: Detailed information about the vulnerability
3. **Wait**: Allow us time to address the issue before disclosure

### Security Issue Process

1. **Assessment**: Evaluate vulnerability severity and impact
2. **Development**: Create and test security patches
3. **Coordination**: Coordinate with reporter on disclosure timeline
4. **Disclosure**: Public disclosure after patch deployment

## Issue Quality Standards

### Good Issue Reports Include

- **Clear Title**: Descriptive and specific title
- **Detailed Description**: Comprehensive explanation of the issue
- **Reproduction Steps**: Clear steps to reproduce the problem
- **Environment Information**: Relevant system and software details
- **Expected vs Actual**: Clear comparison of expected and actual behavior
- **Supporting Evidence**: Screenshots, logs, or other evidence

### Poor Issue Reports

- **Vague Titles**: Generic titles like "It doesn't work"
- **Insufficient Details**: Lack of specific information
- **No Reproduction Steps**: Unable to reproduce the issue
- **Missing Environment**: No system or version information
- **Multiple Issues**: Combining multiple unrelated issues

## Issue Lifecycle

### States

1. **Open**: Issue is created and awaiting triage
2. **Triage**: Issue is being reviewed and categorized
3. **In Progress**: Issue is being actively worked on
4. **Ready for Review**: Solution is ready for review
5. **Closed**: Issue is resolved or closed for other reasons

### Closure Reasons

- **Fixed**: Issue has been resolved
- **Duplicate**: Issue duplicates an existing issue
- **Wont Fix**: Issue will not be addressed (with explanation)
- **Not Reproducible**: Unable to reproduce the issue
- **Out of Scope**: Issue is outside project scope
- **No Response**: Reporter did not respond to clarification requests

## Community Guidelines

### Contributing to Issues

- **Help Others**: Assist fellow community members with their issues
- **Provide Solutions**: Suggest potential solutions or workarounds
- **Share Knowledge**: Share relevant experiences and insights
- **Be Constructive**: Provide helpful, constructive feedback

### Issue Etiquette

- **One Issue Per Report**: Keep each issue focused on one problem
- **Avoid Bumping**: Don't bump issues unnecessarily
- **Search First**: Avoid duplicate issues by searching first
- **Be Patient**: Understand that maintainers have limited time

## Tools and Resources

### Issue Tracking

- **GitHub Issues**: Primary issue tracking system
- **Project Boards**: Visual organization of issues and tasks
- **Milestones**: Tracking progress toward releases
- **Labels**: Categorization and filtering of issues

### Communication Channels

- **GitHub Issues**: Primary channel for issue discussions
- **Discussions**: General questions and community discussions
- **Discord/Slack**: Real-time community discussions
- **Email**: Private communications and security reports

## Getting Help

### Self-Service Resources

- **Documentation**: Comprehensive project documentation
- **FAQs**: Frequently asked questions
- **Examples**: Code examples and tutorials
- **Community Forums**: Community discussions and solutions

### Direct Support

- **GitHub Issues**: For bug reports and feature requests
- **GitHub Discussions**: For general questions
- **Email**: For private matters and security issues
- **Community Chat**: For real-time assistance

---

These guidelines help us maintain an efficient and effective issue management process. Thank you for helping us improve our projects!

*Last updated: January 2026*
