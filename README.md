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

step 8 Tasks:
- [x] Implement distance vector exchange
- [x] Implement table updates
- [x] Add convergence detection
- [x] Commit: "Implement core Distance Vector algorithm"

---

## Stage 4: Testing & Refinement (Days 5-7)

### 4.1 Output Formatting



Step 9 Tasks:
- [x] Implement required output format
- [x] Test output against expected format
- [x] Test algorithm convergence in 3 rounds
- [x] Commit: "Implement required output formatting"

Step 10 Tasks:
- [x] Add routing table generation from distance tables
- [x] Implement best route selection with tie-breaking
- [x] Print routing tables in CSV format
- [x] Commit:"Implement routing table generation and printing"
- [x] Fix duplicate convergence blocks bug

### 4.2 Initial Testing

Tasks:
- [x] Test with sample topology
- [x] Compare output with manual calculations
- [x] Fix any discrepancies

Step 11 Tasks (FINAL STEP):
- [x] Restructure main() to handle UPDATE and END triggers
- [x] Implement apply_topology_updates() function
- [x] Handle link removal with -1 weight values
- [x] Handle new node addition in updates
- [x] Run DV algorithm twice with topology changes
- [x] Test complete assignment with sample input
- [x] Commit: "ASSIGNMENT COMPLETE - Successfully implemented topology updates and dual algorithm runs"

### 4.3 Gradescope Submission #1
Step 12
Tasks:
- [x] Submit to Gradescope for acceptance testing
- [x] Fix any issues found
- [x] Commit: "Fix issues from Gradescope acceptance testing"
### 4.4 Critical Fixes for Gradescope (Step 12a-12f)

**Step 12a**: Fix syntax error
- [x] Fix `def def` → `def`
- [x] Commit: "Fix syntax error in run_dv_algorithm"

**Step 12b**: Show only neighbors in tables
- [x] Update print_distance_tables to show only neighbor columns
- [x] Commit: "Update distance table display to show only neighbors"

**Step 12c**: Track historical neighbors
- [x] Add ever_neighbors tracking for removed links
- [x] Commit: "Add historical neighbor tracking"

**Step 12d**: Fix convergence at t=2
- [x] Check convergence BEFORE updating tables
- [x] Commit: "Fix convergence detection - now converges at t=2"

**Step 12e**: Preserve routing info
- [x] Save routing tables before updates
- [x] Use previous costs when reinitializing
- [x] Commit: "Preserve routing information during topology updates"

**Step 12f**: Continue time steps
- [x] Time continues from t=3 (not reset to t=0)
- [x] Commit: "Fix time step continuity after updates"

**Verify**: 
- [x] Converges at t=2, continues at t=3
- [x] Shows all historical neighbors after link removal
- [x] Output matches expected exactly

---

## Stage 5: Enhanced Testing (Days 7-9)
Step 13-16

- [x] Remove all debug print statements for Gradescope compatibility
- [x] Fix algorithm calculation bug - use old_tables for synchronous updates
- [x] Verified Y-Z distance now correctly calculates as 12 (not 10)
- [x] Fix time step continuity between algorithm runs
- [x] Fix output spacing to match expected format exactly
- [x] Fix time sequence
- [x] Pass Gradescope acceptance tests
- [x] Commit:"Fixed DV equation to use previous round data for synchronous updates"
- [x] fixed more bugs and Enhanced apply_topology_updates()
### 5.1 Additional Test Cases

Tasks:
- [x] Create and test multiple topologies
- [x] Test topology updates/changes
- [x] Verify convergence in all cases
- [x] Commit: "Add comprehensive test suite and fix edge cases"

### 5.2 Code Quality Review

Tasks:
- [x] Add method documentation
- [x] Clean up variable names
- [x] Remove magic numbers
- [x] Ensure methods < 80 lines
- [x] Commit: "Code quality improvements and documentation"

---

## Stage 6: Poisoned Reverse (Days 9-11) - BONUS

### 6.1 Algorithm Study

Tasks:
- [X] Study poisoned reverse mechanism
- [X] Plan implementation differences
- [X] Commit: "Studied poisoned reverse algorithm"

### 6.2 Implementation

Files to create:
- `PoisonedReverse` (Python file)

Tasks:
- [X] Copy DistanceVector as starting point
- [x] Implement poisoned reverse logic
- [x] Test with same topologies
- [x] Commit: "Implement poisoned reverse algorithm"

---

## Stage 7: Final Testing & Submission (Days 11-12)

### 7.1 Final Validation

Tasks:
- [x] Test both programs thoroughly
- [X] Verify all edge cases
- [X] Clean up any remaining issues
- [x] Commit: "Final testing and bug fixes"

### 7.2 Submission Preparation

Files to check:
- [X] `DistanceVector` (working Python file)
- [X] `PoisonedReverse` (working Python file, if doing bonus)
- [x] All test cases and documentation

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
- [x] Manual calculation of expected results BEFORE coding
- [x] Test with provided sample topology first
- [x] Create additional test topologies
- [x] Test topology changes/updates
- [x] Verify convergence in all scenarios
- [x] Use input/output redirection for testing
- [x] Compare outputs with expected results using diff

### Submission Requirements
- [X] Python files with proper shebang: `#!/usr/bin/env python3`
- [X] UNIX line endings (test on uni system)
- [X] Programs named exactly: `DistanceVector` and `PoisonedReverse`
- [X] No file extensions (.py) for final submission
- [X] All code works on submission system, not just personal machine

---