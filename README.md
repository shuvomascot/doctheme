<!-- Language switcher buttons -->
<div class="language-switcher">
    <button onclick="showCode('python')" class="active">Python</button>
    <button onclick="showCode('php')">PHP</button>
</div>

<!-- Code blocks -->
<div id="python" class="code-block active">
    <pre><code class="language-python">def hello():
    print("Hello, World!")</code></pre>
</div>

<div id="php" class="code-block">
    <pre><code class="language-php">&lt;?php
    echo "Hello, World!";
    ?&gt;</code></pre>
</div>

<!-- CSS to hide and show code blocks -->
<style>
    .code-block {
        display: none;
    }
    .code-block.active {
        display: block;
    }
    .language-switcher button {
        margin: 5px;
        padding: 5px 10px;
        cursor: pointer;
        background-color: #007bff;
        color: white;
        border: none;
        border-radius: 4px;
    }
    .language-switcher button.active {
        background-color: #0056b3;
    }
</style>

<!-- JavaScript to toggle code blocks -->
<script>
    function showCode(language) {
        // Hide all code blocks
        var codeBlocks = document.querySelectorAll('.code-block');
        codeBlocks.forEach(function(block) {
            block.classList.remove('active');
        });

        // Remove active class from buttons
        var buttons = document.querySelectorAll('.language-switcher button');
        buttons.forEach(function(button) {
            button.classList.remove('active');
        });

        // Show the selected code block and add active class to the clicked button
        document.getElementById(language).classList.add('active');
        event.target.classList.add('active');
    }
</script>

