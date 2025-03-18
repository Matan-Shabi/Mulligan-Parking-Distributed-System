# Test Execution Report

| # | Artifact Tested | Pre-conditions | Test Steps | Expected Result | Passed? |
|---|----------------|----------------|------------|-----------------|---------|
{{#each tests}}
| {{@index}} | {{className}} | {{preConditions}} | {{testSteps}} | {{expectedResult}} | {{#if passed}}✅{{else}}❌{{/if}} |
{{/each}}

### Summary
- Total Tests: {{total}}
- Passed: {{passed}}
- Failed: {{failed}}
- Skipped: {{skipped}} 