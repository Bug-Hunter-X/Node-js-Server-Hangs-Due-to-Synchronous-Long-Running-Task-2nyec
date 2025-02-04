# Node.js Server Hang - Synchronous Operation

This repository demonstrates a common issue in Node.js where a long-running synchronous operation blocks the event loop, causing the server to hang and become unresponsive.  The problem is highlighted in `server.js`, and a solution using asynchronous operations is provided in `serverSolution.js`.

## Problem

The `server.js` file includes a `while` loop that simulates a long-running task. This loop occupies the event loop, preventing the server from handling new requests until the loop completes, resulting in the server hanging. 

## Solution

The `serverSolution.js` file demonstrates how to use asynchronous operations to avoid blocking the event loop. This allows the server to handle multiple requests concurrently.