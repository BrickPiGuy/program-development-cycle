# The Program Development Cycle - Interactive Educational Website

A fun, interactive, and **fully accessible** website for teaching the Program Development Cycle in Introduction to Programming courses.

## 🎯 Features

### Educational Content
- **7-Step Development Cycle**: Interactive accordion cards explaining each step
- **Common Student Mistakes**: Expandable sections highlighting frequent errors
- **Dr. D's Insights**: Professional perspective on software development
- **Interactive Quiz**: Self-assessment tool to reinforce learning
- **Responsive Design**: Works seamlessly on all devices (mobile, tablet, desktop)

### Interactive Elements
- **Expandable Sections**: Click cycle steps and mistake cards to reveal detailed information
- **Smooth Scrolling**: Easy navigation between sections
- **Mobile Navigation**: Hamburger menu for smaller screens
- **Live Quiz Feedback**: Instant feedback on quiz answers

## ♿ Web Accessibility Standards

This website meets or exceeds **WCAG 2.1 Level AA** accessibility standards. Here's what we've implemented:

### 1. **Semantic HTML Structure**
- Proper heading hierarchy (h1, h2, h3, h4)
- Semantic elements: `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`
- Meaningful link text instead of generic "click here"
- Proper form structure with `<fieldset>` and `<legend>`

### 2. **ARIA Attributes**
- `aria-label`: Descriptive labels for interactive buttons
- `aria-expanded`: Indicates state of expandable/collapsible sections
- `aria-controls`: Links buttons to the content they control
- `aria-labelledby`: Associates headings with sections
- `aria-describedby`: Provides additional context for forms
- `aria-live`: Announces dynamic content changes
- `role` attributes: Clarifies interactive elements (menubar, alert, etc.)

### 3. **Keyboard Navigation**
- **Tab**: Navigate through all interactive elements
- **Enter/Space**: Expand/collapse accordions, submit forms
- **Escape**: Close mobile menu
- **Skip Link**: Jump directly to main content (hidden until focused)
- Logical tab order throughout the page

### 4. **Visual Accessibility**
- **Color Contrast**: 
  - Text on background: 4.5:1 ratio (WCAG AA for normal text)
  - Focus indicators: 3px solid outline with 2px offset
- **Focus Indicators**: Clearly visible on all interactive elements
- **Clear Visual Hierarchy**: Proper font sizing and spacing
- **No Color Dependency**: Information doesn't rely solely on color

### 5. **Screen Reader Support**
- All interactive elements have proper labels
- Hidden content marked with `[hidden]` attribute
- Form inputs have associated labels
- Error messages announced with `role="alert"`
- Status updates use `aria-live="polite"`

### 6. **Mobile & Responsive Design**
- Mobile-first approach
- Touch-friendly button sizes (minimum 44x44px)
- Responsive text sizing
- Flexible layouts using CSS Grid

### 7. **Form Accessibility**
- Radio buttons with proper `<label>` associations
- Grouped with `<fieldset>` and `<legend>`
- Clear error messages with ARIA alerts
- Keyboard navigable form controls

## 📁 File Structure

```
program-development-cycle/
├── index.html          # HTML structure with semantic markup
├── styles.css          # Accessible styling with WCAG AA compliance
├── script.js           # Interactive features and accessibility enhancements
└── README.md           # This file
```

## 🚀 Getting Started

### Quick Start
1. Open `index.html` in any modern web browser
2. No build process or dependencies required
3. Works offline

### Using with a Web Server
For best results, serve with a local web server:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (with http-server)
npx http-server

