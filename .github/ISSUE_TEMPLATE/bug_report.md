const { ethers } = require('ethers');
const data = '0x095ea7b3...'; // your calldata
const iface = new ethers.utils.Interface(['function approve(address,uint256)']);
const decoded = iface.decodeFunctionData('approve', data);
console.log(decoded[0]); // spender
console.log(decoded[1].toString()); // amount in wei
console.log(ethers.utils.formatUnits(decoded[1], 18)); // amount as human-readable with 18 decimals

---

name: Bug report
about: Create a report to help us improve
title: ''
labels: bug
assignees: ''
---

<!--
Welcome! Before creating a new issue:
* This is the GIT EXTENSION for JupyterLab repository. Unrelated issues will be closed.
* Look at the README *Troubleshooting* section
* Search for relevant issues
* Check that you have updated both the jupyterlab extension and the python package to the same version
* Check that you have installed Git version 2 or higher
-->

## Description

<!--Describe the bug clearly and concisely. Include screenshots if possible-->

## Reproduce

<!--Describe step-by-step instructions to reproduce the behavior-->

1. Go to '...'
2. Click on '...'
3. Scroll down to '...'
4. See error '...'

## Expected behavior

<!--Describe what you expected to happen-->

## Context

<!--Complete the following for context, and add any other relevant context-->

- Python package version:
<!-- Results of `conda list jupyterlab-git` or `pip show jupyterlab-git` -->
- Extension version:
<!-- Results of `jupyter labextension list` -->
- Git version:
<!-- Results of `git --version` -->
- Operating System and its version:

<details><summary>Command Line Output</summary>
<pre>
Paste the output from your command line running `jupyter lab` here, use `--debug` if possible.
</pre>
</details>

<details><summary>Web Browser Output</summary>
<pre>
Paste the output from your browser web console here.
</pre>
</details>

<!--
To open the browser, please refer to the documentation:
Chrome: https://developers.google.com/web/tools/chrome-devtools/open#console
Firefox: https://developer.mozilla.org/en-US/docs/Tools/Web_Console#Opening_the_Web_Console
-->
