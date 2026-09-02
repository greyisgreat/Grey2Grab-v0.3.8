# GREY2GRAB

**AI-powered GRAB map generation from natural-language ideas.**

GREY2GRAB is a GRAB-focused AI system designed to turn map ideas into detailed, playable GRAB levels.

Unlike A Normal Prompt Which Is What Grey2Grab Started With You Can See Edits And Creations In Real Time

The goal isn't simply to generate valid JSON. GREY2GRAB is designed to understand the structure and design of high-quality GRAB maps so it can create levels with intentional gameplay, visual detail, natural variation, and meaningful progression.

## What It Does

You describe the map you want, for example:

> Make me a difficult futuristic parkour map with a massive central tower, multiple routes, vertical climbing, hidden shortcuts, and a challenging final section.

GREY2GRAB processes the idea and generates GRAB level data that can be used with a compatible level editor.

Generated maps are intended to contain:

* Parkour and movement challenges
* Vertical gameplay
* Multiple routes
* Large landmarks
* Environmental structures
* Visual details
* Difficulty progression
* Secrets and optional areas
* Start and finish areas
* Organized groups and nested structures

## How It Works

GREY2GRAB uses a GRAB-specific knowledge base rather than relying on a general-purpose AI alone.

```text
Map Idea
   ↓
GRAB Knowledge
   ↓
Map Design Planning
   ↓
Gameplay + Visual Planning
   ↓
GRAB Level Generation
   ↓
Validation
   ↓
Error Correction
   ↓
Final GRAB Level
```

The knowledge base can contain GRAB format documentation, examples, showcase maps, gameplay references, visual references, and analyzed map-design patterns.

Reference maps are used to teach the system how high-quality levels are constructed rather than simply copying existing maps.

## Map Design

GREY2GRAB is specifically designed to avoid the common problem of AI-generated maps looking overly repetitive or perfectly symmetrical.

The system should be able to combine:

* Large structures
* Medium gameplay structures
* Small environmental details
* Varied platform sizes
* Natural rotations
* Asymmetrical architecture
* Intentional empty space
* Strong landmarks
* Different gameplay sections

The objective is to produce maps that feel **designed**, rather than procedurally filled with identical objects.

## GRAB Knowledge

The knowledge system is built around references such as:

```text
GRAB format
Node structures
Shapes
Materials
Colors
Transforms
Quaternions
Groups
Gameplay patterns
Parkour layouts
Visual composition
Showcase maps
```

High-quality maps can also be analyzed and converted into additional design knowledge, allowing the system to learn patterns such as object density, level flow, structural composition, and gameplay progression.

## Validation

Generated level data is checked before being returned.

Validation can check:

* JSON syntax
* GRAB node structures
* Required properties
* Node nesting
* Shapes and materials
* Transform data
* Quaternion structure
* Colors
* Start and finish nodes
* Object counts and complexity

If generation produces an error, the system can send the problem back through the generation process and attempt to correct it.

## Technology

GREY2GRAB is designed to run as a web application using:

* **Groq** — AI inference and map generation
* **Vercel** — hosting and serverless API
* **GitHub** — source control and deployment
* **JavaScript / TypeScript** — application and API
* **GRAB level JSON** — generated map data

The frontend communicates with a server-side API so the Groq API key is never exposed to the browser.

```text
Browser
   ↓
Vercel API
   ↓
Groq
   ↓
GRAB Generator
   ↓
Validator
   ↓
Generated Level
```

## Goal

GREY2GRAB aims to make GRAB map creation accessible through natural language while maintaining the complexity and creativity of manually designed levels.

**Idea in. GRAB level out.**
