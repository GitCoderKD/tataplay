# Tataplay API

This project is a Flask-based web service that integrates with external APIs to provide various functionalities, including channel redirection, license key provisioning, and M3U playlist generation.

## Features

- **Channel Redirection**: Redirects to the appropriate channel URL fetched from an external HMAC service.
- **License Key Provisioning**: Provides license keys in JSON format for a given TVG ID.
- **M3U Playlist Generation**: Generates an M3U playlist with links and metadata based on data from external services.

## Setup

To set up the project, you'll need Python 3.7 or higher. Follow these steps:

1. **Clone the Repository**

    ```bash
    git clone https://github.com/GitCoderKD/tataplay.git
    cd tataplay
    ```

2. **Create a Virtual Environment**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Dependencies**

    ```bash
    pip install -r requirements.txt
    ```

4. **Set Environment Variables**

    Set the `FQDN` environment variable to the Fully Qualified Domain Name where the application will be hosted. You can do this in your terminal or by adding it to your `.env` file:

    ```bash
    export FQDN='localhost:5000'
    ```

5. **Run the Application**

    ```bash
    python api/index.py
    ```

    The application will be available at `http://localhost:5000`.

## Endpoints

- **`/`**: Redirects to the channel URL obtained from the HMAC service.
- **`/tataplay/keys/<tvg_id>`**: Provides license key for the given TVG ID.
- **`/tataplay/playlist`**: Generates and serves an M3U playlist.

## One-Click Deploy

Deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme):

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FGitCoderKD%2Ftataplay%2Ftree%2Fmain&demo-title=Flask%203%20%2B%20Vercel&demo-description=Use%20Flask%203%20on%20Vercel%20with%20Serverless%20Functions%20using%20the%20Python%20Runtime.&demo-url=https%3A%2F%2Ftataplay-learner.vercel.app%2F&demo-image=https://assets.vercel.com/image/upload/v1669994156/random/flask.png)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
