# 👻 Ghost Note

**Anonymous Social Messaging Platform** - Connect with others through thoughtful, anonymous conversations with a beautiful, modern interface.

🌐 **Live Demo**: [ghost-note.vercel.app](https://ghost-note.vercel.app/)

## ✨ Features

### 🔐 **Authentication & Security**
- **Secure User Registration** with email verification
- **OTP-based Password Reset** with 10-minute expiry
- **Last Login Tracking** for user analytics
- **Session Management** with NextAuth.js
- **Password Hashing** with bcrypt
- **Username Uniqueness Validation**

### 💬 **Anonymous Messaging**
- **AI-Powered Message Suggestions** using Google Gemini 2.5 Pro
- **Anonymous Message Sending** to any user
- **Message Management** (view, delete messages)
- **Message Acceptance Toggle** (enable/disable receiving messages)
- **Real-time Message Updates**
- **Smart Fallback System** when AI limits are exceeded

### 📊 **Analytics & Insights**
- **Message Sentiment Analysis** (positive, negative, neutral)
- **Emotion Detection** (joy, sadness, anger, surprise, fear, disgust)
- **Topic Extraction** from message content
- **Timing Analytics** (peak hours, days, weekly patterns)
- **Sentiment Trends** over time
- **Message Statistics** (length, question ratio, exclamation ratio)

### 🎨 **Modern User Experience**
- **Beautiful Gradient Design** with glassmorphism effects
- **Responsive Design** optimized for all devices
- **Smooth Animations** and transitions
- **Toast Notifications** for user feedback
- **Loading States** with modern spinners
- **Error Handling** with contextual messages
- **Form Validation** with Zod schemas
- **Accessibility Features** for inclusive design

### 🤖 **Advanced AI Integration**
- **Smart Message Suggestions** that are engaging and conversation-worthy
- **Diverse Question Themes**: personal reflection, hypothetical scenarios, creativity
- **Context-Aware Prompts** for better message quality
- **Intelligent Fallback System** with curated default messages
- **Real-time AI Processing** with error handling

## 🚀 Tech Stack

- **Frontend**: Next.js 14 (App Router), React 18, TypeScript
- **Styling**: Tailwind CSS, shadcn/ui components, Lucide React icons
- **Backend**: Next.js API Routes, MongoDB with Mongoose
- **Authentication**: NextAuth.js with Credentials provider
- **AI**: Google Generative AI (Gemini 2.5 Flash)
- **Email**: Nodemailer with Gmail SMTP
- **Validation**: Zod schemas with React Hook Form
- **Deployment**: Vercel
- **Database**: MongoDB Atlas

## 📦 Installation

### Prerequisites
- Node.js 18+ 
- MongoDB Atlas account
- Google Cloud account (for Gemini AI)
- Gmail account (for email sending)

### Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ghost-note
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Variables**
   Create a `.env.local` file:
   ```env
   # Database
   MONGODB_URI=your_mongodb_atlas_connection_string
   
   # NextAuth
   NEXTAUTH_SECRET=your_nextauth_secret
   NEXTAUTH_URL=http://localhost:3000
   
   # Email (Gmail)
   GHOST_NOTE_EMAIL=your_gmail@gmail.com
   GHOST_NOTE_PASS=your_gmail_app_password
   
   # AI (Google Gemini)
   GOOGLE_GENERATIVE_AI_API_KEY=your_gemini_api_key
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🔧 Configuration

### MongoDB Setup
1. Create a MongoDB Atlas cluster
2. Get your connection string
3. Add it to `MONGODB_URI` in `.env.local`

### Gmail Setup (for email sending)
1. Enable 2-factor authentication on your Gmail account
2. Generate an App Password
3. Use the app password in `GHOST_NOTE_PASS`

### Google Gemini AI Setup
1. Go to [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create an API key
3. Add it to `GOOGLE_GENERATIVE_AI_API_KEY`

## 📱 Usage

### For Users
1. **Sign Up**: Create an account with email verification
2. **Get Your Link**: Copy your unique profile link from the dashboard
3. **Share**: Share your link with friends or on social media
4. **Receive Messages**: Get anonymous messages from others
5. **Manage**: View, delete, and control message acceptance
6. **Analytics**: View insights about your messages

### For Senders
1. **Visit Profile**: Go to any user's Ghost Note profile
2. **Get Suggestions**: Click "Suggest Messages" for AI-generated ideas
3. **Send Message**: Write your own message or use a suggestion
4. **Stay Anonymous**: Your identity remains hidden

## 🏗️ Project Structure

```
src/
├── app/                    # Next.js 14 app directory
│   ├── (auth)/            # Authentication pages (sign-in, sign-up, forgot-pass, verify)
│   ├── (app)/             # Protected app pages (dashboard, analytics, user profiles)
│   ├── api/               # API routes (auth, messages, analytics, AI suggestions)
│   └── globals.css        # Global styles with custom background
├── components/            # Reusable UI components
│   ├── ui/               # shadcn/ui components
│   ├── User.tsx          # User profile component
│   ├── Navbar.tsx        # Navigation component
│   └── ...               # Status components (Not, NotFound, Verified, etc.)
├── context/              # React context providers (AuthProvider)
├── helpers/              # Email utility functions
├── lib/                  # Database connection and utilities
├── models/               # MongoDB schemas (User model)
├── schemas/              # Zod validation schemas
└── types/                # TypeScript type definitions
```

## 🎨 Design System

### Color Palette
- **Primary**: Stone gradient (stone-50 to stone-100)
- **Text**: Stone-800 to stone-600 gradients
- **Cards**: White with 70% opacity and backdrop blur
- **Accents**: Consistent stone color variations

### Components
- **Glassmorphism Cards**: Modern translucent design
- **Gradient Backgrounds**: Subtle stone gradients
- **Responsive Grid**: Adaptive layouts for all devices
- **Modern Icons**: Lucide React icon set
- **Smooth Transitions**: CSS transitions and animations

## 🔒 Security Features

- **Password Hashing**: bcrypt with salt rounds
- **Email Verification**: OTP-based account verification
- **Session Management**: Secure session handling with NextAuth.js
- **Input Validation**: Zod schema validation on all forms
- **Rate Limiting**: Built-in Next.js protection
- **CORS Protection**: Configured for production
- **Environment Variables**: Secure configuration management

## 🚀 Deployment

### Vercel (Recommended)
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add environment variables in Vercel dashboard
4. Deploy automatically with zero configuration

### Environment Variables for Production
```env
MONGODB_URI=your_production_mongodb_uri
NEXTAUTH_SECRET=your_production_secret
NEXTAUTH_URL=https://your-domain.vercel.app
GHOST_NOTE_EMAIL=your_production_email
GHOST_NOTE_PASS=your_production_email_password
GOOGLE_GENERATIVE_AI_API_KEY=your_production_ai_key
```

## 🧪 Testing

The application is production-ready with:
- **Type Safety**: Full TypeScript coverage
- **Form Validation**: Comprehensive Zod schemas
- **Error Handling**: Graceful error states
- **Loading States**: User-friendly loading indicators
- **Responsive Design**: Tested across devices

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Next.js** for the amazing React framework
- **shadcn/ui** for beautiful UI components
- **Google Gemini** for AI-powered message suggestions
- **MongoDB** for reliable database storage
- **Vercel** for seamless deployment
- **Tailwind CSS** for utility-first styling
- **Lucide React** for beautiful icons

## 📞 Support

- **Live Demo**: [ghost-note.vercel.app](https://ghost-note.vercel.app/)
- **Issues**: [GitHub Issues](https://github.com/samdeepsharma/ghost-note/issues)
- **Email**: [services.ghost.note@gmail.com](mailto:services.ghost.note@gmail.com)

---

**Made with ❤️ for anonymous conversations**

*Ghost Note - Where thoughts flow freely, identities stay hidden.*
