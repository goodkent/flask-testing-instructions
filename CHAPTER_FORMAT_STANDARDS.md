# Chapter Format Standards

## Mandatory Formatting Requirements for All Chapters

Every chapter must follow these exact formatting standards to maintain consistency across the course.

---

## 0. HTML Head Section (Required Structure)

**Location:** Every chapter file must start with this exact head structure

**Format:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chapter X: Chapter Title - Flask Testing Mastery</title>
    <link rel="stylesheet" href="css/style.css">
    <link rel="stylesheet" href="css/prism.css">
</head>
<body>
    <div class="container">
```

**Rules:**
- **CRITICAL:** Use local `css/prism.css` for syntax highlighting (dark VSCode theme)
- Include proper meta tags for charset and viewport
- Title format: "Chapter X: Chapter Title - Flask Testing Mastery"
- Main stylesheet link: `css/style.css`
- Prism stylesheet: `css/prism.css` (local file, not CDN)
- No line-numbers plugin CSS (we don't use line numbers)

**Why css/prism.css:**
- Custom dark theme (VSCode-style with #1e1e1e background)
- Provides excellent contrast for code readability
- Professional appearance
- Consistent across all chapters
- Faster loading (local vs CDN)

---

## 1. Top Navigation Block

**Location:** Immediately after opening `<div class="container">`

### Chapter 1 Format:
```html
<div class="nav-links">
    <a href="index.html">← Index</a>
    <a href="chapter02.html">Next Chapter →</a>
</div>

<h1>Chapter 1: Chapter Title</h1>
<p class="chapter-subtitle">Brief subtitle describing the chapter</p>
```

### Chapters 2-14 Format:
```html
<div class="nav-links">
    <a href="chapterXX.html">← Previous Chapter</a>
    <a href="index.html">Index</a>
    <a href="chapterYY.html">Next Chapter →</a>
</div>

<h1>Chapter X: Chapter Title</h1>
<p class="chapter-subtitle">Brief subtitle describing the chapter</p>
```

### Chapter 15 (Final) Format:
```html
<div class="nav-links">
    <a href="chapter14.html">← Previous Chapter</a>
    <a href="index.html">Index</a>
</div>

<h1>Chapter 15: Chapter Title</h1>
<p class="chapter-subtitle">Brief subtitle describing the chapter</p>
```

**Rules:**
- Use `<div class="nav-links">` wrapper
- Chapter 1: Only Index and Next Chapter (no previous)
- Chapters 2-14: Previous Chapter | Index | Next Chapter (three links with spacing)
- Chapter 15: Only Previous Chapter and Index (no next)
- **NO chapter titles in navigation links** (e.g., "Next Chapter →" not "Next: Chapter 3 - Title →")
- Use arrows: `←` for previous/index, `→` for next
- Links are simple: "← Previous Chapter", "Index", "Next Chapter →"
- The CSS provides spacing, so just list the links cleanly

---

## 2. GitHub Links Section

**Location:** Immediately after chapter subtitle

**Format:**
```html
<div class="github-links">
    <span class="github-label">Chapter Code:</span>
    <a href="https://github.com/goodkent/flask-testing/tree/chXX-end" class="github-link">Browse</a>
    <a href="https://github.com/goodkent/flask-testing/archive/refs/tags/chXX-end.zip" class="github-link">Zip</a>
    <a href="https://github.com/goodkent/flask-testing/compare/chXX-end...chXX-end" class="github-link">Diff</a>
</div>
```

**Rules:**
- Use inline format (not bullet list)
- Include `<span class="github-label">Chapter Code:</span>` label
- All links use `class="github-link"`
- Replace XX with two-digit chapter number (01, 02, 03, etc.)
- Diff link compares previous chapter to current chapter

**Tag Naming Convention:**
- Chapter 1 end: `ch01-end`
- Chapter 2 end: `ch02-end`
- Chapter 3 end: `ch03-end`
- etc.

---

## 3. Introduction Section

**Location:** After GitHub links

**Format:**
```html
<div class="intro-section">
    <p>Welcome back! [Connect to previous chapter...]</p>
    <p>[Explain what this chapter covers...]</p>
    <!-- Additional intro paragraphs -->
</div>

<h2>Learning Objectives</h2>
<ul>
    <li>Objective 1</li>
    <li>Objective 2</li>
    <li>Objective 3</li>
</ul>
```

**Rules:**
- Wrap intro paragraphs in `<div class="intro-section">`
- Start with "Welcome back!" for chapters 2+
- Learning Objectives immediately follows intro section
- 4-6 specific, actionable objectives

---

## 4. Chapter Content

Follow standard content structure with proper headings hierarchy:
- `<h2>` for main sections
- `<h3>` for subsections
- Use `<div class="note">` for important notes
- Use `<div class="troubleshooting">` for troubleshooting sections
- Use `<div class="exercise">` for hands-on exercises

---

## 5. Chapter Conclusion: "What We've Learned" Section

**Location:** Near end of chapter, before "Before You Continue"

**Format:**
```html
<h2>What We've Learned</h2>

<p>Take a moment to appreciate everything you've accomplished in this chapter:</p>

