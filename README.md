# File Server

A simple file upload server built with [Express](https://expressjs.com/) and [Multer](https://github.com/expressjs/multer) for handling file uploads.

## Features
- Upload files to the server using a REST API
- Stores uploaded files in a local `downloads` directory

## Requirements
- [Node.js](https://nodejs.org/) (v14 or newer recommended)
- npm (Node package manager)

## Getting Started

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd file-server
```

### 2. Install dependencies
```bash
npm install
```

### 3. Start the server
```bash
npm start
```

The server will run on [http://localhost:3000](http://localhost:3000).

## API

### Upload a File
- **Endpoint:** `POST /upload`
- **Form Field:** `file` (the file to upload)
- **Response:**
  - `200 OK` on success: `File uploaded successfully!`
  - `400 Bad Request` if no file is uploaded

#### Example using `curl`:
```bash
curl -F "file=@/path/to/your/file.txt" http://localhost:3000/upload
```

## File Storage
- Uploaded files are saved in the `downloads` directory at the root of the project.

## Project Structure
```
file-server/
├── downloads/      # Uploaded files are stored here
├── index.js        # Main server file
├── package.json    # Project metadata and dependencies
└── README.md       # This documentation
```

## License
MIT License
