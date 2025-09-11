# Shimmie2 AI Tagger Plugin

## Installation

1. Download or clone this repository into your Shimmie2 `ext/` directory:
   ```
   git clone https://github.com/Saetron/Shimmie2-Plugins.git
   ```
   or copy the `automatic1111_tagger` folder to `shimmie2/ext/`.

2. Enable the plugin in your Shimmie2 admin panel under Extensions.

3. Configure the API endpoint, model, and threshold in the plugin settings (admin panel > Extensions > Automatic1111 Tagger).

## Usage

- On each post page, you will see an "Interrogate" button and a "Get Rating" button.
- "Interrogate" will send the image to Automatic1111 and add tags to the post.
- "Get Rating" will send the image to Automatic1111 and add the appropriate rating tag (`rating:safe`, `rating:questionable`, or `rating:explicit`).

## Setting up Automatic1111 with WD Tagger

1. Install [AUTOMATIC1111/stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui) on your server.

2. Install the [WD14 Tagger extension](https://github.com/toriato/stable-diffusion-webui-wd14-tagger) for Automatic1111:
   - Clone the extension into your `stable-diffusion-webui/extensions/` directory:
     ```
     git clone https://github.com/toriato/stable-diffusion-webui-wd14-tagger.git
     ```
   - Restart Automatic1111.

3. Start Automatic1111 with the API enabled:
   ```
   python launch.py --api
   ```

4. Make sure the WD tagger endpoint is available (default: `http://localhost:7860/tagger/v1/interrogate`).

5. In Shimmie2, set the API endpoint in the plugin settings to match your Automatic1111 server.

## Requirements
- Shimmie2 (latest version recommended)
- Automatic1111 stable-diffusion-webui with WD14 Tagger extension
- Python 3.8+
