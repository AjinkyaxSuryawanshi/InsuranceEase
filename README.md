# 🛡️ InsureEase - AI driven Policy Management system
**Deployed Project:** [https://insure-webapp.vercel.app/](https://insure-webapp.vercel.app/) ✅  
[![Deployed on Vercel](https://img.shields.io/badge/Live%20Demo-Vercel-brightgreen?style=for-the-badge&logo=vercel)](https://insure-webapp.vercel.app/)


InsuranceEase is a feature-rich, responsive insurance comparison web application.
Users can browse, filter, and compare insurance policies across major categories like Health, Vehicle, Mobile, and Life.
It includes a built-in premium calculator that adjusts based on user inputs such as age, vehicle type, coverage, etc.
The frontend is crafted using React.js with Tailwind CSS for clean UI and responsiveness across devices.
UI components leverage Radix UI for accessibility and Lucide for modern icons.
Authentication is handled with JWT tokens, and all sensitive data is secured using AES-256 encryption.
The app also supports a dynamic dashboard layout with stateful UI updates.
The backend is built on Node.js and Express.js, providing RESTful APIs for CRUD operations.
MongoDB is used as the database with Mongoose for schema definition.
Hosted locally with Vite for fast development, with Git for version control.
Clean folder structure and component separation make it highly maintainable.
Features a Stripe-inspired modern design with hover effects and animations.
Uses reusable components, centralized utility functions, and protected routes.
Built with scalability and developer experience in mind.
Ideal for users seeking a clean, secure, and user-friendly insurance comparison solution.



![InsureEase Platform](https://img.shields.io/badge/Next.js-15.2.0-black?style=for-the-badge&logo=next.js)
![React](https://img.shields.io/badge/React-18.2.0-blue?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)
![Flask](https://img.shields.io/badge/Flask-2.3.3-green?style=for-the-badge&logo=flask)
![MongoDB](https://img.shields.io/badge/MongoDB-6.14.2-green?style=for-the-badge&logo=mongodb)

## ✨ Features

### 🎯 Core Features
- **Multi-Insurance Support**: Health, Vehicle, Life, Home, and Travel Insurance and many more.
- **User Authentication**: Secure login/register with JWT tokens.
- **Admin Dashboard**: Complete policy and application management.
- **Policy Application**: Streamlined application process with document upload.
- **Claims Management**: Submit and track insurance claims.
- **Document Vault**: Secure document storage and management, using whenever required.
- **Payment Integration**: Razorpay payment gateway integration.
- **PDF Processing**: AI-powered PDF summarization and analysis.

### 🤖 AI & Voice Features
- **Smart Chatbot**: FAQ-based insurance assistant with keyword matching
- **Voice Navigation**: Speech-to-text and text-to-speech capabilities
- **Policy Recommendations**: AI-driven policy suggestions based on user needs
- **Document Analysis**: Intelligent PDF processing and summarization

### 🎨 Modern UI/UX
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Dark/Light Mode**: Theme switching with next-themes
- **Smooth Animations**: Framer Motion powered interactions
- **Accessible Components**: Radix UI components for better accessibility
- **Real-time Updates**: Live notifications and status updates

## 🏗️ Architecture

```
InsureEase/
├── Frontend_next/          # Next.js 15 frontend application
│   ├── app/               # App router pages and layouts
│   ├── components/        # Reusable React components
│   ├── pages/api/         # API routes for backend integration
│   ├── services/          # API client and service layers
│   └── types/            # TypeScript type definitions
├── Chatbot_Backend/       # Flask-based AI chatbot service
│   ├── app.py            # Main Flask application
│   ├── voice_nav_backend.py # Voice navigation backend
│   └── insurance_dataset.csv # FAQ dataset
├── k8s/                  # Kubernetes deployment configs
├── nginx/                # Nginx configuration
└── terraform/            # Infrastructure as Code
```

## 🚀 Tech Stack

### Frontend
- **Next.js 15** - React framework with App Router
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Animation library
- **Radix UI** - Accessible component primitives
- **Zustand** - State management
- **Axios** - HTTP client

### Backend
- **Flask** - Python web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB ODM
- **JWT** - Authentication tokens
- **Razorpay** - Payment gateway
- **Cloudinary** - Cloud storage for documents

### AI & ML
- **SpeechRecognition** - Voice processing
- **gTTS** - Text-to-speech
- **scikit-learn** - Machine learning utilities
- **Pandas** - Data processing

### DevOps
- **Docker** - Containerization
- **Kubernetes** - Container orchestration
- **Terraform** - Infrastructure as Code
- **Nginx** - Reverse proxy

## 📦 Installation

### Prerequisites
- Node.js 18+ 
- Python 3.8+
- MongoDB
- Git

### Frontend Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/insure-ease.git
cd insure-ease/Frontend_next

# Install dependencies
npm install

# Set up environment variables
cp env.example .env.local
# Edit .env.local with your configuration

# Run development server
npm run dev
```

### Backend Setup

```bash
# Navigate to backend directory
cd ../Chatbot_Backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
export FLASK_APP=app.py
export FLASK_ENV=development

# Run Flask server
python app.py
```

### Environment Variables

Create `.env.local` in the frontend directory:

```env
# Database
MONGODB_URI=your_mongodb_connection_string

# Authentication
JWT_SECRET=your_jwt_secret_key
NEXTAUTH_SECRET=your_nextauth_secret

# Payment Gateway
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_secret

# Cloud Storage
CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_key
CLOUDINARY_API_SECRET=your_cloudinary_secret

# Email Service
RESEND_API_KEY=your_resend_api_key

# Backend URLs
NEXT_PUBLIC_BACKEND_URL=http://localhost:5000
NEXT_PUBLIC_CHATBOT_URL=http://localhost:5001
```

## 🎮 Usage

### For Users
1. **Register/Login**: Create an account or sign in
2. **Browse Policies**: Explore different insurance categories
3. **Apply for Insurance**: Complete application forms with document upload
4. **Make Payment**: Secure payment through Razorpay
5. **Track Applications**: Monitor application status
6. **Submit Claims**: File and track insurance claims
7. **Manage Documents**: Store and organize insurance documents

### For Admins
1. **Admin Login**: Access admin dashboard
2. **Review Applications**: Approve or reject policy applications
3. **Manage Policies**: Create and update insurance policies
4. **Process Claims**: Handle user claims and settlements
5. **User Management**: Monitor user activities and accounts

### AI Chatbot
- Ask questions about insurance policies
- Get instant answers to common queries
- Navigate through the platform using voice commands

## 🔧 API Endpoints

### Authentication
- `POST /api/register` - User registration
- `POST /api/login` - User login
- `POST /api/logout` - User logout
- `POST /api/admin/login` - Admin login

### Policies
- `GET /api/policies` - Get all policies
- `POST /api/policy-apply-form` - Submit policy application
- `GET /api/user-policies` - Get user's policies

### Claims
- `POST /api/submit-claim` - Submit insurance claim
- `GET /api/user-claims` - Get user's claims

### Documents
- `POST /api/documents/upload` - Upload documents
- `GET /api/documents/[documentId]` - Get document

### Chatbot
- `POST /api/chat` - Chat with AI assistant
- `GET /api/health` - Health check

## 🚀 Deployment

### Frontend (Vercel)
```bash
# Build the application
npm run build

# Deploy to Vercel
vercel --prod
```

### Backend (Heroku/Railway)
```bash
# Set up Procfile
echo "web: gunicorn app:app" > Procfile

# Deploy to Heroku
heroku create your-app-name
git push heroku main
```

### Docker Deployment
```bash
# Build and run with Docker Compose
docker-compose up -d
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing React framework
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS
- [Radix UI](https://www.radix-ui.com/) for accessible components
- [Framer Motion](https://www.framer.com/motion/) for animations
- [Razorpay](https://razorpay.com/) for payment integration

## 📞 Support

For support, create an issue in the repository.