<ul>
    <li>✓ You can [skill/concept 1]</li>
    <li>✓ You understand [skill/concept 2]</li>
    <li>✓ You know how to [skill/concept 3]</li>
    <li>✓ You've learned [skill/concept 4]</li>
    <!-- 5-7 items total -->
</ul>

<p>[Celebratory closing statement about their progress]</p>
```

**Rules:**
- Title is always "What We've Learned"
- Use checkmark (✓) before each bullet point
- Each bullet starts with: "You can", "You understand", "You know how to", "You've learned"
- Include 5-7 accomplishments
- End with an encouraging statement

---

## 6. "Before You Continue..." Section

**Location:** After "What We've Learned", before "Next Up"

**Format:**
```html
<h2>Before You Continue...</h2>

<p>Before moving on to Chapter X, make sure you:</p>

<ol>
    <li>Verification item 1</li>
    <li>Verification item 2</li>
    <li>Verification item 3</li>
    <li>Verification item 4</li>
</ol>

<p>If something doesn't make complete sense yet, that's okay! [Encouraging statement about learning throughout the course]</p>
```

**Rules:**
- Title is always "Before You Continue..."
- Use ordered list (`<ol>`)
- 4-5 specific checks/prerequisites
- End with encouraging "it's okay" statement
- Reference "throughout this course" or similar

---

## 7. "Next Up" Preview Section

**Location:** After "Before You Continue"

**Format:**
```html
<div class="success">
    <strong>Next Up:</strong> In Chapter X, [brief exciting preview of what's coming]. [Specific examples of what they'll build/learn]. [Encouraging connection to current chapter]!
</div>
```

**Rules:**
- Must use `<div class="success">` wrapper
- Start with `<strong>Next Up:</strong>`
- 2-4 sentences
- Mention specific chapter number
- Be specific about what they'll build/learn
- Use exciting, forward-looking language
- End with exclamation point

**Example:**
```html
<div class="success">
    <strong>Next Up:</strong> In Chapter 4, you're going to learn about testing forms and validation. You'll discover how to test WTForms, handle CSRF protection in tests, and even test file uploads. Forms are where users interact with your application, so testing them well is crucial. You'll create registration and login forms for FlaskBlog Pro and test every aspect of form validation!
</div>
```

---

## 8. Bottom Navigation Links

**Location:** After "Next Up" section, before footer

### Chapter 1 Format:
```html
<div class="nav-links">
    <a href="index.html">← Index</a>
    <a href="chapter02.html">Next Chapter →</a>
</div>
```

### Chapters 2-14 Format:
```html
<div class="nav-links">
    <a href="chapterXX.html">← Previous Chapter</a>
    <a href="index.html">Index</a>
    <a href="chapterYY.html">Next Chapter →</a>
</div>
```

### Chapter 15 (Final) Format:
```html
<div class="nav-links">
    <a href="chapter14.html">← Previous Chapter</a>
    <a href="index.html">Index</a>
</div>
```

**Rules:**
- Use `<div class="nav-links">` wrapper
- **Same format as top navigation** (keep it consistent)
- Chapter 1: Two links (Index | Next Chapter)
- Chapters 2-14: Three links (Previous Chapter | Index | Next Chapter)
- Chapter 15: Two links (Previous Chapter | Index)
- **NO chapter titles** in navigation links
- Simple text: "← Previous Chapter", "Index", "Next Chapter →"
- Use arrows: `←` for previous/index, `→` for next

---

## 9. Footer

**Location:** After navigation links, before closing `</div>` (container)

**Format:**
```html
<footer>
    <p>Flask Testing Mastery - A comprehensive course on testing Flask applications</p>
    <p style="font-size: 0.9em;">Questions or feedback? Let me know!</p>
</footer>
```

**Rules:**
- Exact text as shown
- Two paragraphs
- Second paragraph has inline style for smaller font
- Same footer for all chapters (no variations)

---

## 10. Scripts Section

**Location:** After footer, before closing `</body>`

**Format:**
```html
<!-- Prism.js for syntax highlighting -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-python.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-bash.min.js"></script>
</body>
</html>
```

**Rules:**
- Include comment explaining purpose
- Three scripts: core, Python, Bash
- Only add additional language scripts if needed (rare)
- **Do NOT include line-numbers plugin** (we don't use line numbers)
- **CSS theme is in head section:** See section 0 for `prism-tomorrow.min.css` requirement

**Complete Head-to-Close Structure:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="stylesheet" href="css/style.css">
    
    <!-- Prism.js CSS for syntax highlighting -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css" rel="stylesheet" />
</head>
<body>
    <!-- Chapter content here -->
    
    <!-- Prism.js for syntax highlighting -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-python.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-bash.min.js"></script>
</body>
</html>
```

---

## Complete Chapter End Template (Chapters 2-14)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chapter X: Chapter Title - Flask Testing Mastery</title>
    <link rel="stylesheet" href="css/style.css">
    
    <!-- Prism.js CSS for syntax highlighting -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css" rel="stylesheet" />
