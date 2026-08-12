# How to Set Up HTTP Server

This guide explains how to run your portfolio website locally using `http-server`.

## Prerequisites

Before you begin, make sure you have the following installed on your system:

- **Node.js** (v12 or higher) - Download from [nodejs.org](https://nodejs.org/)
- **npm** (comes with Node.js)

You can verify your installation by running:

```bash
node --version
npm --version
```

## Installation

### Option 1: Using npx (Recommended - No Installation Required)

If you have Node.js and npm installed, you can run `http-server` without installing it globally using `npx`:

```bash
npx http-server -p 8080
```

This will automatically download and run the latest version of `http-server`.

### Option 2: Install Globally

If you want to install `http-server` globally for repeated use:

```bash
npm install -g http-server
```

Then you can simply run:

```bash
http-server -p 8080
```

## Running the Server

1. Open your terminal or command prompt
2. Navigate to your portfolio project directory:
   ```bash
   cd path/to/Portfolio
   ```

3. Start the server using one of the methods above:
   ```bash
   npx http-server -p 8080
   ```

4. You should see output similar to:
   ```
   Starting up http-server, serving ./
   
   http-server version: 14.1.1
   
   Available on:
     http://192.168.0.192:8080
     http://127.0.0.1:8080
   
   Hit CTRL-C to stop the server
   ```

## Accessing Your Website

Once the server is running, open your web browser and visit one of these URLs:

- **Local Access**: `http://localhost:8080` or `http://127.0.0.1:8080`
- **Network Access**: `http://192.168.0.192:8080` (from other devices on your network)

The home page will load, displaying your portfolio website.

## Common Options

Here are some useful command-line options for `http-server`:

| Option | Description | Example |
|--------|-------------|---------|
| `-p` | Port number (default: 8080) | `http-server -p 3000` |
| `-c` | Cache control max-age header value in seconds | `http-server -c 3600` |
| `--gzip` | Enable gzip compression | `http-server --gzip` |
| `--cors` | Enable CORS support | `http-server --cors` |
| `-o` | Open default browser automatically | `http-server -o` |

### Example: Launch with Auto-Open

To automatically open the website in your default browser:

```bash
npx http-server -p 8080 -o
```

## Stopping the Server

To stop the server, press **`Ctrl + C`** in your terminal.

## Troubleshooting

### Port Already in Use

If port 8080 is already in use, use a different port:

```bash
npx http-server -p 3000
```

Then access your site at `http://localhost:3000`

### Python Alternative (Deprecated)

If you prefer Python (note: Python 3 must be installed):

```bash
python -m http.server 8080
```

## Additional Resources

- [http-server Documentation](https://github.com/http-party/http-server)
- [Node.js Documentation](https://nodejs.org/docs/)
- [npm Documentation](https://docs.npmjs.com/)
