import os

# Project directory structure
project_structure = {
    "Dataman": [
        "src",
        "data",
        "tests",
        "requirements.txt",
        "README.md"
    ],
    "src": [
        "main.py",
        "modules",
        "utils"
    ],
    "tests": [],
    "modules": [],
    "utils": []
}

def create_directory(path):
    """ Create a directory if it doesn't exist """
    if not os.path.exists(path):
        os.makedirs(path)

def create_file(path):
    """ Create a file if it doesn't exist """
    if not os.path.exists(path):
        with open(path, 'w') as f:
            pass  # Create an empty file

def setup_project_structure(base_path, structure):
    """ Recursively create project structure """
    for key, values in structure.items():
        dir_path = os.path.join(base_path, key)
        create_directory(dir_path)

        for item in values:
            if '.' in item:  # It's a file
                create_file(os.path.join(dir_path, item))
            else:  # It's a directory
                setup_project_structure(dir_path, {item: structure[item]})

# Setting up the project structure
project_base_path = os.getcwd()  # or replace with a specific path
setup_project_structure(project_base_path, project_structure)

print("Project structure created successfully!")
