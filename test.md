# Legal Documents Meet AI: from Python Setup to AI Document Analysis!
Hey there, tech enthusiasts and legal eagles! Have you ever wondered about the spectacular possibilities that could arise from the intersection of artificial intelligence and the legal domain? Well, you're in luck, because we're about to embark on an exciting journey exploring just that!

In this blog post, we'll be setting you up with all the tools you need to harness the power of AI for legal document analysis. We'll guide you through the process of setting up Python and pip on your machine, creating and activating a Python virtual environment, and installing the necessary Python packages.

But that's not all! We'll also dive into the world of OpenAI, providing you with tips on securing your API key and running the language model with your own documents and system prompts. We'll show you how to use a document chat program and even set up aliases to make the running of the program a breeze.

And finally, we'll explore the bright future of AI in the legal domain, discussing its potential applications and how it's being utilized today at LawPilot. LawPilot is an AI legal assistant builder that trains ChatGPT on your legal documents, helping you summarize and revise documents, generate and optimize arguments, and so much more. You can even upload multiple files, give your AI assistant instructions, and rest assured knowing that your data is securely stored on GCP/AWS servers​1​.

So, fasten your seatbelts and get ready to delve into the thrilling world of AI and legal documents!

# How to Setup Python3 and pip3 on Your Computer

In this section, we'll cover the basics of how to install Python3 and pip3 on your computer and set them as the default. We'll focus on three main operating systems: Windows, Linux, and macOS. But first, let's have a quick primer on what Python, pip, and the command line/terminal are.

## A Quick Primer
### Python
Python is a high-level, interpreted programming language that's loved by many for its clear syntax and readability. Python 3 is the latest version of the language, and it's what we'll be installing.
### pip
pip is a package manager for Python. This means that it's a tool that allows you to install and manage additional libraries and dependencies that are not part of the standard Python library.
### Command Line/Terminal
The command line (also known as the terminal in macOS and Linux) is a text-based interface where you can type commands for your computer to execute. For our purposes, you'll use the command line to install Python and pip, and to run Python programs.

