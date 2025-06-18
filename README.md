# Tutedude_Devops
Commands for Flask App
Here's a concise list of all the Linux commands used in your Flask-MongoDB project with explanations:

1. Project Setup
bash
# Create project directory
mkdir mongo-flask-app && cd mongo-flask-app
mkdir: Creates a new directory

&&: Chains commands (enters the directory after creation)

2. Virtual Environment
bash
# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate  # Activates the environment
python3 -m venv: Creates a Python virtual environment

source: Loads environment settings (replaces venv\Scripts\activate on Windows)

3. Dependency Management
bash
# Install packages
pip install flask pymongo python-dotenv

# Freeze dependencies to requirements.txt
pip freeze > requirements.txt
pip freeze: Lists all installed packages

>: Redirects output to a file

4. Environment Configuration
bash
# Create/modify .env file
nano .env  # Text editor to add DB credentials
nano: Lightweight terminal text editor (alternatives: vim, gedit)

5. File Operations
bash
# Rename environment file
mv modify.env .env

# Verify file contents
cat .env  # Displays file content
ls -la    # Lists all files (including hidden)
mv: Renames/moves files

cat: Prints file content

ls -la: Lists files with permissions/hidden files

6. Run Flask App
bash
# Run the application
python3 app.py
Starts Flask development server (default: http://127.0.0.1:5000)

7. Network & Debugging
bash
# Check if port 5000 is in use
sudo lsof -i :5000  # Lists processes using the port

# Allow external access (if needed)
sudo ufw allow 5000  # Configures firewall
lsof: Lists open files/ports

ufw: Uncomplicated Firewall (Ubuntu)

8. Git Version Control
bash
# Initialize and push to GitHub
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/repo.git
git push -u origin main
git init: Creates a new Git repo

git add .: Stages all files

git remote add: Links to remote repository

Key Notes:
Use Ctrl+C to stop the Flask server.

For MongoDB troubleshooting:

bash
curl http://localhost:5000/api  # Test API endpoint
Let me know if you'd like to dive deeper into any command! 🐧
