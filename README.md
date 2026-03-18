# MiniMax Extension for pi

AI-powered extension providing web search, image understanding, and image generation tools.

## Tools

### `web_search`
Search the web and get structured results with titles, URLs, snippets, and related searches.

### `understand_image`
Analyze images using AI - supports URLs and local file paths.

### `generate_image`
Generate images from text prompts using MiniMax AI.

**Parameters:**
- `prompt` (required): Text description of the image to generate (max 1500 characters)
- `model` (optional): Model to use, default "image-01"
- `aspect_ratio` (optional): Image aspect ratio - "1:1", "16:9", "4:3", "3:2", "2:3", "3:4", "9:16", "21:9"
- `width`/`height` (optional): Specific dimensions in pixels (512-2048, divisible by 8)
- `response_format` (optional): "url" (default, expires 24h) or "base64"
- `seed` (optional): Random seed for reproducible generation
- `n` (optional): Number of images to generate (1-9, default 1)
- `prompt_optimizer` (optional): Enable automatic prompt optimization

### `transform_image`
Transform an existing image using AI (image-to-image generation). Takes a source image and generates a new image based on the text prompt.

**Parameters:**
- `prompt` (required): Text description of the desired transformation (max 1500 characters)
- `image` (required): Source image - URL, local path, or base64 data URL
- `model` (optional): Model to use, default "image-01"
- `subject_type` (optional): Type of subject reference, default "character"
- `aspect_ratio` (optional): Image aspect ratio - "1:1", "16:9", "4:3", "3:2", "2:3", "3:4", "9:16", "21:9"
- `width`/`height` (optional): Specific dimensions in pixels (512-2048, divisible by 8)
- `response_format` (optional): "url" (default, expires 24h) or "base64"
- `seed` (optional): Random seed for reproducible generation
- `n` (optional): Number of images to generate (1-9, default 1)
- `prompt_optimizer` (optional): Enable automatic prompt optimization

## Setup

### 1. Get MiniMax API Key

1. Sign up at [MiniMax Platform](https://www.minimax.io/platform)
2. Get your API key from your account settings
3. Note your region and corresponding API host:
   - **Global**: `https://api.minimax.io`
   - **Mainland China**: `https://api.minimax.cn`

### 2. Configure Environment Variables

Set the required environment variables before running pi:

```bash
# For Global users
export MINIMAX_API_KEY="your-api-key-here"
export MINIMAX_API_HOST="https://api.minimax.io"

# For Mainland China users
export MINIMAX_API_KEY="your-api-key-here"
export MINIMAX_API_HOST="https://api.minimax.cn"
```

### 3. Add to pi Settings

pi install https://github.com/joshleblanc/pi-minimax
```

## Usage

### Web Search Example
```
Search for: "latest TypeScript features 2024"
```

### Image Analysis Example
```
Analyze: "./screenshot.png"
Prompt: "What does this diagram show?"
```

### Image Generation Example
```
Generate an image with prompt: "A serene beach at sunset with palm trees"
Aspect ratio: 16:9
Number of images: 2
```

### Image Transformation Example
```
Transform an image with:
  Prompt: "A girl looking into the distance from a library window"
  Image: "./portrait.png"
  Aspect ratio: 16:9
```

## Requirements

- pi-coding-agent
- MINIMAX_API_KEY environment variable
- MINIMAX_API_HOST environment variable (optional, defaults to https://api.minimax.io)
