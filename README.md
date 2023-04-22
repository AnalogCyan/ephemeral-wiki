# Ephemeral Wiki

Ephemeral Wiki is a Flask application that uses GPT-3.5-Turbo to generate ephemeral web pages on the fly. It was inspired by LiveOverflow on YouTube, but there was no live version or source code available at the time of writing the code. Visit the live app here: https://ephemeral.wiki/

You can find LiveOverflow's video and repo here:

- https://youtu.be/M2uH6HnodlM
- https://github.com/LiveOverflow/everything-api

## About

The Ephemeral Wiki is a website where every page is ephemeral and generated by GPT-3.5-Turbo. Web pages only exist while they are being viewed and are re-generated each time they are visited. Users can visit any URL path on the site, and the server will generate a response document.

Please note that the site is rate-limited to 3 requests per minute.

## Installation

### Clone the repository:

```bash
git clone https://github.com/yourusername/ephemeral-wiki.git
```

### Change directory to the project folder:

```bash
cd ephemeral-wiki
```

### Install the required dependencies (if running locally):

```bash
pip install -r requirements.txt
```

### Set up your OpenAI API key:

This implementation utilizes Google Cloud Secrets to store the OpenAI API key. If you're not using Google Cloud, you'll need to modify the code to suit your setup. See the `get_secret_value` function in `app.py` and replace it with an appropriate method for fetching the API key based on your own setup and infrastructure.

If you also deploy to Google Cloud, be sure to update the code to match your configuration.

### Select a model:

This implementation uses the GPT-3.5-Turbo model from OpenAI. If you wish to use a different model, you can modify the `generate` function in `app.py`.

### Adjust the Prompt

This implementation uses a predefined prompt for generating content with the GPT-3.5-Turbo model, and includes some specific notes for the Ephemeral Wiki. If you wish to change the prompt, you can modify the `generate` function in `app.py`.

## Usage

Run the application:

```bash
python app.py
```

Open your web browser and visit http://localhost:8080, or the deployed location on your hosting service, to see the Ephemeral Wiki in action.

## Contributing

Contributions are welcome! Feel free to submit issues, feature requests, or pull requests.

## License

This project is licensed under the [MIT License](./LICENSE).
