
<h1 align="center">
  <img align="center" src="./assets/amethyst2.png" width="200px" style="margin: 20px auto; display: block;" />
</h1>

<p align="center"><b>A Python extension for real-time feedback with <a href="https://docs.python.org/3.9/library/typing.html#module-typing" target="_blank">Python Type Hints</a></b>
</p>

<div align="center">

![versions](https://img.shields.io/badge/Amethyst-1.0.0-946adf?style=for-the-badge)
![versions](https://img.shields.io/badge/Python-3.7%20%7C%203.8.%20%7C%203.9%20%7C%203.10%20%7C%203.11-blue?style=for-the-badge)

</div>

\!\[feature X\]\(images/feature-x.png\)

## Amethyst for Visual Studio Code

Amethyst is a developer productivity tool for rapid Python prototyping, code inspection, and exploration. Runtime values are displayed directly in your editor as you code. Amethyst supports Python versions 3.7 - 3.11.x and includes support for inline static typing feedback.


## 💎 What Amethyst is great for
📖 Learning and exploring the Python language in real time<br/>
🧪 Testing out a new libary and getting feedback quickly<br/>
💡 Rapid prototyping the functionality of an idea that popped into your head<br/>
⚡️ Instant feedback as you learn to use Python features like <a href="https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html">static typing</a><br/>
➡️ Having others easily follow along with you as you code<br/>
🧠 Remember values so you can easily follow along with yourself as you code

## ❌ What Amethyst is *not* for
⛔ Running Amethyst in scripts and applications that listen for incoming requests (Flask/Tornado apps)<br/>
⛔ Getting input from the user using built-in `input()`. One solution is to simulate the input as a variable yourself<br/>
⛔ Playing with highly destructive code. Amethyst evaluates as you type and this can have consequences with dangerous code

## ☑️ Requirements

Amethyst for Python requires Python 3.5+, preferrably 3.10.x. For those who want additional protection Amethyst has support for [MyPy](https://github.com/python/mypy#mypy-static-typing-for-python), optional static typing. You must install MyPy in order for static typing to work, but it is not required.

## ⚙️ Extension Settings

Include if your extension adds any VS Code settings through the `contributes.configuration` extension point.

For example:

This extension contributes the following settings:

* `myExtension.enable`: Enable/disable this extension.
* `myExtension.thing`: Set to `blah` to do something.

## Credits
Amethyst is essentially a continuation of the Wolf extension for Python, inspired by the QuokkaJS extension for JavaScript/TypeScript. The plan is to be reasonably active with development for Amethyst and push out a few more features and eventually shift away from the idea of the "live scratchpad" to a go-to fully-featured development and debugging tool.


## 💭 FAQ

### Why is it called Amethyst?
This extension is for the Python programming language so to stay on theme it was named after a kind of Pythonidae called the Amethystine Python which gets its name from the iridescent scales that appear to have a purple hue in certain lighting conditions!

### How do I learn Python Static Typing?
I recommend getting into static typing once you have established at least some familiarity with the core language of Python and how computer programs work in general. I say that because most online resources for Python are written *without* static typing. When you're ready, [here is a great resource for getting started](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html).

### Can I use this with Django and Flask?
Amethyst was neither tested nor designed for use with scripts that are meant to run and wait indefinitely for requests, so I don't recommend it. It's more suited for learning and trying out new techniques to improve your understanding of Python which makes Django and Flask easier 😉

### Known issues

##### Errors messages can stack on a single line
When dealing with multiple simultaneous errors, it is possible for them to stack up on a single line. The goal is to get any given errant line of code to show only the topmost error and to reveal errors underneath only when that one is resolved. This issue seems to be tolerable so long as you can eventually solve your issue.

##### Pressing return at the end a line clips Amethyst annotation
When you are at the end of a line of code that has output next to it and you press [RETURN], the annotation will briefly get clipped. This is only visible for a second, but I understand that this can be distracting and other extensions do this better. Working to resolve this ASAP.

## 📄 Release Notes

### 1.0.0

Initial release of Amethyst
