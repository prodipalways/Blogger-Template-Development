# Add Copy Button In Blogger

## STEP 1 — Add CSS (inside <b:skin><![CDATA[ )

```
/* ==== COPY CODE BUTTON ==== */
<style>
    .code-boxrk {
      position: relative;
      background: #0d1117;
      /* GitHub dark theme */
      padding: 18px;
      border-radius: 8px;
      border: 1px solid #30363d;
      overflow: auto;
      margin: 20px 0;
    }

    .code-boxrk pre {
      margin: 0;
      color: #c9d1d9;
      font-size: 14px;
      white-space: pre-wrap;
      word-wrap: break-word;
      font-family: Consolas, Monaco, "Courier New", monospace;
    }

    /* GitHub-style copy button */
    .copy-btnrk {
      position: absolute;
      top: 10px;
      right: 10px;
      background: #21262d;
      color: #c9d1d9;
      border: 1px solid #30363d;
      padding: 5px 10px;
      border-radius: 6px;
      font-size: 13px;
      cursor: pointer;
      transition: background 0.2s, border-color 0.2s;
    }

    /* Hover effect like GitHub */
    .copy-btnrk:hover {
      background: #30363d;
      border-color: #58a6ff;
    }

    .copy-btnrk:active {
      transform: scale(0.95);
    }
  </style>
```

## STEP 2 — Add HTML To Your Post or Page

```
<h3>Google Form Quiz Script</h3>
  <div class="code-boxrk">
    <button class="copy-btnrk" onclick="copyCode(this)">Copy</button>
    <pre><code>
Your Text Here
      </code></pre>
  </div>
```

## STEP 3 — Add JavaScript (before </body )

```
<script>
    function copyCode(button) {
      let code = button.nextElementSibling.innerText;

      navigator.clipboard.writeText(code).then(() => {
        button.innerText = "Copied!";
        button.style.borderColor = "#2ea043"; // GitHub green border
        setTimeout(() => {
          button.innerText = "Copy";
          button.style.borderColor = "#30363d";
        }, 1500);
      });
    }
  </script>
```
