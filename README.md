<!DOCTYPE html>
<!-- saved from url=(0035)http://127.0.0.1:5500/AI%20web.html -->
<html lang="en"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CodeMentor - Learn Coding</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.14/codemirror.min.css">
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: #f4f7fa;
      color: #333;
    }
    header {
      background: #1f2937;
      color: white;
      padding: 1rem 2rem;
      text-align: center;
      font-size: 1.5rem;
    }
    .container {
      display: flex;
      flex-wrap: wrap;
      padding: 1rem;
      gap: 1rem;
    }
    .left-panel, .right-panel {
      flex: 1;
      min-width: 300px;
    }
    .editor-section {
      background: white;
      padding: 1rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.05);
    }
    .editor-title {
      font-weight: bold;
      margin-bottom: 0.5rem;
    }
    .output-section {
      margin-top: 1rem;
      background: #fff;
      padding: 1rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.05);
    }
    .output-section h3 {
      margin-top: 0;
    }
    textarea, .CodeMirror {
      width: 100%;
      height: 300px;
      font-family: monospace;
      font-size: 1rem;
    }
    button {
      padding: 0.5rem 1rem;
      margin-top: 1rem;
      background: #3b82f6;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #2563eb;
    }
    @media (max-width: 768px) {
      .container {
        flex-direction: column;
      }
    }
  </style>
<!-- Code injected by live-server -->
<script>
	// <![CDATA[  <-- For SVG support
	if ('WebSocket' in window) {
		(function () {
			function refreshCSS() {
				var sheets = [].slice.call(document.getElementsByTagName("link"));
				var head = document.getElementsByTagName("head")[0];
				for (var i = 0; i < sheets.length; ++i) {
					var elem = sheets[i];
					var parent = elem.parentElement || head;
					parent.removeChild(elem);
					var rel = elem.rel;
					if (elem.href && typeof rel != "string" || rel.length == 0 || rel.toLowerCase() == "stylesheet") {
						var url = elem.href.replace(/(&|\?)_cacheOverride=\d+/, '');
						elem.href = url + (url.indexOf('?') >= 0 ? '&' : '?') + '_cacheOverride=' + (new Date().valueOf());
					}
					parent.appendChild(elem);
				}
			}
			var protocol = window.location.protocol === 'http:' ? 'ws://' : 'wss://';
			var address = protocol + window.location.host + window.location.pathname + '/ws';
			var socket = new WebSocket(address);
			socket.onmessage = function (msg) {
				if (msg.data == 'reload') window.location.reload();
				else if (msg.data == 'refreshcss') refreshCSS();
			};
			if (sessionStorage && !sessionStorage.getItem('IsThisFirstTime_Log_From_LiveServer')) {
				console.log('Live reload enabled.');
				sessionStorage.setItem('IsThisFirstTime_Log_From_LiveServer', true);
			}
		})();
	}
	else {
		console.error('Upgrade your browser. This Browser is NOT supported WebSocket for Live-Reloading.');
	}
	// ]]>
</script>
</head>
<body>
  <header>🚀 CodeMentor: Learn, Debug, and Master Coding</header>
  <div class="container">
    <!-- LEFT PANEL -->
    <div class="left-panel">
      <div class="editor-section">
        <div class="editor-title">💻 Code Editor (Python)</div>
        <textarea id="code" name="code">print("Hello, World!")</textarea>
        <button onclick="analyzeCode()">Analyze Code</button>
      </div>

      <div class="output-section" id="error-output">
        <h3>🛑 Error Detection</h3>
        <p>No errors yet. Write some code and click "Analyze".</p>
      </div>

      <div class="output-section" id="debug-suggestions">
        <h3>🧠 Debugging Suggestions</h3>
        <p>Suggestions will appear here after code analysis.</p>
      </div>
    </div>

    <!-- RIGHT PANEL -->
    <div class="right-panel">
      <div class="output-section">
        <h3>📘 Interactive Tutorial</h3>
        <p>
          Today's topic: <strong>Loops in Python</strong><br>
          <em>For loops let you iterate over lists, ranges, and more.</em><br>
          Example:<br>
          <code>
            for i in range(5):<br>
            &nbsp;&nbsp;&nbsp;&nbsp;print(i)
          </code>
        </p>
      </div>

      <div class="output-section">
        <h3>🎯 Exercise Generator</h3>
        <p><strong>Task:</strong> Write a function that returns the factorial of a number.</p>
        <p><strong>Difficulty:</strong> Beginner</p>
      </div>
    </div>
  </div>

  <!-- CodeMirror -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.14/codemirror.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.14/mode/python/python.min.js"></script>
  <script>
    // Initialize CodeMirror
    const editor = CodeMirror.fromTextArea(document.getElementById("code"), {
      lineNumbers: true,
      mode: "python",
      theme: "default"
    });

    // Placeholder simulate API response
    function analyzeCode() {
      const code = editor.getValue();

      // Replace this with actual API call to analyze code
      // Simulated results for demo purposes
      let errors = '';
      let suggestions = '';

      if (code.includes('pritn')) {
        errors = 'SyntaxError: Did you mean "print"?';
        suggestions = 'Check your spelling of built-in functions.';
      } else if (code.includes('while True')) {
        errors = 'Warning: Infinite loop detected.';
        suggestions = 'Make sure to have a break condition.';
      } else {
        errors = '✅ No syntax errors detected.';
        suggestions = 'Try adding input validation or edge case handling.';
      }

      document.getElementByI 
</script></body></html>
