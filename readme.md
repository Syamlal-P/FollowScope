📸 Instagram Non-Follower Tracker (Interactive Web App)

An interactive and responsive web application that allows users to upload their official Instagram data export (JSON format) and instantly discover who does not follow them back.

This project is designed to be safe, privacy-focused, and deployable on Vercel using a modern frontend with a Python backend (serverless or Flask-based).
---
🚀 Live Features










- 📂 Upload Instagram JSON files securely
- 🔍 Automatically detects multiple Instagram data formats
- 📊 Displays:
  - Total Followers
  - Total Following
  - Users Not Following Back
- 📥 Download results as TXT file
- 📱 Fully responsive (Mobile + Desktop)
- ⚡ Fast processing using Python set operations
- 🔐 No login, no scraping, no API abuse

---

🛡️ Privacy & Safety

This application:

- Does NOT use Instagram login
- Does NOT scrape Instagram
- Does NOT require password access
- Only processes files manually uploaded by the user
- Does not permanently store user data

All processing happens within your deployed environment.

---

📥 How to Get Your Instagram Data

1. Visit:
   https://www.instagram.com/download/request/

2. Select:
   
   - Format: JSON

3. Download the ZIP file sent to your email.

4. Extract the ZIP file.

5. Navigate to:
   connections/

6. Locate:
   
   - followers_1.json
   - following.json

Upload these files into the application.

---

🧠 How It Works (Technical Overview)

1. The app reads uploaded JSON files.

2. Extracts usernames from:
   
   - "title" fields (new Instagram format)
   - "string_list_data" fields (older format)

3. Converts followers and following lists into Python sets.

4. Performs set difference:
   
   not_following_back = following - followers

5. Returns the results to the frontend.

Time Complexity: O(n)
Space Complexity: O(n)

---

📂 Project Structure

instagram-nonfollower-tracker/
│
├── api/                  # Python backend (Vercel Serverless Functions)
│   └── check.py
│
├── public/               # Frontend files
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── requirements.txt
├── vercel.json
└── README.md

---

🖥️ Local Development Setup

1️⃣ Clone Repository

git clone https://github.com/yourusername/instagram-nonfollower-tracker.git
cd instagram-nonfollower-tracker

2️⃣ Create Virtual Environment (Recommended)

python -m venv venv
venv\Scripts\activate   (Windows)

3️⃣ Install Dependencies

pip install -r requirements.txt

4️⃣ Run Locally (If Using Flask Backend)

python app.py

Then open:
http://127.0.0.1:5000

---

🚀 Deploying on Vercel

Step 1

Push your project to GitHub.

Step 2

Go to:
https://vercel.com

Step 3

Import your GitHub repository.

Step 4

Framework Preset:

- Select "Other"
- Enable Python runtime

Step 5

Deploy 🎉

Vercel will automatically build and deploy your serverless Python function inside the "/api" directory.

---

📊 Example Output

Total Following: 400
Total Followers: 255
Not Following Back: 145

A downloadable file:
not_following_back.txt

---

📱 Responsive Design

- Mobile-first layout
- Flexbox / Grid structure
- Smooth transitions
- Clean minimal UI
- Works across modern browsers

---

🧩 Supported Instagram Formats

This app supports:

Old Format:

- string_list_data → value

New Format:

- title field inside relationships_following

Multiple file versions can be extended easily.

---

🔮 Future Improvements

- 📦 Direct ZIP upload support
- 📊 Analytics dashboard
- 📁 CSV / Excel export
- 🔄 Mutual followers list
- 🌙 Dark mode toggle
- 📈 Follower growth tracking
- 🔐 Optional authentication layer

---

⚠️ Disclaimer

This project is intended for educational and personal productivity use only.

It does not bypass Instagram restrictions and does not violate Instagram policies because it only uses official user-downloaded data.

Users are responsible for their own usage.

---

👨‍💻 Author

Syamlal P
Palakkad, Kerala, India

GitHub: https://github.com/Syamlal-P
LinkedIn: https://www.linkedin.com/in/syam-lal-p

---

⭐ Support

If you found this project useful:

- Star the repository ⭐
- Share it with friends
- Fork and improve it

---

🧠 Why This Project Matters

This project demonstrates:

- File handling in Python
- JSON parsing with multiple formats
- Set operations for efficient comparison
- Serverless deployment
- Responsive frontend design
- Privacy-first engineering approach

It is a clean portfolio-ready full-stack mini project.

---

Built with ❤️ using Python, HTML, CSS, and JavaScript.
