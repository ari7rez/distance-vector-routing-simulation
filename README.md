# Distance Vector Assignment Roadmap
# this road map draft template created via AI 

## Stage 1: Foundation & Understanding (Days 1-2)

### 1.1 Study Phase

Tasks:
- [X] Read DV algorithm in course notes & Kurose-Ross 5.2.2
- [X] Study Wikipedia DV entry
- [X] Commit: "Initial algorithm study - key concepts understood"

### 1.2 Manual Calculation Practice

Files to create:
- `manual_calculations.md` - Your hand-worked examples
- `sample_topology.txt` - Copy the provided sample input

Tasks:
- [X] Manually work through the sample topology step-by-step
- [X] Calculate expected distance tables for each round
- [X] Calculate final routing tables
- [X] Commit: "Manual calculation complete - understand convergence"

---

## Stage 2: Planning & Design (Days 2-3)

### 2.1 Implementation Planning

Files to create:
- `design.md` - Your implementation plan
- `data_structures.md` - Planned data structures

Tasks:
- [x] Choose Python as language
- [x] Design data structures:
  ```python
  # Distance tables: dict of dict
  # Routing tables: dict 
  # Topology: dict of neighbors
  ```
- [x] Plan input parsing strategy
- [x] Plan output formatting
- [x] Commit: "Add design documentation and data structure planning"

### 2.2 Test Case Planning

Files to create:
- `test_cases/` directory
- `test_cases/simple_3node.txt` - Basic 3-node test
- `test_cases/expected_output_3node.txt` - Expected results

Tasks:
- [x] Create 2-3 simple test topologies
- [x] Manually calculate expected outputs
- [x] Commit: "Add initial test cases and expected outputs"

---

## Stage 3: Basic Implementation (Days 3-5)

### 3.1 Input Parsing

Files to create:
- `DistanceVector` (Python file)

Step 3 Tasks:
- [x] Add shebang: `#!/usr/bin/env python3`
- [x] Implement topology input parsing
- [x] Test with sample input
- [x] Commit: "Implement topology input parsing"

Step 4 Tasks:
- [X] Implement update parsing until END keyword
- [X] Handle -1 weight values for link removal  
- [X] Test with complete sample input
- [X] Commit: "Implement topology update parsing"

Step 5 Tasks:
- [X] Implement update parsing until END keyword
- [X] Handle -1 weight values for link removal
- [X] Test with complete sample input
- [X] Commit: "Implement topology update parsing"

### 3.2 Data Structure Setup

Step 6 Tasks:
- [x] Implement distance table initialization
- [x] Implement routing table structures
- [x] Add debug output for verification
- [x] Commit: "Add distance and routing table data structures"

Step 7 Tasks:
- [x] Implement distance initialization logic
- [x] Set direct neighbor costs from topology
- [x] Set INF for non-neighbor routes  
- [x] Commit:"Implement distance table initialization logic"

### 3.3 Basic DV Algorithm

Tasks:
- [ ] Implement distance vector exchange
- [ ] Implement table updates
- [ ] Add convergence detection
- [ ] Commit: "Implement core Distance Vector algorithm"

---

## Stage 4: Testing & Refinement (Days 5-7)

### 4.1 Output Formatting

Files to create:
- `output_formatter.py` (if you modularize)

Tasks:
- [ ] Implement required output format
- [ ] Test output against expected format
- [ ] Commit: "Implement required output formatting"

### 4.2 Initial Testing

Files to create:
- `test_script.sh` - Automated testing script
- `results/` directory for test outputs

Tasks:
- [ ] Test with sample topology
- [ ] Compare output with manual calculations
- [ ] Fix any discrepancies
- [ ] Commit: "Fix algorithm issues found in testing"

### 4.3 Gradescope Submission #1

Tasks:
- [ ] Submit to Gradescope for acceptance testing
- [ ] Fix any issues found
- [ ] Commit: "Fix issues from Gradescope acceptance testing"

---

## Stage 5: Enhanced Testing (Days 7-9)

