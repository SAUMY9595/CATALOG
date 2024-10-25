Steps to Run the Code
1. Clone the Repository
First, clone the repository to your local machine using the command:

git clone <repository-url>



2. Install Dependencies
Make sure to have the nlohmann/json library for JSON parsing in C++. You can use the single-header version by downloading from here. Place the json.hpp file in your project directory.

Alternatively, if you are using a package manager like vcpkg or brew, you can install it directly:

vcpkg install nlohmann-json




3. Prepare the Input JSON
Create a file named input.json in the same directory as the source code. This file will contain the polynomial data in JSON format. Here is an example:



json code:
{
    "keys": {
        "n": 4,
        "k": 3
    },
    "1": {
        "base": "10",
        "value": "4"
    },
    "2": {
        "base": "2",
        "value": "111"
    },
    "3": {
        "base": "10",
        "value": "12"
    },
    "6": {
        "base": "4",
        "value": "213"
    }
}



4. Compile the Code
Compile the C++ program using the following command:

command: g++ -o secret_finder main.cpp -std=c++11




5. Run the Program
Run the compiled program. It will read from the input.json file, decode the points, and apply Lagrange interpolation to calculate the constant term:


bash : ./secret_finder



6. View the Output
The output will display the calculated constant term  c

c, which is the secret of the polynomial. Example output:The constant term (secret c) is: 3