</head>
<body>
    <div class="container">
        <!-- Chapter content... -->
        
        <h2>What We've Learned</h2>

        <p>Take a moment to appreciate everything you've accomplished in this chapter:</p>

        <ul>
            <li>✓ You can [accomplishment 1]</li>
            <li>✓ You understand [accomplishment 2]</li>
            <li>✓ You know how to [accomplishment 3]</li>
            <li>✓ You've learned [accomplishment 4]</li>
            <li>✓ [Additional accomplishments as needed]</li>
        </ul>

        <p>[Celebratory closing statement]</p>

        <h2>Before You Continue...</h2>

        <p>Before moving on to Chapter X, make sure you:</p>

        <ol>
            <li>Prerequisite/check 1</li>
            <li>Prerequisite/check 2</li>
            <li>Prerequisite/check 3</li>
            <li>Prerequisite/check 4</li>
        </ol>

        <p>If something doesn't make complete sense yet, that's okay! [Encouraging statement]</p>

        <div class="success">
            <strong>Next Up:</strong> In Chapter X, [preview of next chapter content]. [Specific examples]. [Connection to current work]!
        </div>

        <div class="nav-links">
            <a href="chapterXX.html">← Previous Chapter</a>
            <a href="index.html">Index</a>
            <a href="chapterYY.html">Next Chapter →</a>
        </div>

        <footer>
            <p>Flask Testing Mastery - A comprehensive course on testing Flask applications</p>
            <p style="font-size: 0.9em;">Questions or feedback? Let me know!</p>
        </footer>
    </div>

    <!-- Prism.js for syntax highlighting -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-python.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-bash.min.js"></script>
</body>
</html>
```

---

## Quality Checklist

Before finalizing any chapter, verify:

- [ ] **HTML Head uses prism-tomorrow.min.css** (dark theme, NOT prism.min.css)
- [ ] No line-numbers plugin CSS or JS (we don't use line numbers)
- [ ] Navigation at top matches chapter position (Ch1: 2 links, Ch2-14: 3 links, Ch15: 2 links)
- [ ] Navigation at bottom matches top navigation exactly
- [ ] NO chapter titles in navigation links (e.g., "Next Chapter →" not "Next: Chapter 3 - Title")
- [ ] GitHub links use inline format with proper classes
- [ ] Intro wrapped in `<div class="intro-section">`
- [ ] "What We've Learned" section with checkmarks (✓)
- [ ] "Before You Continue..." with ordered list
- [ ] "Next Up" in `<div class="success">` wrapper
- [ ] Navigation uses `<div class="nav-links">`
- [ ] Footer matches exact format
- [ ] Prism.js scripts included (core, Python, Bash - no line-numbers)
- [ ] Proper spacing between navigation links (CSS handles this)

---

## Common Mistakes to Avoid

❌ **Don't:**
- Include chapter titles in navigation links ("Next: Chapter 3 - Database Testing")
- Use different navigation at top vs bottom of chapter
- Use "Back to Index" (should be just "Index")
- Format GitHub links as bullet lists
- Use "Looking Ahead" instead of "What We've Learned"
- Use `<div class="navigation">` (should be `<div class="nav-links">`)
- Vary footer text between chapters
- Forget the "Before You Continue..." section
- Put chapter previews in `<div class="note">` (should be `<div class="success">`)
- Use different link text like "Previous: Chapter X" (should be "← Previous Chapter")

✅ **Do:**
- Keep navigation simple: "← Previous Chapter", "Index", "Next Chapter →"
- Use same navigation format at top and bottom
- Keep all chapters perfectly consistent
- Use the exact HTML structures shown above
- Include all required sections in order
- Maintain encouraging, forward-looking tone
- Reference FlaskBlog Pro project consistently
- Remember: Chapter 1 has no previous, Chapter 15 has no next

---

## Navigation Visual Examples

### ❌ WRONG - Don't include chapter titles:
```html
<div class="nav-links">
    <a href="chapter02.html">← Previous: Chapter 2 - Unit Testing Routes</a>
    <a href="index.html">Back to Index</a>
    <a href="chapter04.html">Next: Chapter 4 - Testing Forms →</a>
</div>
```

### ✅ CORRECT - Simple, clean navigation:
```html
<div class="nav-links">
    <a href="chapter02.html">← Previous Chapter</a>
    <a href="index.html">Index</a>
    <a href="chapter04.html">Next Chapter →</a>
</div>
```

### ✅ CORRECT - Chapter 1 (no previous):
```html
<div class="nav-links">
    <a href="index.html">← Index</a>
    <a href="chapter02.html">Next Chapter →</a>
</div>
```

### ✅ CORRECT - Chapter 15 (no next):
```html
<div class="nav-links">
    <a href="chapter14.html">← Previous Chapter</a>
    <a href="index.html">Index</a>
</div>
```

---

## Key Principles

1. **Simplicity**: Navigation should be clean and minimal
2. **Consistency**: Top and bottom navigation must match exactly
3. **Clarity**: Users should immediately know where each link goes
4. **Spacing**: CSS handles spacing - just list links cleanly in the div
5. **No Titles**: Chapter titles belong in headers, not navigation links
