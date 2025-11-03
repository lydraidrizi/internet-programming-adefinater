# Hugo Books Exam Grading Rubric

## Quick Reference
- **Total Points**: 100 (+ 25 bonus)
- **Pass Threshold**: 60%
- **Excellence Threshold**: 90%

## Tier 1: Basic Functionality (60 points)

### Table Display (25 points)
**Full Credit (25 pts):**
- ✅ All 7 required columns displayed correctly
- ✅ Data loads from JSON file
- ✅ Proper formatting (series false → "None", genres as comma-separated)
- ✅ Responsive table layout

**Partial Credit:**
- Missing 1-2 columns: -5 pts each
- Poor formatting: -3 pts
- Non-responsive: -3 pts
- Data doesn't load: -10 pts

### Sorting (20 points)
**Full Credit (20 pts):**
- ✅ Click column headers to sort
- ✅ Toggle ascending/descending
- ✅ Works for text, numbers, and booleans
- ✅ Visual indicators (arrows/highlighting)

**Partial Credit:**
- Sorting works but no toggle: -5 pts
- Some columns don't sort: -3 pts each
- No visual indicators: -2 pts
- Broken sort logic: -10 pts

### Text Filter (10 points) 
**Full Credit (10 pts):**
- ✅ Text input filters by title
- ✅ Case-insensitive
- ✅ Real-time filtering (no submit button)
- ✅ Partial matches work

**Partial Credit:**
- Case-sensitive only: -3 pts
- Requires submit/button: -3 pts
- Exact match only: -2 pts
- Doesn't work: -10 pts

### Loading/Error States (5 points)
**Full Credit (5 pts):**
- ✅ Shows loading indicator
- ✅ Handles fetch errors gracefully

**Partial Credit:**
- Missing loading state: -2 pts
- No error handling: -3 pts

## Tier 2: Edge Case Handling (25 points)

### Data Edge Cases (15 points)
**Test with provided edge case books:**

**series: false handling (4 pts):**
- ✅ Displays "None" or "—" instead of "false"
- ❌ Shows "false" or crashes: -4 pts

**Empty genres array (3 pts):**
- ✅ Shows "None" or "—" for empty arrays
- ❌ Shows empty or crashes: -3 pts

**Multiple genres display (3 pts):**
- ✅ Shows all genres, comma-separated
- ❌ Shows only first genre: -1 pt
- ❌ Poor formatting: -2 pts

**Long titles (3 pts):**
- ✅ Handles overflow gracefully (wrap/ellipsis)
- ❌ Breaks layout: -3 pts

**Special characters (2 pts):**
- ✅ Displays quotes, apostrophes correctly
- ❌ Encoding issues: -2 pts

### Advanced Filtering (10 points)
**No results state (5 pts):**
- ✅ Shows "No books found" or similar
- ❌ Shows empty table: -2 pts
- ❌ Crashes: -5 pts

**Filter robustness (5 pts):**
- ✅ Works with edge case data
- ✅ Handles special characters in search
- ❌ Crashes on edge cases: -5 pts

## Tier 3: Advanced Features (15 points)
**Must choose 2 of 4 options. Each worth 7.5 points.**

### Performance Optimization (7.5 pts)
- ✅ Handles 100+ books smoothly: 4 pts
- ✅ Includes optimization comment: 3.5 pts
- Partial: Works but slow: 3 pts

### Multi-Column Sorting (7.5 pts)
- ✅ Shift+click adds secondary sort: 4 pts
- ✅ Visual indicators of sort order: 3.5 pts
- Partial: Basic multi-sort: 4 pts

### Advanced Filtering (7.5 pts)
- ✅ Winner/Nominee dropdown: 3 pts
- ✅ Decade filter: 2.5 pts
- ✅ Has Series filter: 2 pts
- Partial: 1-2 filters working: 4 pts

### Smart Search Relevance (7.5 pts)
- ✅ Exact title matches first: 3 pts
- ✅ Progressive relevance ranking: 3 pts
- ✅ Clear relevance logic: 1.5 pts
- Partial: Basic relevance: 4 pts

## Bonus Features (25 points total)
**Each worth 5 points:**

1. **CSV Export (5 pts):**
   - ✅ Downloads filtered results: 5 pts
   - Partial: Basic export: 3 pts

2. **Genre Filter (5 pts):**
   - ✅ Multi-select dropdown: 5 pts
   - Partial: Single select: 3 pts

3. **Year Range Filter (5 pts):**
   - ✅ Slider or dual inputs: 5 pts
   - Partial: Basic year filter: 3 pts

4. **Author Filter (5 pts):**
   - ✅ Dropdown from data: 5 pts
   - Partial: Basic implementation: 3 pts

5. **Publisher Filter (5 pts):**
   - ✅ Dropdown from data: 5 pts
   - Partial: Basic implementation: 3 pts

## Deductions

### Major Issues
- **Page doesn't load (-15 pts):** Code has syntax errors
- **Crashes on interaction (-10 pts):** Unhandled exceptions
- **Console errors on load (-5 pts):** JavaScript errors in console

### Minor Issues  
- **Poor code quality (-3 pts):** No indentation, unclear variable names
- **Missing basic CSS (-3 pts):** Unstyled or very poor appearance
- **Non-functional HTML (-2 pts):** Invalid markup, accessibility issues

## Grade Boundaries

| Grade | Points | Description |
|-------|--------|-------------|
| A+ | 95-100+ | Excellent implementation with bonus features |
| A | 90-94 | Strong work, all tiers completed well |
| A- | 85-89 | Good work, minor issues in Tier 3 |
| B+ | 80-84 | Solid Tiers 1&2, attempted Tier 3 |
| B | 75-79 | Complete Tiers 1&2, minimal Tier 3 |
| B- | 70-74 | Good Tier 1, partial Tier 2 |
| C+ | 65-69 | Complete Tier 1, minimal Tier 2 |
| C | 60-64 | Complete Tier 1 only |
| F | 0-59 | Incomplete Tier 1 |

## Testing Checklist

### Functionality Tests
- [ ] Table displays all 24 books correctly
- [ ] All columns present and formatted
- [ ] Sort each column (both directions)
- [ ] Filter by various terms
- [ ] Test edge case books specifically
- [ ] Try filtering with no results
- [ ] Test special characters in search

### Edge Case Tests
- [ ] Books with `series: false` show "None"
- [ ] Books with empty genres show "None" 
- [ ] Long title book displays properly
- [ ] Special character book displays properly
- [ ] Multi-genre book shows all genres

### Advanced Feature Tests
- [ ] Performance with full dataset
- [ ] Advanced features work as specified
- [ ] Bonus features function correctly

## Common Student Mistakes

1. **Showing "false" instead of "None"** - loses 4 points
2. **Only showing first genre** - loses 1-2 points  
3. **Case-sensitive filter** - loses 3 points
4. **No loading state** - loses 2 points
5. **Poor handling of special characters** - loses 2 points
6. **Table breaks with long content** - loses 3 points
7. **No error handling** - loses 3 points

## Grader Notes
- Test with the exact provided dataset
- Check browser console for errors
- Verify responsiveness on different screen sizes
- Test all interactive features thoroughly
- Look for code comments explaining complex logic