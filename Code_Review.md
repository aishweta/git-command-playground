
## Code Review Guidelines

1. **Understand the Requirements:** Before starting the review, ensure you understand the requirements and purpose of the code you're reviewing.

2. **Check Naming Conventions for the files:** For module file names, Use all lowercase letters and limit symbols to numbers or underscores. `_`
```
my_module.py (correct)
My_Module.py (incorrect)
module_1.py (correct)
module-1.py (incorrect)
```
3. **Ensure naming conventions for variables, functions, and classes are meaningful and relevant to their purpose.**
```
Variable: user_age (relevant) [mostly in lowercase]
Function: calculate_total_cost() (relevant) [mostly in lowercase]
Class: CustomerDatabase (relevant) [mostly in CamelCase]
```
4. **Remove all comments and Opt for Comprehensive Docstrings:** Instead of using numerous in-line comments, focus on writing descriptive docstrings for functions, classes, and modules to explain their purpose, parameters, and return values effectively.We prefer to follow the [numpy style](https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_numpy.html)

5. Define class attributes in the constructor to group together the parameters used in class methods, promoting cleaner code organization and ensuring all parameters are accessible within the class.

Additionally; You can make most of class methods with no parameters. Simplify class methods by eliminating unnecessary parameters.

- **Before:**
```
class Adder:
    def __init__(self):
        pass
    
    def add(self, num1, num2):
        return num1 + num2
```
- **After:**
```
class Adder:
    def __init__(self, num1: int = 0, num2: int = 0):
        self.num1 = num1
        self.num2 = num2
    
    def add(self):
        return self.num1 + self.num2
```
6. **Code Style and Standards:** Ensure that the code follows coding standards and style guidelines. Check for consistency in formatting, indentation, spacing, etc.

7. **Consider Static Methods for General Utility Functions:**
If a method within a class does not require access to instance attributes, consider making it a static method, allowing it to be called outside the class without creating an instance. For example, to convert a dataset into a JSON format, define a static method save_dataset_to_json that takes the dataset and file name as parameters.
```
class DatasetProcessor:
    @staticmethod
    def save_dataset_to_json(dataset: List[Dict], file_name: str) -> None:
        """Your DocString
        """
        with open(file_name, 'w') as f:
            json.dump(dataset, f)
```
```
# Example usage:
data = [
    {"id": 1, "name": "John"},
    {"id": 2, "name": "Alice"}
]

DatasetProcessor.save_dataset_to_json(data, "dataset.json")
```
8. **Security:** Avoid including sensitive information like API keys or tokens in your code repositories, especially when pushing to GitHub. Instead, utilize secure storage solutions like AWS Parameter Store for managing sensitive credentials.

9. You should add dependencies with versions to the requirements.txt file of the project.

10. Create a notebook to show-case the module you implemented, show sample output in a notebook.

11. Remove duplicate files, notebook from GitHub.

12. Do not save any .json, .txt or .csv files in GitHub

13. Remove unnecessary import functions from your module and notebook.

14. Try to replace default values to the parameter of functions.

15. In every python file add a single blank-line at the end. PEP8 convention

16. A single blanc line/space between class methods.
