# CourseFlow Telegram

🎓 **Modern Next.js platform for organizing Telegram course groups into structured learning experiences with video streaming, modules, and lessons management**

## 🌟 Features

- ✅ **Telegram Bot Integration** - Automatically scan Telegram course groups
- ✅ **Auto-Organization** - Intelligently parse and organize courses into modules and lessons
- ✅ **Video Streaming** - Watch Telegram videos without downloading
- ✅ **Modern UI** - Built with Next.js 14, React 18, and TailwindCSS
- ✅ **Firebase Backend** - Real-time database with Firestore
- ✅ **Responsive Design** - Works on desktop, tablet, and mobile
- ✅ **Progress Tracking** - Track your learning progress
- ✅ **Search & Filter** - Find courses and lessons easily

## 🚀 Tech Stack

### Frontend
- **Next.js 14** - React framework with App Router
- **React 18** - UI library
- **TypeScript** - Type-safe development
- **TailwindCSS** - Utility-first CSS framework
- **Framer Motion** - Animations library
- **React Player** - Video player component
- **Zustand** - State management
- **React Hot Toast** - Notifications

### Backend & Services
- **Node.js** - Runtime environment
- **Firebase** - Authentication and database
- **Firestore** - NoSQL database
- **Telegraf** - Telegram bot framework
- **Axios** - HTTP client

### DevTools
- **TypeScript** - Static typing
- **PostCSS & Autoprefixer** - CSS processing
- **ESLint** - Code linting

## 📋 Project Structure

```
courseflow-telegram/
├── src/
│   ├── app/              # Next.js App Router
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── courses/      # Courses pages
│   │   ├── lessons/      # Lessons pages
│   │   └── api/          # API routes
│   ├── components/       # React components
│   │   ├── Header.tsx
│   │   ├── CourseCard.tsx
│   │   ├── VideoPlayer.tsx
│   │   └── ...
│   ├── types/            # TypeScript types
│   ├── utils/            # Utility functions
│   ├── styles/           # Global styles
│   ├── bot/              # Telegram bot logic
│   │   └── telegram.js   # Bot handler
│   └── lib/              # Library functions
├── public/               # Static assets
├── package.json
├── tsconfig.json
├── tailwind.config.js
├── next.config.js
└── README.md
```

## 🛠️ Installation & Setup

### Prerequisites
- Node.js 18+ and npm/yarn
- Telegram Account
- Firebase Project
- Git

### 1. Clone Repository
```bash
git clone https://github.com/AllehKeyroz/courseflow-telegram.git
cd courseflow-telegram
```

### 2. Install Dependencies
```bash
npm install
# or
yarn install
```

### 3. Environment Setup
Create `.env.local` file in root:
```env
# Telegram Bot
NEXT_PUBLIC_TELEGRAM_TOKEN=your_bot_token_here
NEXT_PUBLIC_TELEGRAM_BOT_USERNAME=your_bot_username

# Firebase
NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

# Firebase Admin (Server-side)
FIREBASE_ADMIN_SDK_KEY=your_admin_sdk_key

# Database
DATABASE_URL=your_database_url
```

### 4. Create Telegram Bot
- Message [@BotFather](https://t.me/botfather) on Telegram
- Create a new bot and get the token
- Turn off "Group Privacy" to read group messages
- Add bot to your course groups

### 5. Setup Firebase
- Create Firebase project at [firebase.google.com](https://firebase.google.com)
- Enable Firestore Database
- Set up Authentication (Email/Password recommended)
- Download service account key for admin SDK

### 6. Run Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000)

### 7. Run Telegram Bot
```bash
npm run bot
```

## 📚 How It Works

### Course Organization Flow
1. **Bot Joins Group** - Bot is added to Telegram course group
2. **Message Parsing** - Bot analyzes message structure
3. **Parsing Logic**:
   - Pinned messages = Module titles
   - Message threads = Lesson groups
   - Media files = Lesson content
   - Links/text = Additional resources
4. **Data Sync** - Organized structure saved to Firestore
5. **Display** - Platform shows beautiful course structure
6. **Streaming** - Videos available for direct watching

## 🎮 Usage

### For Users
1. Visit the platform
2. View your enrolled courses
3. Browse modules and lessons
4. Watch videos directly (no download needed)
5. Track progress

### For Admins
1. Add CourseFlow bot to course group
2. Bot automatically organizes content
3. Course appears in platform
4. Manage courses via dashboard

## 🔧 Configuration

### Tailwind CSS
Edit `tailwind.config.js` for custom styling

### Next.js Config
Edit `next.config.js` for build optimization

### TypeScript
Edit `tsconfig.json` for compiler options

## 📖 API Documentation

### GET /api/courses
Fetch all courses

### GET /api/courses/[id]
Fetch specific course with modules

### GET /api/lessons/[id]
Fetch lesson details

### POST /api/webhook/telegram
Telegram bot webhook handler

## 🚀 Deployment

### Deploy to Vercel
```bash
npm install -g vercel
vercel
```

### Deploy to Railway/Render
- Connect GitHub repository
- Set environment variables
- Deploy automatically on push

## 🐛 Troubleshooting

**Bot not joining groups?**
- Check bot token is correct
- Ensure privacy mode is OFF
- Bot needs admin permissions

**Videos not loading?**
- Check Telegram token
- Verify video file exists in group
- Check browser network tab for errors

**Courses not appearing?**
- Check Firestore rules
- Verify bot permissions in group
- Check console for parsing errors

## 📝 Contributing

1. Fork repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open Pull Request

## 📄 License

MIT License - see LICENSE file for details

## 🤝 Support

- GitHub Issues: Report bugs or request features
- Discussions: Share ideas and get help
- Email: support@courseflow.dev

## 👨‍💻 Author

**Alleh Keyroz** - Full Stack Developer
- GitHub: [@AllehKeyroz](https://github.com/AllehKeyroz)
- Email: alleh@example.com

---

**⭐ If you found this project helpful, please give it a star!**
