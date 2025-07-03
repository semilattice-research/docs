# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Mintlify documentation site for Semilattice, a computational research platform that predicts how specific populations of people would answer questions. The documentation is built using Mintlify's documentation framework and focuses on API integration for developers.

## Architecture

- **Documentation Framework**: Mintlify-based documentation site
- **Configuration**: `docs.json` contains site configuration, navigation, theming, and API reference setup
- **Content Structure**: 
  - MDX files for documentation pages (`.mdx` extension)
  - Organized into sections: language-specific quickstarts, populations, and API reference
  - Images stored in `/images/` directory organized by section
- **API Integration**: OpenAPI specification integrated at `https://api.semilattice.ai/openapi.json`
- **SDKs**: Python (https://pypi.org/project/semilattice/) and Node.js (https://www.npmjs.com/package/semilattice/)

## Key Components

### Core Documentation Files
- `introduction.mdx` - Main documentation landing page with language selection
- `python-quickstart.mdx` - Python SDK getting started guide
- `nodejs-quickstart.mdx` - Node.js SDK getting started guide
- `populations/introduction.mdx` - Core concept explanation (What are Populations?)
- `populations/create-population.mdx` - API workflow for creating populations
- `populations/seed-data-requirements.mdx` - CSV format and data quality requirements
- `populations/evaluation.mdx` - Testing process and accuracy metrics
- `answers/introduction.mdx` - Core concept explanation (What are Answers?)
- `answers/simulate-answer.mdx` - Predicting responses to new questions
- `answers/benchmark-answer.mdx` - Testing accuracy against known data
- `api/` directory - API reference documentation

### Navigation Structure
The site has two main tabs:
1. **Documentation** - Developer guides and conceptual content
2. **API Reference** - Auto-generated from OpenAPI spec

## Development Commands

This project uses Mintlify for documentation. The `package.json` is currently empty, suggesting this may be a pure Mintlify project without additional Node.js dependencies.

For Mintlify projects, common commands would typically be:
- `mintlify dev` - Local development server
- `mintlify build` - Build documentation site

## Content Guidelines

- Use MDX format for all documentation files
- Focus on developer-centric content and API integration
- Follow the established navigation structure in `docs.json`
- Use Mintlify components (Steps, Frame, CardGroup, etc.) for enhanced formatting
- Include code examples for both Python and Node.js SDKs
- Images should be organized by section in the `/images/` directory
- Introduction page provides overview and language selection with big card buttons
- Quickstart guides should follow the pattern: API key setup → installation → initialization → usage → polling for results
- Population documentation follows a logical flow: concept introduction → creation workflow → data requirements → evaluation metrics
- Answer documentation covers the prediction workflow: concept introduction → simulation for new questions → benchmarking for validation

## Theming

The site uses a custom green theme (#29A383) with custom background colors for light and dark modes. Logo files are provided in both light and dark variants.