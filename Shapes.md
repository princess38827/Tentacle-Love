# Shapes.inc D&D Dungeon Master Bot

This project provides a Python-based chatbot that leverages the **Shapes.inc API** to act as a full-featured **Dungeons & Dragons (D&D) Dungeon Master (DM)**. The bot is designed to handle storytelling, manage character sheets, and perform dice rolls through direct messages (DMs).

## Features

| Feature | Description |
| :--- | :--- |
| **Immersive Storytelling** | The bot uses a specialized system prompt to maintain a consistent DM persona, describing environments and NPCs vividly. |
| **Dice Rolling Tool** | An integrated tool allows the AI to roll dice (e.g., 1d20, 2d6+3) for skill checks, combat, and saving throws. |
| **Character Management** | Persistent storage for player character sheets, including stats, HP, inventory, and quest progress. |
| **State Persistence** | Game state is saved to a local `character_sheets.json` file, allowing adventures to continue across sessions. |
| **Tool Integration** | Uses the Shapes.inc `Tool` class to give the AI programmatic access to game mechanics. |

## Prerequisites

1.  **Python 3.7+**
2.  **Shapes.inc API Key**: Obtain your API key from the [Shapes.inc Developer Portal](https://shapes.inc).
3.  **Install Dependencies**:
    ```bash
    pip install shapesinc -U
    ```

## Setup and Usage

1.  **Set Environment Variable**:
    Set your Shapes.inc API key as an environment variable:
    ```bash
    export SHAPES_API_KEY='your_api_key_here'
    ```

2.  **Run the Bot**:
    Execute the main script to start the interactive DM session:
    ```bash
    python dnd_bot.py
    ```

3.  **Interaction**:
    - The bot will prompt you for a **User ID**. This allows it to load your specific character sheet.
    - Once started, you can describe your actions in natural language (e.g., "I search the room for traps" or "I attack the goblin with my longsword").
    - The DM will respond, calling the dice roller or updating your character sheet as needed.

## Code Structure

- `dnd_bot.py`: The main application logic, including tool definitions, system prompts, and the chat loop.
- `character_sheets.json`: (Generated automatically) Stores player data in a structured format.

## Customization

You can customize the DM's personality or the starting adventure by modifying the `DM_SYSTEM_PROMPT` variable in `dnd_bot.py`. This allows you to set different themes, such as high fantasy, gothic horror, or sci-fi RPGs.

## References

- [Shapes.inc API Documentation](https://shapesinc-py.readthedocs.io/) [1]
- [Shapes.inc Developer Portal](https://shapes.inc) [2]
- [D&D 5th Edition Rules](https://dnd.wizards.com/what-is-dnd/basic-rules) [3]

---
**Author**: Manus AI
**Date**: April 28, 2026
