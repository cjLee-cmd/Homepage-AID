# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file static website for AID., Inc., a company specializing in AI-powered power grid monitoring solutions. The project is a bilingual (Korean/English) landing page built with vanilla HTML, CSS, and JavaScript.

## Architecture

**Single File Structure**: The entire application is contained within `index.html` with embedded:
- CSS styles (including Tailwind CSS via CDN)
- JavaScript for language switching and interactive effects
- Korean and English content with dynamic language toggling

**Key Technologies**:
- Tailwind CSS (loaded via CDN)
- Custom CSS variables for theming
- Vanilla JavaScript for interactivity
- Korean web fonts (Pretendard, Paperlogy)
- English web fonts (Space Grotesk, Noto Sans)

**Bilingual Implementation**: 
- Uses `lang` attribute switching between 'ko' and 'en' on the `<html>` element
- CSS rules hide/show content based on current language
- JavaScript `toggleLanguage()` function switches between languages
- All text content has both Korean and English versions in the DOM

## Development Commands

Since this is a static HTML project, development is straightforward:

**Local Development**:
```bash
# Serve the file locally (any HTTP server)
python -m http.server 8000
# or
npx serve .
```

**File Editing**:
- All changes are made directly to `index.html`
- No build process or compilation required
- Refresh browser to see changes

## Code Conventions

**Language Content Structure**:
```html
<span lang="ko">Korean content</span>
<span class="hidden" lang="en">English content</span>
```

**CSS Custom Properties**: 
- Primary color scheme defined in `:root` with CSS variables (--primary-50 through --primary-950)
- Responsive design using Tailwind classes
- Dark theme with background color `#0D1117`

**Interactive Features**:
- Mouse-following parallax effect on hero section
- Hover animations and transforms on cards and buttons
- Language toggle button in header

## Key Features

1. **Responsive Design**: Mobile-first approach with Tailwind responsive classes
2. **Interactive Hero Section**: Mouse parallax effect with 3D transforms
3. **Language Switching**: Complete bilingual support with seamless toggling
4. **Modern UI Components**: Cards, buttons, and sections with hover effects
5. **Performance**: Single file with CDN resources for fast loading

## Content Areas

The page includes:
- Hero section with company introduction
- Core technology showcase (3 feature cards)
- How it works process (3-step workflow)
- Call-to-action section
- Footer with policy links

When making content changes, ensure both Korean and English versions are updated simultaneously to maintain consistency across languages.