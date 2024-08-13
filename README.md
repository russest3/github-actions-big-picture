# Project repository for the Pluralsight course, GitHub Actions: The Big Picture

This repository contains the core web application files and configuration you'll need to follow along in the Pluralsight course, GitHub Actions: The Big Picture.

To follow along with the step-by-step instructions in the Essentials module, you will need to create a copy of this repository by doing the following:
1. Click **Use this template** above the file list and select **Create a new repository**.
2. Use the **Owner** dropdown menu to select the account you want to own the repository. 
3. Name your repository something fun and add a simple description to make it easier to identify later.
4. Set the default visibility for the repo to public, as private repositories use Actions minutes, while public repositories can use GitHub-hosted runners for free.

Click Create repository from template and we’re ready to build our first Actions workflow!

## Lab Info
[https://github.com/a-a-ron/github-actions-big-picture](https://github.com/a-a-ron/github-actions-big-picture)
- Fork repo

## Workflow file
<pre>
name: learn-github-actions
on: [push]
jobs:
  checks-bats-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
      - run: npm install -g bats
      - run: bats -v
</pre>

## Build, Test, and Deploy an App with Github Actions
- In Github click Settings -> Environments -> New Environment
- Enable Github Pages
    - Settings -> Pages
    - Select Source = GitHub Actions
