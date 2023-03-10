<h1 align="center">
  <img align="center" src="https://raw.githubusercontent.com/rmdashrfv/amethyst-python/main/assets/amethyst2.png" width="200px" style="margin: 20px auto; display: block;"/>
</h1>

<p align="center"><b>A Python extension for real-time feedback with <a href="https://docs.python.org/3.9/library/typing.html#module-typing" target="_blank">Python Type Hints</a></b>
</p>

<div align="center">

![versions](https://img.shields.io/badge/Amethyst-1.0.0-946adf?style=for-the-badge)
![versions](https://img.shields.io/badge/Python-3.7%20%7C%203.8.%20%7C%203.9%20%7C%203.10%20%7C%203.11-blue?style=for-the-badge)

</div>

<h3 align="center" style="margin-bottom: 40px">
  <img align="center" src="https://raw.githubusercontent.com/rmdashrfv/amethyst-python/main/assets/demo.gif" width="100%" height="auto" style="margin: 20px auto; display: block;" />
</h3>

## Amethyst for Visual Studio Code

Amethyst is a developer productivity tool for rapid Python prototyping, code inspection, and exploration. Runtime values are displayed directly in your editor as you code. Amethyst supports Python versions 3.7 - 3.11.x and includes support for inline static typing feedback.


## ๐ What Amethyst is great for
๐ Learning and exploring the Python language in real time<br/>
๐งช Testing out a new libary and getting feedback quickly<br/>
๐ก Rapid prototyping the functionality of an idea that popped into your head<br/>
โก๏ธ Instant feedback as you learn to use Python features like <a href="https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html">static typing</a><br/>
โก๏ธ Having others easily follow along with you as you code<br/>
๐ง  Remember values so you can easily follow along with yourself as you code

## โ What Amethyst is *not* for
โ Running Amethyst in scripts and applications that listen for incoming requests (Flask/Tornado apps)<br/>
โ Getting input from the user using built-in `input()`. One solution is to simulate the input as a variable yourself<br/>
โ Playing with highly destructive code. Amethyst evaluates as you type and this can have consequences with dangerous code

## โ๏ธ Requirements

Amethyst for Python requires Python 3.5+, preferrably 3.10.x. For those who want additional protection Amethyst has support for [MyPy](https://github.com/python/mypy#mypy-static-typing-for-python), optional static typing. You must install MyPy in order for static typing to work, but it is not required.

## โ๏ธ Extension Settings

Here are the Settings for Amethyst. Feel free to change them to your liking/needs.


| Setting        | Description   | Default  |
|:------------- |:-------------|:-----|
| Amethyst enabled | Amethyst runs and gives you live feedback when this is `true` | `true` (CMD+SHIFT+R to toggle) |
| Python command| The command that your computer uses to run Python 3.7 or greater |   `python3` |
| Evaluate with MyPy | Adhere to typing and type hints when this is `true` | `false` |
| Debounce time | The minimum amount of time between calls to Amethyst to process your code | `125` (in milliseconds) |
| Inline text color Correct | The color of the text for correct code | `#966ce0` |
| Inline text color Incorrect | The color of the text for errors | `#fd3333` |
| Inline text color Background Correct | The bg color of the text for errors | `transparent` |
| Inline text color Background Incorrect | The bg color of the text for errors | `transparent` |

## Credits
Amethyst is essentially a continuation of the Wolf extension for Python, inspired by the QuokkaJS extension for JavaScript/TypeScript, LightTable, LiveCode, AREPL, and more. The plan is to be reasonably active with development for Amethyst and push out a few more features and eventually shift away from the idea of the "live scratchpad" to a go-to fully-featured development and debugging tool.


## ๐ญ FAQ

### Why is it called Amethyst?
This extension is for the Python programming language so to stay on theme it was named after a kind of Pythonidae called the Amethystine Python which gets its name from the iridescent scales that appear to have a purple hue in certain lighting conditions!

### I'm having trouble getting Amethyst to start
This is most likely do to your Python binary setup. Make sure you have Python 3.7 or greater installed, and make sure that the verison Python you want to use is mapped to your `python3` command. Otherwise you can open your terminal, run `which python` and then take the result of that command and paste it into the setting for the Python Command setting.

### How do I learn Python Static Typing?
I recommend getting into static typing once you have established at least some familiarity with the core language of Python and how computer programs work in general. I say that because most online resources for Python are written *without* static typing. When you're ready, [here is a great resource for getting started](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html).

### Can I use this with Django and Flask?
Amethyst was neither tested nor designed for use with scripts that are meant to run and wait indefinitely for requests, so I don't recommend it. It's more suited for learning and trying out new techniques to improve your understanding of Python which makes Django and Flask easier ๐

### API calls & external requests?
I wanted to release this with HTTP request caching built-in at launch, but unfortunately ran out of time. Caching for external requests and API calls is a high priority for this project, so if you have any ideas or you want to help, please feel free to [join the discussion](https://github.com/rmdashrfv/amethyst-python/issues/1).

## Known issues

### Live feedback for static typing is very slow
Working on this and should have a fix soon. Because MyPy involves a heavy extra step on every keystroke and due to the nature of type checking I am considering altering Amethyst so that these extra checks run only on save or with a higher amount of debounce. The vanilla Python feedback would still occur responsively on every keypress. If you have thoughts or suggestions, please [open or chime in on an issue](https://github.com/rmdashrfv/amethyst-python/issues).

### Errors messages can stack on a single line
When dealing with multiple simultaneous errors, it is possible for them to stack up on a single line. The goal is to get any given errant line of code to show only the topmost error and to reveal errors underneath only when that one is resolved. This issue seems to be tolerable so long as you can eventually solve your issue.

### Pressing return at the end a line clips Amethyst annotation
When you are at the end of a line of code that has output next to it and you press [RETURN], the annotation will briefly get clipped. This is only visible for a second, but I understand that this can be distracting and other extensions do this better. Working to resolve this ASAP.

## ๐ Release Notes

### 1.1.0
Fixed loading issue on Windows machines

### 1.0.0
Initial release of Amethyst
