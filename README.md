# 📂 Local File Upload & Management System

🌟 **Overview**  
The **Local File Upload & Management System** is a simple yet powerful web application built with **Node.js** and **Express.js**. It allows users to upload, manage, view, and delete photos and videos directly from their devices. Whether you're transferring files between your PC and phone or organizing your media, this app provides a seamless experience.

---

## 🚀 Features

- **📤 Upload Files**: Easily upload images and videos from your PC or phone to the server.
- **🖼️ Preview Uploaded Files**: View images and videos directly from the file list.
- **🗑️ Delete Files**: Permanently remove uploaded files from the server.
- **📥 File Download**: Download any uploaded file with a single click.
- **📊 Progress Bar**: Real-time upload progress tracking.
- **📱 Responsive Design**: Works flawlessly on both desktop and mobile devices.
- **🔁 Seamless Transfer**: Transfer photos and videos between your phone and PC effortlessly.

---

## ⚙️ Requirements

- **Node.js**: Version 12 or later
- **npm**: Version 6 or later

---

## 🛠️ Installation & Setup

### Step 1: Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/soul-dev07/lfs-soul.git
```

Navigate to the project folder:

```bash
cd localfileshare
```

### Step 2: Install Dependencies
Install the required dependencies:

```bash
npm install
```

### Step 3: Configuration

The project comes with a default **`config.json`** file. Ensure that the `config.json` file is located in the root directory of the project, with the following content:

```json
{
  "port": 3000,
  "dir": "uploads",
  "logFileUploads": false
}
```

- **`port`**: The port the server will run on (default is `3000`).
- **`dir`**: The directory where uploaded files are stored (default is `uploads`).
- **`logFileUploads`**: Set to `true` to log timestamps of uploaded files (default is `false`).

### Step 4: Run the Application

Start the server:

```bash
npm start
```

The server will be accessible at:

```
http://localhost:3000
```

---

 ## 🖥️ Application Workflow
###  📤 Upload Files:

   - Drag files directly into the drop area or use the file picker to select files.
   - Supported file types include images (`.jpeg`, `.jpg`, `.png`, `.gif`) and videos (`.mp4`, `.mov`, `.avi`).
   - The progress bar shows the upload progress.

### 🖼️ View Uploaded Files:
  - After uploading, the files are listed with their names, sizes, and previews (images will show thumbnails, videos will show playable previews).

### 🗑️ Manage Files:

  - You can delete uploaded files by clicking the **Delete** button next to each file.
  - You can download files by clicking the **Download** button next to each file.

---

### 🌐 API Endpoints
The application provides the following API endpoints:

### `POST /upload`

Uploads a file to the server.

- **Request body**: Form-data with a `file` key (required).
- **Response**: 
  ```json
  {
    "message": "File uploaded successfully",
    "file": {
      "originalname": "file.jpg",
      "filename": "timestamp.jpg",
      "size": 1024
    }
  }
  ```

### `GET /files`
Lists all uploaded files.

- **Response**: 
  ```json
  [
    {
      "name": "file1.jpg",
      "url": "/uploads/file1.jpg",
      "size": 1024
    },
    {
      "name": "file2.mp4",
      "url": "/uploads/file2.mp4",
      "size": 2048
    }
  ]
  ```
  
### `DELETE /file/:filename`

Deletes a specific file from the server.

- **Request**: `DELETE /file/file1.jpg`
- **Response**: 
  ```json
  {
    "message": "File deleted successfully"
  }
  ```

---


## 🎨 Front-End Features

### Drag-and-Drop

- Drag files directly into the drop area to upload them. This feature is available for both desktop and mobile users.

### File Picker

- Alternatively, users can click the **Choose File** button to open a file picker for selecting files.

### Progress Bar

- As files are uploaded, a progress bar displays the upload status in real-time.

### File Previews

- **Images** are shown as thumbnails.
- **Videos** are shown with a playable preview.

### File Management

- Files can be **deleted** from the server with the click of a button.
- Files can be **downloaded** by clicking the download button next to each file.

---


## 📜 License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contribution
Feel free to submit issues or pull requests. Contributions are welcome! 🎉

---

## 📧 Contact
- **Developer**: [Soul-dev](github.com/soul-dev07/)
- **Repository**: [GitHub Link](https://github.com/soul-dev07/lfs-soul/)

---

## 🤖 AI-Generated Documentation
This documentation was generated using AI tools. While every effort has been made to ensure the accuracy and comprehensiveness of the content, please note that it may not always 
reflect the most up-to-date or complete information. Use this documentation at your own risk.

---

## ⚠️ Disclaimer
By using this application, you agree to the following:

1. **No Responsibility**: The developer is not responsible for any damages, data loss, or issues that may arise from using this software.
2. **Use at Your Own Risk**: The software is provided "as-is" without any guarantees or warranty. It is your responsibility to ensure that your files are secure and backed up.
