StudyScroll
Scroll. Learn. Grow.
An AI-powered learning platform that turns students' study materials
into an interactive, personalized learning feed.

StudyScroll is a work-in-progress project focused on making studying
more engaging and accessible. Students will be able to upload their
notes and documents, generate AI-assisted learning content, practise
through a vertical scrolling feed, and track their progress.
Project status: In development
Current stage: Initial project setup and planning

Table of Contents
- Vision
- Planned Features
- Technology Stack
- How It Works
- Project Structure
- Getting Started
- Environment Variables
- Development Roadmap
- Security Notes
- Contributing
- License
Vision
Traditional study tools can make revision feel repetitive and
disconnected. StudyScroll aims to bring learning into a simple,
mobile-first experience inspired by the ease of scrolling through a
content feed.

The goal is to help students turn their own study material into
bite-sized, useful learning activities---while keeping the learning
process structured and measurable.
Planned Features
Learning materials
- Upload PDF, PPTX, DOCX, and TXT files.
- Organize materials by subject, semester, unit, and topic.
- Extract document text and retain source-page or slide references.
AI-powered learning
- Generate multiple-choice questions (MCQs).
- Create concise notes and topic summaries.
- Generate flashcards.
- Provide answer explanations grounded in uploaded material.
- Support different question difficulty levels.
- Offer an AI tutor for questions about a student's materials.
Interactive study feed
- Browse learning cards in a vertical feed.
- Answer MCQs and receive feedback.
- Read explanations and source references.
- Bookmark useful questions and notes.
- Load more learning content as the student scrolls.
Practice and progress
- Create and attempt quizzes.
- Review previous attempts and answers.
- Track accuracy, study activity, and topic-wise performance.
- Identify topics that need revision.
- Recommend revision activities based on learning progress.
Student experience
- Student accounts and profiles.
- Subject and topic organization.
- Responsive, mobile-first interface.
- A clean, accessible visual design.
Features are planned and will be delivered incrementally. Not every
feature is implemented yet.
Technology Stack
The planned stack is:

  Layer                 Technology
  Frontend              React, TypeScript, Vite
Styling               Tailwind CSS
Routing               React Router
Client state          Zustand
API communication     Axios
Backend               Node.js, Express, TypeScript
Database              MongoDB Atlas, Mongoose
AI                    Google Gemini API (@google/genai)
Authentication        JWT, bcrypt
Validation            Zod
File uploads          Multer
Document processing   PDF.js, Mammoth, JSZip
Android app           Capacitor
Frontend hosting      Vercel (planned)
Backend hosting       Render (planned)

The technology choices may be refined as development progresses.
How It Works
The intended core workflow is:
1. A student creates an account and adds subjects.
2. The student uploads study material.
3. The backend validates the file and extracts its text.
4. The extracted content is prepared and sent to the AI service.
5. The AI generates structured learning content, such as MCQs, notes,
   and flashcards.
6. The backend validates and stores the generated content.
7. The student studies through the interactive feed.
8. Study attempts are recorded to calculate progress and recommend
   revision.
Project Structure
The planned repository structure is:
StudyScroll/
├── client/                 # React + TypeScript frontend
│   ├── public/
│   └── src/
│       ├── assets/
│       ├── components/
│       ├── pages/
│       ├── services/
│       ├── hooks/
│       ├── store/
│       ├── types/
│       └── utils/
│
├── server/                 # Express + TypeScript backend
│   └── src/
│       ├── config/
│       ├── models/
│       ├── controllers/
│       ├── middleware/
│       ├── routes/
│       ├── services/
│       │   ├── ai/
│       │   ├── documents/
│       │   ├── quiz/
│       │   └── revision/
│       ├── validators/
│       └── utils/
│
├── docs/                   # Requirements and technical documentation
├── .gitignore
└── README.md
Folders and modules will be added as implementation progresses.
Getting Started
Prerequisites
Install the following before starting development:
- Node.js 22 LTS
- Git
- Visual Studio Code or another code
  editor
- A MongoDB Atlas account
- A Google AI Studio API key for
  Gemini integration
Check your installations:
node --version
npm --version
git --version
Clone the repository
git clone https://github.com/Shweta-V-Mahadik/StudyScroll.git
cd StudyScroll
Install dependencies
Once the frontend and backend package files have been created, install
their dependencies:
cd client
npm install

cd ../server
npm install
Configure environment variables
Create a .env file inside the server directory. Add the required
values once the corresponding configuration is implemented:
PORT=5000
NODE_ENV=development
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_strong_random_secret
GEMINI_API_KEY=your_gemini_api_key
CLIENT_URL=http://localhost:5173
Do not use the example values as real credentials. Never commit .env
files or secrets to Git.
Run the application
The exact scripts will be documented here after the frontend and backend
development configurations are added.
Development Roadmap
Development will follow these milestones:
- [ ] Requirements and system design
- [ ] Repository and frontend/backend setup
- [ ] MongoDB connection and data models
- [ ] Registration, login, and student profiles
- [ ] Subject and topic management
- [ ] Document upload and text extraction
- [ ] Gemini integration and structured content generation
- [ ] Interactive scrolling study feed
- [ ] Quizzes and flashcards
- [ ] Bookmarks and study history
- [ ] Analytics and revision recommendations
- [ ] AI tutor
- [ ] Testing, security review, and performance improvements
- [ ] Responsive production deployment
- [ ] Android packaging with Capacitor
- [ ] Google Play release preparation
First MVP goal
The first end-to-end milestone is:

Upload a PDF → extract its text → generate 10 MCQs → answer them in
the study feed → view explanations and save the result.
Security Notes
- Keep Gemini and other private API keys on the backend.
- Store secrets in environment variables and exclude .env files from
  version control.
- Hash passwords; never store plain-text passwords.
- Protect private routes with authentication and authorization checks.
- Verify that users can access only their own documents and learning
  data.
- Validate uploaded file types and sizes.
- Keep uploaded student documents private.
- Avoid exposing correct answers before a question is submitted.
Contributing
StudyScroll is currently an individual project in active development.
Suggestions, bug reports, and improvement ideas are welcome.

If you want to contribute:
1. Fork the repository.
2. Create a feature branch.
3. Make and test your changes.
4. Commit your changes with a clear message.
5. Open a pull request describing the update.