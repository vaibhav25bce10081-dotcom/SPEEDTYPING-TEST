## Typing Speed Test Python Project

-----

### **Overview**

This is a simple console-based Python application designed to test and measure a user's **typing speed** and **accuracy**. It presents the user with a random test sentence and calculates the typing speed in words per second (w/sec) and the total number of errors made.

### **Features**

  * **Randomized Test Sentences:** Selects a typing prompt at random from a predefined list.
  * **Speed Calculation:** Measures the time taken to complete the test and calculates the typing speed.
  * **Error Counting:** Compares the user's input with the test text character by character to calculate the number of mistakes.
  * **Interactive Interface:** Allows the user to start or quit the test session.

### **How to Run the Project**

#### **1. Prerequisites**

You need to have **Python 3.x** installed on your system.

#### **2. Running the Script**

1.  Save the provided code as a Python file (e.g., `typing_test.py`).

2.  Open your terminal or command prompt.

3.  Navigate to the directory where you saved the file.

4.  Execute the script using the Python interpreter:

    ```bash
    python typing_test.py
    ```

#### **3. Using the Test**

1.  The program will ask you: ` ready to test : yes / no :  `.
2.  Type **`yes`** to begin the test.
3.  A random sentence will be displayed.
4.  The script will record the start time. **Type the sentence exactly as displayed** and press **Enter**.
5.  The script will display your **Speed** and the total **Error** count.
6.  Type **`no`** when prompted to exit the program.

### **Code Explanation**

The project is built around three core functions:

#### **`speed_time(time_s, time_e, userinput)`**

  * **Purpose:** Calculates the typing speed.
  * **Logic:**
    1.  Calculates the `time_delay` (time elapsed).
    2.  Divides the length of the `userinput` (characters typed) by the `time_delay`.
    3.  Returns the result rounded to the nearest integer, representing **characters/sec** (labeled as 'word/sec' in the output).

#### **`mistake(partest, usertest)`**

  * **Purpose:** Calculates the total number of errors.
  * **Logic:**
    1.  Iterates through both the `partest` (actual text) and `usertest` (user's input) character by character.
    2.  Increments the `error` counter if the characters at the same index do not match, or if the user's input is shorter than the test text (handled by the `try-except` block).
    3.  Returns the total `error` count.

#### **`if __name__ == "__main__":`**

  * **Purpose:** The main loop that runs the application.
  * **Logic:**
    1.  Uses a `while True` loop to keep the test running until the user enters `no`.
    2.  Prompts the user to start the test.
    3.  If `yes`, a random test sentence is selected.
    4.  Records `time_1`, captures `testinput`, and records `time_2`.
    5.  Calls `speed_time` and `mistake` to display the results.