# Using Ruby
ruby -run -ehttpd . -p8000
```

Then open http://localhost:8000 in your browser.

## ♿ Accessibility Testing

### How to Test Keyboard Navigation
1. Press **Tab** to navigate through the page
2. Use **Enter** or **Space** to activate buttons
3. Press **Escape** to close the mobile menu
4. Use **Shift+Tab** to navigate backwards

### How to Test with Screen Readers

**Windows (NVDA - Free)**
1. Download NVDA: https://www.nvaccess.org/
2. Open the page in Firefox or Chrome
3. Press **Insert+N** to toggle NVDA on/off

**Mac (VoiceOver - Built-in)**
1. Press **Cmd+F5** to toggle VoiceOver
2. Use **VO+U** (VO is Control+Option) to open rotor for navigation

**Online Tools**
- WAVE Browser Extension: https://wave.webaim.org/extension/
- axe DevTools: https://www.deque.com/axe/devtools/

### Automated Testing Tools
- **axe DevTools**: Browser extension for automated accessibility checking
- **WAVE**: Web accessibility evaluation tool
- **Lighthouse**: Built into Chrome DevTools (Audits tab)
- **NVDA Screen Reader**: Manual testing with screen reader

## 🎓 Educational Design

### Interactive Cycle Cards
Each of the 7 development cycle steps can be expanded to reveal detailed information. This encourages students to explore and learn at their own pace.

### Mistake Cards
Common student errors are presented in expandable cards, helping students recognize and avoid these pitfalls early in their programming journey.

### Self-Assessment Quiz
Three questions test student understanding of core concepts:
1. The most critical development step
2. What to do before coding
3. The meaning of "a program that runs"

Instant feedback helps reinforce correct understanding.

## 💻 Browser Compatibility

- **Chrome/Edge**: Full support (latest 2 versions)
- **Firefox**: Full support (latest 2 versions)
- **Safari**: Full support (latest 2 versions)
- **Mobile browsers**: iOS Safari, Chrome Mobile, Firefox Mobile

## 🔧 Customization

### Change Colors
Edit the color variables in `styles.css`:
```css
/* Primary colors */
#667eea /* purple/blue */
#764ba2 /* purple */
#ff6b6b /* red for mistakes */
#ffa500 /* orange for warnings */
```

### Add More Content
1. Add new `<section>` elements in `index.html`
2. Follow the same semantic structure
3. Update the navigation menu links
4. Test keyboard navigation and screen reader compatibility

### Extend the Quiz
Add more questions following the pattern in the HTML:
```html
<fieldset>
    <legend>Question N: Your question here?</legend>
    <div class="radio-group">
        <label class="radio-label">
            <input type="radio" name="qN" value="correct" required>
            Correct answer
        </label>
        <!-- More options -->
    </div>
</fieldset>
```

The JavaScript will automatically handle them if you use `name="qN"` and `value="correct"` for correct answers.

## 📚 WCAG 2.1 Compliance Checklist

### Perceivable
- ✅ Text alternatives for all images/icons
- ✅ Sufficient color contrast (4.5:1 for normal text)
- ✅ Content is not solely dependent on color
- ✅ Resizable text (responsive design)

### Operable
- ✅ All functionality available via keyboard
- ✅ Sufficient time for interactions (no time-based content)
- ✅ No seizure-inducing content
- ✅ Skip navigation links
- ✅ Clear focus indicators

### Understandable
- ✅ Clear and simple language
- ✅ Consistent navigation
- ✅ Descriptive headings and labels
- ✅ Helpful error messages with suggestions

### Robust
- ✅ Valid HTML5
- ✅ Proper ARIA implementation
- ✅ Works with assistive technologies
- ✅ Semantic HTML structure

## 🐛 Reporting Issues

If you find any accessibility issues, please note:
1. The specific issue (e.g., "radio buttons not labeled")
2. Your testing method (keyboard, screen reader, browser)
3. Browser and operating system
4. Steps to reproduce

## 📖 Resources

### WCAG Guidelines
- [WCAG 2.1 Overview](https://www.w3.org/WAI/WCAG21/quickref/)
- [WebAIM - Web Accessibility](https://webaim.org/)
- [MDN Web Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility)

### ARIA & Semantic HTML
- [MDN ARIA](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- [HTML Semantic Elements](https://html.spec.whatwg.org/multipage/sections.html)
- [ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/)

### Testing Tools
- [WAVE Web Accessibility Evaluation Tool](https://wave.webaim.org/)
- [axe DevTools](https://www.deque.com/axe/devtools/)
- [Lighthouse](https://developers.google.com/web/tools/lighthouse)
- [NVDA Screen Reader](https://www.nvaccess.org/)

## 📝 License

This project is provided as an educational resource. See LICENSE file for details.

## 👨‍🎓 Created For

Introduction to Programming courses to make learning the Program Development Cycle engaging, interactive, and accessible to all students, including those with disabilities.

---

**Last Updated**: January 15, 2026

**Accessibility Level**: WCAG 2.1 Level AA

**Status**: ✅ Fully Accessible
