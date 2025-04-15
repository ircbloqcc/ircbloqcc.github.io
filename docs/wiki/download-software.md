**ircBloqV4 Agent** needs to be used with online webpages. According to the actual download, you don’t need to start them all.

## IrcBloqV4 Agent

!!! warning
    This software is only used when accessing the ircBloqV4 online web. Do not open the ircBloqV4 Desktop and ircBloqV4-Agent at the same time.

![](assets/IrcBloq-Agent.png)

### ![GitHub release (latest by date)](https://img.shields.io/github/v/release/ircbloqcc/ircbloq-link-releases)

<style>
  .download-container {
    margin: 1em 0;
    padding: 1em;
    border: 1px solid #ddd;
    border-radius: 8px;
    background-color: #f9f9f9;
    max-width: 400px;
  }

  .download-container label {
    font-weight: bold;
    display: block;
    margin-bottom: 0.5em;
  }

  .download-container select {
    width: 100%;
    padding: 0.5em;
    border-radius: 6px;
    border: 1px solid #ccc;
    font-size: 1em;
    margin-bottom: 1em;
  }

  .download-container button {
    padding: 0.6em 1.2em;
    background-color: #ff007f;
    color: white;
    border: none;
    border-radius: 6px;
    font-size: 1em;
    cursor: pointer;
    transition: background-color 0.2s ease;
  }

  .download-container button:disabled {
    background-color: #ccc;
    cursor: not-allowed;
  }

  .download-container button:hover:not(:disabled) {
    background-color: #e60072;
  }
</style>

<div class="download-container">
  <label for="os-select">Select your operating system:</label>
  <select id="os-select">
    <option value="">-- Select an option --</option>
    <option value="https://github.com/ircbloqcc/ircbloq-link-releases/releases/download/v4.2.2/IrcBloq-Agent_v4.2.2_win.exe">Windows x64/x86</option>
    <option value="https://github.com/ircbloqcc/ircbloq-link-releases/releases/download/v4.2.2/IrcBloq-Agent_v4.2.2_win_x64.exe">Windows x64</option>
    <option value="https://github.com/ircbloqcc/ircbloq-link-releases/releases/download/v4.2.2/IrcBloq-Agent_v4.2.2_win_ia32.exe">Windows x86</option>
    <option value="https://github.com/ircbloqcc/ircbloq-link-releases/releases/download/v4.2.2/IrcBloq-Agent_v4.2.2_mac_x64.dmg">macOS x64</option>
    <option value="https://github.com/ircbloqcc/ircbloq-link-releases/releases/download/v4.2.2/IrcBloq-Agent_v4.2.2_linux_amd64.deb">Linux x64</option>
  </select>

  <button id="download-button" disabled>Download</button>
</div>

<script>
  const select = document.getElementById('os-select');
  const button = document.getElementById('download-button');

  select.addEventListener('change', () => {
    button.disabled = !select.value;
  });

  button.addEventListener('click', () => {
    if (select.value) {
      window.location.href = select.value;
    }
  });
</script>
