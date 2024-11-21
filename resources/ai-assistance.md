I'll help improve the document while maintaining its structure and tone. Here's a clearer, more coherent version:

## AI Assistance Guidelines

AI tools can enhance your development process, particularly for debugging, UI/UX design, and library integration. Follow the [Final Project Guide](./final-project-guide.md) when using AI assistance.

Recommended AI Tools:

- [ChatGPT](https://chat.openai.com): General-purpose AI assistant
- [Claude](https://claude.ai): Specialized in detailed guidance and problem-solving
- [Prompt Engineering Guide](./prompt-engineering.md)

## Using AI for Interface Development

Here are effective ways to leverage AI for your project's interface:

### Web Interface (Flask)

Claude excels at creating HTML/CSS templates. To generate a Flask web interface:

1. Provide your `core.py` file and interface mockups/sketches
2. Request Tailwind CSS styling for maintainable code

Example prompt:

```
I have my business logic in core.py and sketches of my desired interface for a journaling app that lets users add, view, and search entries. Please create a Flask app that:
1. Connects to my business logic
2. Creates a clean, simple interface
3. Uses Tailwind CSS for styling

Include step-by-step instructions for integrating and running the app locally in VSCode.
```

### Game Interface (Pygame)

For games and desktop applications, AI can help build Pygame interfaces:

1. Share your `core.py` file and interface designs
2. Request implementation guidance

Example prompt:

```
I have core.py and sketches for a game where players move on a grid collecting items. Please create a Pygame interface that:
1. Integrates with my business logic
2. Displays the game world
3. Handles player movement and item collection

Include step-by-step setup instructions for VSCode.
```

### Report Generation

For projects requiring data reports:

1. Provide your `core.py` file and reporting requirements
2. Request specific output formats (PDF/Excel)

Example prompt:

```
I need to generate reports for my inventory management system. Using my core.py, please create a script that:
1. Generates monthly sales PDF reports
2. Includes data visualizations
3. Integrates with my existing code

Include implementation steps for VSCode.
```

### Custom Interfaces

Apply these patterns to other interface types. Request:

1. Basic structure generation
2. Integration guidelines
3. Step-by-step implementation instructions

Note: Claude works best with Flask and Pygame. For other frameworks, use the generated code as a foundation for customization.
