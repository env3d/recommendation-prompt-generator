# Recommendation Prompt Generator

A simple webpage that generates a structured prompt for LLMs to create recommendation letters.

## Purpose

This tool allows you to send a personalized link to someone writing you a recommendation letter. They fill out a form, copy the generated prompt, paste it into their favorite LLM (ChatGPT, Claude, etc.), and receive a polished recommendation letter draft.

## Usage

Send a link like this to your recommender:

https://env3d.github.io/recommendation-prompt-generator/?for=John%20Doe&pronoun=he


### URL Parameters

- **`for`** (required): The name of the person being recommended (you)
  - Example: `for=Jane%20Smith`
  
- **`pronoun`** (optional): Preferred pronouns for the letter. Options: `he`, `she`, or `they` (defaults to `they`)
  - Example: `pronoun=she`

## How It Works

1. Your recommender opens the personalized link
2. They fill out the form with details about your relationship and qualifications
3. They click "Generate" to create an LLM prompt
4. They copy the prompt and paste it into an LLM
5. The LLM generates a professional recommendation letter

## Local Development

To test locally in the dev container:

```bash
python3 -m http.server 8080
"$BROWSER" http://localhost:8080/?for=Test%20User&pronoun=they
```

## Features

- **Form persistence**: All inputs are saved to localStorage so recommenders can return later
- **Conditional sections**: Empty fields are omitted from the generated prompt
- **Pronoun support**: Automatically uses correct pronouns throughout the letter
- **One-click copy**: Copy button for easy prompt transfer to LLMs

