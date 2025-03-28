cat << 'EOF' > README.md
# 🥠 Fortune Cookie App - React

<div align="center">
  <img src="https://github.com/user-attachments/assets/48640e82-c35c-4117-8390-8323fbdc74d2" width="550" style="border-radius:15px;box-shadow:0 4px 12px rgba(0,0,0,0.15)" alt="App Screenshot">
  
  [![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
  ![React Version](https://img.shields.io/badge/React-18+-61DAFB?logo=react)
  ![Vite Build](https://img.shields.io/badge/Build-Vite-646CFF?logo=vite)
  ![Framer Motion](https://img.shields.io/badge/Animation-Framer_Motion-0055FF?logo=framer)
</div>

## ✨ Key Features

- 🎲 Random inspirational quotes
- 🖼️ Beautiful background images
- ✨ Smooth fade animations
- 📜 Famous wisdom phrases
- 🎨 Elegant card design
- 🖱️ Interactive button

## 🛠️ Tech Stack

<div align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB">
  <img src="https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E">
  <img src="https://img.shields.io/badge/Framer_Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
</div>

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/estefaniii/fortune-cookie-app.git
cd fortune-cookie-app

# Install dependencies
npm install

# Start development server
npm run dev
```

## 📂 Project Structure

```
src/
├── assets/            # Background images
├── components/        # Reusable components
│   ├── Button.jsx     # Interactive button
│   ├── FadeContainer.jsx # Animation wrapper
│   └── PhraseCard.jsx # Quote display
├── utils/
    └── index.js       # Utility function collection
├── App.jsx            # Main application
└── index.css          # Global styles of the app
└── main.jsx           # Entry point
└── phrases.json       # famous phrases
```

## 🎨 Code Example

```jsx
// Main App Component
function App() {
  const [phrase, setPhrase] = useState(randomItem(phrases));
  const [image, setImage] = useState(randomItem(images));
  
  const changePhrase = () => {
    setFade(true);
    setTimeout(() => {
      setPhrase(randomItem(phrases));
      setImage(randomItem(images));
      setFade(false);
    }, 500);
  };

  return (
    <FadeContainer fade={fade}>
      <div style={{ backgroundImage: \`url('\${image}')\` }}>
        <PhraseCard phrase={phrase.phrase} author={phrase.author} />
        <Button onClick={changePhrase}>New Quote</Button>
      </div>
    </FadeContainer>
  );
}
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (\`git checkout -b feature/amazing-feature\`)
3. Commit your changes (\`git commit -m 'Add amazing feature'\`)
4. Push to the branch (\`git push origin feature/amazing-feature\`)
5. Open a Pull Request

## 💖 Support the Project

If you find this useful, consider supporting development:

[![Donar con PayPal](https://img.shields.io/badge/Donar-PayPal-00457C?style=for-the-badge&logo=paypal)](https://paypal.me/estefanniii?country.x=PA&locale.x=es_XC)

---
<div align="center">
  <p>✨ Made with ❤️ by Estéfani Torres</p>
</div>
EOF
