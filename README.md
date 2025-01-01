# Python Quiz Community

This project aims to create an interactive online platform where Python beginners can test their knowledge and enhance their learning experience through quizzes.

## Getting Started

This project requires Python and a few additional libraries. You can set up the environment using the following steps:

1. **Clone the repository:**

   ```bash
      git clone https://github.com/TBJr/python-quiz-community.git
   ```
   [GitHub Repo](https://github.com/TBJr/python-quiz-community.git)
   
2. **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   
3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   
## Project Structure
   ```
   python-quiz-community/
   ├── app/
   │   ├── __init__.py
   │   ├── main.py
   │   ├── templates/
   │   │   ├── index.html
   │   │   ├── quiz.html
   │   │   └── results.html
   │   ├── static/
   │   │   ├── style.css
   │   │   └── js/script.js
   │   ├── questions.json
   │   └── utils.py
   ├── requirements.txt
   ├── Procfile
   └── README.md
   ```

- app/: Contains the core Python code for the web application.
- templates/: Stores HTML templates for the user interface.
- static/: Holds static files like CSS and JavaScript for styling and interactivity.
- questions.json: Stores quiz questions and answers in JSON format.
- utils.py: Contains utility functions used throughout the application.
- requirements.txt: Lists all project dependencies.
- Procfile: Defines the deployment process using gunicorn (optional).
- README.md: The project documentation (this file).

## Running the Application
   1. Start the development server:
   ```bash
      python app/main.py
   ```
   2. Access the application in your web browser at http://localhost:5000/

## Deployment
This project can be deployed to GitHub Pages for public accessibility. You'll need to configure a workflow in GitHub Actions to automate the build, install dependencies, deploy the application, and push the built files to the gh-pages branch.

## Contributing
We welcome contributions to this project! Feel free to create pull requests with improvements, bug fixes, or new features.

## License
This project is licensed under the [MIT License](). See the LICENSE file for details.

## Project Scope
This project focuses on core functionalities like creating quizzes, taking quizzes, and viewing results. It's designed to be beginner-friendly and easy to use.

## Additional Notes
- Consider adding user accounts and login features for future enhancements.
- Explore integrating with code editors or learning platforms for a more comprehensive learning experience.
- Always refer to the documentation for Flask and GitHub Pages for best practices.

We hope this project empowers Python beginners to learn and practice their skills in a fun and interactive way!