## Setting up Python3 and pip3
### Windows
1. **Download the Python installer:** Head to the [official Python website](https://www.python.org/downloads/windows/) and download the latest version of Python 3.

2. **Run the installer:** Once the download is complete, locate the .exe file in your Downloads folder and double-click on it to run the installer.

3. **Customize the installation:** In the installer, check the box next to "Add Python 3.x to PATH". This will make Python3 your default Python. Then, click on "Customize Installation".

4. **Ensure pip gets installed:** In the next screen, ensure that the "pip" checkbox is ticked. Then, continue with the installation.
### macOS
1. **Download and install Homebrew:** Homebrew is a package manager for macOS. It'll make installing Python3 and pip3 easier. Open the Terminal application and paste the following command to install Homebrew:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
  
2. **Install Python3:** Once Homebrew is installed, you can install Python3 by typing the following command in Terminal:

```bash
brew install python3
```

3. **Check Python3 and pip3 installation:** Python3 comes with pip3. You can check your installation by typing these commands in Terminal:

```bash
python3 --version
pip3 --version
```
### Linux
The exact process for installing Python3 and pip3 on Linux depends on the distribution you're using. Here are the general steps for Debian-based distributions like Ubuntu:

1. **Update your package list:** Open the Terminal and type the following command:

```bash
sudo apt-get update
```

2. **Install Python3:** Then, install Python3 with this command:

```bash
sudo apt-get install python3
```

3. **Install pip3:** You can install pip3 with the following command:

```bash
sudo apt-get install python3-pip
```

4. **Check Python3 and pip3 installation:** Type these commands to verify your installation:

```bash
python3 --version
pip3 --version
```

To make Python3 the default on your Linux system, you can use an alias. Open your .bashrc or .bash_aliases file (in your home directory) and add this line at the end:

```bash
alias python='python3'
```
# How to Create and Activate a Python Virtual Environment
Now that we have Python3 and pip3 installed on your computer, let's move to the next step: setting up a Python virtual environment. A virtual environment is a tool that helps to keep dependencies required by different projects separate by creating isolated Python environments for them. This is a good practice to ensure that the libraries and dependencies of one project don't mess with those of another.
## Creating a Virtual Environment
Regardless of your operating system, you can create a virtual environment in Python3 with the following command in the command line/terminal:

```bash
python3 -m venv myenv
```

Replace `myenv` with the name you want to give to your virtual environment. This command creates a folder in the current directory which contains the Python executable files and a copy of the `pip` library.
## Activating the Virtual Environment
Once you've created a virtual environment, you can activate it.
### On Windows
Use the following command:

```bash
myenv\Scripts\activate
```

### On macOS/Linux
Use the following command:

```bash
source myenv/bin/activate
```

Remember to replace `myenv` with the name you've given to your virtual environment.

When the virtual environment is activated, the name of your virtual environment will appear on the left side of the terminal line – something like `(myenv) Your-Computer:your_project UserName$`. This means that the virtual environment `myenv` is currently active, and when you install packages, they get installed in this environment.

## Deactivating the Virtual Environment

If you want to switch projects or otherwise leave your virtual environment, simply type:

```bash
deactivate
```

You're now back to your system’s default Python settings.

# Installing Python Packages in the Virtual Environment

With your virtual environment active, you're ready to install some Python packages. The ones you mentioned - `langchain`, `openai`, and `dotenv` - can be installed using pip, Python's package manager. Here's how to do it:

1. Make sure your virtual environment is activated. If it's activated, you should see its name in the command line/terminal. If not, refer to the previous section on how to activate it.
```bash
myenv\Scripts\activate
```

```bash
source myenv/bin/activate
```

2. To install the packages, you can use the `pip install` command, followed by the name of the package. Here are the commands to install `langchain`, `openai`, and `dotenv`:

```bash
pip install langchain
pip install openai
pip install python-dotenv
```

And that's it! You've successfully installed these packages in your virtual environment. You can verify this by using the `pip list` command, which shows all installed packages in the current environment.

Keep in mind that these packages are only installed within the active virtual environment. If you switch to a different project or deactivate the environment, you'll need to reinstall these packages in your new environment if you want to use them there.

# Securing Your OpenAI API Key

Before you can start leveraging the power of OpenAI's models for your applications, you need to obtain your own OpenAI API key. The API key is a unique identifier that allows OpenAI to authenticate your requests. Here's a step-by-step guide on how to get your OpenAI API key:

1. **Create an OpenAI Account:** Go to the OpenAI website and click on the 'Sign Up' button to create a new account. You will need to provide your email address and set up a password. You may also need to agree to OpenAI's Terms of Service and Privacy Policy.

2. **Verify Your Email:** After signing up, you will receive an email from OpenAI to verify your account. Click on the link in the email to verify your account. 

3. **Login to Your Account:** After verifying your account, log in to your OpenAI account.

4. **Navigate to the API Section:** Once you are logged in, you will see your dashboard. On the left-hand side of the dashboard, there is a menu. Click on the 'API' option. 

5. **Generate Your API Key:** On the API page, you will see a 'Create New API Key' button. Click on this button to generate your API key. A modal will appear with your new API key.

6. **Copy Your API Key:** Your API key will be a long string of characters. Make sure to copy this key and store it safely. You will need this key to make requests to the OpenAI API. 

7. **Keep Your API Key Secure:** Remember that your API key is like a password. It should be kept secure and not shared with anyone. If you believe your API key has been compromised, you should generate a new one immediately.

Now that you have your OpenAI API key, you are ready to start integrating OpenAI's models into your applications. In the next section of this blog, we will look at how to use this API key to make a request to the API.

# Interpreting and Running the OpenAI Language Model using your own Documents and System Prompts

Great - now that we have everything installed, let’s write the code in a file called `document_chat.py`!

**Code Block 1: Importing Modules**
```python
import os
import openai
from langchain.llms import OpenAI
from langchain.chat_models import ChatOpenAI
from langchain import PromptTemplate
from langchain import LLMChain
from dotenv import load_dotenv
```
This first block of code imports all the necessary Python modules and functions. Here we are importing:

- `os`: This is a built-in Python module that interacts with the operating system.
- `openai`: This is the OpenAI API client. 
- `langchain.llms.OpenAI` and `langchain.chat_models.ChatOpenAI`: These are classes from the `langchain` library that handle the OpenAI language model.
- `PromptTemplate` and `LLMChain`: These are classes from the `langchain` library that help format prompts and execute chains of language models.
- `dotenv`: This is a module that reads from a `.env` file where we store environment variables, like the OpenAI API key.

**Code Block 2: Loading Environment Variables**
```python
load_dotenv()
openai.api_key = os.environ["OPENAI_API_KEY"]
```
Here, we use `load_dotenv` to load environment variables from a `.env` file. We then set `openai.api_key` to the OpenAI API key we stored in our environment variables. 

**Code Block 3: Initializing the Language Model**
```python
llm = ChatOpenAI(model_name="gpt-3.5-turbo")
```
This line initializes the `ChatOpenAI` object with the "gpt-3.5-turbo" model.

**Code Block 4: Main Loop**
```python
while True:
    try:
        # Code omitted for brevity
    except KeyboardInterrupt:
        print("\n\033[31mGoodbye!\033[0m")
        break
```
This is the main loop of the program. It continuously prompts the user for a legal document path and a question until the user manually stops the program (using a KeyboardInterrupt, usually Ctrl+C).

**Code Block 5: Reading the Legal Document**
```python
legal_doc = input("\033[34mWhat is the path to the document you want to evaluate?\n\033[0m")
        
with open(legal_doc, "r") as f:
    legal_doc = f.read()
```
This block of code prompts the user for the path to the legal document they want to evaluate. It then reads the contents of the file at that path.

**Code Block 6: Getting the User's Question**
```python
query = input("\033[34mWhat is your question?\n\033[0m")
if query.lower() == "exit":
    print("\n\033[31mGoodbye!\033[0m")
    break
```
This block of code prompts the user for their question. If the user types "exit", the program ends.

**Code Block 7: Setting Up the Prompt Template and LLMChain**
```python
template = """
# Code omitted for brevity
"""
prompt = PromptTemplate(template=template, input_variables=["query", "legal_doc"])
llm_chain = LLMChain(prompt=prompt, llm=llm)
```
This block of code sets up the template for the prompt that will be given to the AI model. The `PromptTemplate` object takes the template and a list of input variables. The `LLMChain` object is initialized with the prompt and the language model.

**Code Block 8:

Running the Language Model**
```python
print("\033[32m" + llm_chain.run(query=query, legal_doc=legal_doc) + "\n")
```
This line of code runs the language model using the `LLMChain` object. It passes in the user's question and the contents of the legal document as parameters. The result is then printed to the console.

**Handling Interrupts**
```python
except KeyboardInterrupt:
    print("\n\033[31mGoodbye!\033[0m")
    break
```
Finally, if the user interrupts the program (commonly by pressing `Ctrl+C`), a goodbye message is printed and the main loop is broken, ending the program.

**The Whole Code**

Let's now put it all back together:

```python
import os
import openai
from langchain.llms import OpenAI
from langchain.chat_models import ChatOpenAI
from langchain import PromptTemplate
from langchain import LLMChain
from dotenv import load_dotenv

load_dotenv()

openai.api_key = os.environ["OPENAI_API_KEY"]
llm = ChatOpenAI(model_name="gpt-3.5-turbo")

while True:
    try:
        legal_doc = input("\033[34mWhat is the path to the document you want to evaluate?\n\033[0m")
        
        with open(legal_doc, "r") as f:
            legal_doc = f.read()

        query = input("\033[34mWhat is your question?\n\033[0m")
        if query.lower() == "exit":
            print("\n\033[31mGoodbye!\033[0m")
            break
    
        template = """
        You are LegalDoc AI. You are a superintelligent AI that answers questions about legal documents.

        You are:
        - helpful & friendly
        - good at answering complex questions in simple language
        - an expert in the law
        - able to infer the intent of the user's question

        The user will ask a question about their legal document, and you will answer it.

        When the user asks their question, you will answer it by searching the legal document for the answer.

        Here is the user's question and legal_doc file(s) you found to answer the question:

        Question:
        {query}

        Legal Document(s):
        {legal_doc}
        
        [END OF LEGAL DOCUMENT(S)]

        Now answer the question using the legal document (s) above.
        """
        prompt = PromptTemplate(template=template, input_variables=["query", "legal_doc"])
        llm_chain = LLMChain(prompt=prompt, llm=llm)
        print("\033[32m" + llm_chain.run(query=query, legal_doc=legal_doc) + "\n")

    except KeyboardInterrupt:
        print("\n\033[31mGoodbye!\033[0m")
        break
```


Now that the code is written, let’s make it easy to run!

# Running the Document Chat Program and Setting up Aliases

After going through the code of `document_chat.py`, it's now time to execute the program and interact with it. Here's a step-by-step guide on how to run the program, and how to set up aliases for ease of use.

## Running the Program

1. **Activate Your Virtual Environment:** Before running the program, make sure you have activated your Python virtual environment. This can be done by navigating to the directory containing your virtual environment (let's call it `venv`) and using the command `source venv/bin/activate` for Linux/macOS, or `venv\Scripts\activate` for Windows.

2. **Run the Program:** After activating the virtual environment, you can run the `document_chat.py` program using the command `python document_chat.py`.

## Setting Up Aliases

Typing the commands to activate the virtual environment and run the program every time can be a bit tedious. To streamline this, you can set up an alias that does both with a single command.

### Linux/macOS:

On a Linux or macOS system, you can add the following line to your `~/.bashrc` or `~/.zshrc` file (depending on whether you use Bash or Zsh):

```bash
alias docchat='source /path/to/venv/bin/activate && python /path/to/document_chat.py'
```
Replace `/path/to/venv` and `/path/to/document_chat.py` with the actual paths to your virtual environment and the `document_chat.py` file.

After adding this line, you can use the command `docchat` to activate your virtual environment and run `document_chat.py`.

### Windows:

On Windows, you can create a batch file with the commands to activate the virtual environment and run the program. Here's how you can do it:

1. Open Notepad or any other text editor.
2. Write the following lines in the editor:

```bat
@echo off
call C:\path\to\venv\Scripts\activate
python C:\path\to\document_chat.py
```

Replace `C:\path\to\venv` and `C:\path\to\document_chat.py` with the actual paths to your virtual environment and the `document_chat.py` file.

3. Save the file with a `.bat` extension, for example, `docchat.bat`.

You can now run the `docchat.bat` file to activate your virtual environment and run `document_chat.py`.

Remember, aliases and batch files should be used carefully. They're powerful tools that can make your workflow more efficient, but they can also execute any command that you put into them. Always double-check your commands before creating an alias or batch file.

# A Bright Future with AI and Legal Documents
As we come to the close of this guide, it's exciting to consider how AI, and specifically OpenAI, is transforming various industries, including the legal sector. You've now learned how to use the OpenAI API to create powerful applications that can read, understand, and answer questions about legal documents.

For those interested in seeing AI's potential in legal documents, consider checking out LawPilot. LawPilot leverages AI to distill crucial insights from your legal documents and craft compelling arguments. It's an AI legal assistant builder that trains ChatGPT on your legal documents, enabling you to summarize and revise your documents and generate and optimize arguments​1​.

You can simply upload one or multiple files in various formats (.pdf, .txt, .doc, .docx) and create a legal assistant that can answer any question about the content​1​. You can even give your AI assistant instructions on how to answer questions​1​.

By default, the AI legal assistant uses ChatGPT (specifically, the gpt-3.5-turbo model), and they're currently working on adding GPT-4, which promises even more power and flexibility​1​. Rest assured that the content of your documents is hosted securely on GCP/AWS servers​1​.

So why not take the next step on your AI journey with LawPilot? It's a fantastic example of how AI can be a game-changer for legal professionals and anyone dealing with legal documents. As you've seen in this guide, the power of AI is just a few lines of code away. Dive in, and let AI be your co-pilot in the vast legal skies!

