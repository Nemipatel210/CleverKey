<h1 align="center">CleverKey</h1>


<p align="center">
  CleverKey is your AI-powered shortcut for everyday tasks, designed to fit seamlessly into your workflow. With just a hotkey, you can summarize long articles, correct grammar, refine code, translate text, or simply chat for quick answers — all without leaving your current app.
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#contributing">Contributing</a> •
  <a href="#contact">Contact</a>
</p>

<hr>

<h2 id="features">✨ Features</h2>

<ul>
  <li>Text Summarization</li>
  <li>Grammar Correction</li>
  <li>Code Refinement</li>
  <li>Translation</li>
  <li>Normal Conversation</li>
</ul>

<h2 id="installation">🚀 Installation</h2>

<h3>Prerequisites</h3>

<ul>
  <li>Python 3.7 or higher</li>
  <li>Ollama (for local processing)</li>
  <li>API keys for Gemini, Anthropic, or OpenAI (if using API approach)</li>
</ul>

<h3>Required Libraries</h3>

<ul>
  <li><code>pynput</code></li>
  <li><code>pyperclip</code></li>
  <li><code>httpx</code></li>
  <li><code>langchain</code></li>
  <li><code>langchain_google_genai</code></li>
</ul>

<h3>Installation Steps</h3>

<ol>
  <li>Clone the repository:
    <pre><code>git clone https://github.com/Nemipatel210/CleverKey.git
cd CleverKey</code></pre>
    <p>There are two folders namely local_assistant which requires inference from LLM locally and remote_assistant which uses api to make inference. Just an advice, use remote_assistant folder files to get faster responses as compared to local_assistant files</p>
    <p>Using gemini-1.5-flash is most suitable for regular task because it is built to address developers’ top request for speed and affordability.</p>
  </li>
  <li>Create and activate a virtual environment:
    <pre><code>python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate</code></pre>
  </li>
  <li>Install the required libraries:
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li>Set up Ollama for local processing:
    <p>Follow the installation instructions from the <a href="https://ollama.ai/docs/getting-started">official Ollama documentation</a> for your PC.</p>
    <p>Install your desired LLM based on your application like for code_refiner.py you can use codellama</p>
  </li>
  <li>Find the Global Hotkey for F9 and F10:
    <pre><code>from pynput.keyboard import Key
print(Key.f9.value, Key.f10.value)</code></pre>
  </li>
</ol>

<h2 id="usage">💻 Usage</h2>

<h3>Local Processing using Ollama</h3>

<ol>
  <li>Select the text you want to process.</li>
  <li>Press F9 to process the selected text locally.</li>
  <li>The request is sent to Ollama via an HTTP POST method on port 11434, which the Ollama API is configured to listen on.</li>
</ol>

<h3>API Processing</h3>

<ol>
  <li>Set Up API Keys: Obtain API keys for Gemini, Anthropic, or OpenAI and store them in a <code>.env</code> file.</li>
  <li>Configure API settings in the project.</li>
  <li>Select the text and press F9 to process using the API.</li>
</ol>
<h3>Considerations</h3>
<p>The python files in any of the folder can be used directly without any modification on MACBOOK's.</p>
<p>You may need to modify the hotkey bindings depending on your system and keyboard layout.</p>
<p>Specifically for MAC system with ventura or later version you need to first disable your default input of F9 and F10 keys. Follow this link to diable https://support.apple.com/en-in/102439</p>

<h3>Inspired by</h3>
<li>Andrej Karpathy's Twitter post about GPT's correcting minor typos. <a href="https://x.com/karpathy/status/1725553780878647482">Post</a></li>
<li>Patrick Loeber's video about using httpx requests to call ollama api locally</li>


