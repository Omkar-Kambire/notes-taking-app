# 📝 Notes Taking App

A simple, elegant web-based note-taking application built with Node.js, Express, and EJS. Create, view, and manage your notes with a clean, dark-themed interface.

![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![EJS](https://img.shields.io/badge/EJS-B4CA65?style=for-the-badge&logo=ejs&logoColor=black)

## ✨ Features

- 🎨 **Modern Dark UI** - Beautiful dark theme with Tailwind CSS
- 📝 **Create Notes** - Add new notes with title and detailed content
- 👁️ **View Notes** - Read your saved notes in a clean interface
- ✏️ **Edit Filenames** - Rename your note files easily
- 📱 **Responsive Design** - Works seamlessly on all devices
- ⚡ **Fast & Lightweight** - Built with efficient Node.js backend

## 🚀 Quick Start

### Prerequisites

Make sure you have Node.js installed on your machine:
- [Node.js](https://nodejs.org/) (version 14 or higher)
- npm (comes with Node.js)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Omkar-Kambire/notes-taking-app.git
   cd notes-taking-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create the files directory**
   ```bash
   mkdir files
   ```

4. **Start the application**
   ```bash
   node index.js
   ```

5. **Open your browser**
   Navigate to `http://localhost:3000`

## 🏗️ Project Structure

```
note-making-app/
├── 📁 files/              # Directory where notes are stored
├── 📁 public/             # Static assets
│   ├── 📁 images/
│   ├── 📁 javascripts/
│   └── 📁 stylesheets/
├── 📁 views/              # EJS templates
│   ├── 📄 index.ejs       # Home page with note list
│   ├── 📄 show.ejs        # Individual note view
│   └── 📄 edit.ejs        # Edit note filename
├── 📄 index.js            # Main server file
├── 📄 package.json        # Project dependencies
└── 📄 README.md           # Project documentation
```

## 🛠️ Technology Stack

| Technology | Purpose | Version |
|------------|---------|---------|
| **Node.js** | Runtime Environment | Latest |
| **Express.js** | Web Framework | ^5.1.0 |
| **EJS** | Template Engine | ^3.1.10 |
| **Tailwind CSS** | Styling Framework | v4 (CDN) |
| **File System (fs)** | File Operations | Built-in |

## 📋 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/` | Display all notes |
| `GET` | `/file/:filename` | View specific note content |
| `GET` | `/edit/:filename` | Show edit filename form |
| `POST` | `/create` | Create a new note |
| `POST` | `/edit` | Update note filename |

## 🎯 Usage

### Creating a Note
1. Enter a title in the "Enter Title" field
2. Add your note content in the "Details about the task..." textarea
3. Click "Create Task" to save your note

### Viewing Notes
- All notes are displayed as cards on the homepage
- Click "Read More..." to view the full content of any note

### Editing Filenames
- Click "Edit filename" on any note card
- Enter the new filename and save

## 🎨 UI Preview

The application features a modern dark theme with:
- **Dark Background** (`bg-zinc-900`)
- **Card Layout** for notes (`bg-zinc-800`)
- **Green Action Buttons** with hover effects
- **Responsive Grid Layout** for note cards
- **Clean Typography** with proper spacing

## 📝 Code Highlights

### Server Setup
```javascript
const express = require('express');
const app = express();

app.set('view engine', 'ejs');
app.use(express.urlencoded({extended:true}));
app.listen(3000);
```

### File Operations
```javascript
// Create note
fs.writeFile(`./files/${title}.txt`, content, callback);

// Read all notes
fs.readdir('./files', callback);

// Rename note
fs.rename(`./files/${oldName}`, `./files/${newName}`, callback);
```

## 🔧 Configuration

### Environment Variables
Currently, the app runs on port 3000. You can modify this in `index.js`:

```javascript
const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
    console.log(`Server running on port ${PORT}`);
});
```

### File Storage
Notes are stored as `.txt` files in the `files/` directory. The filename is created by:
- Taking the note title
- Removing spaces with `split(" ").join('')`
- Adding `.txt` extension

## 🚧 Development

### Adding New Features
1. **Fork** the repository
2. Create a **feature branch**: `git checkout -b feature-name`
3. **Commit** your changes: `git commit -m 'Add feature'`
4. **Push** to the branch: `git push origin feature-name`
5. Open a **Pull Request**

### Running in Development Mode
For auto-restart during development, install nodemon:
```bash
npm install -g nodemon
nodemon index.js
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Areas for Improvement
- [ ] Add note deletion functionality
- [ ] Implement search feature
- [ ] Add categories/tags
- [ ] User authentication
- [ ] Database integration
- [ ] Export notes feature
- [ ] Rich text editor

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Omkar Kambire**
- GitHub: [@Omkar-Kambire](https://github.com/Omkar-Kambire)

## 🙏 Acknowledgments

- Built with ❤️ using Node.js and Express
- Styled with Tailwind CSS
- Templating powered by EJS

---

⭐ **Star this repository if you found it helpful!**

## 📞 Support

If you have any questions or run into issues, please [open an issue](https://github.com/Omkar-Kambire/notes-taking-app/issues) on GitHub.

---
*Made with 💜 by Omkar Kambire*