### 5.1 Additional Test Cases

Files to create:
- `test_cases/complex_topology.txt`
- `test_cases/link_failure.txt`
- `test_cases/various_weights.txt`

Tasks:
- [ ] Create and test multiple topologies
- [ ] Test topology updates/changes
- [ ] Verify convergence in all cases
- [ ] Commit: "Add comprehensive test suite and fix edge cases"

### 5.2 Code Quality Review

Tasks:
- [ ] Add method documentation
- [ ] Clean up variable names
- [ ] Remove magic numbers
- [ ] Ensure methods < 80 lines
- [ ] Commit: "Code quality improvements and documentation"

---

## Stage 6: Poisoned Reverse (Days 9-11) - BONUS

### 6.1 Algorithm Study

Tasks:
- [ ] Study poisoned reverse mechanism
- [ ] Plan implementation differences
- [ ] Commit: "Studied poisoned reverse algorithm"

### 6.2 Implementation

Files to create:
- `PoisonedReverse` (Python file)

Tasks:
- [ ] Copy DistanceVector as starting point
- [ ] Implement poisoned reverse logic
- [ ] Test with same topologies
- [ ] Commit: "Implement poisoned reverse algorithm"

---

## Stage 7: Final Testing & Submission (Days 11-12)

### 7.1 Final Validation

Tasks:
- [ ] Test both programs thoroughly
- [ ] Verify all edge cases
- [ ] Clean up any remaining issues
- [ ] Commit: "Final testing and bug fixes"

### 7.2 Submission Preparation

Files to check:
- [ ] `DistanceVector` (working Python file)
- [ ] `PoisonedReverse` (working Python file, if doing bonus)
- [ ] All test cases and documentation

Tasks:
- [ ] Final Gradescope submission
- [ ] Verify GitHub repository is complete
- [ ] Commit: "Final submission ready"

---

## Detailed Commit Message Template

```
[Stage X.Y] Brief description

What was accomplished:
- Specific changes made
- Features implemented
- Bugs fixed

What was learned:
- New concepts understood
- Algorithm insights gained
- Technical decisions made

Challenges faced:
- Problems encountered
- How they were solved
- What didn't work

Next steps:
- What to tackle next
- Remaining tasks
- Areas needing attention

Testing results:
- What was tested
- Results observed
- Issues found
```

---

## Key Success Factors

1. Commit frequently - Aim for 1-2 commits per day minimum
2. Use detailed commit messages - Document learning progression
3. Test early and often - Don't wait until the end
4. Start with simple cases - Build complexity gradually
5. Use Gradescope early - Don't wait for perfection

---

## Important Reminders

### Development Process (Worth 150 marks!)
- Regular commits with detailed messages showing learning progression
- Evidence of iterative development, not sudden code appearance
- Clear documentation of testing and debugging process through commits
- Commit messages must show what you learned and challenges faced

### Code Quality Checklist
- [ ] Comments above each method header (purpose, inputs, outputs)
- [ ] Special cases documented in comments
- [ ] Modular code following cohesion/coupling principles
- [ ] No magic numbers
- [ ] Proper variable names (not incomprehensible)
- [ ] Methods under 80 lines
- [ ] No TODO blocks remaining
- [ ] No spelling errors in comments

### Testing Strategy
- [ ] Manual calculation of expected results BEFORE coding
- [ ] Test with provided sample topology first
- [ ] Create additional test topologies
- [ ] Test topology changes/updates
- [ ] Verify convergence in all scenarios
- [ ] Use input/output redirection for testing
- [ ] Compare outputs with expected results using diff

### Submission Requirements
- [ ] Python files with proper shebang: `#!/usr/bin/env python3`
- [ ] UNIX line endings (test on uni system)
- [ ] Programs named exactly: `DistanceVector` and `PoisonedReverse`
- [ ] No file extensions (.py) for final submission
- [ ] All code works on submission system, not just personal machine

---

## VS CODE SETUP READY

Now let's set up your VS Code project structure!