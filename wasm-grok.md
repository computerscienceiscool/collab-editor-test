This document specifies the requirements and design for a WebAssembly (WASM) build of Grokker's commit message generation functionality. The WASM module will run entirely in the browser, providing AI-powered commit message generation for single-file changes in a collaborative editor environment.
1.1 Purpose

Build a WASM wrapper for Grokker's GitCommitMessage() functionality that enables:

    Privacy-focused, client-side commit message generation
    Zero hosting costs (no server infrastructure)
    Seamless integration with githubCommitDialog.js
    Full Grokker semantic analysis and formatting capabilities

1.2 Use Case

Target Application: Single-file collaborative editor with GitHub integration

Workflow:

    User makes changes to a single file in the browser
    User initiates commit via githubCommitDialog.js
    WASM module analyzes the diff using user's OpenAI API key
    WASM returns formatted conventional commit message
    User reviews/edits message before committing to GitHub
