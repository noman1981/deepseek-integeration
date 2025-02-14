# deepseek-integeration
Deepseek intergeration with web site
WSP ChatBot

Overview

WSP ChatBot is a simple web-based chatbot interface that allows users to ask questions and receive AI-generated responses. The chatbot uses the OpenRouter API to communicate with an AI model and provide real-time responses.

Features

Simple and clean user interface built with Bootstrap 4.3.1

Uses OpenRouter AI API for chatbot responses

Supports Markdown formatting for chatbot replies

Provides instant feedback with a loading message while waiting for a response

Requirements

Internet connection (for API requests and Bootstrap CDN)

A web browser that supports JavaScript

Installation & Usage

Download or clone this repository.

Open the index.html file in a web browser.

Enter a question in the input field and click the "Ask!" button.

The chatbot will generate a response based on the input query.

Technologies Used

HTML5: For structuring the webpage

CSS3: Basic styling using Bootstrap 4.3.1

JavaScript (ES6): For handling user input and making API requests

OpenRouter AI API: Provides AI-generated chatbot responses

Marked.js: Parses and renders Markdown-formatted responses

API Integration

The chatbot fetches responses from OpenRouter AI API using a POST request. The request includes:

Authorization token (API Key)

Model selection (deepseek/deepseek-r1:free)

User input formatted as a JSON request

Example API Request

fetch('https://openrouter.ai/api/v1/chat/completions', {
    method: 'POST',
    headers: {
        Authorization: 'Bearer YOUR_API_KEY',
        'HTTP-Referer': 'https://yourwebsite.com',
        'X-Title': 'YourTitle',
        'Content-Type': 'application/json',
    },
    body: JSON.stringify({
        model: 'deepseek/deepseek-r1:free',
        messages: [{ role: 'user', content: input }],
    }),
});

Security Warning

Do not expose API keys in client-side JavaScript. Consider using a backend server to handle API requests securely.

Be mindful of the API rate limits and usage restrictions.

License

This project is released under an open-source license. Modify and distribute as needed.

Author

Developed by Noman Mazher
