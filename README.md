# AI Business Operations Assistant

## Overview

A Google Apps Script-powered AI assistant that analyzes team reports and project data from various sources (Google Forms, Google Docs, ClickUp) to provide strategic insights for leadership. The system uses the Gemini API to extract structured data from unstructured text and analyzes it against defined business objectives.

## Core Features

- **Daily Report Analysis:** Automatically processes daily reports submitted via a Google Form.
- **AI-Powered Data Extraction:** Uses Gemini to parse text reports and extract structured data (tasks, projects, time spent, sentiment) into a central Google Sheet ("Knowledge Hub").
- **Strategic Weekly Analysis:** Compares all collected data against high-level goals defined in a "Strategy Journal" to provide deep insights on project progress, team rhythms, and potential blockers.
- **Automated Email Summaries:** Delivers daily and weekly summaries in a clean, HTML-formatted email.
- **Intelligent Reminders:** A configurable reminder system to prompt leadership for weekly strategic reviews.

## Setup & Configuration

1.  **Google Workspace Setup:**
    * A main **Google Sheet** to act as the hub, containing tabs for:
        * `Form Responses 1`: Raw data from the Google Form.
        * `VA Roster`: A list of team members with their names and emails.
        * `Knowledge Hub`: The central database populated by the script.
    * A **Google Doc** named "Strategy Journal" to store high-level, natural language objectives.
2.  **Google AI Studio:**
    * Generate an API key from `aistudio.google.com`.
3.  **Apps Script Configuration:**
    * Deploy the code as a script attached to the main Google Sheet.
    * Store the Gemini API key as a Script Property named `API_key`.
    * Update the configuration constants at the top of the script (`STRATEGY_JOURNAL_DOC_ID`, etc.).
    * Set up time-driven triggers for daily and weekly functions.

## Project Roadmap

-   **Phase 1: Core Foundation.** Daily report processing and analysis against strategic goals. (COMPLETE)
-   **Phase 2: Meeting Intelligence.** Integration with Google Meet transcripts from a dedicated Google Drive folder.
-   **Phase 3: Platform Integration.** Direct API connection with ClickUp and/or Slack.
